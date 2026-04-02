# SEO Audit — Centaurion.me
*April 2026 · Skill: seo-audit · Author: Malik Palamar*

---

## Executive Summary

Centaurion.me is an early-stage advisory and methodology site (Phase 1). The primary SEO challenge is not technical — it is **establishing topical authority in a space that barely exists as a search category yet**. No one searches "Free Energy Principle AI consulting." The opportunity is to own the vocabulary *before* the category matures, making Centaurion the reference point competitors cite.

**Overall health**: Not yet auditable live (container egress restrictions apply). Assessment based on known stack and strategic context.

**Top 5 priorities:**

| # | Priority | Type |
|---|---|---|
| 1 | Define and lock keyword architecture before publishing at scale | Strategy |
| 2 | Implement schema for Person + Organization + FAQPage from day one | Technical |
| 3 | Create a `/methodology` hub page as SEO cornerstone | Content |
| 4 | Submit sitemap to GSC immediately — clock starts on crawl budget | Technical |
| 5 | Publish 11 Levels as long-form page (GitHub repo ≠ indexed content) | Content |

---

## Site Context

| Field | Value |
|---|---|
| **Site type** | Advisory / thought leadership / methodology |
| **CMS** | Unknown — likely custom or Ghost/Webflow given VPS self-hosting |
| **Hosting** | Hostinger VPS |
| **Primary goal** | Establish topical authority, generate inbound advisory leads |
| **Stage** | Phase 1 (Foundation) — site may be minimal or pre-launch |
| **GSC access** | Not confirmed |
| **Organic traffic baseline** | Not confirmed |

---

## Technical SEO Findings

### TECH-01 · Robots.txt and Sitemap
**Impact**: High
**Issue**: Unknown state — not confirmed that robots.txt and XML sitemap exist or are submitted to GSC.
**Fix**:
1. Create `robots.txt` at root — allow all by default, disallow `/wp-admin/` or equivalent
2. Generate XML sitemap and reference it in robots.txt: `Sitemap: https://centaurion.me/sitemap.xml`
3. Submit sitemap in Google Search Console immediately

---

### TECH-02 · HTTPS and Canonical Consistency
**Impact**: High
**Issue**: Self-hosted VPS — SSL and canonical consistency must be verified manually.
**Fix**:
1. Confirm HTTPS enforced site-wide with valid certificate
2. Choose canonical form: `https://centaurion.me` (no www) and enforce via 301 redirect
3. Set `rel=canonical` on all pages pointing to the canonical URL
4. Verify no mixed content (HTTP assets on HTTPS pages)

---

### TECH-03 · Core Web Vitals Baseline
**Impact**: Medium
**Issue**: Self-hosted VPS with no confirmed CDN. Without a CDN, LCP and TTFB will likely be suboptimal, especially for international visitors.
**Fix**:
1. Run PageSpeed Insights on homepage and `/methodology` (once live)
2. Target: LCP < 2.5s, CLS < 0.1, INP < 200ms
3. Add Cloudflare (free tier) as CDN layer — keeps VPS benefits, adds edge caching
4. Compress and serve images in WebP

---

### TECH-04 · URL Structure
**Impact**: Medium
**Issue**: No confirmed URL schema exists. Advisory sites often default to flat structure which limits topical clustering.
**Recommendation** (define before publishing):

```
centaurion.me/                          # Homepage
centaurion.me/methodology/              # Cornerstone — The Centaurion Method
centaurion.me/methodology/three-laws/   # Three Laws deep-dive
centaurion.me/methodology/sensing-layers/
centaurion.me/agentic-engineering/      # 11 Levels hub
centaurion.me/agentic-engineering/level-[1-11]/
centaurion.me/blog/                     # Content hub
centaurion.me/case-studies/             # Proof points
centaurion.me/about/
centaurion.me/work-with-us/             # Engagement CTA
```

---

### TECH-05 · Mobile and Viewport
**Impact**: Medium
**Issue**: Unknown. VPS-hosted custom site may miss viewport meta tag or have desktop-only layout.
**Fix**: Confirm `<meta name="viewport" content="width=device-width, initial-scale=1">` on all pages. Test with Google's Mobile-Friendly Test.

---

## On-Page SEO Findings

### ONPAGE-01 · Missing Cornerstone Page
**Impact**: High
**Issue**: The methodology (Three Laws, Fitness Equation, Five Sensing Layers) is Centaurion's primary differentiator — but it appears to exist only as a document, not as an indexed web page. GitHub repos are not reliably indexed or ranked for informational queries.
**Fix**: Publish `/methodology/` as a long-form, schema-marked cornerstone page. This becomes the internal linking hub for all sub-pages.

---

### ONPAGE-02 · 11 Levels Not in Indexable Form
**Impact**: High
**Issue**: The 11 Levels of Agentic Engineering are published on GitHub (`MalikJPalamar/centaurion-agentic-engineering-lvl`) but GitHub repo pages rank poorly vs. native web pages for informational queries. The IP is not capturing search traffic.
**Fix**: Publish each level as a standalone page at `centaurion.me/agentic-engineering/level-[N]-[slug]/`. This is the programmatic SEO play (see `strategy/programmatic-seo.md`).

---

### ONPAGE-03 · Title Tag and Meta Description Architecture
**Impact**: Medium
**Issue**: Not confirmed. Advisory sites frequently publish with CMS-default title formats.
**Fix**: Define templates before publishing:
- Homepage: `Centaurion | Human-AI Augmentation Advisory`
- Methodology hub: `The Centaurion Method: Human-AI Fitness Framework`
- Blog posts: `[Post Title] | Centaurion`
- Each meta description must include primary keyword + one compelling differentiator sentence

---

### ONPAGE-04 · Keyword Cannibalization Risk
**Impact**: Medium
**Issue**: Multiple pages will cover overlapping concepts (Free Energy Principle, active inference, prediction error) across the methodology, blog, and case study sections.
**Fix**: Create a keyword map (see `strategy/content-strategy.md`) assigning each keyword to exactly one canonical page. Other pages reference it but do not target it as primary.

---

### ONPAGE-05 · Author E-E-A-T Signals
**Impact**: Medium
**Issue**: Centaurion's authority is tied to Malik Palamar as a credentialed practitioner. Most advisory sites bury or omit this entirely.
**Fix**:
1. Create `/about/malik-palamar/` with full bio, credentials, and links to published work
2. Add `Person` schema (see `strategy/schema-markup.md`)
3. Link GitHub (`MalikJPalamar/centaurion-agentic-engineering-lvl`) from author page
4. Add byline + author schema to every blog post

---

## Content Quality Assessment

### E-E-A-T Status

| Signal | Status | Action |
|---|---|---|
| **Experience** | Strong in private assets (AOB pilot, dashboards, scorecards) | Publish case studies |
| **Expertise** | High — 11 Levels published, theoretical framework documented | Needs web-indexed version |
| **Authoritativeness** | Early-stage — no inbound links or citations yet | Target niche publications for guest posts |
| **Trustworthiness** | Unknown — contact info, privacy policy not confirmed live | Confirm these exist |

---

### Content Gaps

| Gap | Priority | Notes |
|---|---|---|
| Methodology hub page | P0 | Core differentiator, not yet indexed |
| 11 Levels long-form web page | P0 | Currently only on GitHub |
| AOB case study (public version) | P1 | Most powerful proof point |
| Glossary (Free Energy Principle, Markov Blanket, etc.) | P1 | Owned vocabulary = search moat |
| Comparison: Centaurion vs. traditional AI consulting | P2 | High-intent, commercial audience |

---

## Prioritized Action Plan

### Phase 1 — Foundations (Do Before Publishing at Scale)

- [ ] Confirm HTTPS, canonical form, robots.txt, sitemap
- [ ] Define URL structure (above)
- [ ] Create keyword map (one page per keyword cluster)
- [ ] Submit sitemap to Google Search Console
- [ ] Add `Organization` and `Person` schema to homepage and about page

### Phase 2 — Cornerstone Content (First 60 Days)

- [ ] Publish `/methodology/` hub page
- [ ] Publish `/agentic-engineering/` with 11 individual level pages
- [ ] Publish AOB case study (sanitized for public)
- [ ] Add `Article` schema to all blog posts

### Phase 3 — Authority Building (60–180 Days)

- [ ] Launch `/glossary/` with 15–30 definitions
- [ ] Guest post on 2–3 AI/systems publications with backlinks to methodology
- [ ] Publish `/case-studies/` section
- [ ] Build comparison pages for commercial-intent queries

---

## Tools to Set Up

| Tool | Priority | Purpose |
|---|---|---|
| Google Search Console | P0 | Crawl monitoring, index coverage, CTR |
| PageSpeed Insights | P0 | Core Web Vitals baseline |
| Google Rich Results Test | P0 | Schema validation |
| Ahrefs / SEMrush | P1 | Keyword research, backlink tracking |
| Screaming Frog | P1 | Full technical crawl once site is live |

---

*Next audit: run Screaming Frog crawl once site has 20+ published pages. Revisit GSC coverage report at 90 days post-launch.*
