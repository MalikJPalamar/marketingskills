# Form CRO — Centaurion.me
*April 2026 · Skill: form-cro · Author: Malik Palamar*

---

## Forms on Centaurion.me

| Form | Location | Goal | Fields |
|---|---|---|---|
| Newsletter signup | Inline on all content pages | Email capture | Email only |
| Discovery call intake | Work With Us pages | Qualify + book | Name, Email, 1 question |
| Assessment form | `/agentic-engineering/assessment` | Lead capture | 10 questions → email |
| Contact form | `/contact` | General inquiry | Name, Email, Message |
| Course enrollment (Phase 2) | `/course` | Paid conversion | Name, Email, Payment |

---

## Newsletter Signup Form

### Optimized version
```
[Single line: Email address        ] [Subscribe →]
```
Below: "Weekly. No spam. Unsubscribe anytime."

**What to avoid**:
- First name field (adds friction; personalization not worth the drop-off at this stage)
- Checkbox for "I agree to receive emails" (implied by subscribing)
- Dropdown for "How did you hear about us?" (track via UTM instead)

**Placement rules**:
- After first H2 on blog posts (not top of page — reader needs context first)
- End of every blog post
- Sidebar on methodology pages (if layout supports it)
- NOT as a popup (brand voice conflict)

---

## Discovery Call Intake Form

### Optimized version
```
Name: [                    ]
Email: [                   ]
In one sentence, describe your AI situation: [                    ]

[Book My Discovery Call →]
```

**What the qualifying question does**:
- Pre-qualifies intent (someone typing a sentence is serious)
- Gives Malik context before the call (no wasted first 5 minutes)
- Reduces no-show rate (commitment via effort)

**What to remove**:
- Company name (can ask on call)
- Phone number (can ask on call)
- "How did you hear about us?" (UTM)
- Budget range (off-putting before trust is established)
- "What's your timeline?" (creates false urgency pressure)

**Confirmation page**:
```
You're booked.

Here's how to make our call valuable:
1. Read the Centaurion Methodology overview (15 min): centaurion.me/methodology
2. Take the Agentic Engineering Assessment (3 min): centaurion.me/assessment
3. Come with one specific question you want answered

Calendar invite sent to [email].
```

---

## Contact Form

### Optimized version
```
Name: [                    ]
Email: [                   ]
Message: [                 ]

[Send →]
```

**Response SLA**: 48 hours. State this on the form: "We respond within 48 hours."

---

## Form Optimization Principles (Applied to Centaurion)

### 1. One field per line
Never two fields side by side. Side-by-side increases cognitive load.

### 2. Labels above fields, not placeholder text
Placeholder text disappears on focus — users forget what the field is for.

### 3. Submit button copy = action + value
- "Subscribe →" not "Submit"
- "Book My Discovery Call →" not "Send"
- "Get My Results →" not "Submit Form"

### 4. Error messages on field blur, not on submit
Show validation errors immediately when user leaves a field, not after they hit submit.

### 5. Mobile-first form width
On mobile: full-width fields, touch-target height minimum 44px for submit button.

### 6. No CAPTCHA on newsletter or contact forms
CAPTCHA reduces conversions by 10-15%. Use honeypot fields instead (invisible to users, catches bots).

---

## Assessment Form CRO

The assessment is a 10-question form — longest form on the site. Apply these patterns:

- **Progress bar**: "Question 3 of 10" visible at all times
- **One question per screen** (not all 10 on one page)
- **Back button visible** — users are more likely to complete if they feel in control
- **No required answer** — let users skip a question rather than abandon
- **Estimated time upfront**: "3 minutes" reduces abandonment from uncertainty
- **Save progress** (Phase 2 V2): Allow users to resume if they close the browser
