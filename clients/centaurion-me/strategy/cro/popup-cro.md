# Popup CRO — Centaurion.me
*April 2026 · Skill: popup-cro · Author: Malik Palamar*

---

## Popup Strategy for Centaurion

**Short version: minimal popups.** The Centaurion ICP is analytically rigorous and has a low tolerance for interruption-based marketing. Popups that feel manipulative will damage the brand more than they'll grow the list.

The exception: **exit-intent and scroll-depth triggers** that feel contextual rather than intrusive.

---

## Permitted Popup Types

### 1. Exit-Intent Popup (Methodology Pages Only)

**Trigger**: User moves cursor toward browser tab/address bar (exit intent)
**Location**: `/methodology` and methodology sub-pages only
**Timing**: Only after 60 seconds on page (user has engaged, not bounced)

**Copy**:
```
[Headline]: Before you go — the full methodology as a PDF

[Body]: The Three Laws, Fitness Equation, and Five Sensing Layers 
in a single 4-page document. No fluff.

[Email field]

[CTA]: Send it to me →
[Dismiss]: No thanks
```

**What makes this acceptable**: It offers genuine value (a formatted PDF of content they're already reading). It doesn't lie about scarcity or manufacture urgency.

---

### 2. Scroll-Depth Slide-In (Blog Posts)

**Trigger**: User reaches 70% scroll depth on a blog post
**Location**: Blog posts only
**Format**: Slide-in from bottom-right (not full-screen overlay)

**Copy variant A** (newsletter):
```
[Small header]: Found this useful?

The Prediction Error Brief goes deeper.
Weekly signal from a live system.

[Email] [Subscribe →]
```

**Copy variant B** (assessment):
```
[Small header]: What agentic engineering level are you?

Take the 3-minute assessment →
```

**Dismiss**: X in top-right corner, visible immediately. No "I don't want to improve my AI systems" guilt dismiss text — these are condescending and damage trust.

---

### 3. Assessment Results Upgrade (In-Flow, Not a Popup)

Not technically a popup — but functionally similar: appears inline after showing the level result.

```
You're at Level 7: Background Agents.

[Level description — 2 sentences]

→ What separates Level 7 from Level 8?
→ The 3 highest-leverage actions to get there

[Enter your email for your full Level 7 → 8 roadmap]
```

This converts at 35–50% because the user just completed 10 questions and is highly motivated to see the result.

---

## Prohibited Popup Patterns

| Pattern | Why Prohibited |
|---|---|
| Timed popup (appears after 5 seconds) | Interrupts before value is established |
| Full-screen overlay on page load | Aggressive; signals desperation |
| "Wait! Don't leave!" headlines | Manipulative framing conflicts with brand voice |
| Countdown timers | Manufactured urgency; ICP sees through it |
| "I don't want to transform my AI strategy" dismiss text | Condescending; damages trust |
| Popups on every page | Trains visitors to dismiss without reading |
| Re-showing popup to same visitor within 30 days | Annoying; set cookie to suppress |

---

## Implementation

**Tool recommendation**: Convertflow or a lightweight custom implementation (JS + CSS). Avoid Sumo or Optinmonster — they add significant page weight.

**Suppress rules**:
- Never show to email subscribers (they're already captured)
- Never show on contact, work-with-us, or checkout pages (interrupt the conversion flow)
- 30-day cookie to suppress to returning visitors who've already dismissed

**Mobile**: Slide-in formats work on mobile. Full-screen exit-intent does not (exit intent can't be detected reliably on mobile). On mobile, replace exit-intent with scroll-depth trigger at 80%.
