# AGENTS.md

Shared Renovate preset for the agntn org. This is not a TypeScript package.

## Status

- Private shareable config repository.
- Consumers extend `local>agntn/_renovate`, which resolves `default.json`.
- Mend Renovate is installed on the `agntn` org. It keeps the Dependency Dashboard in issue #1.

## Rules

- Change inherited policy in `default.json`. Every consumer picks it up on the next Renovate run.
- Keep `renovate.json` pointing at this preset. Do not fork policy there.
- Do not add Dependabot version updates in consumers that extend this preset.
- Do not scaffold an npm package unless the task is preset validation in CI.
- Issues stay enabled. Renovate puts the Dependency Dashboard there.
- The Renovate GitHub App must keep read access while the repo is private.

## Layout

```
default.json   - inherited preset
renovate.json  - this repository
README.md      - how to extend
LICENSE        - MIT
```
