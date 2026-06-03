# Changelog

All notable changes are documented here. Format loosely follows Keep a Changelog.

## 2026-06-03 — Cleanup and consolidation

### Added
- All core game code under `src/core`, `src/data`, `src/systems`, `src/ui`
- GitHub Actions Pages deploy workflow
- Historical research archive under `research/` and `data/`
- Legacy plans and audit snapshots under `legacy-docs/`
- README, TODO, ISSUES, CHANGELOG restored from v2 repository history
- Issue templates under `.github/ISSUE_TEMPLATE/`
- Preview and playtest helpers under `scripts/`

### Fixed
- GitHub Pages enabled with GitHub Actions source
- CI workflow pinned and stabilized (pnpm workflow, esbuild/vitest versions)

### Changed
- Remaining build artifacts, lockfiles, and workspace configs cleaned up
- Docs unified under single live URL: https://bayarddevries.github.io/metis-trail-game/

## Notes
- v1 site baseline: https://bayarddevries.github.io/metis-trail/
