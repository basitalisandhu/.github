# .github

Default community health files and shared CI for every repository under [github.com/basitalisandhu](https://github.com/basitalisandhu).

GitHub applies the files in this repository to any repository of the account that does not have its own copy. A repo-local `SECURITY.md`, `CONTRIBUTING.md`, issue template or similar always wins.

## What is here

| File | Purpose |
|---|---|
| [SECURITY.md](SECURITY.md) | How to report vulnerabilities: private advisories, 90-day coordinated disclosure |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute: issues, commits, pull requests, datasets |
| [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) | Contributor Covenant 2.1 |
| [SUPPORT.md](SUPPORT.md) | Where to get help and what to expect |
| [FUNDING.yml](FUNDING.yml) | Sponsor button |
| [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) | Bug report and feature request forms, plus links for security and support |
| [PULL_REQUEST_TEMPLATE.md](PULL_REQUEST_TEMPLATE.md) | Pull request checklist |
| [.github/workflows/reusable-security.yml](.github/workflows/reusable-security.yml) | Reusable security baseline: CodeQL, gitleaks, dependency review, OpenSSF Scorecard |
| [workflow-templates/](workflow-templates/) | Starter workflow that calls the baseline |

## Using the security baseline in a repository

Add `.github/workflows/security.yml`:

```yaml
name: Security
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  schedule:
    - cron: "23 4 * * 1"
  workflow_dispatch:

permissions:
  contents: read

jobs:
  baseline:
    uses: basitalisandhu/.github/.github/workflows/reusable-security.yml@main
    permissions:
      actions: read
      contents: read
      security-events: write
      id-token: write
      pull-requests: write
    secrets: inherit
```

Inputs (all optional):

| Input | Default | Meaning |
|---|---|---|
| `codeql` | `true` | Run CodeQL with the `security-extended` query suite |
| `codeql-languages` | `""` (auto-detect) | Comma-separated CodeQL languages, for example `javascript-typescript,python` |
| `gitleaks` | `true` | Scan the full git history for secrets |
| `dependency-review` | `true` | Fail pull requests that add vulnerable dependencies (runs on `pull_request` only) |
| `dependency-fail-on-severity` | `high` | Lowest severity that fails dependency review |
| `scorecard` | `true` | Run OpenSSF Scorecard on the default branch and upload results to code scanning |

Notes:

- Scorecard results go to the repository's code scanning tab. Publishing to the public Scorecard API (needed for the badge) requires the standalone official Scorecard workflow in each repository, because that service verifies the workflow file and does not accept results from reusable workflows.
- `secrets: inherit` only matters for an optional `GITLEAKS_LICENSE`. Personal accounts do not need one.
- Workflow templates in `workflow-templates/` are only surfaced by GitHub's "New workflow" page for organizations. For a personal account, copy the snippet above.
- Pin the `@main` reference to a tag or commit SHA if you need reproducible CI; Dependabot keeps pinned references current.

## Keeping it honest

These files are the public version of how the projects are run. If something here does not match what actually happens in a repository, that is a bug: open an issue.
