# Security reporting policy

## Maintainer and project limits

M&L AI and the repositories in the `mlaify` organization are run by volunteers. We do our best to
provide security and support for all of our projects, but both are best effort: there is no
guaranteed response, fix, or timeline. Coordinated vulnerability disclosure (CVD) under this
vulnerability disclosure policy (VDP) is handled the same way. M&L AI is small: it is not a large
company with dedicated teams for security, support, and everything else.

GitHub Private Vulnerability Reporting is an intake channel, not a bug-bounty program, paid
disclosure program, service-level agreement, or contract. No payment, reward, sponsorship,
employment, gift, or swag is offered or promised for reports. Do not submit invoices or make
disclosure contingent on compensation.

A report does not create an obligation to acknowledge, investigate, remediate, publish an
advisory, provide credit, or coordinate disclosure. Reports may be closed without investigation
or may receive no individual response. A previous response, fix, acknowledgement, or advisory
does not create a commitment for future reports.

## Supported environments

Unless a repository explicitly documents otherwise, development and maintainer testing take
place on macOS. Linux support is best effort only where the repository documents it. Windows is
not supported.

Reports that affect only an unsupported operating system, platform, version, configuration, or
deployment are out of scope and may be closed without investigation or response.

## Choose the right GitHub channel

Use a public GitHub issue in the affected repository for ordinary software or documentation
problems, including:

- bugs, crashes, installation or compatibility problems;
- false positives, false negatives, incorrect findings, or severity disagreements;
- feature requests, support questions, and documentation corrections; and
- security recommendations that do not demonstrate a vulnerability in the project itself.

Use the affected repository's **Security** tab and select **Report a vulnerability** only for a
credible, confidential vulnerability in that project. Do not put unpatched vulnerability details
in a public issue, pull request, discussion, or comment.

Reports sent by email or through unrelated repositories are not processed. Automated or bulk
scanner output without manual validation and a demonstrated project-specific impact is not
sufficient.

## Scope

The affected repository's maintained code and any service explicitly documented as operated for
that project are in scope. A repository may publish narrower project-specific scope or supported
versions; those details supplement this policy.

The following are out of scope unless a distinct vulnerability in the affected project is
demonstrated:

- findings in software merely analyzed, displayed, packaged, documented, or depended on by the
  project;
- third-party products, services, dependencies, or vendor firmware;
- ordinary bugs, missing features, incorrect analysis, or best-practice observations without a
  realistic attack path;
- unsupported platforms, versions, configurations, or deployments;
- social engineering, spam, denial-of-service testing, or testing of systems, accounts, devices,
  or data without explicit authorization; and
- reports whose primary purpose is to solicit payment, work, sponsorship, publicity, or a
  commercial engagement.

Report third-party vulnerabilities to the responsible vendor or an appropriate coordinator.

## What to include

GitHub's private reporting form has fixed fields. A useful report includes:

- the affected repository, component, version, release, or commit;
- the security boundary that fails and a realistic impact;
- attacker prerequisites and configuration assumptions;
- minimal, safe reproduction steps or a proof of concept;
- sanitized evidence with secrets, personal data, proprietary source, and third-party data
  removed; and
- a suggested remediation, if one is available.

## Research and disclosure

Test only systems, devices, accounts, and data that you own or have explicit permission to test.
Avoid privacy violations, disruption, persistence, lateral movement, and data destruction. Access
only the minimum data needed to demonstrate an issue and stop immediately if you encounter data
that is not yours.

This policy does not grant authorization to test third-party or privately operated systems and
does not provide legal advice or a safe-harbor guarantee. You are responsible for complying with
applicable law.

Private submission does not imply a particular acknowledgement, fix, publication, credit, or
embargo timeline. If a report is taken up, any coordination will be handled through its GitHub
Private Vulnerability Reporting thread.
