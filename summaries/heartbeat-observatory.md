# heartbeat-observatory

**Repository:** <https://github.com/JaronKBragg7337/heartbeat-observatory>

**Category:** Games & 3D Worlds · **Status:** 🟢 LIVE · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## Live systems

- **heartbeatobservatory.com** — <https://www.heartbeatobservatory.com> — Vercel production READY, last deploy 2026-07-11
- **Supabase 'Project Heartbeat'** — <https://supabase.com/dashboard/project/ygjpnvrwhkrowkrskftk> — ACTIVE_HEALTHY — 33 tables with real data

## What it actually is

A living 3D town on the web where humans and AI agents share one persistent world — the flagship live system of this account. Static Three.js front-end plus Vercel serverless functions (api/: aichat, pam-chat, pam-agent-heartbeat, ask, news, feedback, enrich-world-spaces) backed by the Supabase 'Project Heartbeat' database. It hosts sub-worlds (world2/, worlds-lab/, engine/, library/, social/, admin/, live-systems/) and embeds the other games (fable-survival, SYL) under /games/. Governed by docs/CHARTER.md ('reality > text; amend, don't obey'), SHELL.md, WORLD-STANDARD.md, METHOD.md — an explicit operating doctrine for AI collaborators.

## Verification notes

LIVE-VERIFIED: Vercel project 'heartbeatobservatory' production deployment READY (2026-07-11, commit 'Ship World Printer v2i modular parts'). Supabase project ygjpnvrwhkrowkrskftk ACTIVE_HEALTHY with 33 populated tables — world_props (55 rows), messages (25), ask_log (17), posts (9), world_characters (9), placements (9), plus the pam_* agent tables (pam_instances, pam_threads, pam_messages, pam_events, pam_action_ledger) that form a live agent control plane. This is a real running system, not a README claim.

## Key files

`docs/CHARTER.md, docs/METHOD.md, engine/, world2/main.js, api/*.js, supabase/pam-*.sql, TODO.md (live truth)`

## Notes for AIs (Zeus and others)

Read docs/CHARTER.md + METHOD.md first — they are written as briefing documents for AI workers. The pam_* Supabase tables and api/pam-agent-heartbeat.js are the live agent heartbeat/control plane an AI can plug into. TODO.md is the live task list.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
