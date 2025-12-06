---
scope:
  - ".github/workflows/*.yaml"
last_updated: "2025-12-06T02:00:43Z"
---

# Domain

## Glossary

| Term | Definition |
|------|------------|
| workflow_call | GitHub Actions trigger that allows workflows to be called by other workflows |
| CHECK_NAME | Environment variable defining the status check context displayed in PR checks |
| ignoreErrors | Input parameter that allows workflows to succeed despite validation failures |
| OIDC | OpenID Connect - authentication method for AWS that eliminates static credentials |
| SHA pinning | Referencing actions by commit SHA instead of version tag for security |
| Semantic versioning | Version numbering based on commit types (feat=minor, fix=patch, breaking=major) |
| Conventional commits | Commit format with type prefix (feat:, fix:, chore:, etc.) |

## Business Rules

- All consumer-facing workflows must accept an `ignoreErrors` input for flexibility
- All PR-based workflows must set pending/success/failure status checks via GitHub API
- All third-party actions must be pinned by SHA with version comment
- Default versions must be provided for all configurable tool versions
- Workflows must support monorepo structures via directory input parameters
