# Lead Magnets — Centaurion.me

**Client:** Centaurion.me (Malik Palamar)
**Phase:** Lead magnets 1 and 2 in Phase 1 (Q1–Q2 2026); Lead magnets 3 and 4 in Phase 2
**Purpose:** Provide a first-value exchange that demonstrates Centaurion's precision, earns an email address or contact, and qualifies intent for discovery call outreach.

---

## Lead Magnet Philosophy

Centaurion's audience is skeptical of generic content. They have been given a thousand AI readiness guides and transformation checklists. A lead magnet from Centaurion must:

1. Demonstrate the specificity and rigor of the Centaurion Method
2. Be immediately useful — not a 20-page PDF that "we'll read later"
3. Leave the reader with a clear gap to fill — ideally one that Centaurion's engagement addresses
4. Qualify itself: the reader who finds the lead magnet valuable is exactly the type of person who should book a discovery call

Do not create lead magnets that appeal to everyone. Create ones that appeal precisely to the ICP and repel the wrong audience.

---

## Lead Magnet 1: The Closed-Loop AI Checklist

### Description

A single-page, 12-point diagnostic checklist that allows a technical leader or executive to evaluate whether their current AI implementation has a functioning closed-loop architecture. Each point is actionable and specific — not "do you have feedback mechanisms?" but "can you name the specific data signal your system uses to measure prediction error and the latency between measurement and model update?"

The checklist is usable in 10 minutes. It produces a binary score (points present / absent) and a clear signal: "If you checked fewer than 7 of 12 items, your system is a thermostat, not a turbine."

### Format

- Single-page PDF (printable, clean layout)
- 12 checkboxes with 1-sentence descriptions
- Score interpretation at the bottom: 0–4 (Level 1–2), 5–7 (Level 3–4), 8–10 (Level 5–6), 11–12 (Level 7+)
- Centaurion branding, Malik's name and contact
- One-line CTA at the bottom: "Ready for a full diagnosis? Book a discovery call: centaurion.me/call"

### The 12 Points (Checklist Content)

```
THE CLOSED-LOOP AI CHECKLIST
Centaurion.me / Malik Palamar

For each item, mark Y (yes, this is true), N (no, this is not in place), or P (partial/in progress).

SENSING LAYER
[ ] 1. We can name the specific signals our AI system uses as inputs, their source, and their refresh rate
[ ] 2. We have a signal quality measurement — we know when input data degrades and have a process to address it
[ ] 3. Human judgment is explicitly incorporated at the points where context is most ambiguous

REASONING LAYER
[ ] 4. Our AI system produces discrete, measurable predictions (not just outputs)
[ ] 5. We can distinguish between a model predicting and a model executing a rule
[ ] 6. We have a defined confidence threshold below which the system escalates to human review

FEEDBACK LOOP
[ ] 7. Every prediction our system makes is compared against a measured outcome
[ ] 8. We have a defined latency between outcome measurement and model update
[ ] 9. We track prediction error rate over time and can show whether it is improving

ARCHITECTURE
[ ] 10. We can draw the complete data flow from input signal to action to measurement to feedback
[ ] 11. We have assigned ownership of the feedback loop to a specific role or team
[ ] 12. Our AI fitness score (sensing × reasoning × feedback / complexity) has been calculated at least once

---
SCORE INTERPRETATION
0–4 ✓ checked: Thermostat architecture. Functional but not compounding.
5–7 ✓ checked: Transitional. You have loops, but they're incomplete.
8–10 ✓ checked: Emerging turbine. Compounding is beginning.
11–12 ✓ checked: Closed-loop system. Focus on reducing implementation complexity.

Ready for a full audit? centaurion.me/call
```

### Gate vs. Ungate Decision

**Gate with email.** This checklist is the entry point into the Centaurion email nurture sequence. It is short enough that friction of giving an email is low, and specific enough that only the right ICP will bother.

**Gate mechanism:**
- Homepage CTA: "Take the free 12-point checklist →"
- Leads to a simple form: First name, Email
- PDF delivered immediately via email
- Triggers Welcome Sequence Email W1

### Email Trigger

Upon download, add contact to:
1. The Welcome Sequence (if not already subscribed)
2. Tag: `downloaded_checklist`
3. Lead score: +10 points (behavioral)

---

## Lead Magnet 2: The Agentic Engineering Assessment

### Description

An interactive 5-minute self-assessment tool that places the user's organization on the 11 Levels of Agentic Engineering and identifies their top 2–3 architectural gaps. Not a quiz with generic results — a structured diagnostic that asks specific questions about sensing infrastructure, feedback loop design, agent coordination, and human oversight architecture.

This is the highest-intent lead magnet in the stack. Completing it signals that the user is serious about understanding their current state — not just browsing.

### Format

**Interactive tool (web-based)** — not a PDF. Build as a multi-step form with conditional logic. Recommended platforms:

- **Typeform** (professional, clean UI, conditional logic, integrates with email platforms) — $25/mo
- **Tally** (free tier available, simpler design, good for Phase 1) — free
- **Custom build** on Centaurion.me stack — best long-term but higher Phase 1 effort

Assessment structure:
- 15–20 questions, organized into 4 sections (Sensing, Reasoning, Feedback, Complexity)
- Each question has 4–5 answer options that map to Level indicators
- Progress bar visible throughout
- Results screen: Level placement, gap identification, score on Fitness Equation
- Email capture: "Enter your email to receive your full results PDF"

### Question Examples

**Section 1: Sensing Layer**
Q: "When your AI system receives input data, how would you characterize the data quality process?"
- A) We have no systematic process — data goes directly to the model
- B) We do basic cleaning before ingestion
- C) We have signal quality metrics and alerts when input quality degrades
- D) We have a dedicated sensing layer with quality measurement, filtering, and human escalation protocols

**Section 2: Feedback Loop**
Q: "After your AI system produces an output or takes an action, what happens?"
- A) We use the output manually; there's no automatic feedback
- B) We sometimes compare outputs to outcomes but not systematically
- C) We track outcomes and update models periodically (quarterly or annually)
- D) We have a continuous measurement loop — every prediction is compared to an outcome with defined latency

**Section 3: Coordination**
Q: "If you have multiple AI agents or systems, how do they coordinate?"
- A) They don't — each system operates independently
- B) They share data via a common database but don't directly communicate
- C) They pass outputs to each other in a defined pipeline
- D) They coordinate dynamically with shared context and can redirect based on each other's outputs

### Results Output

**Level badge + description:**
"Your organization is operating at Level [X] of the 11 Levels of Agentic Engineering."
[Description of what Level X means in plain language]

**Top gaps identified:**
"Based on your answers, your highest-priority gaps are:"
1. [Gap 1 — specific, named]
2. [Gap 2]
3. [Gap 3]

**Fitness Equation estimate:**
"Your estimated Fitness Score is [X] — [interpretation]"

**Next step CTA:**
"Want a full diagnosis? The 30-Day Pilot Audit measures all variables precisely and delivers a prioritized roadmap. [Book a Discovery Call →]"

### Gate vs. Ungate Decision

**Partially gated.** Show the Level result immediately (no email required) to reduce friction and maximize completion. Gate the detailed gap analysis and Fitness Equation breakdown behind an email.

This produces two types of leads:
- Level result only: curious user, not yet committed
- Full results: motivated user, ready for engagement

### Email Trigger

Upon completion (email submitted):
1. Send Email A1 (Assessment Track Sequence, immediate)
2. Tag: `assessment_completed`, `level_[X]`, `top_gap_[area]`
3. Lead score: +25 points (highest single behavioral signal)
4. If lead score > 60: queue for personal outreach within 24 hours

### Cross-reference

This assessment links to the `free-tool-strategy.md` document in the strategy folder. See that document for SEO and distribution strategy for the tool.

---

## Lead Magnet 3: AI Transformation Readiness Report Template (Phase 2)

### Description

A structured template for internal AI champions to use when building the business case for AI transformation investment within their organization. Fills the "how do we present this to our board/CEO" gap for Segment A (technical leaders who need to bring business leaders along).

### Format

**Google Slides or Notion template** — 15-slide deck structure with placeholder content, guiding questions, and data fields to fill in. Includes:

- Executive summary format (Fitness Equation score, gap summary, investment case)
- Current state documentation framework (sensing, reasoning, feedback, complexity scored)
- Roadmap template (Phase 1, 2, 3 with milestone and investment inputs)
- ROI model: blank spreadsheet with formulas for calculating cost of inaction and projected compounding value
- Appendix: 11 Levels visual for board context

### Who It's For

The internal AI champion at a mid-market organization who understands the Centaurion Method and needs to bring their executive team into the decision. This lead magnet serves Segment A and accelerates the internal sales process.

### Gate vs. Ungate Decision

**Gate with email + company name.** This template is a signal of serious intent. The contact who downloads this is either already engaged in an AI transformation initiative or building the case to start one. Both are high-value.

**Additional gate option:** Gate behind the completion of Lead Magnet 2 (Assessment). "Get the full readiness report template after completing your assessment." This sequences engagement and increases the quality of contacts receiving this asset.

### Email Trigger

1. Tag: `downloaded_readiness_template`
2. Lead score: +15 points
3. If assessment also completed (score > 40): trigger personal outreach from Malik within 72 hours
4. Add to Assessment Track Sequence if not already in it

### Phase 2 Timing

Develop this lead magnet after:
- At least 2 client Pilot Audits completed (so the template reflects real diagnostic outputs)
- The 11 Levels framework is fully documented with examples at each level
- A case study exists that the template's ROI model can reference

---

## Lead Magnet 4: The Thousand-Day Window

### Description

A 2-page strategic brief (PDF) that makes the structural argument for why the next 1,000 days of AI adoption decisions are disproportionately important — not from a hype or FOMO standpoint, but from a systems and competitive structure standpoint.

The argument: AI systems that compound (turbines) create durable competitive advantages because the architecture that produces compounding is expensive to replicate after the fact. Organizations that implement closed-loop systems now will have more learning cycles, more training data, more refined sensing layers, and more developed internal capability by 2029 than organizations that implement later — even if they implement with technically superior models.

The window is not "AI is peaking and then declining." The window is "the compounding gap between early closed-loop implementers and later thermostats becomes irreversible within 1,000 days."

### Format

- 2-page PDF (executive brief format)
- Page 1: The argument (the compounding gap, the structural advantage, why the window exists)
- Page 2: What the organizations building turbines have in common (Three Laws, architecture choices, the internal champion) + What to do this week
- Centaurion branding, Malik's name, link to centaurion.me

### Tone

This brief is not alarmist. It is precise and analytical. The Thousand-Day Window is a structural observation, not a sales tactic. It should read like something a systems engineer would write after thinking carefully about competitive dynamics — not like a marketing piece designed to create urgency.

### Gate vs. Ungate Decision

**Ungate — freely available.** The Thousand-Day Window brief is the top-of-funnel awareness piece. It should spread. It should be attached to cold emails (see cold-email-sequences.md). It should be the thing Malik's network shares with people who say "I don't know where to start on AI."

**Email capture on the download page:** Optional. Offer: "Subscribe to The Prediction Error Brief for weekly analysis of exactly this kind of structural AI question." This converts a percentage of brief readers to newsletter subscribers without creating a hard gate.

### Email Trigger

If email captured on download:
1. Send brief delivery confirmation immediately
2. Tag: `downloaded_thousand_day_window`
3. Lead score: +15 points
4. Add to Welcome Sequence on Day 2 (not Day 0, since they didn't subscribe through the normal path)
5. If lead score + demographic score > 60 within 14 days: personal outreach

### Distribution Strategy

The Thousand-Day Window is designed to be shared:
- Attach to cold outreach email sequences as a free resource (no email required when delivered directly in outreach)
- Post the key argument as a LinkedIn long-form article with PDF linked
- Share in Slack communities and forums where technical leaders discuss AI strategy
- Include as a PS in newsletter issues: "If you haven't read The Thousand-Day Window brief, it's the 2-page argument behind why I think Phase 1 matters more than most think."

---

## Lead Magnet Sequencing (The Funnel Logic)

The four lead magnets form a progression from awareness to high intent:

```
Awareness tier (wide aperture):
  Lead Magnet 4: Thousand-Day Window [free, shareable, spreads the argument]
        ↓
Engagement tier (demonstrates analytical depth):
  Lead Magnet 1: Closed-Loop AI Checklist [email required, immediate value, specific]
        ↓
Diagnostic tier (high intent, self-selection):
  Lead Magnet 2: Agentic Engineering Assessment [email required, personalizes the diagnosis]
        ↓
Internal selling tier (Phase 2, very high intent):
  Lead Magnet 3: AI Transformation Readiness Report Template [email + company, serious commitment]
```

A contact moving through all four is a hot lead. The progression itself is a qualifying mechanism.

---

## Production Notes

### Phase 1 Build Order

1. The Closed-Loop AI Checklist (Week 1 of Phase 1 — lowest effort, immediate value)
2. The Thousand-Day Window Brief (Week 2 — highest distribution value)
3. The Agentic Engineering Assessment (Week 4–6 — requires form build and scoring logic)
4. AI Transformation Readiness Template (Phase 2)

### Design Standards

- No stock photography
- Centaurion color palette (define before production)
- Technical diagrams preferred over decorative graphics
- Dense, analytical content preferred over whitespace-heavy "premium" feel
- PDF naming convention: `centaurion-[magnet-name]-v[version].pdf`

### Version Control

When lead magnets are updated, maintain a version number and archive prior versions. Some contacts will have the older version — the version number helps Malik know which version a contact received when discussing it in a discovery call.
