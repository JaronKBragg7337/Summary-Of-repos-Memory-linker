# fable-survival

**Repository:** <https://github.com/JaronKBragg7337/fable-survival>

**Category:** Games & 3D Worlds · **Status:** 🟢 LIVE · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## Live systems

- **fable-survival.vercel.app** — <https://fable-survival.vercel.app> — Vercel production READY, last deploy 2026-07-09
- **On Heartbeat** — <https://www.heartbeatobservatory.com/games/fable-survival/> — mirrored into the Heartbeat town

## What it actually is

A DayZ-inspired, mobile-first browser survival game built with Three.js + Vite. Safe-zone spawn, trader economy, tree/rock harvesting, hunger/thirst, infected enemies, base building (floors/walls/doors/campfires/storage), repairable drivable cars, day/night cycle, save system with optional cloud saves, and an in-game AI chat (api/aichat.js) where Claude can act on live game state through a bounded, key-gated tool set (give_item/heal/give_coins/set_time/teleport).

## Verification notes

LIVE-VERIFIED: Vercel production READY (2026-07-09, 'Shaped characters… real car model…'). CAUTION: the companion Supabase project 'fable-survival' (ukguppzfpvdcemyxzdbn) is INACTIVE/paused — the game front-end is live but cloud-save/DB features will fail until the project is restored. Local saves unaffected.

## Key files

`src/main.js, src/world.js, src/building.js, src/vehicles.js, api/aichat.js, HEARTBEAT_SYNC_PROMPT.md, PLAYER_FEEDBACK.md`

## Notes for AIs (Zeus and others)

api/aichat.js is a working example of an AI acting on a live game via a small validated tool schema. HEARTBEAT_SYNC_PROMPT.md documents the mirror-deploy protocol to Heartbeat. Flag to operator: restore the paused Supabase project if cloud saves are wanted.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
