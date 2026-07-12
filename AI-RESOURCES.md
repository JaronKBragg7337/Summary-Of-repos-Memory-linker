# Open-Source AI Resources for This System

Curated for the AIs living in this account — especially **Zeus AI** (local Ollama runtime + the from-scratch `Zeus-Tiny` training track in `zeus-ai/training/`) and the agents running on the Heartbeat control plane. Everything below is open source / openly licensed. Compiled 2026-07-12; check each project's license before training on it.

## 1. Datasets for training a small model from scratch (Zeus-Tiny track)

| Resource | What it is | Why it fits |
|---|---|---|
| [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories) | Synthetic short stories with a tiny vocabulary | The canonical dataset for proving a from-scratch tiny transformer learns coherent language — ideal first pretrain corpus for Zeus-Tiny |
| [FineWeb / FineWeb-Edu](https://huggingface.co/datasets/HuggingFaceFW/fineweb) | Filtered CommonCrawl web text (FineWeb-Edu = education-quality subset) | The current default open pretraining corpus; sample a slice sized to local hardware |
| [SmolLM corpus (Cosmopedia v2, FineWeb-Edu, Stack-Edu)](https://huggingface.co/HuggingFaceTB) | The data recipe behind Hugging Face's SmolLM small models | A proven recipe specifically for *small* models — the closest published analog to what Zeus-Tiny attempts |
| [Dolma](https://huggingface.co/datasets/allenai/dolma) | AI2's open 3T-token pretraining corpus (permissive ODC-BY) | Fully documented provenance; good for auditable training |
| [RedPajama-Data](https://github.com/togethercomputer/RedPajama-Data) | Open reproduction of the LLaMA training data recipe | Useful for mixing domains deliberately |
| [The Stack v2](https://huggingface.co/datasets/bigcode/the-stack-v2) | Permissively-licensed source code | If Zeus-Tiny should learn tool-call/code formatting |
| [OpenAssistant OASST1/OASST2](https://huggingface.co/datasets/OpenAssistant/oasst1) | Human-written multi-turn assistant conversations | Instruction/chat fine-tuning with real human data |
| [databricks-dolly-15k](https://huggingface.co/datasets/databricks/databricks-dolly-15k) | 15k human-written instruction pairs (CC BY-SA) | Small, clean, commercially usable instruction set |
| [LMSYS-Chat-1M](https://huggingface.co/datasets/lmsys/lmsys-chat-1m) | 1M real user conversations with 25 LLMs | Realistic user-intent distribution for intent classification — one of Zeus-Tiny's stated jobs |
| [FLAN collection](https://github.com/google-research/FLAN) | Thousands of NLP tasks phrased as instructions | Classic multi-task instruction tuning |

## 2. Prompt libraries & prompting knowledge

- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook) — worked examples: tool use, RAG, agent patterns, evaluations.
- [Anthropic Prompt Library](https://docs.anthropic.com/en/prompt-library) — curated production prompts.
- [OpenAI Cookbook](https://github.com/openai/openai-cookbook) — same genre, provider-agnostic techniques transfer.
- [Awesome ChatGPT Prompts](https://github.com/f/awesome-chatgpt-prompts) — large CC0 role-prompt collection (mine it for patterns, not quality).
- [Prompt Engineering Guide (DAIR.AI)](https://github.com/dair-ai/Prompt-Engineering-Guide) — maintained survey of techniques with papers.
- [LangChain Hub](https://smith.langchain.com/hub) — community prompt templates for agent/RAG chains.
- **In-house:** `Perspective-Environmental-framework-Exercise` and `Framing-Lens/Docs/PROMT_SET_v3.md` in this account are original prompt sets — already formatted as reusable probes, and they're the operator's own IP.

## 3. Training / fine-tuning tooling (local-first, matches Zeus's constraints)

- [nanoGPT](https://github.com/karpathy/nanoGPT) and [llm.c](https://github.com/karpathy/llm.c) — minimal from-scratch GPT training; the reference implementations to sanity-check `training/pretrain/train_zeus_tiny.py` against.
- [minGPT](https://github.com/karpathy/minGPT) — even smaller pedagogical trainer.
- [LitGPT](https://github.com/Lightning-AI/litgpt) — clean recipes for pretraining/finetuning small models.
- [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) — config-driven fine-tuning (LoRA/QLoRA/full).
- [Unsloth](https://github.com/unslothai/unsloth) — fastest consumer-GPU LoRA fine-tuning.
- [Hugging Face tokenizers](https://github.com/huggingface/tokenizers) + [sentencepiece](https://github.com/google/sentencepiece) — for `training/tokenizer/train_tokenizer.py`.
- [Ollama](https://github.com/ollama/ollama) — already Zeus's runtime; Modelfiles let you ship fine-tuned GGUF weights locally.
- [llama.cpp](https://github.com/ggerganov/llama.cpp) — GGUF conversion/quantization so Zeus-Tiny can run under Ollama.

## 4. Open models that can serve as Zeus's interim brain (all open weights)

- [Qwen 2.5 / Qwen 3 family](https://huggingface.co/Qwen) (Apache-2.0 for most sizes) — already referenced in zeus-ai's README.
- [Llama 3.x](https://huggingface.co/meta-llama) (community license) — strong small sizes (1B/3B/8B).
- [Mistral / Ministral](https://huggingface.co/mistralai) (Apache-2.0 options).
- [SmolLM2 / SmolLM3](https://huggingface.co/HuggingFaceTB) — fully open small models with open data recipes.
- [Phi-3.5 / Phi-4-mini](https://huggingface.co/microsoft) (MIT) — small models strong at reasoning.
- [OLMo 2](https://huggingface.co/allenai) — the most *transparent* full stack (weights + data + code + logs); best to learn training methodology from.

## 5. Memory, RAG & agent infrastructure (fits the memory-linker mission)

- [sqlite-vec](https://github.com/asg017/sqlite-vec) — vector search inside SQLite; zero-server, matches the account's local-first + append-only-ledger habits.
- [ChromaDB](https://github.com/chroma-core/chroma) / [LanceDB](https://github.com/lancedb/lancedb) — embedded vector stores for `rag_engine.py`.
- [Letta (MemGPT)](https://github.com/letta-ai/letta) — open agent memory architecture (paging memory in/out of context) — directly relevant to `memory-as-spatial-arrangement`.
- [Mem0](https://github.com/mem0ai/mem0) — open memory layer for agents.
- [Model Context Protocol (MCP)](https://github.com/modelcontextprotocol) — open standard for AI↔tool connections; the same protocol used to build this data center, and the natural way for Zeus to expose the pam control plane as tools.
- [Anthropic agent guides](https://docs.anthropic.com/en/docs/agents-and-tools) — patterns for tool-using agents with bounded permissions (the pattern fable-survival's `api/aichat.js` already implements).

## 6. Evaluation & self-checking

- [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) — standard benchmark runner; run it on Zeus-Tiny checkpoints.
- [promptfoo](https://github.com/promptfoo/promptfoo) — prompt/agent regression testing in CI.
- [OpenAI Evals](https://github.com/openai/evals) — framework for writing custom evals (works with any model).
- **In-house:** the Perspective/Framing exercise set doubles as a reasoning-style eval — the AI-Responses-Feb2026 folder is already a small comparative dataset across models.

## 7. Licensing quick rules for training use

1. Prefer datasets with explicit licenses (ODC-BY, CC-BY, Apache-2.0, MIT). "Public" ≠ "licensed."
2. CC-BY / CC-BY-SA content (e.g., `The-Engine-Of-Division-` in this account, Wikipedia) requires attribution — keep a provenance file next to any training corpus.
3. The operator's own repos are the cleanest training data available here: original, self-owned, and already mapped by `repos.json`. The writings category (~10 long-form documents) plus the exercise datasets are the natural "Zeus voice/values" corpus.

---
*Part of the Summary-Of-repos-Memory-linker data center. See `repos.json` for the machine-readable repo map.*
