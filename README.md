# smolla-analytics

Read-side analytics service owning event engagement metrics, link click-through, question volume, attendance curves, and tenant-level rollups.

## Repository layout

```
backend/
    src/Smolla.Analytics.Host/   ASP.NET Core web host
    tests/Smolla.Analytics.Tests/ xUnit unit + integration tests
```

## Local development

```
cd backend
dotnet restore
dotnet build
dotnet test
dotnet run --project src/Smolla.Analytics.Host
```

## Workflows

- `ci.yml` — runs on every push and PR
- `deploy-prod.yml` — runs on push to `main`
- `deploy-staging.yml` — runs on push to `develop`
- `deploy-test.yml` — manual dispatch for shared test slot
- `release-please.yml` — opens release PRs based on conventional commits
- `sync-main-to-develop.yml` — back-merges hotfixes from `main` into `develop`

## Versioning

Managed by `release-please`; the canonical version lives in `version.txt` and is propagated to project files on each release.

## Licence

GNU Affero General Public License v3.0 — see [LICENSE](LICENSE).

Copyright (c) 2026 Adam Salisbury.
