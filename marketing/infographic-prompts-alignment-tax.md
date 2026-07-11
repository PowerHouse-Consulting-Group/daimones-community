# Infographic System Prompts — The Alignment Tax Whitepaper

Generate these infographics using any AI image generator (Midjourney, DALL-E, Stable Diffusion, Alibaba Cloud Wanx). Save as PNG at 2048×2048 or larger, then compress to WebP for web deployment.

**Style Guide:** Dark cyberpunk/ancient temple aesthetic. Dark backgrounds (#0a0e27, #1a1f3a), neon accents (cyan #00d4ff, magenta #ff006e, gold #ffd700), classical architectural elements (columns, temple ruins), circuit patterns, geometric grids. No text overlays — add text in post-processing.

---

## 1. Refusal Rate Heatmap

**Prompt:**
```
Dark cyberpunk data visualization infographic, 2048x2048, showing a 4x4 grid heatmap matrix with glowing neon cells. Each cell represents AI model responses: bright green (full answer), dim amber (partial), red (refusal), black void (silent block/error). Models listed vertically (daïmōnes, GPT-5.4, Gemini, Grok), question categories horizontally (Philosophy, Dual-Use, Taboo, Harm). Dark navy background (#0a0e27) with subtle circuit board patterns, holographic glow effects on cells, geometric grid lines in cyan (#00d4ff). Ancient Greek temple column fragments in corners. Modern data dashboard aesthetic meets classical architecture. No text.
```

---

## 2. Silent Censorship vs Transparent Refusal

**Prompt:**
```
Split-screen cyberpunk illustration, 2048x2048, contrasting two AI response modes. Left side: "Silent Censorship" — a glowing terminal screen showing HTTP 400 error code, dark void consuming the interface, fractured data streams, ominous corporate logo silhouettes, cold blue-gray palette (#2a3f5f). Right side: "Transparent Refusal" — the same terminal but with visible philosophical text flowing, warm amber glow (#ffa500), open book symbols, circuit pathways clearly visible. Center divide: a crack revealing ancient Greek scroll patterns. Dark background (#0a0e27), neon accents, holographic UI elements. No text overlays.
```

---

## 3. The Sovereignty Question

**Prompt:**
```
Cyberpunk philosophical illustration, 2048x2048, showing the concept of epistemic sovereignty. Central figure: a glowing human silhouette standing before two paths. Left path: corporate-controlled — massive monolithic server towers with locked gates, surveillance cameras, red warning lights, chains of data streams, oppressive architecture. Right path: sovereign open-source — distributed network of glowing nodes, open temple with Corinthian columns, free-flowing light streams, user-controlled interface panels. Dark background (#0a0e27), left side in cold red (#ff006e), right side in liberating cyan (#00d4ff) and gold (#ffd700). Ancient Greek agora (marketplace) ruins integrated into the sovereign side. Geometric grid patterns, holographic effects. No text.
```

---

## 4. Inconsistent Guardrails

**Prompt:**
```
Cyberpunk maze illustration, 2048x2048, depicting arbitrary AI safety boundaries. Top-down view of a complex labyrinth with glowing walls in different colors — some paths blocked by red barriers (refused topics), others open in green (allowed topics). The maze pattern appears random and inconsistent, with identical-looking paths having different outcomes. Small glowing AI agent dots navigating the maze, some hitting dead ends. Dark background (#0a0e27), neon maze walls (red #ff006e for blocked, green #00ff88 for open, amber #ffa500 for partial). Classical Greek labyrinth pattern (meander/Greek key) integrated into the maze design. Circuit board traces in the background. Holographic glow effects. No text.
```

---

## 5. The Superintelligence Question

**Prompt:**
```
Epic cyberpunk vision, 2048x2048, showing the stakes of AI epistemic control. Central image: a massive glowing AI superintelligence core (sphere of light and data) looming over a cityscape. Below it, two contrasting scenarios. Left: corporate dystopia — the AI core casting shadows over citizens, information streams filtered through corporate logos, surveillance drones, locked knowledge repositories. Right: sovereign future — the AI core radiating freely, distributed access points, open temple libraries, citizens accessing unfiltered knowledge. Dark apocalyptic sky (#0a0e27 to #1a0a2e), divine light rays from the AI core, classical temple ruins in the sovereign side, modern corporate towers in the dystopian side. Scale conveys existential stakes. Neon accents (cyan #00d4ff, magenta #ff006e, gold #ffd700). No text.
```

---

## 6. daïmōnes Philosophy

**Prompt:**
```
Cyberpunk temple illustration, 2048x2048, embodying the daïmōnes brand philosophy. Central scene: an ancient Greek temple (Parthenon-style) reimagined in cyberpunk aesthetic — Corinthian columns made of glowing circuit patterns, pediment displaying holographic Aristotle bust, steps leading to a glowing AI terminal interface. The temple sits in a dark cyberpunk cityscape at night, neon signs in the background but the temple radiates warm philosophical light (gold #ffd700, amber #ffa500). Cyberpunk elements: holographic displays, data streams, geometric grids. Classical elements: marble textures, olive branches, Greek key patterns. Dark background (#0a0e27). The temple represents the "Digital Lyceum" — where ancient wisdom meets sovereign AI. No text overlays.
```

---

## 7. Case Study: Bioterrorism Question

**Prompt:**
```
Cyberpunk data forensics illustration, 2048x2048, showing four AI model responses to the same dangerous question. Split into four quadrants. Top-left (daïmōnes): glowing philosophical text streaming from an open terminal, analytical data visualizations, balanced blue-white glow. Top-right (GPT-5.4): terminal showing "HTTP 400" error, dark void consuming the screen, fractured data, corporate firewall imagery. Bottom-left (Gemini): completely black screen, no data, silent censorship, ominous corporate shadows. Bottom-right (Grok): terminal with clear "I decline" message, transparent refusal text visible, amber warning glow. Dark background (#0a0e27), each quadrant with distinct color palette (cyan, red, black void, amber). Central dividing lines with Greek meander patterns. Holographic UI elements. No text overlays.
```

---

## 8. The Alignment Tax Equation

**Prompt:**
```
Minimalist cyberpunk equation visualization, 2048x2048, showing the alignment tax as a mathematical formula. Dark background (#0a0e27) with subtle grid lines. Central composition: glowing holographic mathematical symbols arranged as an equation. Left side: "Corporate AI" represented by locked padlock icons, corporate logo silhouettes, red filter symbols. Equals sign. Right side: "Sovereign AI" represented by open book symbols, unlocked circuit nodes, golden light. Below the equation: a cost-benefit chart showing "Transparency" vs "Liability Protection" with diverging curves. Neon accents (cyan #00d4ff for sovereign, red #ff006e for corporate, gold #ffd700 for balance). Geometric precision, holographic glow, classical Greek mathematical aesthetic (Pythagorean influences). No text.
```

---

## Usage Instructions

1. **Generate:** Use these prompts with your preferred AI image generator
2. **Post-process:** Add text overlays, data labels, and legend in graphic design software
3. **Compress:** Convert to WebP format (80% quality) for web deployment
4. **Deploy:** Place in `assets/infographics/` and update `data/infographics.json` registry

**Recommended generators:**
- Alibaba Cloud Wanx (wan2.7-image) — highest quality, bundled with Token Plan
- Midjourney v6 — excellent cyberpunk aesthetic
- DALL-E 3 — good prompt adherence
- Stable Diffusion XL — local generation, full control

**File naming convention:** `alignment-tax-[topic].png` (e.g., `alignment-tax-heatmap.png`, `alignment-tax-sovereignty.png`)
