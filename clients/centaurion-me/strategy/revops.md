# Revenue Operations (RevOps) — Centaurion.me

**Client:** Centaurion.me (Malik Palamar)
**Phase:** Foundation (Q1–Q2 2026)
**Context:** Malik is a solo operator handling marketing, sales, and delivery simultaneously. RevOps here does not mean a dedicated ops team — it means structured processes so that nothing falls through the cracks and Malik can run his pipeline without constant context-switching.

---

## Lead Lifecycle Model

Every contact at Centaurion passes through a defined set of stages. The goal is not to automate the human out of the relationship — it is to ensure Malik always knows exactly where each contact stands and what the next action is.

```
Stage 1: Awareness
    ↓  [discovers content, visits site, sees LinkedIn post]
Stage 2: Engaged
    ↓  [subscribes to newsletter, downloads lead magnet, follows on LinkedIn]
Stage 3: Assessment Taker
    ↓  [starts and/or completes Agentic Engineering Assessment]
Stage 4: Marketing Qualified Lead (MQL)
    ↓  [email subscriber who has engaged with 2+ content pieces OR completed assessment]
Stage 5: Sales Qualified Lead (SQL)
    ↓  [booked discovery call OR responded to cold outreach with interest]
Stage 6: Discovery Call Held
    ↓  [call completed, basic qualification confirmed]
Stage 7: Proposal Sent
    ↓  [Pilot Audit or Fractional CAO proposal delivered]
Stage 8: Closed Won — Pilot Audit
    ↓  [Pilot Audit contract signed, payment received]
Stage 9: Closed Won — Retainer
    ↓  [Fractional CAO retainer contract signed]
Stage 10: Active Client
    ↓  [engagement in progress]
Stage 11: Alumni / Referral Source
    ↓  [engagement completed, relationship maintained]

Parallel dead-end stages (do not delete these contacts — archive):
- Closed Lost: No fit, no budget, competitor chosen
- Nurture: Long-cycle prospect — not ready now, re-engage in 60–90 days
- Unresponsive: 3+ touches with no response — pause outreach, maintain on newsletter
```

---

## CRM Evaluation

Malik does not have a confirmed CRM. This section evaluates three realistic options for a solo operator in Phase 1, with a recommendation.

### Option A: HubSpot Free CRM

**Strengths:**
- Genuinely free for core contact/deal management
- Email integration (Gmail/Outlook)
- Meeting scheduling link (replaces Calendly for basic use)
- Deal pipeline with drag-and-drop stages
- Basic email sequences in the free tier
- Large knowledge base, strong integrations with GA4, LinkedIn, Stripe

**Weaknesses:**
- HubSpot Free nudges aggressively toward paid tiers ($45–$800/mo)
- Reporting is limited on free tier
- Form embed and landing page tools are paid features
- Can feel bloated for a one-person operation

**Verdict:** Best choice if Malik anticipates hiring a sales or operations person in 12–18 months, or if he wants to grow into marketing automation later. The free tier is genuinely capable for 0–25 active deals.

### Option B: Notion CRM

**Strengths:**
- Already in many operators' workflows
- Infinitely customizable pipeline views
- Excellent for notes and documentation alongside deal tracking
- No additional cost if Notion is already in use
- Can embed in existing Notion workspace alongside delivery materials, proposals, and content planning

**Weaknesses:**
- No native email integration or send-from-CRM capability
- No automated follow-up sequences
- Manual data entry only — no contact enrichment
- Not designed as a CRM — will hit limits on filtering, reporting, and automation

**Verdict:** Best choice if Malik prioritizes documentation quality over automation and is managing fewer than 20 active leads simultaneously. Not recommended if outbound sequences are a core activity.

### Option C: Pipedrive

**Strengths:**
- Designed specifically for individual sellers and small teams
- Visual pipeline is intuitive and fast
- Email sync and tracking built in
- Activity reminders and follow-up prompts are excellent for one-person operations
- Solid reporting on deal velocity, win rates, and pipeline value
- Affordable: $14–$24/mo at basic tiers

**Weaknesses:**
- Paid from Day 1 (14-day trial)
- Marketing automation is a paid add-on
- Less extensible than HubSpot for future team growth

**Verdict:** Best choice if Malik wants a purpose-built sales tool at low cost and doesn't need marketing automation to be part of the same system.

### Recommendation

**Use HubSpot Free in Phase 1.** The free tier covers the full lead lifecycle without cost, and it integrates with the tools Centaurion already uses or will use (Gmail, Calendly, Stripe, GA4). If HubSpot's upsell pressure becomes friction, migrate to Pipedrive at $14/mo — the data export is clean.

Do not use Notion as the primary CRM. Use it for delivery documentation, content planning, and proposal drafting — but track the pipeline in a purpose-built tool.

---

## Lead Scoring Model

Lead scoring tells Malik where to focus his limited sales time. Centaurion's scoring model is behavioral (what the contact has done) and demographic (who they are).

### Behavioral Score (Actions on centaurion.me and via email)

| Action | Points |
|---|---|
| Completed Agentic Engineering Assessment | +25 |
| Visited /work-with-us or pricing page | +20 |
| Downloaded "Thousand-Day Window" brief | +15 |
| Downloaded "Closed-Loop AI Checklist" | +10 |
| Read 3+ methodology pages | +15 |
| Engaged with 3+ newsletter issues (opens + clicks) | +10 |
| Clicked discovery call link (but didn't book) | +20 |
| Responded to a cold email | +30 |
| Followed on LinkedIn + engaged with a post | +5 |
| Email subscriber (no other engagement) | +5 |

### Demographic Score (Who they are)

| Characteristic | Points |
|---|---|
| Title: CEO, COO, President | +20 |
| Title: CTO, VP Engineering, Head of AI | +15 |
| Title: Director level | +10 |
| Company size: 50–250 employees | +20 |
| Company size: 251–500 employees | +15 |
| Company size: > 500 or < 50 employees | +0 |
| Industry: Technology, Professional Services, SaaS | +15 |
| Industry: Healthcare, Financial Services, Manufacturing | +10 |
| Geography: US (Malik's primary market) | +10 |
| Geography: International | +5 |

### Score Thresholds

| Total Score | Stage |
|---|---|
| 0–20 | Awareness |
| 21–40 | Engaged |
| 41–60 | MQL — add to email nurture |
| 61–80 | SQL — personal outreach warranted |
| 81+ | Hot lead — immediate personal contact |

### Phase 1 Scoring Method

HubSpot Free does not have automatic lead scoring. In Phase 1, run lead scoring manually:
1. Export email subscriber list weekly
2. Cross-reference GA4 conversion events (assessment completions, pricing page views)
3. Manually update HubSpot contact scores
4. Review top-10 highest-scored contacts every Monday morning

In Phase 2, implement HubSpot's predictive lead scoring (paid tier) or use a Zapier workflow to update scores automatically based on GA4 events.

---

## Handoff Criteria: Marketing to Sales

Malik handles both functions, but establishing clear handoff criteria prevents two failure modes:
1. Chasing too early (contacting someone who isn't ready — damages the relationship)
2. Contacting too late (warm lead goes cold while waiting for "the right moment")

### Marketing → Sales Handoff Triggers (Any one of these warrants personal outreach)

**Tier 1 — Immediate outreach (within 24 hours):**
- Contact books a discovery call via Calendly
- Contact completes the assessment AND submits email AND is SQL by demographic score
- Contact responds to a cold email with interest or a question
- Contact sends LinkedIn DM about working together

**Tier 2 — Outreach within 48 hours:**
- Lead score crosses 80 (hot threshold)
- Contact visits /work-with-us page after completing the assessment
- Contact opens the same email 3+ times (strong intent signal if visible in HubSpot)
- Contact clicks "Book a Call" link in any email but doesn't complete booking

**Tier 3 — Include in next outreach batch (within 5 business days):**
- Lead score crosses 60 (SQL threshold)
- Contact downloads second lead magnet (demonstrates continued intent)
- Contact responds to newsletter with a question or comment

### What "Personal Outreach" Looks Like

For Centaurion, personal outreach is always Malik. It is a brief, direct message — not a templated sequence:

```
Hi [Name],

I noticed you [completed the assessment / downloaded the Thousand-Day Window / visited the pilot audit page]. That usually means [specific problem they're likely experiencing].

If you want to talk through what you found, I have time this week for a 30-minute call. No prep required.

[Calendar link]

— Malik
```

The template is the frame, not the message. Malik should customize the middle sentence based on what he knows about the contact.

---

## Discovery Call Process

### Pre-Call Preparation (10 minutes)

Before every discovery call, Malik should review:
1. Lead source: How did this person find Centaurion?
2. Lead score: What engagement signals have they shown?
3. Assessment results (if completed): What did they score, where are the gaps?
4. LinkedIn profile: Company size, tenure, recent posts, mutual connections
5. Company context: What do they do, how large are they, any recent news?

Prepare one personalized observation: "I saw you posted about [X] last week — that connects directly to what I want to ask you about."

### Discovery Call Structure (30–45 minutes)

**Minutes 0–5: Context setting**
"Thanks for making time. Before I tell you anything about Centaurion, I want to understand your situation. I'll ask you a few questions, and if it turns out we're a fit, I'll explain exactly how we'd work together. If we're not a fit, I'll tell you that too."

**Minutes 5–20: Diagnostic questions**
1. "What's driving your interest in this area right now? What changed?"
2. "Tell me about the AI initiatives you have in place or are planning. What's working? What isn't?"
3. "When you think about the gap between where you are and where you need to be on AI capability — how would you describe it?"
4. "Who else is involved in making a decision like this? Is it just you, or is there a team?"
5. "What does success look like in 12 months? How do you know if you've gotten this right?"
6. "What have you already tried? What didn't work and why?"

**Minutes 20–30: Centaurion positioning (only if they're a fit)**
"Based on what you've described, here's how I'd think about your situation through the Centaurion lens..."
- Name the specific gap in their 11 Levels assessment (if available) or frame their problem using the relevant Centaurion framework
- Describe the Pilot Audit as the natural starting point
- Be explicit: "I typically work with organizations that [fit criteria]. Based on what you've described, [you do / you might / you're not quite there yet]."

**Minutes 30–40: Next steps and close**
"If this sounds like a fit, the next step is the 30-Day Pilot Audit. It costs $[price], it takes 30 days, and at the end you have a complete diagnosis and a prioritized roadmap. Would you like me to send you the scope document?"

If not ready: "What would need to be true for this to be a priority in the next 60 days?"

**Close with clear next action:**
- "I'll send the scope document today — expect it by [time]."
- "Let's schedule a follow-up call for [date] once you've had a chance to review."
- "If it makes sense, I'll have a contract ready to sign by [date]."

### Post-Call Notes Template

Log in CRM immediately after the call:

```
Contact: [Name], [Title], [Company]
Date: [Date]
Call duration: [X] minutes
Lead source: [How they found Centaurion]
Assessment score: [Score if completed, or N/A]

Situation summary:
[2–3 sentences on their current AI state]

Pain points identified:
- [Pain 1]
- [Pain 2]
- [Pain 3]

Fit assessment:
[ ] Strong fit — proceed to proposal
[ ] Conditional fit — [condition]
[ ] Not a fit — [reason]

Decision-makers involved:
[Names and titles]

Next action:
[What Malik committed to do and by when]

Follow-up date:
[Date for next contact]
```

---

## Proposal → Contract Flow

### Proposal Timing

Send proposals within 24–48 hours of a qualifying discovery call. Proposals sent later than 72 hours lose momentum. If the proposal cannot be ready in 48 hours, send a brief "preview" email:

```
[Name],

Enjoyed our call today. I'll have the full Pilot Audit scope document to you by [date].

In the meantime — based on what you described about [specific problem], the area I'd focus the audit on is [sensing layer / agentic level / specific gap]. That tells me the pilot will be directionally useful regardless of what we find in the broader diagnostic.

More soon.

— Malik
```

### Proposal Components

1. **Executive summary (1 paragraph):** What we heard, what we're proposing, what success looks like
2. **Scope of work:** Phase 1 (Pilot Audit, 30 days), deliverables, access requirements
3. **Investment:** Price, payment terms, optional retainer transition language
4. **What we're not doing:** Scoping boundaries — clear exclusions prevent scope creep
5. **Timeline:** Start date, key milestones, final delivery date
6. **About Centaurion:** Malik's credentials, methodology overview, one or two relevant case studies (add as they develop)
7. **Next steps:** "To proceed, sign below and return a 50% deposit"

### Contract and Payment

**Tool recommendation:** Use Bonsai, HoneyBook, or PandaDoc for contract + e-signature + invoice in one flow. All three offer a free tier or low-cost entry tier.

**Payment terms:**
- Pilot Audit: 50% deposit upon signing, 50% upon final report delivery
- Fractional CAO retainer: Monthly, invoiced on the 1st of each month, net-15
- Workshop: 100% paid 7 days before the workshop date

**Deposit collection:** Stripe (already in Centaurion's infrastructure stack) via Stripe Checkout link embedded in the proposal

### Follow-Up Cadence After Proposal

```
Day 0: Proposal sent + follow-up call scheduled
Day 3: "Did you have a chance to review the proposal? Any questions?"
Day 7: "Following up — I want to reserve [start date] for your audit if this is moving forward."
Day 14: "I want to close my calendar for [month]. If the timing doesn't work now, let me know when would be better."
Day 21: "I'm going to assume the timing isn't right at the moment. I'll follow up in [X weeks]. If anything changes, you have my info."
```

Do not follow up more than 4–5 times. Persistence beyond this with a high-caliber prospect reads as desperation.

---

## Pipeline Health Metrics

Review these weekly (10 minutes, Monday morning):

| Metric | Target |
|---|---|
| Open discovery calls (scheduled) | 3–7 |
| Proposals outstanding | 2–5 |
| Avg. days from discovery call → proposal | < 2 days |
| Avg. days from proposal → close | < 21 days |
| Pipeline value (proposals outstanding) | > $25,000 |
| Monthly closed revenue | $15,000–$40,000 (Phase 1 ramp) |
| Win rate on proposals | > 30% |

**Velocity alert:** If any proposal has been outstanding for > 30 days without a decision, the deal is either dead or requires a direct "go/no-go" conversation.
