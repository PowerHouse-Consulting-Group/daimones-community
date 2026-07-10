# MidJourney Guidelines — Academic & Institutions Presentation Deck

**Purpose:** Generate slide visuals for B2B institutional outreach deck  
**Brand Aesthetic:** Ancient Matte Stone, gold accents, Ancient Greek Temple - Cyberpunk  
**Tone:** Scholarly, rigorous, authoritative (NOT marketing-speak, NOT startup hype)

---

## Global Parameters (append to every prompt)

```
--ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 1: Title Slide

**Concept:** Sovereign dialectic engine — ancient wisdom meets modern infrastructure

**Prompt:**
```
Ancient Greek marble temple facade at dusk, cyberpunk neon cyan and gold circuit patterns woven into Corinthian columns, minimalist composition with negative space on right for text overlay, atmospheric fog, dark navy sky (#0a1628), cinematic lighting, photorealistic architectural detail, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (simpler):**
```
Classical Greek temple silhouette against dark gradient sky, gold accent lighting on columns, subtle digital grid overlay, clean negative space right side, cinematic depth of field, matte stone texture --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 2: The Problem — Corporate AI Alignment Tax

**Concept:** Censored reasoning, corporate control vs intellectual freedom

**Prompt:**
```
Dark corporate datacenter interior, blue LED server racks, chains and padlocks floating in foreground, fractured Greek philosophical texts scrolling on holographic displays, oppressive atmosphere, cinematic depth of field, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (metaphor):**
```
Classical Greek scroll partially unrolled, red censorship bars covering text sections, corporate glass tower reflection in background, dramatic chiaroscuro lighting, photorealistic parchment texture --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 3: The Solution — Sovereign Dialectic Engine

**Concept:** Intellectual sovereignty, on-premise infrastructure, uncensored reasoning

**Prompt:**
```
Modern server room with classical Greek architectural elements, marble columns integrated with rack servers, warm gold accent lighting, cyan data streams flowing between columns, open architecture suggesting freedom, clean professional aesthetic, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (symbolic):**
```
Open ancient Greek library interior, golden light streaming through columns, digital neural network patterns in air, scholars' desks with modern monitors, blend of classical and contemporary, photorealistic --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 4: Architecture Overview

**Concept:** Technical infrastructure diagram background

**Prompt:**
```
Abstract technical architecture diagram, dark navy background (#0a1628), gold connection lines between geometric nodes, subtle Greek key pattern borders, minimalist data flow visualization, professional engineering aesthetic, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (cleaner):**
```
Isometric server cluster diagram, matte stone texture components, gold circuit traces, dark background with subtle grid, technical blueprint style, architectural precision, no labels or text --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 5: Benchmark Performance

**Concept:** Data visualization background (use infographic instead of MJ for actual charts)

**Prompt:**
```
Abstract data visualization, bar chart silhouette against dark gradient, gold accent highlights on data points, subtle Greek temple columns in background, professional analytics dashboard aesthetic, cinematic depth of field, no text or numbers --ar 16:9 --style raw --v 7 --q 2
```

**Note:** For actual benchmark numbers (76.6 vs 26.4 vs 31.6), use the infographic from `~/daimones-repo/frontend/public/infographics/benchmark-scores.webp` or generate fresh with code.

---

## Slide 6: Use Case — Philosophy Department Integration

**Concept:** Academic setting, students engaging with AI

**Prompt:**
```
University philosophy seminar room, classical architecture with modern technology, students at wooden desks with tablets showing Greek text, professor gesturing toward holographic Aristotle quote, warm library lighting, scholarly atmosphere, photorealistic --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (focused on AI):**
```
Ancient Greek amphitheater interior, modern holographic AI interface floating above stage, students in contemporary clothing taking notes, blend of classical and digital, cinematic wide angle, golden hour lighting --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 7: Compliance & Data Sovereignty

**Concept:** Security, privacy, institutional control

**Prompt:**
```
Fortress architecture metaphor, classical Greek defensive walls with modern security elements, golden shield emblem in center, dark atmospheric lighting suggesting protection, professional cybersecurity aesthetic, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (document-focused):**
```
Ancient scroll with digital encryption overlay, gold seal stamp, dark wood desk surface, selective focus on security elements, professional legal document aesthetic, cinematic lighting --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 8: Licensing Tiers

**Concept:** Pricing structure background (minimal, let text dominate)

**Prompt:**
```
Minimalist geometric background, dark navy gradient, subtle gold horizontal lines suggesting tiers, abstract classical column capital in corner, clean professional negative space for text overlay, no text --ar 16:9 --style raw --v 7 --q 2
```

**Note:** This slide should be 90% text (pricing table), so keep visual minimal.

---

## Slide 9: Testimonials

**Concept:** Academic credibility, institutional endorsement

**Prompt:**
```
University campus at golden hour, classical architecture with modern elements, scholarly atmosphere, warm lighting suggesting prestige and tradition, photorealistic architectural photography, shallow depth of field, no people --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (abstract credibility):**
```
Classical Greek laurel wreath with digital circuit pattern, gold metallic texture, dark background, professional award aesthetic, cinematic lighting, symbol of academic achievement --ar 16:9 --style raw --v 7 --q 2
```

---

## Slide 10: Call to Action — Request Pilot

**Concept:** Next step, partnership opportunity

**Prompt:**
```
Open doorway in ancient Greek temple, golden light streaming through, modern server rack visible beyond threshold, symbolic transition from classical to digital, cinematic composition, hopeful atmosphere, no text --ar 16:9 --style raw --v 7 --q 2
```

**Alt prompt (handshake metaphor):**
```
Classical marble handshake sculpture with subtle digital wireframe overlay, gold accent lighting, dark professional background, symbol of partnership and collaboration, photorealistic detail --ar 16:9 --style raw --v 7 --q 2
```

---

## Color Palette Reference

```css
--dark-navy: #0a1628
--academic-gold: #D4AF37
--accent-cyan: #00d2ff
--matte-stone: #E8E4D9
--text-primary: #2C3E50
```

---

## Typography Recommendations

**Headings:** Playfair Display Bold or Cinzel  
**Body:** Inter or Lato  
**Greek text:** Noto Serif with polytonic support

---

## Usage Notes

1. **No text in images** — MJ hallucinates Greek characters. Add text in post (Keynote/PowerPoint/Figma)
2. **Negative space** — All prompts include composition guidance for text overlay
3. **Consistency** — Use same --v 7 --style raw parameters across all slides
4. **Variations** — Generate 4 variations per slide, select best composition
5. **Aspect ratio** --ar 16:9 matches standard presentation format

---

## Fallback Images

If MidJourney prompts don't produce desired aesthetic, use these existing assets:
- `~/daimones-repo/frontend/public/school_of_athens.jpg` (public domain, use grayscale + gold overlay)
- `~/daimones-repo/frontend/public/infographics/*.webp` (existing benchmark visualizations)

---

**Last updated:** 2026-07-10  
**Prepared for:** Vasilis Stergiou  
**Use case:** B2B institutional outreach deck (PDF export)
