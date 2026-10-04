# Contributing

Thanks for your interest. These are the default contribution guidelines for every repository under [github.com/basitalisandhu](https://github.com/basitalisandhu). A repository may add its own `CONTRIBUTING.md` with project-specific setup; read that first when it exists.

## Ways to contribute

- Report bugs and propose features through the issue templates.
- Add or correct entries in the datasets (public, citable sources only).
- Write rules, policies, examples and docs.
- Review open pull requests. Reviews are contributions too.
- Report security issues privately: see [SECURITY.md](SECURITY.md). Never open a public issue for a vulnerability.

## Before you start

1. Search existing issues and pull requests so work is not duplicated.
2. For anything bigger than a small fix, open an issue first and describe the change. Agreeing on the approach early saves everyone time.
3. Issues labelled `good first issue` and `help wanted` are the best entry points.

## Development

Each repository's README has its own setup, test and lint instructions. The common expectations:

- The test suite passes locally before you open a pull request.
- New behaviour comes with tests. Bug fixes come with a regression test.
- Linters and formatters configured in the repo are clean (they also run in CI).
- No secrets, tokens, private keys or real credentials in code, tests, fixtures or commit history. CI runs secret scanning and will fail the build.

## Commits and pull requests

- Use [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, `chore:` and so on). Release notes are generated from them.
- Sign off your commits (`git commit -s`) to certify the [Developer Certificate of Origin](https://developercertificate.org/). Cryptographically signed commits (`git commit -S`) are appreciated.
- Keep pull requests focused. One change per PR is much easier to review than a bundle.
- Fill in the pull request template; the checklist is short on purpose.
- CI must be green. Repositories that call the shared security baseline (CodeQL, secret scanning, dependency review) run it on every pull request; the others run their own checks.

## Security-relevant changes

Changes to policy evaluation, credential handling, audit logging, cryptography, authentication or CI workflows get extra review. Please explain the threat you are addressing or the invariant you are preserving in the PR description, and add a test that pins the behaviour.

## Dataset contributions

For the incident dataset and similar data repositories:

- Only publicly documented events, with at least one primary source link.
- No speculation presented as fact; use the fields provided for confidence and open questions.
- No non-public personal data.
- Entries must validate against the repository's JSON schema (CI checks this).

## Licensing

By contributing you agree that your contribution is licensed under the licence of the repository you are contributing to (MIT, Apache-2.0 or CC BY 4.0, as stated in each repo).

## Code of conduct

These projects follow the [Contributor Covenant](CODE_OF_CONDUCT.md). Be kind, be direct, assume good intent.
