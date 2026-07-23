# mlaify

Small, security-first open-source tools by [Matt D.](https://matthewd.xyz) — built local-first, documented next to the code, and honest about their status.

Everything here follows the same [build principles](https://matthewd.xyz/principles/): practical systems for real operator workflows, explicit status you can plan around, security architecture treated as design work rather than paperwork, composable module boundaries, and documentation that lives in the repo it describes.

---

## AttackMap

**[github.com/mlaify/AttackMap](https://github.com/mlaify/AttackMap)** · docs at **[docs.matthewd.xyz](https://docs.matthewd.xyz)** · overview at **[matthewd.xyz/attackmap](https://matthewd.xyz/attackmap/)**

A **local-first, open-source defensive security analysis engine**. Point it at a repository and it reads the source, reconstructs the attack surface from first principles, and produces prioritized, evidence-anchored findings — **without sending code off-device and without a cloud account**.

It answers the four questions a security reviewer asks at the start of a review:

1. **What is exposed?** — routes, external calls, data egress, secrets in the wrong places.
2. **What does this look like to an attacker?** — entry points, data stores, trust crossings.
3. **What are the realistic attack chains?** — plausible paths with steps and impact, not isolated findings.
4. **What should I fix first?** — prioritized by practical risk reduction, with evidence attached.

> AttackMap is a **defensive** tool. Its output is oriented entirely toward remediation and improved posture — no exploit code, offensive payloads, or actionable attack instructions.

### What it does

- **Modular analyzer ecosystem** — analyzer plugins across Python, Node/TypeScript, Go, Java/Spring, .NET, Rust, PHP, C/C++, Terraform & IaC (Docker/Compose/GitHub Actions), and AT Protocol; each a separate pip-installable package discovered at runtime. `attackmap suggest` recommends the right set for a repo.
- **Data-flow / injection detection** — an import-graph taint pass (Python, JS/TS, Go, PHP) traces request-to-sink reachability: SSRF, SSTI, NoSQL injection, unsafe deserialization, code/command execution, open redirect, dynamic file open — sanitizer- and parameterized-SQL-aware.
- **Broken object-level authorization (BOLA/IDOR)**, insecure crypto, web-hardening gaps, CI-workflow security, and **novel vulnerability-class detectors** (prototype pollution, mass assignment, JWT weakness, XXE, ReDoS, GraphQL exposure) — each ATT&CK-mapped and anchored on concrete evidence.
- **Anomaly & invariant mining** — surfaces the odd-one-out among sibling routes, and the site that violates an invariant its peers uphold, signature-free.
- **AI-assisted review, verified hard** — an optional LLM layer generates a narrative defensive review and hunts for novel exploit-chain hypotheses, each adjudicated against the real source by an N-vote verifier. Claude or OpenAI/Codex, API key or subscription CLI, all behind one pluggable interface.
- **Fleet / cross-repo analysis** — scan multiple services at once and surface the bugs that live in the *seams*: contract links between callers and routes, confused-deputy flows across a boundary, and trust-assumption gaps where neither side enforces.
- **CI-native** — SARIF for GitHub Code Scanning, a PR-comment bot, and a baseline diff mode that can fail a build on newly-introduced HIGH findings.

### Install

```bash
pip install "attackmap[all]"
```

```bash
brew install mlaify/tap/attackmap
```

Also published as a container image on GHCR (`ghcr.io/mlaify/attackmap`). Requires Python 3.11+. See the [getting-started guide](https://matthewd.xyz/attackmap/getting-started/) for a full walkthrough.

**Status: beta.** It carries an honest status and a "what's not yet hardened" section — beta means beta.

---

## Principles, in one breath

- **Real workflows over demos.** The defensive review is the artifact you hand a reviewer, and it runs against the repo you already have.
- **Status you can trust.** Explicit status badges and known-limits sections; no overselling a `v0.x`.
- **Security as design.** Threat models and exploitability scoring shape the pipeline — they aren't generated after the fact.
- **Composable boundaries.** Analyzers are independent packages; LLM providers are pluggable.
- **Docs next to code.** Canonical documentation lives in each repo. If this profile disagrees with a repo, **the repo is correct**.

## Contributing & security

Contributions and issues are welcome on the individual project repos. To report a security vulnerability, follow the `SECURITY.md` policy in the relevant repository rather than opening a public issue.

## Elsewhere

- **Site:** [matthewd.xyz](https://matthewd.xyz)
- **Docs:** [docs.matthewd.xyz](https://docs.matthewd.xyz)
- **Author:** [Matt D. on GitHub](https://github.com/mdavistffhrtporg) · [Bluesky](https://bsky.app/profile/matthewd.xyz)

_Licensed per repository (AttackMap is MIT). This profile is maintained alongside the mlaify projects._
