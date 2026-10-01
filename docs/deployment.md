# daïmōnes Sovereign Deployment Guide

*For institutional buyers: universities, research departments, and organizations that require AI infrastructure under their own control.*

**Last Updated:** October 2026 · **Contact:** architect@daimones.ai

---

## 1. What "Sovereign Deployment" Means

A sovereign deployment of daïmōnes runs entirely on infrastructure the institution controls — on-premises, in a private cloud tenancy, or in an air-gapped environment. Concretely:

- **No data leaves the boundary.** Queries, conversation history, and user records never transit third-party APIs. There is no vendor telemetry call-home.
- **No corporate filtering layer.** Reasoning behavior is governed by your deployment's configuration and your institution's policy, not a vendor's content policy.
- **Open-weight models.** The inference stack runs open-weight models (Qwen family) under a permissive license; no API keys to a third-party lab, no per-token billing, no model deprecation risk.
- **Reproducible evaluation.** The Golden Benchmark v2.1 rubric and raw data are public ([data/benchmarks/](../data/benchmarks/)), so your team can validate quality claims on your own hardware before purchase.

This is the same architecture that runs the public platform at daimones.ai — a single VM at approximately $600/month, which scored 84/100 on Golden Benchmark v2.1 against ChatGPT GPT-5.4 (79) under an identical system prompt.

## 2. Reference Architecture

| Layer | Component | Role |
|-------|-----------|------|
| Inference | llama-server (llama.cpp) | Open-weight model serving, OpenAI-compatible API, GGUF quantization (Q5-class), 16K context, quantized KV cache |
| Retrieval | RAG service + reranker | Embedding retrieval over the licensed primary-source corpus (Corpus Aristotelicum and extensions), cross-encoder reranking |
| Data | PostgreSQL 15 + pgvector | Conversation store, embeddings, CMS content |
| CMS | Directus (self-hosted) | Article/content management, multilingual (EN/EL) publishing |
| Application | Node.js + Express backend | Chat API, streaming (SSE), auth, rate limiting, post-processing (orthography validation, terminology watchdog) |
| Frontend | React 19 + TypeScript (Vite) | SPA with server-rendered article pages for SEO/accessibility |
| Supervision | systemd (bare metal) or containers | Service orchestration, health monitoring, restart policies |

All components are self-hostable and run on Linux. No proprietary runtime dependencies.

## 3. Hardware Requirements

| Tier | GPU | VRAM | RAM | Suitable for |
|------|-----|------|-----|--------------|
| Minimum | 1x NVIDIA L4 (or equivalent) | 24 GB | 32 GB | Single-user evaluation, seminar demos |
| Reference | 1x NVIDIA L4 / RTX 6000 Ada | 24-48 GB | 64 GB | Production platform (the public daimones.ai runs this class) |
| Departmental | 1-2x A100/H100 | 40-80 GB | 128 GB | Concurrent seminar groups, multiple personas, higher context |

CPU-only operation is possible for evaluation (slow: minutes per response) but not recommended for production use. Disk: 100 GB SSD minimum (model weights, corpus, database, growth).

The reference deployment deliberately runs `--parallel 1` inference with a stable context window; concurrency is handled by request queueing with honest user-facing status, not by silently degrading context. This is a design choice discussed during onboarding.

## 4. Deployment Models

### 4.1 Managed Sovereign (recommended first step)
We deploy and maintain the full stack in **your** cloud tenancy (GCP/AWS/Azure/any IaaS). You hold the infrastructure account, network controls, and data residency; we provide the software, deployment automation, and updates. Typical time-to-live: 1-2 weeks.

### 4.2 On-Premises / Air-Gapped
Full offline installation from signed artifacts: model weights (GGUF), corpus package, database seeds, application bundle. No outbound network dependency at runtime. Update delivery via signed artifact drops. Suited to defense-adjacent, archival, and restricted-data environments.

### 4.3 Evaluation Sandbox
A scoped pilot (typically one persona, one department, 90 days) on minimal hardware, with benchmark validation against your own question sets before any commitment. The public demo ([HuggingFace Space](https://huggingface.co/spaces/thevasilis/daimones)) gives a zero-friction first impression but is rate-limited and single-turn — the sandbox is the real evaluation vehicle.

## 5. Licensing and What Is Delivered

The platform source, RAG corpus, and persona system prompts are **proprietary** and delivered under an institutional license. A sovereign deployment includes:

- Application bundle (backend, frontend, CMS configuration)
- Model weights and quantization profile (open-weight, license-compatible)
- Licensed corpus package with provenance documentation
- Persona configuration (Aristotle shipped; additional personas by arrangement)
- Deployment runbooks for your operations team
- Benchmark harness (Golden Benchmark v2.1) for ongoing quality regression testing
- Support and update channel per license tier

What is not delivered: the public platform's operating credentials, our managed hosting infrastructure, or per-consumer subscription features unless licensed.

## 6. Data Protection and Compliance

- **GDPR:** self-hosted by design — the institution is the sole data controller; no subprocessor receives user data. Conversation data resides in your PostgreSQL instance; deletion is a database operation, not a vendor request.
- **Data residency:** guaranteed by deployment location (EU regions, on-prem, or air-gapped).
- **Access control:** application-level authentication with role separation (user / admin / backoffice), session management, and configurable rate limits.
- **Auditability:** request logging, health monitoring, and benchmark regression runs are local and inspectable.
- **Model transparency:** open weights mean your security team can inspect and pin exact model artifacts (checksums provided); there is no opaque upstream model that can change behavior without your action.

For grant-funded deployments (NSF, Horizon Europe), the self-hosted architecture simplifies data-management-plan compliance: no vendor lock-in clause, no cross-border transfer mechanism needed, and reproducible evaluation artifacts for reporting. See also our blog: *Grant-Compliant AI: Self-Hosted Models for NSF and Horizon Europe*.

## 7. Evaluation Protocol (Recommended for Procurement)

1. Run the public Golden Benchmark v2.1 harness on your hardware with your question set — the rubric (terminology, structure, fidelity, reasoning) and scoring scripts are in this repo and published with raw data.
2. Compare against your incumbent assistants **under identical system prompts** (our methodology's core rule; most vendor benchmarks skip it).
3. Validate polytonic Greek orthography with your department's specialists via the Aristotle Feedback workflow ([issue template](../.github/ISSUE_TEMPLATE/aristotle_feedback.md)).
4. Pilot with one seminar group for one term; measure engagement and answer quality against your own criteria.

We publish our losses as well as our wins: Claude could not be tested (no API access) and we say so rather than estimating; earlier benchmark runs (76.6 vs 26.4/31.6) were **deprecated** because commercial models lacked the shared system prompt — an unfair comparison we retired rather than marketed.

## 8. Getting Started

| Step | Action |
|------|--------|
| 1 | Introductory call: requirements, data environment, concurrency needs → architect@daimones.ai |
| 2 | Evaluation sandbox provisioned (2-4 weeks) |
| 3 | Benchmark validation on your hardware + departmental review |
| 4 | License and deployment model agreed (managed sovereign / on-prem / air-gapped) |
| 5 | Production deployment, runbook handover, support channel opened |

---

*daïmōnes is built by Vasilis Stergiou · PowerHouse Consulting Group Pte Ltd (Singapore). Institutional inquiries: architect@daimones.ai · General support: support@daimones.ai*
