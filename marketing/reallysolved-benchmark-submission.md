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

### Comparison to Commercial Models (same benchmark)

| Model | Greek (30) | Philosophy (70) | Total |
|-------|------------|-----------------|-------|
| **daïmōnes** | 28.3 | 58.1 | 86.4 |
| ChatGPT (GPT-4) | 2.1 | 24.3 | 26.4 |
| Claude (Anthropic) | 3.5 | 28.1 | 31.6 |

**Note:** ChatGPT and Claude scores are from the same rubric. Their low Greek scores reflect that they don't output polytonic Ancient Greek by default. Their philosophy scores (24-28/70) reflect generic responses without Aristotelian structure.

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
