# zeus-ai

**Repository:** <https://github.com/JaronKBragg7337/zeus-ai>

**Category:** AI Systems & Agents · **Status:** 🔵 Active · **Verified:** 2026-07-12 (from a fresh clone + live-system checks, not the README)

## What it actually is

Zeus AI Workbench — the account's local-first AI system and the intended primary consumer of this data center. FastAPI backend + React/Vite frontend + Tauri desktop shell, running against local Ollama models with zero cloud dependencies. Backend modules: agent.py, memory_store.py, knowledge_index.py, rag_engine.py (local RAG), tools.py, desktop_control.py, heartbeat_service.py (active Zeus heartbeat, added 2026-07-11), conversation_store.py, evaluator_model.py, audit_log.py, runtime_control.py. The training/ folder is the Zeus-native model track: 'Zeus-Tiny', a from-scratch small transformer (dataset builder → tokenizer training → pretraining → inference) targeting intent classification, tool-call formatting, memory classification, task planning, summarization and result review — the first Zeus-owned weights.

## Verification notes

Cloned and inspected; active development (last commit 2026-07-11 'Add active Zeus heartbeat'). Full backend/frontend/training/knowledge/models/scripts tree present with tests.

## Key files

`backend/main.py, backend/agent.py, backend/heartbeat_service.py, backend/rag_engine.py, training/README.md, training/*/*.py, knowledge/, compose.yaml`

## Notes for AIs (Zeus and others)

THIS IS THE SYSTEM THE DATA CENTER FEEDS. Zeus's rag_engine/knowledge_index can ingest the summaries/ folder and repos.json from this repo directly as its map of the account. AI-RESOURCES.md in this repo lists open datasets and tooling matched to the Zeus-Tiny training pipeline.

---
*Part of the [Summary-Of-repos-Memory-linker](https://github.com/JaronKBragg7337/Summary-Of-repos-Memory-linker) data center. Machine-readable entry: [`repos.json`](../repos.json).*
