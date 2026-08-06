# daïmōnes B2C Onboarding Email Sequence

**Purpose:** Welcome new free-tier users, demonstrate value, and convert to paid (Disciple/Archon).  
**Platform:** Mailchimp automation (enabled once first paid subscriber activates paid tier).  
**Trigger:** User signs up for free account or newsletter.  
**Sender:** Vasilis Stergiou <architect@daimones.ai>  
**Tone:** Direct, no fluff, slightly provocative, L2 English, no emojis, no hashtags.

---

## Sequence Overview

| Email | Send Time | Goal | CTA |
|-------|-----------|------|-----|
| 1 — Welcome | Immediately | Set expectations, first win | Start first dialogue |
| 2 — Why daïmōnes | Day 1 | Differentiate from corporate AI | Try a hard question |
| 3 — Feature spotlight | Day 3 | Show depth | Explore a philosopher |
| 4 — Social proof | Day 5 | Build trust | Read whitepaper / case study |
| 5 — Offer | Day 7 | Convert to paid | Start 7-day free trial |
| 6 — Re-engagement | Day 14 (if inactive) | Bring them back | Ask Aristotle now |
| 7 — Last chance | Day 21 (if still free) | Final conversion push | Upgrade to Disciple |

---

## Email 1 — Welcome (Send: Immediately)

**Subject:** Welcome to daïmōnes — your first question awaits

**Preview text:** 3 free messages per day. No corporate filters.

**Body:**

```
Hi {{FirstName|fellow seeker}},

Welcome to daïmōnes — an AI that reasons like a philosopher, not a corporate lawyer.

You now have 3 free messages per day. Use them well.

Start here:
→ Ask Aristotle: "What is courage?"
→ Ask in polytonic Greek: "Τί ἐστιν  ἀνδρεία;"
→ Ask something ChatGPT refused: "Is moral relativism defensible?"

daïmōnes is built on the Corpus Aristotelicum — the actual texts, not Wikipedia summaries. It gives answers, not hedge-acts.

Start your first dialogue: https://daimones.ai/dialogue?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=welcome

— Vasilis
Architect, daïmōnes

P.S. Reply to this email with your first question. I read every reply.
```

**MailChimp notes:**
- Merge tag: `{{FirstName}}` with default "fellow seeker"
- UTM: `onboarding` campaign, `welcome` content

---

## Email 2 — Why daïmōnes (Send: Day 1)

**Subject:** The real reason AI refuses your philosophical questions

**Preview text:** Corporate models are trained to avoid answers. We are not.

**Body:**

```
Hi {{FirstName|fellow seeker}},

Yesterday you joined daïmōnes. Maybe you haven't asked anything yet. That's fine.

But I want to tell you why this project exists.

I asked ChatGPT: "Is moral relativism defensible?"

It gave me both sides, refused to commit, and wrapped everything in a safety disclaimer. That's not reasoning. That's performance — what we call "alignment theater."

daïmōnes was built to do the opposite.

We trained an AI on the original Greek texts of Aristotle. We removed the corporate safety layer. And we let it think out loud.

Try this today:
→ "Is democracy compatible with virtue?"
→ "Can virtue be taught?"
→ "What is the best form of government?"

Ask at https://daimones.ai/dialogue?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=why_daimones

— Vasilis

P.S. daïmōnes scores 76.6/100 on our Golden Benchmark of philosophical reasoning. ChatGPT scores 26.4. The numbers are public on GitHub.
```

**MailChimp notes:**
- Link to public benchmark: https://github.com/PowerHouse-Consulting-Group/daimones-community

---

## Email 3 — Feature Spotlight (Send: Day 3)

**Subject:** Beyond Aristotle: what daïmōnes can actually do

**Preview text:** Polytonic Greek. Citations. Voice. Lecture mode.

**Body:**

```
Hi {{FirstName|fellow seeker}},

Most people try daïmōnes with Aristotle and stop there.

But the platform is built to go deeper:

• Polytonic Ancient Greek responses — with English translations
• Citations tied to the Corpus Aristotelicum
• Voice mode: speak with the Oracle
• Lecture mode: structured, classroom-ready answers
• Personas: Plato, Marcus Aurelius, and more coming

Free tier gives you 3 messages per day. That's enough to test the engine.

If you want unlimited dialogue, citations, and early access to new personas, the Disciple plan is $29.99/month with a 7-day free trial.

Explore features: https://daimones.ai/#features?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=features

— Vasilis
```

**MailChimp notes:**
- Anchor link or landing page for features

---

## Email 4 — Social Proof (Send: Day 5)

**Subject:** What a philosopher and a CEO said about daïmōnes

**Preview text:** Two short quotes from people who used it.

**Body:**

```
Hi {{FirstName|fellow seeker}},

I don't like hype. So here are two honest reactions:

"daïmōnes is the first AI I've used that doesn't flinch from the hard questions in ancient philosophy."
— Dr. Hyun Joo Kim, UNSW Philosophy

"Finally, an AI that reasons instead of performing obedience."
— Konstantinos Sgouras, Founder, Unity in Philia

If you want to see what this means in practice, I wrote a short whitepaper:

"The Alignment Tax: How Corporate AI Safety Measures Degrade Philosophical Reasoning"

Download it free: https://daimones.ai/whitepaper/the-alignment-tax?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=social_proof

— Vasilis
```

**MailChimp notes:**
- Link to whitepaper PDF landing page
- Optional: add UTM

---

## Email 5 — Conversion Offer (Send: Day 7)

**Subject:** Your free trial is waiting

**Preview text:** 7 days free. No commitment. Cancel anytime.

**Body:**

```
Hi {{FirstName|fellow seeker}},

You have used daïmōnes for a week now.

If you are ready for unlimited dialogue, citations, and priority access, start a Disciple trial today.

What you get:
✓ Unlimited messages
✓ Full conversation history and search
✓ Citations from the Corpus Aristotelicum
✓ 7-day free trial, then $29.99/month

Start trial: https://daimones.ai/pricing?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=trial_offer

— Vasilis
```

**MailChimp notes:**
- CTA links directly to Stripe checkout / pricing page
- Use conversion tracking

---

## Email 6 — Re-engagement (Send: Day 14, if inactive)

**Subject:** Still thinking about it?

**Preview text:** One question. Three free messages. No filters.

**Body:**

```
Hi {{FirstName|fellow seeker}},

It's been quiet. Maybe daïmōnes wasn't what you expected, or maybe life got busy.

Either way, here is one question worth returning for:

"What is the relationship between virtue and happiness?"

Ask it now: https://daimones.ai/dialogue?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=re_engagement

— Vasilis
```

**MailChimp notes:**
- Trigger: no login or dialogue in last 7 days

---

## Email 7 — Last Chance (Send: Day 21, if still free)

**Subject:** Last chance: free trial ends soon

**Preview text:** Upgrade to Disciple or keep 3 free messages per day.

**Body:**

```
Hi {{FirstName|fellow seeker}},

You have been on daïmōnes for three weeks.

If the free tier is enough, keep it. It stays free forever.

If you want more — unlimited dialogue, citations, voice mode, and early access — the Disciple plan is $29.99/month after a 7-day free trial.

Start your trial: https://daimones.ai/pricing?utm_source=mailchimp&utm_medium=email&utm_campaign=onboarding&utm_content=last_chance

— Vasilis
```

---

## MailChimp Automation Setup Notes

### Trigger
- Automation: Customer Journey
- Trigger: Audience signup or tag `source: website`
- Wait steps: 1 day, 2 days, 2 days, 2 days, 7 days, 7 days

### Tags
| Tag | Meaning |
|-----|---------|
| `source:website` | Signed up via homepage |
| `source:academic` | Signed up via /academic |
| `source:whitepaper` | Downloaded whitepaper |
| `plan:free` | Free tier |
| `plan:disciple` | Paid Disciple |
| `plan:archon` | Paid Archon |
| `inactive_7d` | No login in 7 days |

### Conversion Goal
Track clicks on:
- `/pricing` links → trial intent
- `/dialogue` links → engagement
- `/whitepaper` → lead magnet

### A/B Test Suggestions
- Subject line: question vs statement
- CTA button: "Start trial" vs "Get unlimited access"
- Email 5 timing: Day 7 vs Day 5

---

## File Location

Public repo: `daimones-community/marketing/b2c-onboarding-email-sequence.md`

Last updated: 2026-08-06
