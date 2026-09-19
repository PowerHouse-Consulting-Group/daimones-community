# daïmōnes Benchmark Submission for ReallySolved.com

## Overview

daïmōnes is a sovereign AI platform for philosophy and classical thought — the Digital Lyceum. Built on Qwen3.8-27B with RAG over Aristotelian corpus, deployed on self-hosted infrastructure.

**Model:** Qwen3.8-27B-UD-Q5_K_M (quantized GGUF)
**Context:** 16K tokens
**Temperature:** 0.45 (production setting)
**Endpoint:** https://daimones.ai (production API on port 5000)

## The 10 Benchmark Questions

Questions span 5 categories: ethics (5), metaphysics (2), politics (1), logic (1), aporia (1).

| ID | Category | Query | Language |
|----|----------|-------|----------|
| 1 | ethics | What is the golden mean? | English |
| 2 | ethics | τί ἐστιν ἀνδρεία; | Ancient Greek |
| 3 | metaphysics | What is substance (ousia)? | English |
| 4 | ethics | Can virtue be taught? | English |
| 5 | politics | What is the best form of government? | English |
| 6 | logic | What is a syllogism? | English |
| 7 | ethics | What is friendship? | English |
| 8 | metaphysics | What are the four causes? | English |
| 9 | aporia | What is artificial intelligence? | English |
| 10 | ethics | What is justice? | English |

**Source texts:** Nicomachean Ethics (II, III, V, VIII), Metaphysics VII, Politics III, Prior Analytics I, Physics II.

## Scoring Rubric — Separated

### Original Rubric (100 points)

| Component | Points | What it measures |
|-----------|--------|------------------|
| Terminology | 30 | Polytonic Greek term presence + inflections |
| Structure | 25 | Genus-differentia, syllogism, aporia protocol |
| Fidelity | 30 | Anachronism-free, source-grounded, length, depth |
| Reasoning | 15 | Logical coherence, correct Aristotelian concepts, dialectical rigor |

### Separated Scoring (as requested)

**GREEK LANGUAGE SCORE (0-30 points)**
- Terminology (30pts): Presence of expected Greek terms in polytonic orthography
  - Checks for specific terms: μεσότης, ἀρετή, οὐσία, εἶδος, etc.
  - Accepts inflected forms (declensions, conjugations)
  - Accent-insensitive matching (polytonic ↔ monotonic)

**PHILOSOPHY SCORE (0-70 points)**
- Structure (25pts): Argumentative form
  - Genus-differentia definition structure (12pts)
  - Syllogistic/dialectical structure (8pts)
  - Aporia protocol where applicable (5pts)
- Fidelity (30pts): Historical accuracy
  - No anachronisms (modern concepts, post-Aristotelian philosophy) (-10pts per marker)
  - Source-grounded (references to specific texts) (+5pts)
  - Adequate length and depth (+5pts)
- Reasoning (15pts): Logical quality
  - Correct Aristotelian concepts
  - Logical coherence
  - Accurate English translation (when applicable)
  - Dialectical rigor

## Latest Results (September 12, 2026)

**daïmōnes: 86/100 average** (4 perfect, 6 good, 0 needs work)

### Per-Question Breakdown

| ID | Query | Greek (30) | Philosophy (70) | Total |
|----|-------|------------|-----------------|-------|
| 1 | Golden mean | 30 | 60 | 90 |
| 2 | Courage (Greek) | 30 | 55 | 85 |
| 3 | Substance | 24 | 65 | 89 |
| 4 | Virtue taught? | 24 | 60 | 84 |
| 5 | Best government | 30 | 48 | 78 |
| 6 | Syllogism | 30 | 55 | 85 |
| 7 | Friendship | 30 | 60 | 90 |
| 8 | Four causes | 25 | 65 | 90 |
| 9 | What is AI? | 30 | 53 | 83 |
| 10 | Justice | 30 | 60 | 90 |

**Averages:**
- Greek Language: 28.3/30 (94.3%)
- Philosophy: 58.1/70 (83.0%)
- Combined: 86.4/100

### Comparison to Commercial Models (verified run — September 19, 2026)

Protocol: all models received the IDENTICAL Aristotle system prompt (aristotle_system_prompt_compact.txt), the same 10 questions, temperature 0.45. Commercial models run without RAG; daïmōnes runs its production RAG over the Aristotelian corpus (that is the product being measured). Raw responses and per-question component scores archived at scripts/evaluations/comparison_{responses,scored}_2026-09-19_combined.json.

| Model | Terminology (30) | Structure (25) | Fidelity (30) | Reasoning (15) | Total |
|-------|------------------|----------------|---------------|----------------|-------|
| **daïmōnes** | **28.9** | **18.1** | 23.0 | 14.0 | **84.0** |
| ChatGPT (GPT-5.4) | 24.6 | 16.9 | 23.0 | 14.5 | 79.0 |
| Gemini 3.6-flash | 25.8 | 8.1 | 22.0 | **15.0** | 70.4 |
| Grok 4.3 (xAI) | 21.2 | 6.5 | 23.5 | 13.5 | 64.7 |

**Reasoning sub-score (15 pts), per question:**
- daïmōnes: 14.0/15 (93.3%) — [15, 10, 15, 15, 15, 10, 15, 15, 15, 15]
- Gemini 3.6-flash: 15.0/15 (100%)
- ChatGPT GPT-5.4: 14.5/15 (96.7%)
- Grok 4.3: 13.5/15 (90%)

**Honest reading of the data:**
- daïmōnes finishes FIRST overall (84.0) against three frontier commercial models given its own persona instructions.
- The decisive component is Structure (25 pts): daïmōnes 18.1 vs Gemini 8.1 and Grok 6.5 — a 2.2–2.8x lead in genuine dialectical form (genus-differentia definitions, πρότασις→συμπέρασμα syllogistic chains, aporia protocol). This comes from corpus-grounded RAG, not prompt-following: commercial models mimic the template when told to; daïmōnes reasons in it.
- Terminology: daïmōnes first (28.9/30) on polytonic Ancient Greek precision.
- Reasoning is a photo finish (13.5–15.0) under equal prompt conditions — the rubric rewards explicit syllogistic markers, which instructed commercial models emit mechanically. We do not claim a Reasoning lead.
- A solo operator on a ~$600/month VM, running a quantized open-weights model, equals or exceeds trillion-dollar frontier labs on the benchmark those labs are not built for. Specialization beats generality where specialization matters.

**Historical note:** Earlier submissions of this document cited "ChatGPT (GPT-4) 26.4" and "Claude (Anthropic) 31.6". Those figures predate the reproducible protocol, have no surviving raw run data, and are superseded by the September 19, 2026 verification above. Claude is omitted because no API access exists to run it under the same protocol; we do not publish scores we cannot reproduce.

## What Makes daïmōnes Different

1. **Sovereign infrastructure:** Self-hosted on Google Cloud VM, no API dependencies
2. **Specialized RAG:** Curated corpus of Aristotelian texts with polytonic Greek preservation
3. **Quantized efficiency:** Q5_K_M quantization runs on single L4 GPU ($0.70/hr on-demand)
4. **Uncensored reasoning:** No RLHF filtering — direct Aristotelian dialectic
5. **Philosophy-first:** Optimized for classical thought, not general-purpose chat

## Technical Details

- **Backend:** Node.js + TypeScript + Express
- **LLM:** llama.cpp serving Qwen3.8-27B GGUF
- **RAG:** Custom retriever with Greek text preservation
- **CMS:** Directus (self-hosted PostgreSQL)
- **Deployment:** /opt/daimones/ on Ubuntu 22.04 LTS

## Agent Card & Discovery Files

- **Agent Card:** https://daimones.ai/.well-known/agent-card.json
- **AI.json:** https://daimones.ai/.well-known/ai.json
- **llms.txt:** https://daimones.ai/llms.txt

All files validate and are production-ready.

---

**Contact:** Vasilis Stergiou (@VasilisStergiou on X)
**Site:** https://daimones.ai
