# Live Systems Report — verified 2026-07-12

Checked directly against Vercel and Supabase (authenticated), not against READMEs.
The build sandbox's network policy blocked direct HTTP probes of github.io / vercel.app pages,
so page-level checks below come from platform deployment state instead.

## Vercel (team kylerbragg73-2101s-projects)

| Project | State | Notes |
|---|---|---|
| heartbeatobservatory | 🟢 READY (prod) | Last deploy 2026-07-11 "Ship World Printer v2i modular parts". Serves heartbeatobservatory.com. 7 node functions. |
| world-printer-lab-for-3-d-worlds | 🟢 READY (prod) | Last deploy 2026-07-11 "Add modular world parts and real printer classes". |
| fable-survival | 🟢 READY (prod) | Last deploy 2026-07-09. ⚠️ Its Supabase DB is paused (see below) — cloud saves will fail. |
| pirate-world-sea-of-fortune | 🟠 DEGRADED | **Latest 2 production deploys ERROR** (commit "Character gameplay: walk on ship, crew NPCs…", 2026-07-11, incl. one redeploy attempt). Site serves previous READY build "Add mobile touch controls". Newest gameplay is NOT live. |
| v0-engine-of-division-summary | 🟢 READY (prod) | v0-built companion site for The Engine of Division book. |
| v0-framing-lens-project | ⬜ No deployments | Project shell exists; Framing Lens app never shipped. |
| v0-ai-gateway-starter | ⬜ No deployments | Project shell; no matching repo in the account. |

## Supabase (org nwfiomgulfsvkalonrjs)

| Project | State | Contents |
|---|---|---|
| JaronKBragg7337's Project Heartbeat (`ygjpnvrwhkrowkrskftk`) | 🟢 ACTIVE_HEALTHY | 33 tables, populated: world_props (55), messages (25), ask_log (17), posts (9), world_characters (9), placements (9), people (9), plus the **pam_* agent control plane** (pam_instances, pam_devices, pam_threads, pam_messages, pam_events, pam_action_ledger, pam_device_tokens). RLS enabled on all tables. Backs heartbeatobservatory.com. |
| Pirate World Seas of Fortune (`uxyrwbdknvykgvxkigzh`) | 🟢 ACTIVE_HEALTHY | 6 tables (players, player_ships, crew_members, scores, game_sessions, session_players) — **all 0 rows**. Schema deployed, persistence not yet exercised. |
| fable-survival (`ukguppzfpvdcemyxzdbn`) | 🔴 INACTIVE (paused) | Game front-end is live on Vercel but this DB is paused — cloud-save features broken until restored. |

## GitHub Pages (documented, not probe-able from this sandbox)

- https://jaronkbragg7337.github.io/Free-Game-Hub/ (+ /creators/, /games/*) — repo has .nojekyll and full site structure.
- https://jaronkbragg7337.github.io/President-Sim/
- https://jaronkbragg7337.github.io/persistent-memory-substrate/ — cited by 6 repos.

## Empty repositories

- `physics-lab-sandbox` — zero commits, no branches.
- `EchosOrchestra` — zero commits, no branches.

## Action items surfaced by these checks

1. **Fix Pirate World's failing production build** — newest gameplay commit is not reaching players.
2. **Restore or intentionally retire the fable-survival Supabase project** — live game, dead cloud-save backend.
3. Pirate World's Supabase schema is live but unused (0 rows) — either wire persistence up or note it as pending.
