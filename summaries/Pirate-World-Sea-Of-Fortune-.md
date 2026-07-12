# Pirate-World-Sea-Of-Fortune-

**Repository:** <https://github.com/JaronKBragg7337/Pirate-World-Sea-Of-Fortune->

**Category:** Games & 3D Worlds · **Status:** 🟠 LIVE (degraded) · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## Live systems

- **Vercel project pirate-world-sea-of-fortune** — <https://vercel.com/kylerbragg73-2101s-projects/pirate-world-sea-of-fortune> — latest 2 prod deploys ERROR; last good build live
- **Supabase 'Pirate World Seas of Fortune'** — <https://supabase.com/dashboard/project/uxyrwbdknvykgvxkigzh> — ACTIVE_HEALTHY — 6 tables, 0 rows

## What it actually is

A 3D open-world pirate naval-combat game: Three.js renderer, React 18 + TypeScript + Vite front-end, Cannon.js physics (buoyancy, ballistics), Supabase backend (Postgres + Realtime + Auth), deployed on Vercel. 5 ship classes, crew management, dynamic wind, broadside combat, AI enemies (British patrols, skeleton galleons, merchants), 12 procedural islands, day/night cycle, leaderboard, session-based multiplayer lobby, mobile touch controls.

## Verification notes

LIVE-VERIFIED WITH A PROBLEM: the two newest production deployments (commit 'Character gameplay: walk on ship, crew NPCs, hull damage…', 2026-07-11) are in ERROR state on Vercel; the site serves the previous READY build ('Add mobile touch controls'). The newest gameplay commit is NOT live. Supabase project ACTIVE_HEALTHY with schema deployed (players, player_ships, crew_members, scores, game_sessions, session_players) but all tables empty — persistence wired, unused so far.

## Key files

`src/App.tsx, src/ (game code), vercel.json, .env.example, package.json`

## Notes for AIs (Zeus and others)

First actionable task for any AI here: fix the failing Vercel build of the 'Character gameplay' commit (check build logs; prior failures were npm/lockfile/Node-version related and were fixed by pinning Node 20 / switching package managers).

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
