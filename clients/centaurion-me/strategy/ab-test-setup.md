# A/B Test Strategy — Centaurion.me

**Client:** Centaurion.me (Malik Palamar)
**Phase:** Foundation (Q1–Q2 2026)
**Constraint:** Low-traffic site in Phase 1 — qualitative and behavioral methods must supplement or replace traditional split testing until organic and referral volume scales.

---

## The Testing Problem (And How to Solve It)

Standard A/B testing requires statistical significance. For a site converting at 2–5% with fewer than 500 monthly visitors, a typical A/B test would take 6–12 months to reach 95% confidence. That's not a testing strategy — that's stasis.

Centaurion operates differently. The site is not a conversion machine selling a $49 SaaS product. It is a credibility asset for a high-value advisory practice. A single discovery call conversion is worth more than 1,000 anonymous bounces.

The framework: **run behavioral and qualitative tests in Phase 1** to build directional conviction, then run statistical A/B tests in Phase 2 when traffic volume permits.

---

## Phase 1: Low-Traffic Testing Methods

### 1. Five-Second Tests

**What:** Show a design or copy variant to a panel for exactly 5 seconds, then ask what they remember and what the site does.
**Tool:** Usabilityhub (now Lyssna) — free tier for basic tests; $75/mo for respondent panel access
**Best for:** Homepage hero copy, value proposition clarity, CTA button text

**Test format:**
1. Upload a screenshot of the hero section
2. Ask: "What does this company do?" and "What would you do next?"
3. Recruit 10–20 participants from: LinkedIn connections, past colleagues, Centaurion ICP lookalikes
4. Success signal: Participants can accurately describe "human-AI augmentation advisory" and name a clear next action

**Run this before writing any live homepage copy.** Malik can circulate screenshots of 2–3 hero variants to a small network without any live changes.

### 2. Heatmapping and Session Recording

**Tool:** Microsoft Clarity (free, no session limit) or Hotjar free tier
**What to track:**
- Scroll depth on homepage: Does anyone reach the methodology sections?
- Click map: Are people clicking the CTA or reading the nav?
- Session recordings: Where do people land, what do they read, where do they exit?
- Rage clicks: Any UX friction points triggering frustrated clicking?

**Setup:** Add Clarity/Hotjar script to site. Let it run for 2–4 weeks before drawing conclusions. With low traffic, you may need 4–8 weeks for enough sessions.

**What counts as insight:**
- If 70%+ of visitors exit before the CTA: above-the-fold copy is not earning attention
- If visitors scroll past the methodology but don't click: engagement without conversion = trust gap, not interest gap
- If visitors click on non-clickable elements: navigation or information architecture issue

### 3. Moderated Prototype Testing

**What:** Walk 3–5 target prospects through the homepage via a Loom share or live Zoom session. Ask them to narrate their thinking.
**Who to recruit:** LinkedIn connections who match ICP profiles — COOs at sub-$50M companies, technical VPs, fractional executives in adjacent practices

**Script (15 minutes):**
1. "I'm going to share a website with you. Please think out loud as you look at it."
2. Screen share, do not narrate or explain
3. After 2 minutes: "What does this person/firm do? Would you reach out? Why or why not?"
4. Probe: "What's missing? What would make you more confident?"
5. Probe: "What does 'Centaurion Method' mean to you after reading this?"

**Cadence:** Run once per homepage iteration cycle (every 6–8 weeks in Phase 1)

### 4. Email Variant Testing

Send different subject lines and CTAs to newsletter list segments. Even with a 200-person list, directional data from open rates and click rates is faster and cheaper than homepage A/B testing.

**Method:**
- Split list randomly into A/B groups
- Change one variable per send
- Measure open rate (subject line test) or click rate (CTA test)
- Sample size needed for directional signal at this scale: 100+ recipients per variant

---

## Homepage Hero Tests

### Current Hypothesis

The homepage hero must resolve two competing priorities:
1. **Urgency:** The Thousand-Day Window framing (loss aversion, right now matters)
2. **Credibility:** The Centaurion Method (system, not buzzwords — earns trust from skeptical technical leaders)

Both are true. The question is which leads, and which follows.

---

### Test A: CTA Copy — "Work With Us" vs "Book a Discovery Call"

**Hypothesis:** "Book a Discovery Call" is explicit, lowers cognitive load, and sets expectations. "Work With Us" is softer but may feel less transactional — better for premium positioning.

**Null hypothesis:** No statistically significant difference in click-through rate.

**Variant A (Control):**
```
[Hero copy]
[CTA button] → Book a Discovery Call
```

**Variant B:**
```
[Hero copy]
[CTA button] → Work With Us
```

**Variant C:**
```
[Hero copy]
[CTA button] → Start With a Pilot Audit
```

**Measurement:** Click-through rate on hero CTA button (GA4 event: `hero_cta_click`, parameter: `cta_variant`)

**Phase 1 approach:** Run a 5-second test showing each variant to 10 people. Ask: "What would you click first and why?" Implement winner based on qualitative signal. Revisit with statistical test when monthly sessions exceed 1,000.

**Expected winner hypothesis:** "Book a Discovery Call" outperforms because Malik's audience is analytical and prefers explicit framing over soft sell. "Start With a Pilot Audit" may outperform for visitors who arrive already understanding what they need.

---

### Test B: Hero Framing — Thousand-Day Window Urgency vs. Methodology Credibility

**Hypothesis:** Two different visitor mindsets arrive at centaurion.me:
- **"Why now?" visitor:** Has heard AI hype but hasn't committed. Needs urgency framing to move.
- **"Who is this?" visitor:** Is already running AI initiatives but looking for a rigorous partner. Needs credibility framing, not urgency.

The site currently cannot serve both simultaneously in the hero. This test determines which mindset dominates the current traffic mix.

**Variant A — Urgency/Loss Aversion (Thousand-Day Window):**
```
Headline: The Organizations That Get This Right in the Next 1,000 Days Will Have a Decade-Long Advantage

Subhead: Most AI implementations fail not because the technology is wrong but because the organization treats a closed-loop system like a simple tool. Centaurion.me exists to fix that.

CTA: Book a Discovery Call
```

**Variant B — Methodology Credibility:**
```
Headline: Human-AI Augmentation Is an Engineering Problem. Most Organizations Are Treating It Like a Software Purchase.

Subhead: The Centaurion Method is a structured framework for building organizations where humans and AI systems compound each other's capabilities. Three Laws. A Fitness Equation. Five Sensing Layers.

CTA: Book a Discovery Call
```

**Variant C — Founder Authority:**
```
Headline: Malik Palamar Helps Mid-Market Organizations Build AI Systems That Actually Learn

Subhead: Fractional CAO and Chief Agentic Officer. The Centaurion Method. 11 Levels of Agentic Engineering. If your AI systems aren't getting smarter over time, they're getting more expensive.

CTA: Book a Discovery Call
```

**Measurement:** Time on page, methodology section scroll depth, discovery call booking rate per variant

**Phase 1 approach:** Write all three in a Google Doc. Share with 5 ICP-matched contacts (not clients — adjacent network). Ask which version describes what they need. This is a message-market fit test before a traffic test.

**Expected winner hypothesis:** Variant B outperforms for Segment A (technical leaders). Variant A outperforms for Segment B (business leaders who are panicking about AI readiness). Variant C is the fallback if neither works — personal brand authority converts when the methodology framing is unclear.

---

### Test C: Assessment Tool CTA Placement

**Hypothesis:** The Agentic Engineering Assessment is the highest-intent engagement signal on the site. Visitors who complete it are significantly more likely to book a call. The question is where on the page to introduce it.

**Variant A — Hero placement:**
```
[Hero headline]
[Hero subhead]
[Primary CTA: Book a Discovery Call]
[Secondary CTA: Take the 5-Minute Assessment →]
```

**Variant B — Mid-page placement (after methodology explanation):**
```
[Hero]
[Methodology explanation: Three Laws, Fitness Equation, etc.]
[Section: "Where does your organization stand?"]
[CTA: Take the Agentic Engineering Assessment →]
[Then: Work With Us section with discovery call CTA]
```

**Variant C — Exit-intent only:**
```
[Normal page flow]
[On exit intent or after 90 seconds: pop-up or sticky bar]
"Before you go: find out where your organization sits on the 11 Levels."
[CTA: Take the Free Assessment →]
```

**Measurement:**
- Primary: `assessment_started` event rate
- Secondary: `assessment_completed` → `email_signup` rate
- Tertiary: `discovery_call_booked` rate for assessment-completing cohort vs non-completing cohort

**Expected winner hypothesis:** Variant B will produce higher assessment completion rates because visitors who encounter the assessment after reading methodology context are more motivated to self-diagnose. Variant A dilutes the primary CTA. Variant C is useful as a secondary mechanism but should not be the primary placement.

---

## Phase 2 Tests (Once Monthly Sessions Exceed 1,000–2,000)

### Statistical Testing Infrastructure

**Tool recommendation:** VWO (Visual Website Optimizer) at $199/mo, or Google Optimize replacement via server-side testing with GA4 experiment parameters. Alternatively, use a feature flag service like PostHog (open source, self-hostable on Hostinger VPS) to serve variants and track conversion events in GA4.

### Planned Phase 2 Tests

#### P2-T1: Pricing Page Framing
- Variant A: Lead with Pilot Audit ($8.5K–$12.5K) as the entry point
- Variant B: Lead with Fractional CAO retainer ($5K–$8K/mo) as the anchor, position Pilot as the first step
- Hypothesis: Retainer-first anchoring increases pilot bookings by making the pilot feel like a low-risk commitment

#### P2-T2: Social Proof Format
- Variant A: Named quotes from transformation clients (requires client testimonials to be gathered)
- Variant B: Quantified outcomes ("43% reduction in manual workflow hours in 90 days")
- Variant C: Case study format with before/after methodology diagnosis
- Hypothesis: Quantified outcomes outperform quotes for Centaurion's analytical ICP

#### P2-T3: Assessment Gate vs Ungate
- Variant A: Assessment requires email before results
- Variant B: Assessment shows results immediately, then offers email for full breakdown PDF
- Hypothesis: Ungate → instant results will increase assessment completion 30–50%, and the email capture rate will be sufficient to justify the frictionless approach

#### P2-T4: Methodology Page Layout
- Variant A: Three Laws → Fitness Equation → Five Sensing Layers (logical sequence)
- Variant B: Five Sensing Layers → Fitness Equation → Three Laws (bottom-up, practical first)
- Hypothesis: For technical leaders (Segment A), bottom-up (practical first) generates more time on page

#### P2-T5: Newsletter Opt-in Positioning
- Variant A: Newsletter CTA in homepage footer only
- Variant B: Newsletter CTA mid-page with explicit preview of content ("The Prediction Error Brief: weekly signal, not noise")
- Hypothesis: Mid-page with content preview increases signup rate 2x

---

## Test Log Template

Track all tests, even informal ones, in a shared doc:

```
Test ID: [P1-T1]
Date started: [YYYY-MM-DD]
Test type: 5-second test / heatmap / email split / statistical A/B
Hypothesis: [What we believe and why]
Variants: [A, B, C descriptions]
Measurement method: [How we're collecting signal]
Sample size: [N participants or N sessions]
Result: [Winner or inconclusive]
Action taken: [What was implemented]
Learnings: [What this tells us about the ICP's mental model]
```

---

## Testing Principles for Centaurion

1. **Test mental models, not just buttons.** The most valuable Phase 1 insight is understanding how ICP visitors interpret "Centaurion Method" and "human-AI augmentation" — not whether blue or green CTAs convert better.

2. **One variable per test.** Do not change headline and CTA simultaneously. You will not know which change drove the result.

3. **Statistical significance is a Phase 2 luxury.** In Phase 1, directional confidence from 10 qualitative participants is more valuable than 6 months of inconclusive split test data.

4. **The assessment is the leading conversion indicator.** Every test should eventually measure impact on assessment completion, not just CTA clicks. Assessment completers are a different quality of lead than anonymous email signups.

5. **Failing is data.** If Variant B loses, that is not a failure of the test — it is evidence about what the ICP does not respond to. Document it and move forward.
