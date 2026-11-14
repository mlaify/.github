# Security Policy

## Choose the right reporting channel

Use a public GitHub issue for ordinary software and documentation problems. This includes:

- bugs, crashes, installation or compatibility problems;
- false positives, false negatives, incorrect findings, and disagreements about severity;
- feature requests, support questions, and documentation corrections; and
- security recommendations that do not demonstrate a vulnerability in this project.

Do not send those reports to the security email address. Open the affected repository's
**Issues** tab and select the appropriate form.

Use GitHub Private Vulnerability Reporting only when the project itself creates a credible,
unintended confidentiality, integrity, or availability impact. Open the affected repository's
**Security** tab and select **Report a vulnerability**. Do not put vulnerability details in a
public issue, pull request, discussion, or comment.

This is a coordinated vulnerability disclosure program, not a bug bounty. We do not offer or
promise payment, rewards, or swag for reports.

## What to include

Provide:

- the affected repository, component, version, or commit;
- the realistic attacker prerequisites and security impact;
- complete, minimal reproduction steps or a proof of concept;
- any relevant logs or evidence, with credentials, personal data, proprietary source, and
  third-party data removed; and
- your preferred disclosure and credit details.

Automated scanner output without validation and a demonstrated impact is not sufficient by
itself.

## Scope

This policy covers code maintained in the affected repository and services operated by mlaify
for that project. A repository-specific security policy may define a narrower system boundary,
supported versions, or additional exclusions; that policy takes precedence.

## Generally out of scope

The following are not security vulnerabilities in this project unless you demonstrate a
project-specific security impact:

- ordinary bugs, false positives, false negatives, inaccurate severity, or missing features;
- findings in software merely analyzed, displayed, packaged, documented, or depended on by the
  project;
- missing security headers, version disclosure, clickjacking on non-sensitive pages, or other
  best-practice observations without a realistic attack path;
- automated or bulk scanner reports without manual validation;
- social engineering, spam, denial-of-service testing, or testing accounts, devices, or systems
  you do not own or lack explicit permission to test; and
- vulnerabilities in third-party products, services, dependencies, or vendor firmware, unless
  this project uses or configures them in a way that creates a distinct vulnerability here.

Report third-party vulnerabilities to the responsible vendor or an appropriate coordinator.

## Our commitments

For a complete, in-scope report submitted through an official private channel, we will:

- aim to acknowledge the report within seven calendar days;
- work with you to understand and validate the issue;
- keep you informed as the report is handled, within our operational constraints;
- remediate confirmed vulnerabilities on a risk-informed timeline; and
- coordinate publication and credit when appropriate.

Reports that are incomplete, automated, out of scope, or ordinary support requests may be
redirected, closed, or receive no individual response.

## Our expectations

To participate in good faith:

- test only systems, devices, accounts, and data you own or have explicit permission to test;
- avoid privacy violations, disruption, data destruction, persistence, and lateral movement;
- access only the minimum data needed to demonstrate the issue, and stop immediately if you
  encounter data that is not yours;
- use only the official private channels for vulnerability details;
- allow a reasonable remediation period, normally at least 90 days, before public disclosure;
  and
- do not use threats, extortion, or demands for payment.

## Safe harbor

Research conducted in good faith and in accordance with this policy is considered authorized
under applicable anti-hacking and anti-circumvention laws. We will not initiate or support legal
action for accidental, good-faith violations of this policy, and we waive restrictions in our
terms that would interfere with compliant research on a limited basis.

You remain responsible for complying with applicable law. This safe harbor applies only to legal
claims under our control and does not bind independent third parties.

If you are unsure whether planned research complies with this policy, submit a private report
before continuing.
