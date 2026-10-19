# release-readiness-audit

Staging repository for a **release-readiness audit** of a Node.js command-line tool before it is open-sourced.

This repo tracks the work required to make the tool safe to publish:

- **Pinned dependencies under audit:** `lodash@4.17.15` and `minimist@1.2.0`
- **CI:** a GitHub Actions workflow runs on every push, writes a short build report, and uploads it as the `audit-report` artifact
- **Security findings:** advisories from GitHub's security advisory database affecting the pinned versions are tracked in issues
- **Security policy:** a documented policy for privately reporting vulnerabilities

See the [security policy](SECURITY.md) (once merged) for how to report vulnerabilities.
