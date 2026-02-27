# 🤖 robots.txt for DAIMONES Community GitHub Repository

# This file is for informational purposes only.
# GitHub Pages automatically handles robots.txt for github.io domains.

# For the main DAIMONES website (daimones.ai), see:
# /opt/daimones/public/robots.txt

---

## GitHub-Specific SEO Notes

### GitHub Pages (if enabled)
If you enable GitHub Pages for this repo (e.g., for documentation):

**robots.txt location:** `https://powerhouse-consulting-group.github.io/daimones-community/robots.txt`

**Recommended robots.txt for GitHub Pages:**
```
User-agent: *
Allow: /

# Sitemap
Sitemap: https://powerhouse-consulting-group.github.io/daimones-community/sitemap.xml
```

---

## 📊 SEO Optimizations for GitHub Repo

### 1. Repository Metadata (Already Configured)

✅ **Description:** "AI philosophical dialogue platform featuring Aristotle..."
✅ **Website:** https://daimones.ai
✅ **Topics:** ai, philosophy, aristotle, ancient-greek, etc.

### 2. README SEO (Already Optimized)

✅ **Title:** "🏛️ DAIMONES" with keywords
✅ **Description:** First paragraph contains key terms
✅ **Links:** Internal (docs) and external (daimones.ai)
✅ **Badges:** Shields.io for engagement
✅ **Structure:** H1, H2, H3 hierarchy

### 3. Additional SEO Files (Optional)

#### A. Sitemap (For GitHub Pages)
If you enable GitHub Pages, create `sitemap.xml`:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://powerhouse-consulting-group.github.io/daimones-community/</loc>
    <lastmod>2026-02-27</lastmod>
    <changefreq>weekly</changefreq>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://powerhouse-consulting-group.github.io/daimones-community/docs/FAQ.md</loc>
    <lastmod>2026-02-27</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.8</priority>
  </url>
  <url>
    <loc>https://powerhouse-consulting-group.github.io/daimones-community/CONTRIBUTING.md</loc>
    <lastmod>2026-02-27</lastmod>
    <changefreq>monthly</changefreq>
    <priority>0.7</priority>
  </url>
</urlset>
```

#### B. Open Graph Tags (For Social Sharing)
GitHub automatically generates Open Graph tags from README.

**What GitHub uses:**
- Repository name → `og:title`
- Description → `og:description`
- README images → `og:image`

**Manual override** (if using GitHub Pages):
```html
<meta property="og:title" content="DAIMONES Community - AI Philosophical Dialogue" />
<meta property="og:description" content="Engage with Aristotle in Polytonic Ancient Greek. Community-driven AI philosophy platform." />
<meta property="og:image" content="https://daimones.ai/assets/logo-daimones.png" />
<meta property="og:url" content="https://github.com/PowerHouse-Consulting-Group/daimones-community" />
```

---

## 📈 llms.txt (AI/LLM Discovery)

### What is llms.txt?

`llms.txt` is an emerging standard for helping AI/LLM systems discover and understand your project.

**Location:** Root of repository

**Content:**
```markdown
# DAIMONES Community

**Name:** DAIMONES
**Description:** AI philosophical dialogue platform featuring Aristotle
**Website:** https://daimones.ai
**Repository:** https://github.com/PowerHouse-Consulting-Group/daimones-community

## Key Technologies
- Large Language Models (LLM)
- Retrieval-Augmented Generation (RAG)
- Polytonic Ancient Greek NLP
- React + TypeScript
- Node.js + Express
- PostgreSQL + pgvector

## Documentation
- [FAQ](docs/FAQ.md)
- [Contributing Guide](CONTRIBUTING.md)
- [Code of Conduct](CODE_OF_CONDUCT.md)
- [Labels Guide](docs/LABELS_GUIDE.md)

## Contact
- **Email:** architect@daimones.ai
- **Issues:** https://github.com/PowerHouse-Consulting-Group/daimones-community/issues
```

### Do You Need llms.txt?

**Current Status:** ❓ Optional / Emerging Standard

**Benefits:**
- ✅ Helps AI systems (like Claude, ChatGPT) understand your project
- ✅ Improves AI-generated recommendations
- ✅ Future-proof for AI-powered code search

**Recommendation:** **Create it** (low effort, potential future benefit)

---

## 🎯 SEO Priority Matrix

| Task | Priority | Effort | Impact | Status |
|------|----------|--------|--------|--------|
| **Repository Description** | 🔴 High | Low | High | ✅ Done |
| **Topics/Tags** | 🔴 High | Low | High | ✅ Done |
| **README Optimization** | 🔴 High | Medium | High | ✅ Done |
| **FUNDING.yml** | 🟡 Medium | Low | Medium | ⏳ Pending |
| **llms.txt** | 🟡 Medium | Low | Medium (Future) | ⏳ Pending |
| **robots.txt** | 🟢 Low | Low | Low | ❓ Not needed (GitHub handles) |
| **sitemap.xml** | 🟢 Low | Medium | Low | ❓ Only if GitHub Pages enabled |

---

## ✅ RECOMMENDATIONS

### Do Now (5 minutes)
1. ✅ **FUNDING.yml** - Enable sponsorship link
2. ✅ **llms.txt** - Future-proof for AI discovery

### Do Later (Optional)
- ❓ **GitHub Pages** - Only if you want standalone documentation site
- ❓ **sitemap.xml** - Only if GitHub Pages enabled
- ❓ **robots.txt** - GitHub handles automatically

### Not Needed
- ❌ **Custom robots.txt** - GitHub manages this
- ❌ **Manual Open Graph** - GitHub auto-generates from README

---

## 📁 Files to Create

### 1. FUNDING.yml (GitHub Sponsors)
**Location:** `.github/FUNDING.yml`

**Purpose:** Link to daimones.ai billing page

### 2. llms.txt (AI Discovery)
**Location:** `llms.txt` (root)

**Purpose:** Help AI systems understand the project

---

**Ready to create these files!** 🏛️
