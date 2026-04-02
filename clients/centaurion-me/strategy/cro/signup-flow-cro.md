# Signup Flow CRO — Centaurion.me
*April 2026 · Skill: signup-flow-cro · Author: Malik Palamar*

---

## Centaurion's "Signup" Flows

Centaurion doesn't have a traditional product signup. The equivalent flows are:

| Flow | Entry Point | Goal | Friction Level |
|---|---|---|---|
| Newsletter subscription | Any page CTA, assessment result | Email capture | Very low |
| Assessment completion | `/agentic-engineering/assessment` | Lead capture + qualification | Low |
| Discovery call booking | Work With Us pages | High-intent lead | Medium |
| Course enrollment (Phase 2) | `/course` or `/certification` | Paid conversion | Medium |

---

## Flow 1: Newsletter Subscription

### Current friction points to eliminate
- Don't ask for name + email — email only (add name later via preference center)
- Don't show a popup — use inline or end-of-content CTAs (matches brand voice)
- Confirmation page must reinforce the value: "You're subscribed. First issue arrives [day]. Here's what to read while you wait: [link to methodology hub]"

### Optimized flow
```
[Inline CTA] → [Single field: email] → [Submit]
→ Confirmation page: "You're in. First Prediction Error Brief: [day]. 
   While you wait → [The Centaurion Method / Assessment Tool]"
→ Welcome email (see content/email-sequence.md) within 5 minutes
```

### Double opt-in decision
**Recommendation: No double opt-in** at Phase 1. List quality matters less than list size at this stage. Implement double opt-in once list reaches 1,000+ to manage deliverability.

---

## Flow 2: Assessment Completion → Email Capture

### Optimized flow
```
[Start Assessment] → [10 questions, 3 minutes] → [Level revealed immediately]
→ "Get your full Level [N] analysis + roadmap to Level [N+1]"
→ [Single field: email] → [Submit]
→ Results email with full personalized report (within 2 minutes)
→ Assessment nurture sequence (see content/email-sequence.md)
```

### Key CRO principles
- **Show value before asking**: Level revealed immediately. Email gate is for the depth, not the answer.
- **Specificity drives conversion**: "Your personalized Level 7 → Level 8 roadmap" converts better than "Get your full report"
- **Speed**: Results email must arrive within 2 minutes. Delay kills conversion.

### Friction reduction
- No name field (email only)
- No phone field
- No "how did you hear about us"
- Progress bar visible during assessment (goal-gradient effect)

---

## Flow 3: Discovery Call Booking

### Entry points
- Work With Us pages → "Book a Discovery Call" button
- Homepage secondary CTA
- End of case study
- Cold email response

### Optimized flow
```
[CTA: Book a Discovery Call] 
→ [Calendly/Cal.com embed — show available times immediately]
→ [Booking form: Name, Email, "Describe your AI situation in one sentence"]
→ Confirmation page + calendar invite
→ Pre-call email sequence (24 hours before call):
   Email 1: "Before our call, please read [Methodology overview link]"
```

### CRO principles
- **Calendar embed on page** — don't redirect to another tab (each redirect loses 20-30% of bookers)
- **One qualifying question only** — "Describe your AI situation in one sentence" qualifies without over-screening
- **Confirm immediately** — confirmation page + auto-calendar invite builds commitment
- **Pre-call email** — sets expectations, filters non-serious bookers, improves call quality

### Reducing no-show rate
- Reminder email 24 hours before
- Reminder SMS if phone was collected (optional)
- "What to expect in our call" section on confirmation page
- Rescheduling link in reminder emails (reduces cancellation-with-no-rebook)

---

## Flow 4: Course Enrollment (Phase 2)

### Optimized flow (design now, build Phase 2)
```
[Pricing page] → [Select tier] 
→ [Checkout: Name, Email, Payment]
→ Confirmation: immediate course access + welcome email
→ Onboarding sequence (see strategy/cro/onboarding-cro.md)
```

### Checkout CRO
- Stripe as payment processor (trust signal + saves cards)
- Show what they get immediately below the buy button
- Money-back guarantee prominent
- "Join X practitioners who've completed the certification" social proof
- No account creation required before purchase (create account after payment)

---

## General Principles Across All Flows

1. **Single next action** — every flow ends with one clear next step, not three options
2. **Speed** — automated emails within 2 minutes, not 2 hours
3. **Consistency** — brand voice matches from CTA through confirmation page through first email
4. **No upsell at the gate** — don't try to upsell before the first conversion is complete
