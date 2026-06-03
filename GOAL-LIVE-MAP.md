# Autonomous Goal Prompt — Working Map + Intro + Playable Tested Core Loop

## Context
- Repo path: `/home/bayarddevries/metis-trail-game`
- Live URL: https://bayarddevries.github.io/metis-trail-game/
- Current state: live but buggy. Map not rendering. Core loop incomplete. Intro exists but needs verification.
- Build tooling: pnpm with esbuild. If pnpm blocks on build-script approval, run `pnpm approve-builds esbuild` before building.

## Objective
Get a working, browser-tested version with a functional map, a complete intro that drops the player into the world, and a full core game loop (intro → travel → event → settlement → repeat → end screen) deployed to GitHub Pages.

## Hard Guardrails
1. Do NOT create new repos, rename repos, or delete any repo without explicit approval.
2. Do NOT fabricate historical content. If a citation is missing, mark it `TODO` and leave the field blank.
3. Do NOT modify `metis-research-wiki` unless pulling a specific cited fact into `src/data/sources/`.
4. Do NOT manually edit files under `dist/`. Build with `pnpm run build` or `node scripts/build.mjs`.
5. Do NOT change `.github/workflows/deploy.yml` unless the current workflow is demonstrably broken and you can fix it with evidence.
6. Always browser-verify before declaring anything "done." Use the browser tools or open the built `dist/index.html` locally first.
7. Keep source changes under `src/` unless the task explicitly requires otherwise.

## Execution Steps
1. Intro screen verification
   - Confirm intro overlay displays with title, flavor text, and "Begin Journey" button.
   - Confirm clicking Begin dismisses intro and enters the game state cleanly.
   - Confirm intro is mobile-friendly (readable font, button spacing).

2. Map & init
   - Diagnose why Leaflet/map is not rendering (missing CSS/JS, mount timing, missing container, etc.).
   - Fix the map initialization and ensure trail nodes + player marker render.
   - Confirm player marker starts at Fort Garry and moves as travel advances.

3. Core loop verification
   - Start game → advance through intro → click Travel → advance date and position.
   - Events should fire with dice roll, choices, and source citations where available.
   - Settlements should show Trade / Repair / Rest actions.
   - Camps should allow rest/repair on trail.
   - Inventory/Cart screen should show contents.
   - Win/lose conditions should trigger and display summary screen.

4. UI polish & mobile
   - Test on mobile viewport: touch targets ≥ 48px, readable text, no horizontal scroll.
   - Verify no console errors or missing assets on live site.
   - Check `legacy-docs/` for any useful UI research files, but do not copy broken/old HTML into live game.

5. Build & local test
   - Run build.
   - Open `dist/index.html` in browser; confirm no console errors.
   - Test full playthrough at least once (start to end).

6. Live deploy
   - Commit with conventional messages (`feat:`, `fix:`, `chore:`) and push to `main`.
   - Wait for GitHub Pages deploy to complete.
   - Open the live URL and run a console + interaction check.

7. Halt conditions
   - If you hit a blocker you cannot resolve in 2 attempts, stop.
   - Log exact reproduction steps and evidence in `ISSUES.md`.
   - Do not repeatedly retry the same failed fix.

## Definition of Done
- Intro screen flows into gameplay with one click.
- Map renders nodes and player position at start.
- Travel, events, settlements, crew/cart screens, and end screens all work.
- Playthrough completes without JavaScript console errors on live site.
- Mobile viewport tested and usable.
- If any historical event lacks a source, it is marked `TODO` and left out of the final version.
