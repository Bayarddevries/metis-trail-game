# Métis Trail

An educational web game about the 1878 Carlton Trail journey — built with vanilla ESM, esbuild, and Vitest. Offline-first, no framework, single-page output.

**Live:** https://bayarddevries.github.io/metis-trail-game/

## About

Travel the Carlton Trail from Fort Garry (Winnipeg) toward Fort Edmonton in 1878. Manage supplies, navigate hazards, make choices, and encounter historically-grounded events drawn from primary sources. Every event and location is sourced.

This is a short browser game focused on getting the game loop right. A larger, more ambitious game is a separate future project.

## Repo layout

| Path | Purpose |
|------|---------|
| `src/main.js` | Browser entry point + bootstrap |
| `src/systems/` | Game logic (engine, events, scoring, travel) |
| `src/ui/` | Rendering, overlays, theme, persistence, debug |
| `src/data/` | Game data — nodes, items, events, source citations |
| `src/core/` | Constants, calendar, PRNG, schema |
| `scripts/build.mjs` | esbuild bundler → `dist/app.js` + `dist/index.html` |
| `data/` | Source research material (KML, CSV, reference text) |
| `.github/workflows/deploy.yml` | GitHub Pages deploy on push to `main` |

## Working on the game

1. Read this file, then `CHANGELOG.md` for recent work
2. Make changes in `src/` — **do not touch `dist/` directly**
3. Build: `npm run build` → open `dist/index.html` in a browser
4. Conventional commits only

### Rules

- Offline-first: final output must work without a server
- Every historical claim needs a source citation. If you can't cite one, mark it as a `TODO`
- Never overwrite the established tone without explicit direction

## Historical sources

All game content is rooted in primary-source research. Source citations accompany nodes and events. The research wiki lives at **bayarddevries/metis-research-wiki** — raw research, source documents, and historical analysis. This repo's `data/` folder holds reference copies of key source material for close-at-hand use during development.