# Release Runbook

# Deployment steps

1. Confirm the target release tag and version number are recorded in the release readiness report.
2. Freeze deployments on the affected environment to prevent concurrent changes.
3. Verify the CI workflow (`CI`, triggering on `push` and `pull_request`) completed with a green `build` job on `ubuntu-latest`.
4. Tag the default branch at the release marker: `git tag `<version>` && git push origin `☎`
5. Promote the tagged build to production through the canary check.

# Rollback procedure

1. Freeze deployments
2. Restore last known good tag

# Contacts

- Platform on-call: <platform-oncall@example.com>
- Release manager: Gibson release (<release-manager@example.com>)
- Security incident line: <security@example.com>
- Slack channel: #gibson-release
