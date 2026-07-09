# Code Health

## Current Validation

- `bash scripts/validate.sh`
- Upstream-style deep check: `./test.sh` when `cargo-hack` and native audio
  development packages are available.

`scripts/validate.sh` runs locked dependency fetch, formatting, workspace
`cargo check --all-targets`, workspace tests, optional `cargo audit`, and
DevStudio validation.

## CI and Artifacts

- `.github/workflows/build.yml` builds and tests on Linux and Windows, then
  uploads the debug `librespot` binary as a GitHub Actions artifact.
- `.github/workflows/quality.yml` runs formatting and clippy feature checks.
- Release workflows live in `.github/workflows/release.yml` and
  `.github/workflows/prepare-release.yml`.

## Local Generated Artifacts

- `target/` is Cargo output and stays ignored.
- `.devstudio/runtime/` is generated DevStudio output and stays ignored.
- `.build-image/` is treated as local container-packaging scratch space; do not
  treat the copied `librespot-binary` there as source.

## Follow-Ups

- Install `cargo-audit` locally if dependency advisory checks should be enforced
  on every workstation.
- Install `cargo-hack` plus native audio development packages before running the
  full upstream `./test.sh` feature matrix locally.
