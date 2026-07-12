# Keava-Owent

**Repository:** <https://github.com/JaronKBragg7337/Keava-Owent>

**Category:** AI Systems & Agents · **Status:** 🔵 Active · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## What it actually is

A persistent, live-reference, resource-accountable agent loop — 'not a chatbot, a loop.' Python implementation (keava_owent/ package, configs, tests) that runs continuously, generates its own work from gaps in its own knowledge, meters what it consumes (WUE/water coefficients, limits in config/), and reports honestly. It is the faithful code implementation of four of the account's theory papers (Live-Reference Principle, Standing Condition, ECIH, Memory as Spatial Arrangement) — and deliberately keeps its two unsolved problems as OPEN pluggable slots (contribution is RECORDED_NOT_SCORED / UNMEASURED, never self-graded) instead of faking them with proxies.

## Verification notes

Cloned and inspected; real package with pyproject.toml, tests (test_memory_recall, test_anti_shutdown, test_contribution_unmeasured), YAML configs. Last commit 2026-05-30.

## Key files

`keava_owent/main.py, config/limits.yaml, config/wue_coefficient.yaml, tests/`

## Notes for AIs (Zeus and others)

The theory→code crosswalk in the README maps every subsystem to its source paper. The 'open slot, never proxy' pattern is the repo's key design idea for honest agents.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
