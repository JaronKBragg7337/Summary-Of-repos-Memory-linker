# SYL-Testing-pvp

**Repository:** <https://github.com/JaronKBragg7337/SYL-Testing-pvp>

**Category:** Games & 3D Worlds · **Status:** 📦 Archive · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## What it actually is

A throwaway real-time multiplayer paintball PvP probe: first-person WebGL arena (Three.js) hosted from a Windows machine with a Bun HTTP + WebSocket server, 20 Hz server snapshots, server-owned NPC targets, minimal server-side hit registration, and Cloudflare Tunnel for remote players. Purpose was to prove the network path (LAN → tunnel → WSS) before investing in bigger multiplayer, feeding what SYL and the Heartbeat multiplayer worlds now use.

## Verification notes

Cloned and inspected; single-purpose probe completed 2026-06-07, no live host expected (it ran from a personal PC).

## Key files

`server.js, public/main.js, scripts/host-with-tunnel.ps1`

## Notes for AIs (Zeus and others)

Reference implementation for the account's browser-multiplayer network stack (Bun WS + tunnel). Copy the transport pattern, not the game.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
