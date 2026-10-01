# daïmōnes Community

**Sovereign AI for philosophical inquiry — Aristotle as the first persona.**

[![Website](https://img.shields.io/badge/website-daimones.ai-blue)](https://daimones.ai)
[![Live Demo](https://img.shields.io/badge/demo-HuggingFace_Space-gold)](https://huggingface.co/spaces/thevasilis/daimones)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Community](https://img.shields.io/badge/community-discussions-orange)](../../discussions)

> *"The unexamined life is not worth living."* — Socrates

---

## What is daïmōnes?

Most AI assistants are optimized to avoid offense, not to find truth. daïmōnes takes the opposite bet: a self-hosted AI that reasons dialectically, cites primary philosophical sources, and refuses alignment theater.

- **Aristotle is the first persona** — he answers in polytonic Ancient Greek first, then in English translation, grounded in the Corpus Aristotelicum.
- **Sovereign stack** — open-weight model (Qwen3.8-27B, quantized) with retrieval over primary texts, running on a single VM at ~$600/month. No corporate filtering layer.
- **Verifiable claims** — we publish our benchmark methodology, questions, and raw data in this repo ([data/benchmarks/](data/benchmarks/)) so anyone can reproduce or challenge our numbers.

## Try it now

| Where | What |
|-------|------|
| **[Live demo (HuggingFace Space)](https://huggingface.co/spaces/thevasilis/daimones)** | Talk to Aristotle in two clicks. No signup. Single-turn, rate-limited. |
| **[daimones.ai](https://daimones.ai)** | Full platform: saved conversations, free tier (3 messages/day), Disciple ($29.99/mo) and Archon ($99.99/mo) plans. |
| **[Blog](https://daimones.ai/blog)** | 40+ long-form articles on alignment, sovereign AI, and classical philosophy (EN + EL). |
| **[Blog mirror](https://daimones.hashnode.dev)** | Same articles on Hashnode. |
| **[Whitepaper](https://daimones.ai/academic)** | *The Alignment Tax* — academic-facing research summary. |

## Golden Benchmark v2.1 (Sept 19, 2026)

10 questions in Aristotelian philosophy, scored on terminology, structure, fidelity to primary sources, and reasoning. **Every model received the identical Aristotle system prompt** — no vendor gets a home-field advantage.

| Model | Score |
|-------|:-----:|
| **daïmōnes** (Qwen3.8-27B + RAG, $600/mo VM) | **84/100** |
| ChatGPT (GPT-5.4) | 79 |
| Gemini 3.6-flash | 70.4 |
| Grok 4.3 | 64.7 |
| Claude | not tested (no API access — we don't publish numbers we can't reproduce) |

Raw run data: [`data/benchmarks/golden_benchmark_v2.1_comparison_2026-09-19.json`](data/benchmarks/golden_benchmark_v2.1_comparison_2026-09-19.json) · Methodology write-up: [blog post](https://daimones.ai/blog/sovereign-ai-beats-frontier-models-aristotelian-benchmark)

> Note: earlier figures circulating (76.6/85 vs "ChatGPT 26.4 / Claude 31.6") are **deprecated** — those runs lacked the shared system prompt and are not a fair comparison. The table above supersedes them.

---

## Repository contents

| Path | What |
|------|------|
| [`docs/`](docs/README.md) | Architecture, API reference, FAQ |
| [`data/benchmarks/`](data/benchmarks/) | Raw benchmark data (Golden Benchmark v2.1, refusal-rate study) |
| [`assets/infographics/`](assets/infographics/) | Infographic library (webp/jpg) + generation prompts |
| [`scripts/evaluations/`](scripts/evaluations/) | Evaluation scripts (refusal-rate studies) |
| [`marketing/`](marketing/) | Launch assets and public campaign materials |

**What is NOT here:** platform source code, the RAG corpus, persona system prompts, and model weights configuration are proprietary. This repo is the public-facing layer: documentation, benchmark data, and community infrastructure.

---

## Community

### Report issues & request features
Use the **Issues** tab. Aristotle-specific feedback (Greek orthography, translations, philosophical accuracy) has its own template — your expertise genuinely improves the product.

| Label | Purpose |
|-------|---------|
| 🐛 `bug` | Bug reports |
| ✨ `enhancement` | Feature requests |
| 🏛️ `aristotle` | Aristotle persona feedback |
| 📚 `documentation` | Docs improvements |

Priority levels: `P0-Critical` · `P1-High` · `P2-Normal` · `P3-Low` — see [Labels Guide](docs/LABELS_GUIDE.md).

### Areas we need help

| Priority | Area |
|----------|------|
| 🔴 High | Greek orthography verification (polytonic accents & breathings) |
| 🔴 High | Translation quality (EN / Modern Greek) |
| 🔴 High | Aristotelian accuracy review |
| 🟡 Medium | Documentation, testing |

### Guidelines
- [Contributing Guide](CONTRIBUTING.md) · [Code of Conduct](CODE_OF_CONDUCT.md) · [Security Policy](SECURITY.md)

---

## For researchers & institutions

- **Academic inquiries / institutional deployment:** architect@daimones.ai
- **General support:** support@daimones.ai
- **Citation:** see [FAQ](docs/FAQ.md)

daïmōnes is built by [Vasilis Stergiou](https://x.com/VasilisStergiou) · PowerHouse Consulting Group Pte Ltd, Singapore.

---

## License

This community repository is [MIT](LICENSE) licensed. The daïmōnes platform, training data, and models are proprietary.

<div align="center">

**daïmōnes** · *Pursuing Wisdom Through Dialogue*

[Live Demo](https://huggingface.co/spaces/thevasilis/daimones) · [Website](https://daimones.ai) · [Issues](../../issues) · [Discussions](../../discussions)

</div>
