# SYL-Full-Game

**Repository:** <https://github.com/JaronKBragg7337/SYL-Full-Game>

**Category:** Games & 3D Worlds · **Status:** 🟢 LIVE · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## Live systems

- **Play on Heartbeat** — <https://heartbeatobservatory.com/games/syl/> — documented live route on the verified-live Heartbeat site

## What it actually is

'Space You Land' — the playable web foundation of a world-scale space game: multiple planets with real surface→space→surface traversal (no loading screens or teleports), a modular piece-by-piece ship, factions, persistence, phone controls, plus a separate desktop.html RTX-class route with PBR terrain, GLB models, HDR lighting and bloom. Includes its own test suite (143/143 scene validations passing at v0.4.0) and a Node zero-install local server. Written explicitly as a bridge foundation for other agents (Claude/Codex/Opus) to continue — AGENTS.md is the contract.

## Verification notes

Cloned and inspected; active development (last commit 2026-07-09, v0.4.0 form-language pass). Live route sits on heartbeatobservatory.com which is Vercel-verified READY. This repo is the living blueprint for the eventual Unreal/Unity SYL (see spaceyouland/Kurearthis).

## Key files

`AGENTS.md (read first), VISION.md, ROADMAP.md, DECISIONS.md, HANDOFF.md, src/main.js, src/desktopMain.js, test/run_tests.mjs`

## Notes for AIs (Zeus and others)

AGENTS.md + HANDOFF.md + DECISIONS.md are a complete multi-agent collaboration protocol. The scene-validation test harness (test/run_tests.mjs) shows how the project verifies 3D work without a human looking at it.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
