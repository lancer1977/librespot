# repo-state.md

- repo: librespot
- path: /mnt/data/lancer1977/code/librespot
- updated_utc: 2026-06-24T00:00:00Z
- canonical_tracker: GitHub Issues
- operational_surface: Repo-local docs
- stable_map: docs/index.md
- native_validation: bash scripts/validate.sh

## Current policy

- Durable work lives in GitHub Issues.
- Repo-local docs stay compact and point to the current entrypoints.
- Generated or disposable artifacts belong under `.devstudio/`.
- Local container-packaging scratch files belong under `.build-image/` and stay
  ignored unless promoted into a maintained deploy workflow.
