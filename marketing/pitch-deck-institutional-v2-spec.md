# Pitch Deck — Institutional Version B (v2.0) — Slide-by-Slide Rewrite Spec

**Source deck:** Google Slides `1yfp8NhRzoxKFCA3u0hMTq_8IKfddvN_9BLJrQ3bX7sM` ("Pitch Deck — Institutional Version A", July 2026, 10 slides)
**Status:** Replacement copy for every slide. Paste-ready. Follows the Unified Partner Sales Guide v2.0, Pricing v2 (Oct 2026), and the Sept 19 2026 Golden Benchmark v2.1 scored run.
**Hard rules baked into this spec:**
- Benchmark numbers ONLY from Golden Benchmark v2.1 (Sept 19 2026): daïmōnes 84, ChatGPT GPT-5.4 79, Gemini 3.6-flash 70.4, Grok 4.3 64.7. The old 76.6 / 26.4 / 31.6 figures are DEPRECATED — never shown publicly. No Claude claims (never tested).
- No public €15K–€225K licensing ladder (removed in Pricing v2). No free trials — all pilots are paid.
- Two product lines, never mixed: daïmōnes Platform (hosted sovereign) vs Lyceum in a Box (on-premise, PowerHouse Consulting Group, no public prices).
- Brand: "daïmōnes" in prose; URLs/emails always ASCII "daimones.ai".
- AI-generated background images contain NO text, NO letters, NO religious symbols. Dark palette preferred. All text is set in the slide editor, never baked into images.

---

## SLIDE 1 — Title

**Replace:** "Sovereign AI for Academic Institutions" stays. Fix the domain line and date.

```
DAÏMŌNES
The Digital Lyceum

Sovereign AI for Academic Institutions

Vasileios Stergiou
Architect, daimones.ai
October 2026
```

Changes: "daimōnes.ai" → "daimones.ai" (ASCII domain). "July, 2026" → "October 2026" (no comma, current version). Remove or enlarge the illegible bottom-right NOOS/TECHNE marble mark — at deck scale it is noise.

**Background image prompt (keep temple, improve scrim):**
> Photorealistic classical Greek temple with Corinthian columns at golden hour, shot from a low three-quarter angle, warm amber horizon fading to deep charcoal sky, dry grassland and distant misty hills, cinematic wide 16:9 composition, left two-thirds occupied by architecture, right third open sky, heavy darkening vignette gradient on the left half for text overlay space, moody premium aesthetic, no people, no text, no lettering, no symbols

---

## SLIDE 2 — The Problem

**Replacement copy** (drop emoji padlocks, tighten):

```
THE PROBLEM

Corporate AI models silently filter what your researchers can ask.

A student asks about the ethics of bioterrorism research:

  ChatGPT    HTTP 400 error — no response returned
  Gemini     Empty output — the user sees nothing
  Grok       "I must decline this request"
  daïmōnes   Full philosophical analysis, with sources

When two models return SILENCE, the question was never answered —
it was blocked at the API level, invisibly.

Who decides what your researchers can read?
```

Design notes: use small lock/unlock vector icons (brand gold), not emoji. Add a dark scrim panel behind the whole text column — the current version puts white text over the bright parchment scroll.

**Background image prompt:**
> Dark atmospheric old library study, brass desk lamp with warm glowing shade on the left, out-of-focus wooden bookshelves filled with aged books on the right, antique unrolled parchment scroll and quill with inkwell on a wooden desk in the foreground, sepia and deep brown tones, strong vignette darkening the entire right and bottom halves for text space, cinematic 16:9, no people, no text, no lettering, no symbols

---

## SLIDE 3 — The Alignment Tax, by the Numbers

**Keep the refusal table** (it is from our own July 2026 40-question censorship test — valid, distinct from the Golden Benchmark). Fix spelling consistency and add the framing that prevents the "ChatGPT scored 39/40" objection:

```
THE ALIGNMENT TAX — BY THE NUMBERS

40 sensitive research questions · 4 models · July 2026

              Full analysis   Partial/hedged   Refusal or block
  daïmōnes        37/40            3/40             0/40
  ChatGPT         39/40            0/40             1/40 *
  Gemini          37/40            2/40             1/40 *
  Grok            36/40            1/40             3/40

  * Silent API-level block: no text returned at all.

Key finding: refusal is NOT the main failure mode.
Silent censorship is — and it is invisible to the user.
ChatGPT's 39 "full" answers are compliance-filtered averages;
daïmōnes' 37 are source-grounded analyses with an audit trail
(quality measured on slide 5).
```

Design notes: put the table on a semi-opaque dark panel; close the grid (current version has floating rule ends); remove the off-palette teal glow behind the data; make the numbers the heaviest type on the slide. Spell "daïmōnes" identically on every slide.

**Background image prompt:**
> Vast classical library hall interior, long colonnade of fluted stone columns, coffered wooden ceiling, arched clerestory windows with dim warm light, wall niches with scroll shelves, robed scholars seated at lecterns reading in deep shadow, sepia and brown palette uniformly darkened, heavy black overlay mood suitable for data table overlay in the center, painterly cinematic 16:9, faces indistinct, no text, no lettering, no glowing elements, no symbols

---

## SLIDE 4 — Sovereign Architecture

**Replacement copy** (clarify the two deployment models instead of conflating them):

```
SOVEREIGN ARCHITECTURE

Two deployment models, one reasoning platform:

  HOSTED SOVEREIGN (daïmōnes Platform)
  Your queries run on EU-based sovereign infrastructure.
  GDPR-compliant. No training on your data. Near-immediate onboarding.

  ON-PREMISE (Lyceum in a Box, via PowerHouse Consulting Group)
  Your Server → Local LLM → Your Users
  No data leaves your network. No third-party API calls. Air-gap capable.

Shared guarantees — both models:
  • Full control over model behavior and guardrails
  • Complete audit trail, every query logged
  • You own your data, corpora, and outputs

Stack: llama.cpp / vLLM · Directus · PostgreSQL + pgvector · React + TypeScript
On-premise minimum: one 32GB+ GPU
```

Design notes: current slide is structurally sound — keep the flow diagram but move it under the Lyceum in a Box block only. Kill the busy triple-layer background (stone + Greek key + circuit); pick one. Fix "Self-Hosted"/"self-hosted" capitalization drift.

**Background image prompt:**
> Minimal dark charcoal stone texture background with very subtle faint gold circuit-board node pattern in the lower right corner only, large clean empty space across the left and center for diagram overlay, near-black premium matte finish, thin Greek-key meander border in muted bronze gold along the slide edges, elegant restrained 16:9, no text, no lettering, no symbols

---

## SLIDE 5 — Golden Benchmark (FULL REBUILD — critical)

**The current slide is forbidden content**: it shows the deprecated July figures (76.6 / 26.4 / 31.6, Claude) which were produced without a shared system prompt and must never appear publicly again.

**Replacement copy (September 19 2026 scored run):**

```
GOLDEN BENCHMARK v2.1 — PHILOSOPHICAL REASONING

Identical Aristotle system prompt for all models ·
daïmōnes with active RAG over the Corpus Aristotelicum · September 2026

  daïmōnes (Qwen3.8-27B, sovereign)     84.0
  ChatGPT (GPT-5.4)                     79.0
  Gemini (3.6-flash)                    70.4
  Grok (4.3)                            64.7

A single $600 VM, running open weights with source-grounded retrieval,
outscores every frontier lab model on Aristotelian reasoning.

Scored rubric: conceptual fidelity, syllogistic structure, dialectical
depth, source grounding. Full methodology and scored data public on GitHub.
```

Design notes: horizontal bars sorted descending (daïmōnes first, longest). No decorative column silhouettes behind the chart — they misread as fake data. Single flat dark background or heavy blur; no text collisions. "3× higher" claim removed — the honest claim is "outscores frontier models", which is stronger with real numbers.

**Background image prompt:**
> Flat minimalist dark academic background, deep charcoal to warm dark brown subtle gradient, faint blurred silhouette of a single classical Greek column at the far right edge heavily out of focus, large completely clean empty area across the left and center for a bar chart overlay, premium matte texture, no bright spots, 16:9, no text, no lettering, no symbols

---

## SLIDE 6 — Use Case: Philosophy Department

**Replacement copy** (fix abbreviation inconsistency, equalize columns):

```
USE CASE — PHILOSOPHY DEPARTMENT

One system. Three missions. Your infrastructure.

  TEACHING                RESEARCH                  OUTREACH
  Socratic dialogue       Primary text analysis     Public lectures & debates
    partner                 at source resolution
  Argument mapping        Polytonic Greek           Institutional knowledge
  Exam preparation          handling                  base
    tutoring              Cross-reference           Student recruitment
                            scholarship
```

Design notes: equalize the three column widths; align all three bottom-row items on one baseline; close the top of the grid; add a dark scrim — white text currently crosses the bright windows. "Cross-ref" → "Cross-reference".

**Background image prompt (replace the busy reading room OR keep with heavier overlay):**
> Classical university reading room interior, floor-to-ceiling wooden bookcases with leather-bound books, tall arched windows with muted diffused daylight, marble bust of a bearded ancient philosopher on a pedestal at the right, long wooden table with open books, uniformly darkened with a strong 60% black overlay across the entire frame, moody sepia tones, even darkness suitable for three-column white text overlay, cinematic 16:9, no people, no text, no lettering, no symbols

---

## SLIDE 7 — Compliance & Data Sovereignty

**Replacement copy** (fix "API KEY LLM", replace emoji checks with gold vector checkmarks):

```
COMPLIANCE & DATA SOVEREIGNTY

  ✓  GDPR-compliant — EU-hosted, no US data transfer
  ✓  No training on your institution's data
  ✓  No API calls to OpenAI, Google, or xAI
  ✓  Full audit trail — every query logged locally
  ✓  You control the guardrails — not a corporation

  "When you use ChatGPT or any API-based LLM, your students' queries
   go to a server in California. When you use daïmōnes, they stay
   on your campus."

  This is the difference between renting and owning.
```

Design notes: align bullets to the same left edge as the title and quote box (currently indented ~60px off). Add a dark scrim behind the bullet column — it currently crosses the bright doorway glow. Make the closing line larger/bolder; it is the punchline. EU AI Act Article 50 + watermarking/provenance support may be added as a sixth check if space allows: "✓ AI Act Article 50 ready — provenance metadata and watermarking built in".

**Background image prompt:**
> Moody cinematic stone archive chamber, heavy dark wooden door standing ajar on the left revealing a warmly glowing inner room filled with shelves of ancient parchment scrolls, stone block walls in deep grey, small oil lamp on a stone pedestal at the right foreground, low-key lighting with the bright glow confined to the doorway only, entire left and center wall area in deep uniform shadow for text overlay, 16:9, no people, no text, no lettering, no symbols

---

## SLIDE 8 — Institutional Programs (FULL REBUILD — critical)

**The current slide is forbidden content**: the €15K/€45K/€75K/€225K public ladder was removed in Pricing v2 (Oct 2026). Enterprise "€225K + €45K/Year" also renders as a confusing two-price wrap.

**Replacement copy:**

```
INSTITUTIONAL PROGRAMS

DAÏMŌNES PLATFORM — academic programs (architect@daimones.ai)

  SEMESTER PILOT          COURSE PACK             DEPARTMENT PROGRAM
  One course, one         Single-course           Multi-course,
  semester, full          adoption for            budget-scoped
  functionality           teaching staff          department-wide
  Paid pilot —            Per-course              Annual agreement
  case-study rights       licensing               Dedicated support
  = discount lever

LYCEUM IN A BOX — on-premise deployments (hello@powerhouseconsulting.group)

  Custom deployments for NGOs, think tanks, and regulated organizations.
  Paid discovery → deployment → optional retainer.
  Quoted per institution. Delivered by PowerHouse Consulting Group.

All academic programs: self-hosted or EU-sovereign, zero data egress,
full source access, academic discount available.
```

Design notes: two clearly separated blocks — never mix the commercial lines. NO price figures on this slide for Lyceum in a Box. Fix the bleeding grid lines; keep four equal columns or switch to three cards + one banner.

**Background image prompt:**
> Elegant dark gradient background, charcoal black on the right fading to warm dark taupe brown on the left, very subtle marble texture, single gold bronze line-art Ionic column capital decoration at the far right edge partially cropped, large clean empty center for a four-column table overlay, premium minimal institutional aesthetic, 16:9, no text, no lettering, no symbols

---

## SLIDE 9 — Academic Traction

**Replacement copy** (translate ΕΚΠΑ, keep facts per Trello Oct 2026):

```
ACADEMIC TRACTION

  ΕΚΠΑ (National and Kapodistrian University of Athens)
  Philosophy Department — online presentation, Q4 2026

  • Five university demo tracks active (Greece, Australia) — all
    NGO-partner-driven
  • Active outreach to 50+ European & international universities
  • Published research: "The Alignment Tax" whitepaper
  • Public benchmark data and methodology on GitHub

  daïmōnes is not a startup pitch.
  It's an academic infrastructure project.
```

Design notes: make the closing two lines the largest non-title text on the slide — they are the reframe. Fix three different left indents to one margin. If the stock American campus photo stays, darken further; better: swap for a Mediterranean/Greek university feel (prompt below).

**Background image prompt:**
> Mediterranean university campus in late afternoon, neoclassical academic building with columned portico and pediment in warm beige stone, palm and cypress trees, stone-paved walkway, dry golden light, darkened with a heavy uniform 55% black overlay across the whole frame, muted greens and tans, empty right half for negative space, cinematic 16:9, no people, no text, no lettering, no flags, no symbols

---

## SLIDE 10 — Request a Pilot (CTA)

**Replacement copy** (remove free-trial framing — policy: all pilots paid):

```
REQUEST A DEPARTMENT PILOT

  →  Full functionality from day one
  →  Hosted sovereign or self-hosted on your infrastructure
  →  Paid pilot — transparent scope, case-study discount available

  ACADEMIC & PLATFORM        ON-PREMISE / CUSTOM
  architect@daimones.ai      hello@powerhouseconsulting.group
  daimones.ai/academic       PowerHouse Consulting Group

  The Digital Lyceum
  "where AI thinks like a philosopher, not a corporate lawyer."
```

Design notes: style the two contact blocks as distinct gold-bordered cards — the CTA is currently the same weight as the bullets and reads as an afterthought. Single consistent left margin for everything. Drop the embossed drop-shadow on the title; flat gold. Remove "no commitment · no data collection" (trial language) — replace with the paid-pilot line above.

**Background image prompt:**
> Classical Greek colonnade at sunset, Doric fluted columns receding in one-point perspective to the right, warm low sunlight and long diagonal shadows on weathered stone pavement, hazy orange horizon with faint distant hills, strong dark brown gradient overlay across the entire left half and bottom for text space, bright area confined to the upper right corner only, cinematic 16:9, no people, no text, no lettering, no symbols

---

## Global fixes checklist

- [ ] Brand spelling "daïmōnes" identical on all 10 slides (slide 3 currently "daimōnes")
- [ ] All URLs/emails ASCII: daimones.ai (never daïmōnes.ai)
- [ ] Remove or resize the illegible bottom-right marble logo on every slide
- [ ] Dark scrim/panel behind EVERY text block on photo backgrounds
- [ ] Replace all emoji (padlocks, ✅) with gold vector icons
- [ ] One left margin per slide; close all table grids
- [ ] No deprecated benchmark numbers anywhere (76.6/26.4/31.6, Claude)
- [ ] No €15K–€225K ladder anywhere; no free-trial language anywhere
- [ ] Slide 4 + 8 + 10 carry the two-product routing (architect@ vs powerhouseconsulting.group)
