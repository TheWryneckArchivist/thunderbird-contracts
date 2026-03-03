# thunderbird-contracts

Canonical protobuf contracts for Thunderbird services and domain events.

## Services

- AuthService
- ProfileService
- CatalogService
- SessionService
- OfflineSyncService
- ModerationService

## Events

- SessionCreated
- SessionUpdated
- PackPublished
- ModerationFlagged
- OfflineDeltaAccepted
- OfflineDeltaPartiallyAccepted
- OfflineDeltaRejected

## Tooling

- `buf lint`
- `buf breaking --against '.git#branch=main'`
- `buf generate`

## Outputs

- C#: `Thunderbird.Contracts` (NuGet)
- TypeScript: `@thunderbird/contracts` (npm)
- Python: `thunderbird-contracts` (PyPI)

## Publishing

- CI validation: `.github/workflows/contracts-ci.yml`
- Tagged publish pipeline: `.github/workflows/contracts-publish.yml`
- Private feed setup: `docs/PRIVATE_FEEDS.md`
