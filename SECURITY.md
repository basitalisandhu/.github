# Security Policy

This is the default security policy for every repository under [github.com/basitalisandhu](https://github.com/basitalisandhu). A repository that ships its own `SECURITY.md` overrides this one.

Security is the subject of these projects, so reports are welcome and taken seriously. Thank you for taking the time.

## Reporting a vulnerability

**Please do not report security problems through public issues, discussions or pull requests.**

1. Open the affected repository on GitHub.
2. Go to **Security**, then **Advisories**, then **Report a vulnerability**.
3. Fill in the form. Only you and the maintainer can see the report.

If private vulnerability reporting is not enabled on that repository, open a public issue that says only "security report, please enable private reporting" and nothing else. It will be enabled and you will be asked to resubmit privately.

<!-- Optional email channel. Fill in and uncomment when ready:
If you cannot use GitHub, email security@<domain> and encrypt with the PGP key below.
-->

### What to include

- The repository, version, commit or package release affected.
- A description of the issue and its impact: what an attacker could do.
- Steps to reproduce, a proof of concept, or a failing test.
- Any suggested fix, if you have one.
- How you would like to be credited, or whether you prefer to stay anonymous.

## What happens next

| Step | Target |
|---|---|
| Acknowledgement that the report was received | 3 business days |
| Triage, severity assessment and a first reply with next steps | 7 days |
| Fix or mitigation for confirmed issues | depends on severity; critical issues first |
| Public disclosure | 90 days after the report, or when a fix ships, whichever is earlier |

## Coordinated disclosure

These projects follow a 90-day coordinated disclosure policy:

- The report stays private while a fix is prepared.
- Once a fix is released, a GitHub Security Advisory is published with a CVE where appropriate, release notes name the issue, and the reporter is credited unless they ask otherwise.
- If no fix is available after 90 days, the reporter is free to publish. An extension can be agreed when a fix is close or when downstream users need more time, and the reporter will always be told why.
- Issues under active exploitation may be disclosed earlier so users can protect themselves.

## Scope

In scope:

- Source code in the repositories, including GitHub Actions workflows and release tooling.
- Packages published from these repositories (npm, PyPI, container images) and their build pipeline.
- Documentation that would lead users into an insecure configuration.
- For dataset repositories: entries that leak non-public personal data.

Out of scope:

- Vulnerabilities in third-party dependencies with no demonstrated impact on these projects. Report those upstream, and feel free to open a regular issue so the dependency can be bumped.
- Findings from automated scanners without a working reproduction.
- Denial of service by volume, social engineering, or physical attacks.
- Anything that requires an already-compromised host, administrator account or signing key.

## Safe harbour

Good-faith security research under this policy is welcome. If you make a good-faith effort to follow it, your research is considered authorised, the maintainer will not take legal action against you, and will help if a third party raises a complaint about research done under this policy. Please stay within scope, do not access, modify or exfiltrate data that is not yours, and stop and report as soon as you have confirmed an issue.

There is no bug bounty programme at this time.

## Encrypted reports

A PGP key for encrypted reports will be published here.

<!-- Paste the fingerprint and the ASCII-armoured public key below when ready.

-----BEGIN PGP PUBLIC KEY BLOCK-----

-----END PGP PUBLIC KEY BLOCK-----
-->

## Supported versions

Unless a repository says otherwise, only the latest release on the default branch receives security fixes.
