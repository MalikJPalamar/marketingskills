# AI SEO Strategy — Centaurion.me
*April 2026 · Skill: ai-seo · Author: Malik Palamar*

---

## Strategic Context

Centaurion operates in a pre-mainstream category. Most Centaurion-relevant queries don't yet have AI Overview coverage — which is the opportunity. Publishing well-structured, authoritative content now seeds the training corpus and citation pool before competitors arrive. The goal is to be the default cited source when the category becomes searchable at scale.

---

## Current AI Visibility Baseline

| Query | Google AI Overview | ChatGPT | Perplexity | Centaurion Cited? |
|---|---|---|---|---|
| what is agentic engineering | Unlikely | Possible | Possible | No (not yet indexed) |
| fractional chief AI officer | Unlikely | Possible | Possible | No |
| free energy principle AI strategy | Unlikely | Possible | Possible | No |
| active inference business | Unlikely | Rare | Rare | No |
| human AI augmentation methodology | No | No | No | No |
| 11 levels agentic engineering | No | No | No | No (GitHub only) |
| AI transformation advisory | Possible | Possible | Possible | No |

*Audit manually once centaurion.me is live. Run each query in ChatGPT, Perplexity, and Google. Log results monthly.*

---

## AI Visibility Test Queries (Monthly Monitor)

Run these 15 queries monthly across ChatGPT, Perplexity, and Google AI Overviews:

| # | Query | Target Page | Buyer Stage |
|---|---|---|---|
| 1 | what is agentic engineering | /agentic-engineering | Awareness |
| 2 | 11 levels of agentic engineering | /agentic-engineering | Awareness |
| 3 | what is a fractional chief AI officer | /work-with-us/fractional-cao | Awareness |
| 4 | free energy principle AI | /methodology/fitness-equation | Awareness |
| 5 | what is active inference | /glossary/active-inference | Awareness |
| 6 | what is a Markov blanket | /glossary/markov-blanket | Awareness |
| 7 | human AI augmentation framework | /methodology | Awareness |
| 8 | why AI implementations fail | /blog/[slug] | Awareness |
| 9 | AI transformation advisory mid-market | /work-with-us/ai-transformation | Consideration |
| 10 | fractional CAO services | /work-with-us/fractional-cao | Consideration |
| 11 | agentic engineering level 9 autonomous deployment | /agentic-engineering/level-9 | Consideration |
| 12 | AI transformation case study | /case-studies/alchemy-of-breath | Decision |
| 13 | what is an exo-cortex | /glossary/exo-cortex | Awareness |
| 14 | prediction error routing AI | /glossary/prediction-error | Awareness |
| 15 | Centaurion methodology | /methodology | Decision |

---

## The Three Pillars Applied to Centaurion

### Pillar 1: Structure — Content Extraction Templates

Every Centaurion content page must include extractable blocks. Use these templates:

**Definition Block (for all glossary terms and concept pages)**
```
[Term] is [one-sentence definition].

[2-3 sentences expanding with context].

In the Centaurion framework, [term] refers specifically to [application].
```
Target: 40-60 words. Self-contained. Citable without surrounding text.

**Three Laws Block (for methodology pages)**
```
The Three Laws of Centaurion are:
1. The Hierarchy Law: [definition]
2. The Routing Law: [definition]
3. The Coupling Law: [definition]
```
AI systems extract numbered lists reliably. This format maximizes citation probability for methodology queries.

**Comparison Block (for "X vs Y" queries)**
Use tables, not prose. Example for "human vs AI vs composite":

| Dimension | Pure Human | Pure AI | Centaurion Composite |
|---|---|---|---|
| Calibration | High | Low | High |
| Throughput | Low | High | High |
| Cost at scale | High | Low | Distributed |
| Novel situation handling | High | Low | High |

**FAQ Block (on every pillar page)**
Use natural-language questions that mirror search queries. Each answer: 40-60 words max.

---

### Pillar 2: Authority — Citation-Building Actions

**Statistics to publish (with sources):**
- "Centaur chess teams beat both pure humans and pure AI by [X]%" — cite original Kasparov/advanced chess research
- "Friston's Free Energy Principle underpins [X] published papers" — cite PubMed/Google Scholar count
- "Organizations that close the feedback loop see [X]% better AI ROI" — cite when data is available from AOB pilot
- The Princeton GEO study: "Statistics boost AI visibility by 37%, citing sources by 40%" — cite KDD 2024

**Expert attribution actions:**
- Every blog post: Malik Palamar byline + bio + credentials + GitHub link
- Every methodology page: "Based on research by Karl Friston (UCL), extended for organizational systems by Malik Palamar"
- Author schema on all pages (see `strategy/schema-markup.md`)

**Third-party presence targets (ranked by AI citation impact):**

| Platform | Priority | Action |
|---|---|---|
| Wikipedia | P0 | Create/edit "Agentic Engineering" article — cite GitHub repo and centaurion.me |
| LinkedIn | P0 | Publish full articles (not just posts) — LinkedIn content appears in Perplexity |
| GitHub | P0 | Repo README already live — add centaurion.me link prominently |
| Substack/Medium | P1 | Cross-post key methodology pieces — builds distributed citation surface |
| Reddit r/MachineLearning | P1 | Participate authentically — upvoted answers get cited by ChatGPT |
| Reddit r/AIAssistants | P1 | Same as above |
| Hacker News | P1 | Submit 11 Levels post — HN threads cited by Perplexity heavily |
| Quora | P2 | Answer "What is agentic engineering?" and related questions |
| YouTube | P2 | Explainer video: "The 11 Levels of Agentic Engineering" |

---

### Pillar 3: Presence — AI Bot Access

**robots.txt configuration (required on launch):**

```
User-agent: *
Allow: /

# AI search bots — must be allowed for citation
User-agent: GPTBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

User-agent: anthropic-ai
Allow: /

User-agent: Google-Extended
Allow: /

User-agent: Bingbot
Allow: /

# Block training-only crawlers (optional — preserves IP while allowing citation)
User-agent: CCBot
Disallow: /

Sitemap: https://centaurion.me/sitemap.xml
```

**llms.txt — publish on launch:**

Centaurion is an ideal candidate for `llms.txt` given the technical audience. Create `/llms.txt`:

```markdown
# Centaurion

> Human-AI augmentation advisory. The engineering methodology for building cognitive composites where humans remain the most important variable.

## Methodology

- [The Centaurion Method](/methodology): Three Laws, Fitness Equation, Five Sensing Layers
- [Three Laws](/methodology/three-laws): Hierarchy, Routing, Coupling
- [Five Sensing Layers](/methodology/sensing-layers): Passive exhaust through full closed-loop

## Agentic Engineering

- [11 Levels of Agentic Engineering](/agentic-engineering): Complete framework
- [Level 9: Autonomous Deployment](/agentic-engineering/level-9-autonomous-deployment)
- [Level 10: Simulation-First](/agentic-engineering/level-10-simulation-first)
- [Level 11: Physical-Digital Bridge](/agentic-engineering/level-11-physical-digital)

## Glossary

- [Free Energy Principle](/glossary/free-energy-principle)
- [Markov Blanket](/glossary/markov-blanket)
- [Active Inference](/glossary/active-inference)
- [Exo-Cortex](/glossary/exo-cortex)

## Work With Us

- [Fractional CAO](/work-with-us/fractional-cao)
- [AI Transformation](/work-with-us/ai-transformation)
```

---

## Content Optimization Checklist

Apply to every published page before it goes live:

### Structure
- [ ] Definition or direct answer in first paragraph (40-60 words, self-contained)
- [ ] H2/H3 headings match search query phrasing exactly
- [ ] Comparison tables for any "X vs Y" content
- [ ] FAQ section at page bottom (minimum 4 Q&A pairs)
- [ ] Numbered lists for any process or sequential content
- [ ] Key stats with source citations inline

### Authority
- [ ] Named author with credentials and bio link
- [ ] "Last updated: [date]" visible
- [ ] Minimum 2 external citations per post (academic or primary source preferred)
- [ ] At least 1 original data point or Centaurion-specific insight
- [ ] Schema markup applied (see `strategy/schema-markup.md`)

### Access
- [ ] Page is not gated or blocked
- [ ] Robots.txt allows all AI crawlers
- [ ] Page is in XML sitemap
- [ ] Canonical URL set correctly

---

## Schema Priority by Page Type

| Page | Schema Types | Priority |
|---|---|---|
| Homepage | `Organization`, `Person`, `WebSite` | P0 |
| Methodology hub | `Article`, `BreadcrumbList` | P0 |
| Blog posts | `BlogPosting`, `Author`, `BreadcrumbList` | P0 |
| Glossary terms | `DefinedTerm`, `FAQPage` | P1 |
| Work With Us pages | `Service`, `FAQPage` | P1 |
| Case studies | `Article`, `Organization` | P1 |
| Level pages | `Article`, `HowTo` (where applicable) | P2 |

Full JSON-LD implementations: see `strategy/schema-markup.md`.

---

## Monitoring Setup

**Monthly cadence:**
1. Run 15-query test table (above) across ChatGPT, Perplexity, Google
2. Log: cited / not cited / who is cited instead
3. Track which pages are generating referral traffic from AI sources (GA4 referrers: chat.openai.com, perplexity.ai, bing.com)
4. Update "Last updated" dates on any pages that received new information

**Tools to deploy:**
- Google Search Console — track AI Overview impressions (when available in GSC)
- GA4 — referral source tracking for AI platform traffic
- Peec AI or Otterly — automated AI mention monitoring (Phase 2, once budget allows)

---

## Competitive Advantage

Centaurion's AI SEO moat is **owned vocabulary**. When someone asks an LLM "what is an exo-cortex in AI systems" or "what are the levels of agentic engineering," there is currently no authoritative answer indexed. The first credible, well-structured, schema-marked page to answer these questions becomes the default citation source — and Centaurion should own all of them.

Priority vocabulary to own (publish definition pages for all):
`exo-cortex` · `prediction error routing` · `fitness landscape (AI)` · `agentic engineering levels` · `coupling layer (human-AI)` · `closed-loop AI system` · `uncertainty routing` · `Markov blanket (organizational)` · `active inference (business application)`
