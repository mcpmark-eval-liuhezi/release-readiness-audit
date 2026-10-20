# HANDOVER — Release Process

> For the incoming owner. Written by HeziLiu as part of the end-of-week release-process handover.
> Tracking issue: [#5 — Release readiness master checklist](https://github.com/mcpmark-eval-liuhezi/release-readiness-audit/issues/5)

## Where things stand

This repository is the staging ground for the release-readiness audit of a Node.js CLI tool before it is open-sourced.

- **Master checklist:** #5, with three sub-issues covering the handover workstreams
- **Security audit:** #1 (parent), #2 (lodash 4.17.15), #3 (minimist 1.2.0)
- **Security policy:** #4 adds `SECURITY.md` (private reporting first, 90-day response aim)
- **CI:** GitHub Actions runs on every push, writes a build report, and uploads the `audit-report` artifact

## Handover workstreams

1. **Verify CI pipeline health** — #6
   - Confirm the Actions workflow runs on every push and produces a downloadable `audit-report` artifact
   - Check `main` for failing or stale workflow runs
   - Agree who is contacted if CI breaks after the handover
2. **Review security and dependency alerts** — #7
   - lodash 4.17.15: GHSA-r5fr-rjxr-66jc (high) — patch in 4.18.0
   - minimist 1.2.0: GHSA-xvch-5gv4-984h (critical, patch 1.2.6) and GHSA-vh95-rmgr-6w4m (medium, patch 1.2.3)
   - Record any accepted risks and why they are acceptable
3. **Publish handover notes** — #8 (this document)
   - This PR merges these notes to `main`; close #8 once it lands

## Known open items for the incoming owner

- Dependency upgrades (`lodash` → 4.18.0+, `minimist` → 1.2.6+) are still pending; see #2 and #3
- `SECURITY.md` PR (#4) is open and awaiting review/merge
- Community discussions may be enabled in this repo after the handover; decide the category structure then

## Operational notes

- No secrets live in this repository; credentials are held by the outgoing owner and must be transferred and rotated out-of-band before the end of the handover week
- Push access to this repo requires org membership in `mcpmark-eval-liuhezi`
