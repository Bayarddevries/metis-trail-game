# Métis Trail

An educational web game about the 1878 Métis Carlton Trail journey — historically grounded, offline-first, and optimized for mobile browsers.

**Live:** https://bayarddevries.github.io/metis-trail-game/

## Repo layout

- `src/` — game source: core, systems, UI, data
- `scripts/` — build + run helpers
- `data/` — research references and map assets
- `research/` — archived primary-source research copies from earlier builds
- `legacy-docs/` — superseded plans, audits, and sample HTML snapshots
- `docs/` — supplementary notes and older session docs

## How to contribute

1. Start with `TODO.md` and `ISSUES.md` before editing anything.
2. Edit files under `src/`. Do not edit `dist/`.
3. Use `pnpm run build` and verify before pushing.
4. Follow conventional commits.
5. Every historical claim needs a citation in `src/data/sources/`. If it can't be sourced, mark it `TODO`.

## Non-negotiables

- Offline-first output
- Mobile-friendly first
- Historical accuracy over invention
