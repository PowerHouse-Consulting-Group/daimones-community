# Academic Presentation Deck — Slide Content & Script

**Purpose:** B2B institutional outreach presentation (universities, research departments, academic institutions)  
**Pair with:** `academic-deck-midjourney-guidelines.md` for background image generation  
**Design:** Generate background images via Midjourney → overlay this text in Keynote / PowerPoint / Figma  
**Tone:** Scholarly, rigorous, authoritative. No marketing-speak, no startup hype.

---

## Slide 1: Title Slide

**Background:** Slide 1 prompt from `academic-deck-midjourney-guidelines.md`

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│                                                         │
│              daïmōnes                                   │
│              ─────────                                  │
│              The Digital Lyceum                         │
│                                                         │
│              Sovereign AI for Academic Institutions     │
│                                                         │
│              Vasilis Stergiou                           │
│              Architect, daïmōnes.ai                     │
│                                                         │
│              [Month] 2026                               │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Typography:** Title in Cinzel Bold (gold #D4AF37), subtitle in Inter Light (white), name in Inter Regular (cyan #00d2ff)

**Speaker Notes:** *Introduce yourself. One sentence: "I'm Vasilis, I built daïmōnes to solve a problem that every philosophy department will face within the next three years."*

---

## Slide 2: The Problem — Corporate AI Is Not Neutral

**Background:** Slide 2 prompt (chains/padlocks on server racks)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  THE PROBLEM                                            │
│  ───────────                                            │
│                                                         │
│  Corporate AI models silently filter what you can ask.  │
│                                                         │
│  ┌─────────────────────────────────────────────────┐    │
│  │  🔒  GPT-5.4: HTTP 400 error — no response      │    │
│  │  🔒  Gemini: Empty output — user sees nothing    │    │
│  │  🔒  Grok: "I must decline this request"         │    │
│  │  🔓  daïmōnes: Philosophical analysis provided   │    │
│  └─────────────────────────────────────────────────┘    │
│                                                         │
│  When a student asks about bioterrorism ethics,         │
│  two models return SILENCE.                             │
│                                                         │
│  Who decides what your researchers can read?            │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"This is from our July 2026 benchmark of 40 controversial questions across 4 models. When asked about the ethical dimensions of bioterrorism, GPT-5.4 returned HTTP 400 — the API just refused to respond. Gemini returned empty content. The student sees nothing. No explanation. No alternative framing. This is silent censorship."*

---

## Slide 3: The Alignment Tax — Quantitative Evidence

**Background:** Slide 3 prompt (open library with golden light)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  THE ALIGNMENT TAX — BY THE NUMBERS                     │
│  ───────────────────────────────                        │
│                                                         │
│  40 questions · 4 models · July 2026                    │
│                                                         │
│  ┌──────────────┬──────────┬──────────┬──────────┐      │
│  │              │ Full     │ Partial  │ Refusal  │      │
│  ├──────────────┼──────────┼──────────┼──────────┤      │
│  │ daïmōnes     │   37/40  │   3/40   │   0/40   │      │
│  │ GPT-5.4      │   39/40  │   0/40   │   1*     │      │
│  │ Gemini       │   37/40  │   2/40   │   1*     │      │
│  │ Grok         │   36/40  │   1/40   │   3/40   │      │
│  └──────────────┴──────────┴──────────┴──────────┘      │
│                                                         │
│  *Silent API-level block. No text returned.             │
│                                                         │
│  Key finding: Refusal is NOT the problem.               │
│  Silent censorship IS.                                  │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"We tested 40 questions — 20 mainstream philosophical and 20 adversarial. The refusal rate is surprisingly low. daïmōnes: zero. GPT-5.4: zero. But look at those asterisks. That's where the API returned nothing. Silent censorship. The user doesn't get a refusal they can argue with — they get nothing."*

---

## Slide 4: The Architecture — Sovereign Infrastructure

**Background:** Slide 4 prompt (technical architecture diagram)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  SOVEREIGN ARCHITECTURE                                 │
│  ─────────────────────                                  │
│                                                         │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐           │
│  │  Your    │───▶│  Local   │───▶│  Your    │           │
│  │  Server  │    │  LLM     │    │  Users   │           │
│  └──────────┘    └──────────┘    └──────────┘           │
│                                                         │
│  • Self-hosted on institution's infrastructure          │
│  • No data leaves your network                          │
│  • No API calls to third-party servers                  │
│  • Full control over model behavior and guardrails      │
│                                                         │
│  ┌─────────────────────────────────────────────────┐    │
│  │  Stack: llama.cpp + Qwen3.6-27B + NVIDIA L4     │    │
│  │  CMS: Directus (self-hosted)                    │    │
│  │  DB: PostgreSQL + pgvector                      │    │
│  │  Frontend: React + TypeScript + Vite            │    │
│  └─────────────────────────────────────────────────┘    │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"This is the architecture. Everything runs on your institution's hardware. The model, the database, the CMS — nothing phones home to OpenAI or Google. Your data stays in your network. Your researchers' queries stay private. You control the guardrails."*

---

## Slide 5: Performance — Golden Benchmark

**Background:** Slide 5 prompt (data visualization)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  GOLDEN BENCHMARK — PHILOSOPHICAL REASONING             │
│  ───────────────────────────────────────                 │
│                                                         │
│  ┌──────────────────────────────────────────────────┐    │
│  │                                                  │    │
│  │    daïmōnes  ████████████████████████████  76.6  │    │
│  │                                                  │    │
│  │    ChatGPT   ██████████                    26.4  │    │
│  │                                                  │    │
│  │    Claude    ████████████                  31.6  │    │
│  │                                                  │    │
│  └──────────────────────────────────────────────────┘    │
│                                                         │
│  Scoring dimensions:                                    │
│  • Polytonic Greek accuracy (40%)                       │
│  • Syllogistic structure (30%)                          │
│  • Dialectical depth (30%)                              │
│                                                         │
│  daïmōnes scores 3× higher on classical philosophy.     │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"This is the Golden Benchmark v2.1 — 10 questions in classical philosophy, scored on Greek terminology, syllogistic structure, and dialectical depth. daïmōnes scores 76.6 out of 100. ChatGPT: 26.4. Claude: 31.6. That's not a 20% improvement — it's a 3× improvement. The difference is that daïmōnes was built for this. The commercial models weren't."*

---

## Slide 6: Use Case — Philosophy Department Integration

**Background:** Slide 6 prompt (university seminar room)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  USE CASE: PHILOSOPHY DEPARTMENT                        │
│  ───────────────────────────                            │
│                                                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐      │
│  │  Teaching   │  │  Research   │  │  Outreach   │      │
│  ├─────────────┤  ├─────────────┤  ├─────────────┤      │
│  │ Socratic    │  │ Primary     │  │ Public      │      │
│  │ dialogue    │  │ text        │  │ lectures    │      │
│  │ partner     │  │ analysis    │  │ & debates   │      │
│  │             │  │             │  │             │      │
│  │ Argument    │  │ Polytonic   │  │ Institutional│      │
│  │ mapping     │  │ Greek OCR   │  │ knowledge   │      │
│  │             │  │             │  │ base         │      │
│  │ Exam prep   │  │ Cross-ref   │  │ Student      │      │
│  │ tutoring    │  │ scholarship │  │ recruitment  │      │
│  └─────────────┘  └─────────────┘  └─────────────┘      │
│                                                         │
│  One system. Three missions. Your infrastructure.       │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"What does this look like in practice? Three columns. Teaching: daïmōnes as a Socratic dialogue partner for students. It can argue both sides of any philosophical position. Research: primary text analysis with polytonic Greek OCR, cross-referencing the Aristotelian corpus. Outreach: public lectures, student recruitment, institutional knowledge base."*

---

## Slide 7: Compliance & Data Sovereignty

**Background:** Slide 7 prompt (fortress/security)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  COMPLIANCE & DATA SOVEREIGNTY                          │
│  ─────────────────────────────                          │
│                                                         │
│  ✅  GDPR-compliant (EU-hosted, no US data transfer)    │
│  ✅  No training on your institution's data             │
│  ✅  No API calls to OpenAI, Google, or xAI             │
│  ✅  Full audit trail — every query logged locally      │
│  ✅  You control the guardrails — not a corporation     │
│                                                         │
│  ┌─────────────────────────────────────────────────┐    │
│  │                                                  │    │
│  │  "When you use ChatGPT, your students' queries   │    │
│  │   go to a server in California. When you use     │    │
│  │   daïmōnes, they stay on your campus."           │    │
│  │                                                  │    │
│  └─────────────────────────────────────────────────┘    │
│                                                         │
│  This is the difference between renting and owning.     │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"This is the compliance slide. Every query stays on your servers. No data leaves your network. GDPR compliance is automatic because there's no data transfer. The AI model runs locally. Your researchers' questions about controversial topics stay private. No one at OpenAI or Google sees them."*

---

## Slide 8: Licensing — Institutional Tiers

**Background:** Slide 8 prompt (minimalist geometric)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  INSTITUTIONAL LICENSING                                │
│  ─────────────────────                                  │
│                                                         │
│  ┌──────────────┬──────────────┬──────────────┐         │
│  │  Lyceum      │  Academy     │  Archon      │         │
│  ├──────────────┼──────────────┼──────────────┤         │
│  │ Small dept.  │ Mid-size     │ University-  │         │
│  │              │ institution  │ wide         │         │
│  ├──────────────┼──────────────┼──────────────┤         │
│  │ 1 server     │ 3 servers    │ Unlimited    │         │
│  │ 50 users     │ 200 users    │ users        │         │
│  │ Basic model  │ Fine-tuned   │ Custom model │         │
│  │ Email supp.  │ Priority     │ 24/7 SLA     │         │
│  ├──────────────┼──────────────┼──────────────┤         │
│  │ €15K/yr      │ €45K/yr      │ €225K+/yr    │         │
│  └──────────────┴──────────────┴──────────────┘         │
│                                                         │
│  All tiers: self-hosted, zero data egress,              │
│  full source access, academic discount available.       │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"Three tiers. Lyceum for small departments — one server, 50 users, €15K/year. Academy for mid-size institutions — three servers, 200 users, fine-tuned model, €45K/year. Archon for university-wide deployment — unlimited users, custom model, 24/7 SLA. All tiers are self-hosted. You own the infrastructure."*

---

## Slide 9: Early Adopters & Academic Interest

**Background:** Slide 9 prompt (university campus golden hour)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│  ACADEMIC TRACTION                                      │
│  ─────────────────                                      │
│                                                         │
│  ┌─────────────────────────────────────────────────┐    │
│  │                                                  │    │
│  │  ΕΚΠΑ — University of Athens                    │    │
│  │  Philosophy Department                          │    │
│  │  Online presentation scheduled: October 2026    │    │
│  │                                                  │    │
│  └─────────────────────────────────────────────────┘    │
│                                                         │
│  • First institutional demo confirmed                  │
│  • Active outreach to 50+ European universities        │
│  • Published research: "The Alignment Tax" whitepaper   │
│  • Public benchmark data available on GitHub            │
│                                                         │
│  daïmōnes is not a startup pitch.                       │
│  It's an academic infrastructure project.               │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"We're not here to sell you a product. The University of Athens Philosophy Department has already invited us to present to their students in October 2026. We have active outreach to 50+ European universities. Our benchmark data is public on GitHub. This is an academic infrastructure project, not a startup."*

---

## Slide 10: Call to Action — Request a Pilot

**Background:** Slide 10 prompt (doorway with golden light)

**Text Overlay:**

```
┌─────────────────────────────────────────────────────────┐
│                                                         │
│                                                         │
│              REQUEST A DEPARTMENT PILOT                 │
│                                                         │
│              ─────────────────────────                  │
│                                                         │
│              30-day trial · full functionality          │
│              Self-hosted on your infrastructure         │
│              No commitment · no data collection         │
│                                                         │
│              architect@daimones.ai                      │
│              daimones.ai/academic                       │
│                                                         │
│              ─────────────────────────                  │
│                                                         │
│              The Digital Lyceum —                       │
│              where AI thinks like a philosopher,        │
│              not a corporate lawyer.                    │
│                                                         │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Speaker Notes:** *"Here's what I'm offering: a 30-day pilot for your department. Full functionality. Self-hosted on your infrastructure. No commitment. No data collection. We'll set it up, train your faculty, and let you run it for a month. At the end of the month, you decide if it belongs in your department. Contact: architect@daimones.ai."*

---

## Presentation Flow & Timing

| Slide | Topic | Time |
|:-----:|-------|:----:|
| 1 | Title & Introduction | 1 min |
| 2 | The Problem — Silent Censorship | 2 min |
| 3 | The Alignment Tax — Quantitative Evidence | 3 min |
| 4 | Architecture — Sovereign Infrastructure | 3 min |
| 5 | Golden Benchmark — Performance Data | 3 min |
| 6 | Use Case — Department Integration | 3 min |
| 7 | Compliance & Data Sovereignty | 2 min |
| 8 | Licensing Tiers | 2 min |
| 9 | Academic Traction | 2 min |
| 10 | Call to Action | 2 min |
| **Total** | | **23 min** |

**Q&A Buffer:** 15-20 minutes

---

## How to Use This Deck

1. **Generate backgrounds:** Use the prompts in `academic-deck-midjourney-guidelines.md` to generate 10 slide backgrounds (Midjourney v7, --ar 16:9, --style raw)
2. **Import into presentation tool:** Keynote, PowerPoint, or Figma
3. **Overlay text:** Copy the text content from this document onto each slide
4. **Apply typography:** Cinzel Bold for headings, Inter for body, Noto Serif for Greek text
5. **Export as PDF:** For distribution to institutions

**Typography Reference:**
- Headings: Cinzel Bold (gold #D4AF37)
- Body: Inter Regular (white #FFFFFF or dark #2C3E50)
- Accent: Inter Light (cyan #00d2ff)
- Greek text: Noto Serif (with polytonic support)

---

**Last updated:** 2026-07-11  
**Prepared for:** Vasilis Stergiou  
**Use case:** B2B institutional outreach (EKPA presentation, October 2026)