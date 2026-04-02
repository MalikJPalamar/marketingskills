# Free Tool Strategy — Centaurion.me
*April 2026 · Skill: free-tool-strategy · Author: Malik Palamar*

---

## Strategic Role of Free Tools

For Centaurion, free tools serve three purposes:
1. **Lead qualification** — someone who takes the assessment is already a warm prospect
2. **Category education** — tools demonstrate the framework in action, not just in theory
3. **SEO + AI citation** — tool pages attract links and get cited as reference resources

---

## Tool 1: Agentic Engineering Level Assessment ⭐ (P0)

### What It Is
A 10-question self-assessment that outputs the user's current agentic engineering level (1–11) and a personalized "what's between you and the next level" report.

### Evaluation Scorecard

| Factor | Score | Notes |
|---|---|---|
| Search demand | 3/5 | Low now, growing fast; first mover advantage |
| Audience match | 5/5 | Technical leaders = exact Centaurion ICP |
| Uniqueness | 5/5 | Nothing like this exists |
| Path to product | 5/5 | Level assessment → advisory engagement is a direct bridge |
| Build feasibility | 4/5 | MVP in Typeform (free), custom HTML form is ~1 day of work |
| Maintenance burden | 4/5 | Static content, low maintenance |
| Link-building potential | 5/5 | Engineering communities share assessment tools widely |
| Share-worthiness | 5/5 | "I'm at Level 7" is inherently shareable |
| **Total** | **36/40** | Strong candidate |

### Questions (10-question structure)

```
1. How do you primarily use AI in your development workflow today?
   a) Autocomplete / tab complete in my IDE
   b) Conversational prompting in a chat interface (ChatGPT, Claude, etc.)
   c) The AI reads my codebase and project context
   d) I run the AI in loops — it generates, tests, and iterates

2. Does your AI have live access to external systems?
   a) No, it works in isolation
   b) Sometimes — I paste in data manually
   c) Yes — it has MCP connections or live API access

3. How do you manage risk in your AI workflows?
   a) I review everything manually
   b) I have some guardrails but mostly trust outputs
   c) I have explicit constraints and backpressure systems (harnessed agents)

4. Do your agents work while you sleep?
   a) No — they only run when I'm actively prompting
   b) Occasionally, for simple tasks
   c) Yes — I regularly assign tasks asynchronously and review outputs later

5. Have you coordinated multiple specialized agents working together?
   a) No
   b) Experimentally, but not in production
   c) Yes — I have an orchestrator coordinating specialized agents in production

6. Can your AI system deploy to production without you opening a laptop?
   a) No — I manually deploy everything
   b) Partially — CI/CD is automated but I trigger it
   c) Yes — prompt → code → CI → production, phone-only is possible

7. Do you use simulated or synthetic environments to test before building?
   a) No — I build, then test with real users
   b) Sometimes for edge cases, but not systematically
   c) Yes — I simulate scenarios and synthetic user panels before committing to build

8. Does your AI system interact with the physical world (IoT, sensors, 3D printing, spatial computing)?
   a) No — everything is digital/software
   b) I'm exploring this
   c) Yes — my agents take actions with physical consequences

9. How persistent is your AI system's memory?
   a) Session only — starts fresh every conversation
   b) Some context saved between sessions (files, notes)
   c) Persistent knowledge graph — episodic + semantic memory shared by all agents

10. How do you measure whether your AI system is performing well?
    a) Subjective judgment — "it seems to be working"
    b) Task completion rate or time saved
    c) Prediction error metrics — I track where the system was wrong and how the model updated
```

### Scoring Logic

| Score Range | Level | Output |
|---|---|---|
| 0–5 | Levels 1–2 | Tab Complete / Chat-Driven |
| 6–10 | Levels 3–4 | Context-Loaded / Compounding Sessions |
| 11–15 | Levels 5–6 | MCP-Connected / Harnessed |
| 16–19 | Levels 7–8 | Background / Multi-Agent |
| 20–22 | Level 9 | Autonomous Deployment |
| 23–24 | Level 10 | Simulation-First |
| 25–27 | Level 11 | Physical-Digital Bridge |

### Lead Capture

- Show level result immediately on screen (no gate)
- Gate the full personalized report: "Enter your email to get your complete Level [N] analysis and roadmap to Level [N+1]"
- Email sequence triggered: see `content/email-sequence.md` (assessment track)

### Distribution

- LinkedIn announcement post: "What agentic engineering level are you? Built a quick assessment."
- GitHub README: Prominent link in 11 Levels repo
- All Centaurion bylines and profile bios
- Conference talks: attendees take the assessment live
- Hacker News: "Show HN: Self-assessment for the 11 Levels of Agentic Engineering"

### Build Recommendation

**MVP (Phase 1 — build in 1 day)**:
- Typeform or Tally form (free tier)
- Google Sheets as backend for responses
- Results: redirect to one of 4-5 landing pages based on score range
- Email capture via Typeform + direct to Mailchimp/Resend

**V2 (Phase 2 — build in 1 week)**:
- Custom HTML/JS (host on centaurion.me/assessment)
- Dynamic results page built from score
- Email capture triggers segmented email sequence
- Response data feeds a dashboard (level distribution across all respondents — publish anonymized aggregate as content)

---

## Tool 2: AI Transformation Readiness Checker (P1)

### What It Is
A 12-question assessment for executives and transformation leads. Outputs: "Your organization is [stage] on the AI transformation spectrum. Here are the 3 highest-leverage actions for your stage."

### Target Query
"AI transformation readiness assessment" / "is my organization ready for AI"

### Evaluation Scorecard: 29/40 (Promising)

### Key Differentiator
Most AI readiness tools are vendor-created (Microsoft, Deloitte) and push toward their own products. Centaurion's is methodology-first and framework-grounded — no vendor agenda.

### Lead Capture
Full report requires email. Segments respondents by organizational type (size + industry) — enables targeted follow-up.

### Build: Typeform MVP (Phase 2)

---

## Tool 3: Prediction Error Cost Calculator (P2)

### What It Is
A simple calculator: "What does a bad AI implementation cost your organization?" Input: number of AI initiatives, average team size, average salary. Output: estimated cost of open-loop failure (time + opportunity cost).

### Target Query
"cost of failed AI implementation" / "AI project failure cost calculator"

### Evaluation Scorecard: 24/40 (Promising)

### Build: No-code calculator, Outgrow or custom HTML (Phase 3)

---

## Tool 4: Exo-Cortex Stack Builder (P3)

### What It Is
An interactive wizard that helps practitioners design their personal exo-cortex architecture. Inputs: current tools, data sources, agent needs. Outputs: recommended stack (Neo4j vs. ChromaDB vs. Graphiti, MCP server choices, agent pattern recommendations).

### Target Query
"how to build an exo-cortex" / "personal AI stack builder"

### Evaluation Scorecard: 22/40 (Phase 3 — after course launches)

---

## Tool Roadmap

| Phase | Tool | Build Effort | Expected Leads/Month |
|---|---|---|---|
| Phase 1 (Q2 2026) | Agentic Engineering Assessment (Typeform) | 4 hours | 50–150 |
| Phase 2 (Q3 2026) | Assessment V2 (custom) + AI Readiness Checker | 2 weeks | 200–400 |
| Phase 3 (Q4 2026+) | Cost Calculator + Stack Builder | 3–4 weeks | 100–200 additional |

---

## Tool SEO Strategy

For each tool, publish a companion content page:
- `/agentic-engineering/assessment/` — tool landing page + explainer
- `/resources/ai-transformation-readiness/` — tool + methodology context
- Each tool page gets `SoftwareApplication` schema + `FAQPage` schema
- Tool pages are included in sitemap and submitted to GSC on launch
