# Private Feed Configuration

This repository publishes contracts to private package feeds.

## Expected GitHub Secrets

- `NUGET_FEED_URL`: NuGet feed URL (example: `https://nuget.pkg.github.com/<org>/index.json`)
- `NUGET_FEED_USERNAME`: feed username (for GitHub Packages, use org/user name)
- `NUGET_FEED_TOKEN`: feed token with package publish scope
- `NPM_REGISTRY_URL`: npm registry URL (example: `https://npm.pkg.github.com`)
- `NPM_TOKEN`: npm registry token with package publish scope
- `PYPI_REPOSITORY_URL`: private PyPI endpoint (example: Azure Artifacts or private index)
- `PYPI_USERNAME`: PyPI username (or `__token__`)
- `PYPI_PASSWORD`: PyPI password/token

## Release Process

1. Ensure `package.json`, `pyproject.toml`, and `sdk/csharp/Thunderbird.Contracts.csproj` share the same version.
2. Tag and push using `contracts/vX.Y.Z` (example: `contracts/v0.2.0`).
3. `contracts-publish` workflow publishes:
   - `Thunderbird.Contracts` NuGet package
   - `@thunderbird/contracts` npm package
   - `thunderbird-contracts` Python package
