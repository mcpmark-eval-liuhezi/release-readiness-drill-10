# Release Sign-Off Audit Checklist

Use this checklist to walk the release sign-off audit trail. Every sign-off must be recorded against this checklist, and each sign-off point must be individually traceable from the checklist to the evidence attached in the pull request review comments.

## Scope & ownership

- **Owner:** Release Management
- **Applies to:** All production releases (hotfixes, patch releases, minor and major versions)
- **Review cadence:** Every release, no exceptions

## Sign-off gates

### Gate 1 — Readiness scope and versions

| # | Check | Owner | Evidence | Status |
|---|-------|-------|----------|--------|
| 1.1 | Release scope is documented (what is in / out of scope) | Release Manager | Scope worksheet | Unverified |
| 1.2 | Release version is confirmed and matches the release plan | Release Manager | Release plan document | Unverified |
| 1.3 | Release branch is the branch specified in the release plan | Release Manager | Branch name in release branch output | Unverified |

### Gate 2 — Code completeness and stability

| # | Check | Owner | Evidence | Status |
|---|-------|-------|----------|--------|
| 2.1 | All yahoo design chores and extraction tasks from the release/2 sprint proposal are done on the release branch | Release Manager | Ticket state report | Unverified |
| 2.2 | No open PRs without an assigned owner | Release Manager | PR owner report | Unverified |
| 2.3 | Chore documentation / test task is complete and attached | Release Manager | PR description | Unverified |

### Gate 3 — Test evidence

| # | Check | Owner | Evidence | Status |
|---|-------|-------|----------|--------|
| 3.1 | CI is green on the release branch | Release Manager | CI report | Unverified |
| 3.2 | Smoke tests for the release branch are executed and results recorded | Release Manager | Smoke test results | Unverified |
| 3.3 | Full test suite has passed | Release Manager | Test results report | Unverified |

### Gate 4 — Distribution and monitoring

| # | Check | Owner | Evidence | Status |
|---|-------|-------|----------|--------|
| 4.1 | Granularity settings for reviews of all feature tiers are switched (SaaS Global xpresso experience reviewed) | Release Manager | Settings output | Unverified |
| 4.2 | Distribution list and review cadence are finalised | Release Manager | Distribution plan output | Unverified |
| 4.3 | Monitoring and observability dashboards are on standby | Release Manager | Dashboard readiness check | Unverified |

## Sign-off process

1. The **Release Manager** completes each gate row in this checklist.
2. Each gate owner records their evidence in the pull request comments.
3. **Production Management** reviews the completed checklist and signs off on the audit trail.
4. **Development** attests that the code still meets quality standards and that all features, including extraction tasks, are delivered.
5. Once all gates are verified, the checklist is marked complete and archived as the audit record for this release.

## Review comments (audit trail)

- Reviewer comments are captured here on the `drill/audit-trail` branch's pull request. Every sign-off is traceable to a review comment on the pull request.
- No review may be submitted as an approval, a change request, or a discarded draft that remains open.
- The final audit-trail review should be a **COMMENT review** that documents the checklist verification, not an APPROVE or REQUEST_CHANGES review.
