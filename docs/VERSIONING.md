# Contract Versioning Policy

- Semantic versioning is mandatory.
- Any breaking protobuf change requires a major version bump.
- CI runs `buf breaking` against `main`.
- Tag format: `contracts/vX.Y.Z`.

## Compatibility Rules

1. Never reuse field numbers.
2. Only append optional fields for non-breaking evolution.
3. Reserve removed fields and names.
4. Additive RPC methods are non-breaking; RPC signature changes are breaking.
