# Product Hunt Launch — daïmōnes

## Status: PREPARING
## Target Window: Late July / Early August 2026

---

## Checklist

### Pre-Launch (2 weeks before)
- [ ] Finalize tagline (max 60 chars)
- [ ] Write description (max 500 chars)
- [ ] Create thumbnail (240×240px, square, <3MB)
- [ ] Create 2+ gallery images (1270×760px)
- [ ] Record demo video (60-90s, optional but recommended)
- [ ] Create interactive demo (Arcade/Storylane — optional)
- [ ] Draft first comment (maker story, features, audience, offer)
- [ ] Select 3 launch tags
- [ ] Prepare promo code for PH community
- [ ] Ensure Vasilis has a Product Hunt account
- [ ] Ensure all co-makers have PH accounts (if applicable)
- [ ] Build pre-launch buzz on X ("Launching on PH next week")

### Launch Day
- [ ] Schedule launch at 12:01 AM PST
- [ ] Be online from 12:01 AM PST through midnight
- [ ] Respond to every comment within 1 hour
- [ ] Share launch link on X, Telegram, email list
- [ ] Post in relevant communities (LocalLLaMA, philosophy subs)
- [ ] Do NOT ask for upvotes — ask for feedback

### Post-Launch
- [ ] Analyze traffic spike (Google Analytics / Plausible)
- [ ] Track signups from PH (UTM params)
- [ ] Follow up with engaged commenters
- [ ] Write post-mortem: what worked, what didn't

---

## Assets Needed

| Asset | Spec | Status |
|---|---|---|
| Tagline | 60 chars max | See `prep/tagline-options.md` |
| Description | 500 chars max | See `prep/description-draft.md` |
| Thumbnail | 240×240px | TODO — use logo |
| Gallery Image 1 | 1270×760px | TODO — chat interface screenshot |
| Gallery Image 2 | 1270×760px | TODO — article/pricing screenshot |
| Demo Video | 60s (4×15s clips) | See `prep/promo-video-system-prompts.md` — in production |
| First Comment | Free-form | See `prep/first-comment-draft.md` |
| Promo Code | Code + offer | TODO |

---

## Key Rules
1. **One shot only** — can't re-launch the same product
2. **Don't ask for upvotes** — PH will penalize you
3. **Respond to every comment** — engagement matters more than votes
4. **Be humble and helpful** — marketing-speak gets downvoted
5. **Schedule at 12:01 AM PST** — captures full 24h cycle

---

## Folder Structure
```
marketing/product-hunt-launch/
├── README.md              ← this file
├── assets/
│   ├── thumbnail.png      ← 240×240 (logo)
│   ├── gallery-1.png      ← 1270×760 (chat screenshot)
│   ├── gallery-2.png      ← 1270×760 (article/pricing)
│   └── demo-video.mp4     ← optional
└── prep/
    ├── tagline-options.md
    ├── description-draft.md
    └── first-comment-draft.md
```
