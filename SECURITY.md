# Security policy

This is the default security policy for every repository under [github.com/basitalisandhu](https://github.com/basitalisandhu). A repository that ships its own `SECURITY.md` overrides this one; its scope section says what that project treats as a vulnerability.

Security is the subject of these projects, so reports are welcome and taken seriously.

## Supported versions

Unless a repository says otherwise, only the latest release receives security fixes.

## Reporting a vulnerability

Please use GitHub's private vulnerability reporting on the affected repository (**Security** tab, **Report a vulnerability**) rather than a public issue, discussion or pull request. Only you and the maintainer can see the report. Private reporting is switched on for every public repository of this account.

Include:

- the repository and the version, release or commit affected;
- what an attacker could do, and under which conditions;
- the command you ran or a minimal configuration, proof of concept or failing test that reproduces it;
- a suggested fix, if you have one;
- how you would like to be credited, or that you prefer to stay anonymous.

Do not include real credentials or personal data; a redacted example is enough.

## What happens next

You will get an acknowledgement within 7 days and a fix or a mitigation plan within 30 days for confirmed issues. Critical issues come first. Credit is given in the release notes and the advisory unless you prefer otherwise.

## Coordinated disclosure

- The report stays private while a fix is prepared.
- Once a fix is released, a GitHub Security Advisory is published (with a CVE where appropriate) and the release notes name the issue.
- If no fix is available 90 days after the report, you are free to publish. An extension can be agreed when a fix is close, and you will always be told why.
- Issues under active exploitation may be disclosed earlier so users can protect themselves.

## Scope

In scope:

- Source code in the repositories, including GitHub Actions workflows and release tooling.
- Packages and actions published from these repositories, and their build pipeline.
- Documentation that would lead users into an insecure configuration.
- For dataset repositories: entries that leak non-public personal data.

Not a vulnerability (please open a normal issue instead):

- A missed finding: a risky configuration, skill or file that a scanner or linter here does not report. Include a minimal fixture so a rule can be added.
- Vulnerabilities in third-party dependencies with no demonstrated impact on these projects. Report those upstream; an issue asking for the bump is welcome.
- Output of automated scanners without a working reproduction.

Out of scope: denial of service by volume, social engineering, physical attacks, and anything that needs an already compromised host, administrator account or signing key.

## Safe harbour

Good-faith security research under this policy is welcome and considered authorised. The maintainer will not take legal action against you for it, and will help if a third party complains about research done under this policy. Stay within scope, do not access, change or exfiltrate data that is not yours, and stop and report as soon as you have confirmed an issue.

There is no bug bounty programme.
