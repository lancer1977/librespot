# Project Atlas

`librespot` is a Rust workspace for a Spotify client library and Spotify
Connect receiver.

## Primary Surfaces

- Workspace manifest: `Cargo.toml`
- Main binary: `src/main.rs`
- Core protocol and Spotify integration crates: `core/`, `protocol/`,
  `metadata/`, `oauth/`, `connect/`
- Playback and discovery crates: `audio/`, `playback/`, `discovery/`

## Validation

- Standard local validation: `bash scripts/validate.sh`
- Full upstream-style matrix: `./test.sh` after installing `cargo-hack` and
  native audio development packages.

## Artifact Policy

GitHub Actions build jobs upload debug `librespot` binaries as artifacts. Local
Cargo output stays under ignored `target/`.
