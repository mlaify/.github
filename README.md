# .github

The mlaify organization's profile (`profile/README.md`) and shared GitHub Actions.

## `actions/report-failure`

Opens one issue when a workflow fails on a branch, with the failed jobs and steps and the log up to the
error, and closes it when that workflow next passes. A repeat failure comments on the open issue instead
of opening another, so a broken workflow costs one notification, not one per run. Pull requests,
cancelled runs and jobs that never ran a step (a rejected deployment) report nothing.

Add it as the last job of a workflow, pinned to a commit:

```yaml
  report:
    needs: [build, deploy]          # every job it should watch
    if: always() && github.event_name != 'pull_request'
    runs-on: ubuntu-24.04
    permissions:
      actions: read
      issues: write
    steps:
      - uses: mlaify/.github/actions/report-failure@<commit sha>
        with:
          result: ${{ contains(needs.*.result, 'failure') && 'failure' || (contains(needs.*.result, 'cancelled') && 'cancelled' || 'success') }}
```

Issues get the `ci-failure` label and the title `CI failure: <workflow> on <branch>`.
