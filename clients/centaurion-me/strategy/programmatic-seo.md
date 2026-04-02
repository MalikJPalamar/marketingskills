# Programmatic SEO — Centaurion.me
*April 2026 · Skill: programmatic-seo · Author: Malik Palamar*

---

## Opportunity Overview

Centaurion has four natural programmatic SEO plays, each rooted in proprietary or semi-proprietary data. The 11 Levels framework is the clearest opportunity — it's defined IP that maps directly to 11 standalone indexable pages. The glossary and persona pages follow the same logic: owned vocabulary + defined audience segments = defensible content at scale.

| Playbook | Pages | Data Source | Defensibility | Priority |
|---|---|---|---|---|
| **11 Levels** (Personas/Profiles) | 11 | Proprietary IP | Very High | P0 |
| **Glossary** | 20–40 | Proprietary vocabulary | High | P0 |
| **Personas** ("AI transformation for [segment]") | 8–12 | ICP research | Medium | P1 |
| **Comparisons** ("Centaurion vs [approach]") | 5–8 | Competitive analysis | Medium | P2 |

---

## Playbook 1: 11 Levels of Agentic Engineering

### Opportunity
The 11 Levels framework is published IP. Zero pages currently rank for "level [N] agentic engineering" because the content only exists on GitHub. Publishing each level as a standalone web page creates 11 indexable assets from existing work.

### Keyword Pattern
`[level name] agentic engineering` / `how to reach level [N] agentic engineering` / `what is [level name] AI`

### Page Count: 11

### URL Structure
```
/agentic-engineering/                              (hub — links to all 11)
/agentic-engineering/level-1-tab-complete/
/agentic-engineering/level-2-chat-driven/
/agentic-engineering/level-3-context-loaded/
/agentic-engineering/level-4-compounding-sessions/
/agentic-engineering/level-5-mcp-connected/
/agentic-engineering/level-6-harnessed-agents/
/agentic-engineering/level-7-background-agents/
/agentic-engineering/level-8-multi-agent-orchestration/
/agentic-engineering/level-9-autonomous-deployment/
/agentic-engineering/level-10-simulation-first/
/agentic-engineering/level-11-physical-digital-bridge/
```

### Title Template
`Level [N]: [Level Name] — The 11 Levels of Agentic Engineering | Centaurion`

### Meta Description Template
`[Level Name] is Level [N] of the 11 Levels of Agentic Engineering. Learn what it means, how to reach it, and what separates it from Level [N-1].`

### Page Template (per level)

```
H1: Level [N]: [Level Name]

[DEFINITION BLOCK — 40-60 words, self-contained for AI extraction]
Level [N] of agentic engineering is [definition]. At this level, [what the system can do].
This is distinct from Level [N-1] ([previous level name]) because [key difference].

## What Level [N] Means

[150-250 words: full explanation, practical context, what it looks like in production]

## Prerequisites

- [ ] Level [N-1]: [Previous Level Name] — [one-sentence prerequisite]
- [ ] [Technical/organizational requirement]
- [ ] [Tooling or infrastructure requirement]

## What This Unlocks

[100-150 words: what becomes possible at this level that wasn't before]

## Real-World Example

[100-200 words: concrete example. For Levels 9-11, draw from AOB pilot or own exo-cortex]

## How to Get Here

[HowTo block — 3-5 numbered steps. Maps to HowTo schema]

1. [Step 1]
2. [Step 2]
3. [Step 3]

## Common Mistakes at This Level

- [Mistake 1]
- [Mistake 2]

## Level [N] FAQ

**What separates Level [N] from Level [N-1]?**
[40-60 word answer]

**How long does it take to reach Level [N]?**
[40-60 word answer]

**What tools are needed for Level [N]?**
[40-60 word answer]

## Next Level

→ [Level N+1]: [Next Level Name]

[Previous: Level N-1] | [Back to: 11 Levels Overview] | [Next: Level N+1]
```

### Internal Linking
- Hub page links to all 11 levels
- Each level page links to previous, next, and hub
- Level 9–11 pages (Palamar extensions) cross-link to `/methodology`
- Blog posts referencing any level link to the corresponding page

### Schema
- `HowTo` (Levels 1–8) + `Article` (Levels 9–11) + `BreadcrumbList` on all
- See `strategy/schema-markup.md` for full JSON-LD

---

## Playbook 2: Glossary

### Opportunity
Centaurion uses specialized vocabulary that exists in academic literature but lacks accessible, practitioner-focused definitions. Publishing definitions creates low-competition, AI-citable content for searches that will grow as the category matures.

### Keyword Pattern
`what is [term]` / `[term] definition` / `[term] AI` / `[term] explained`

### Page Count: 20–40 terms (start with 15 seed terms)

### URL Structure
```
/glossary/                             (hub)
/glossary/free-energy-principle/
/glossary/markov-blanket/
/glossary/active-inference/
/glossary/prediction-error/
/glossary/exo-cortex/
/glossary/fitness-landscape/
/glossary/closed-loop-system/
/glossary/open-loop-system/
/glossary/uncertainty-routing/
/glossary/coupling-layer/
/glossary/agentic-engineering/
/glossary/generative-model/
/glossary/active-inference-loop/
/glossary/thermodynamic-cost/
/glossary/minimum-sufficient-model/
```

### Title Template
`What is [Term]? Definition & Application | Centaurion Glossary`

### Meta Description Template
`[Term] is [one-sentence definition]. Learn how [term] applies to human-AI systems and organizational design. Centaurion Glossary.`

### Page Template (per term)

```
H1: What is [Term]?

[DEFINITION BLOCK — 40-60 words, standalone]
[Term] is [precise definition]. [One sentence on origin/context]. [One sentence on relevance to AI systems].

## Origin and Academic Context

[100-150 words: where the concept comes from, who coined it, academic grounding]
[Cite primary source — Friston, Kahneman, etc. as applicable]

## In the Centaurion Framework

[100-150 words: how Centaurion applies this concept specifically]
[Connect to Three Laws, Fitness Equation, or Sensing Layers where relevant]

## Practical Example

[80-120 words: concrete, non-academic example]
[Use organizational or AI system context, not just abstract theory]

## Related Terms

- [Related Term 1] → /glossary/[slug]
- [Related Term 2] → /glossary/[slug]
- [Related Term 3] → /glossary/[slug]

## FAQ

**[Natural language question 1]?**
[40-60 word answer]

**[Natural language question 2]?**
[40-60 word answer]

## Further Reading

- [The Centaurion Method](/methodology) — how [term] applies in practice
- [Related blog post] — [post title]
```

### Schema: `DefinedTerm` + `FAQPage` + `BreadcrumbList`

---

## Playbook 3: Personas ("AI Transformation for [Segment]")

### Opportunity
Different buyer segments have different entry points into the Centaurion methodology. A page for "AI transformation for wellness organizations" serves AOB-like clients; "AI transformation for technical founders" serves a different ICP. Each page addresses the same service from the lens of a specific audience.

### Keyword Pattern
`AI transformation for [segment]` / `fractional CAO for [segment]` / `AI strategy for [segment]`

### Page Count: 8–12 (start with 5)

### URL Structure
```
/work-with-us/ai-transformation/         (hub)
/work-with-us/ai-transformation/wellness-organizations/
/work-with-us/ai-transformation/professional-services/
/work-with-us/ai-transformation/technical-teams/
/work-with-us/ai-transformation/solopreneurs/
/work-with-us/ai-transformation/mid-market-companies/
```

### Title Template
`AI Transformation for [Segment] | Centaurion`

### Page Template (per segment)

```
H1: AI Transformation for [Segment]

[SEGMENT-SPECIFIC HOOK — 60-80 words]
[Why this segment faces a specific version of the human-AI augmentation problem]

## The [Segment] AI Challenge

[150-200 words: specific pain the segment faces with AI adoption]
[Use segment-specific vocabulary — "wellness practitioners" use different language than "engineering teams"]

## How the Centaurion Method Applies

[150-200 words: which of the Three Laws / Sensing Layers is most relevant for this segment]

## What This Engagement Looks Like for [Segment]

[Timeline, deliverables, expected outcomes — segment-specific framing]

## Case Study

[AOB for wellness, or generic framing for segments without a case study yet]

## Frequently Asked Questions

[3-4 FAQs segment-specific]

[CTA: Work With Us →]
```

### Schema: `Service` + `FAQPage` + `BreadcrumbList`

---

## Playbook 4: Comparisons

### Opportunity
Buyers evaluating Centaurion will compare it to generic AI consulting, large firms (Deloitte AI practice), and DIY approaches. Owning these comparison pages controls the narrative at the decision stage.

### Keyword Pattern
`[approach] vs [approach]` / `Centaurion vs [alternative]` / `[alternative] alternative`

### Page Count: 5–8

### URL Structure
```
/compare/                                          (hub)
/compare/centaurion-vs-traditional-ai-consulting/
/compare/centaurion-vs-diy-ai-implementation/
/compare/fractional-cao-vs-full-time-cao/
/compare/centaurion-vs-ai-platform-vendor/
/compare/open-loop-vs-closed-loop-ai/             (conceptual, not brand-vs-brand)
```

### Comparison Page Template

```
H1: [Option A] vs [Option B]: [Outcome comparison headline]

[SUMMARY TABLE]
| Factor | [Option A] | [Option B] |
|---|---|---|
| Scientific grounding | [rating/description] | [rating/description] |
| Human primacy | [rating/description] | [rating/description] |
| Closed-loop architecture | [rating/description] | [rating/description] |
| Cost | [rating/description] | [rating/description] |
| Best for | [description] | [description] |

## Key Differences

[200-300 words: honest, specific comparison. Not a takedown — a genuine analysis]

## When to Choose [Option A]

[100 words: specific situations where Option A wins]

## When to Choose [Option B]

[100 words: specific situations where Option B wins — credibility requires this]

## FAQ

[3-4 comparison-specific FAQs]

[CTA: See how Centaurion works →]
```

### Schema: `FAQPage` + `Article` + `BreadcrumbList`

---

## Launch Sequence

### Phase 1 — Foundation (April–May 2026)
1. Publish glossary hub + 15 seed terms
2. Publish agentic engineering hub + all 11 level pages
3. Submit both sections to Google Search Console

### Phase 2 — Personas (May–June 2026)
4. Publish 5 persona pages
5. Internal link from Work With Us hub to all persona pages

### Phase 3 — Comparisons (June–July 2026)
6. Publish 5 comparison pages
7. Link from relevant blog posts and methodology pages

---

## Quality Gate

Before any programmatic page goes live:
- [ ] Minimum 400 words of unique content (not template boilerplate)
- [ ] Definition block is 40-60 words, self-contained
- [ ] At least 3 internal links (to hub, related pages, and a blog post)
- [ ] Schema validated in Rich Results Test
- [ ] Title is unique across the site
- [ ] Page answers the target query directly in the first paragraph

---

## Crawl Budget Management

At 11 + 30 + 12 + 8 = ~60 pages, crawl budget is not a concern at launch. Maintain a single XML sitemap at `/sitemap.xml` with all programmatic pages included. Reassess when total site reaches 500+ pages.
