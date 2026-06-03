# Changelog

All notable changes are documented here. Format loosely follows Keep a Changelog.

## 2026-06-03 — Initial clean repo (metis-trail-game)

### Added
- Clean repo created at `metis-trail-game`, forked from `metis-trail-v2`
- All core game code: `src/core`, `src/data`, `src/systems`, `src/ui`
- esbuild bundler in `scripts/build.mjs`
- GitHub Actions Pages deploy workflow
- `data/` folder with source research from v1 repo
- README, CHANGELOG, .gitignore

### Removed (from v2 clutter)
- `.claude/` impeccable skill (80+ files — not game-related)
- Raw research scrapes (moved to `metis-research-wiki`)
- Stale build artifacts (`docs/`, multiple `app.v*.js`, trigger files)
- `node_modules/`

### Notes
- v2 source: https://github.com/Bayarddevries/metis-trail-v2
- v1 site: https://bayarddevries.github.io/metis-trail/