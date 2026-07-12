# World-Printer-Lab-For-3D-Worlds

**Repository:** <https://github.com/JaronKBragg7337/World-Printer-Lab-For-3D-Worlds>

**Category:** Games & 3D Worlds · **Status:** 🟢 LIVE · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## Live systems

- **Vercel project world-printer-lab-for-3-d-worlds** — <https://vercel.com/kylerbragg73-2101s-projects/world-printer-lab-for-3-d-worlds> — production READY, last deploy 2026-07-11

## What it actually is

A standalone Three.js laboratory where a simulated 3D printer visibly fabricates world-building parts layer by layer — exact nozzle-tip deposition, hot-to-cool molten material progression, piece-by-piece slicing, a 26-family modular part catalog (structures, roads, vehicles, energy, flight), connector-aware snapping, and three printer sizes with real build envelopes. Parts print, then get picked up, snapped together, and placed into a persistent multiplayer world (Supabase-backed via the Heartbeat control plane). Deliberately kept separate from Fable Survival and SYL so printer mechanics are proven before integration; proven pieces are vendored into heartbeat-observatory.

## Verification notes

LIVE-VERIFIED: Vercel production READY (2026-07-11, 'Add modular world parts and real printer classes'). Deploy history shows the lab→ship pipeline into heartbeat-observatory working commit-for-commit (v2e→v2i).

## Key files

`src/main-current.js, src/runtime-guards.js, VERSION_INVENTORY.md, docs/HANDOFF_*.md, tools/mesh_to_layers.py`

## Notes for AIs (Zeus and others)

docs/HANDOFF_*.md files are per-session AI handoff logs — the working protocol for multi-AI development on this codebase. VERSION_INVENTORY.md maps which main-*.js is canonical.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
