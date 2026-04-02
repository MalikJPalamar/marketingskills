# Analytics Tracking Strategy — Centaurion.me

**Client:** Centaurion.me (Malik Palamar)
**Phase:** Foundation (Q1–Q2 2026)
**Goal:** Instrument the full lead journey from first visit to pilot client conversion, with specific attention to AI-referred traffic and methodology engagement.

---

## Overview

Centaurion.me operates in a low-volume, high-value market. A single pilot audit conversion ($8.5K–$12.5K) justifies significant tracking sophistication. The analytics stack must answer three questions at any point in time:

1. Which channels are producing qualified leads (people who understand the Centaurion Method)?
2. Where are visitors dropping off before booking a discovery call?
3. Is the methodology content (Three Laws, Fitness Equation, Five Sensing Layers) driving engagement or confusion?

This document covers GA4 setup, event taxonomy, UTM conventions, GSC integration, AI referral traffic tracking, and monthly reporting cadence.

---

## GA4 Property Setup

### Property Configuration

```
Property name: Centaurion.me
Reporting timezone: US/Eastern (Malik's operating timezone)
Currency: USD
Data retention: 14 months (maximum on free tier)
Enhanced measurement: Enable all (scroll tracking, outbound clicks, file downloads, form interaction)
```

### Data Streams

**Web stream:** centaurion.me
- Enable cross-domain tracking if subdomain (app.centaurion.me for assessment tool) is added later
- Enable Google Signals for cross-device reporting (requires accepting usage in audience settings)

**App streams:** Not applicable in Phase 1

### Linked Products

| Product | Status | Purpose |
|---|---|---|
| Google Search Console | Required | Organic query data in GA4 |
| Google Ads | Phase 2 | Ad performance → conversion attribution |
| BigQuery | Optional | Long-term raw event export for custom analysis |
| Looker Studio | Recommended | Monthly reporting dashboards |

---

## Key Events to Track

### Conversion Events (Mark as conversions in GA4)

These drive Malik's primary business decisions. Mark each as a conversion in GA4 Admin > Events:

#### 1. `discovery_call_booked`
**Trigger:** Thank-you page load after Calendly/scheduling tool booking
**Method:** Calendly webhook → GA4 Measurement Protocol, or Calendly redirect to `/thank-you/call-booked`
**Parameters:**
```javascript
gtag('event', 'discovery_call_booked', {
  'call_source': 'homepage_hero' | 'methodology_page' | 'assessment_completion' | 'email',
  'ica_segment': 'segment_a' | 'segment_b' | 'segment_c', // populated if known
  'utm_source': utm_source,
  'utm_medium': utm_medium,
  'utm_campaign': utm_campaign
});
```

#### 2. `assessment_completed`
**Trigger:** User reaches final screen of Agentic Engineering Assessment
**Method:** JavaScript event on assessment tool completion
**Parameters:**
```javascript
gtag('event', 'assessment_completed', {
  'assessment_score': integer, // 0-100 readiness score
  'top_gap_area': string, // e.g., 'sensing_layer_2', 'agentic_level_4'
  'completion_time_seconds': integer,
  'email_submitted': boolean
});
```

#### 3. `email_signup`
**Trigger:** Successful newsletter/lead magnet form submission
**Method:** Form submit event, confirmed on server-side where possible
**Parameters:**
```javascript
gtag('event', 'email_signup', {
  'signup_source': 'homepage' | 'assessment_completion' | 'blog_post' | 'lead_magnet',
  'lead_magnet': 'closed_loop_checklist' | 'thousand_day_window' | 'readiness_report' | 'newsletter',
  'page_path': window.location.pathname
});
```

#### 4. `lead_magnet_download`
**Trigger:** PDF download or lead magnet access confirmed
**Method:** Outbound click on file URL, or server-side confirmation
**Parameters:**
```javascript
gtag('event', 'lead_magnet_download', {
  'magnet_name': 'closed_loop_checklist' | 'thousand_day_window' | 'readiness_report',
  'gate_method': 'email_required' | 'free_access',
  'referrer_page': document.referrer
});
```

### Engagement Events (Not conversions, but tracked for funnel analysis)

#### 5. `methodology_section_engaged`
**Trigger:** User scrolls past 75% of a methodology page OR spends >90 seconds on the page
**Method:** Scroll depth listener + time-on-page custom event
**Parameters:**
```javascript
gtag('event', 'methodology_section_engaged', {
  'section': 'three_laws' | 'fitness_equation' | 'five_sensing_layers' | '11_levels',
  'engagement_type': 'scroll_75' | 'time_90s' | 'both',
  'session_source': utm_source or ga4 session source
});
```

#### 6. `outbound_click_github`
**Trigger:** Click on GitHub repository link (11 Levels repo)
**Method:** GA4 enhanced measurement outbound click (already fires automatically) + custom parameter
**Parameters:** Supplement default event with `link_destination: 'github_11_levels'`

#### 7. `case_study_read`
**Trigger:** Scroll past 75% on any case study or transformation story page
**Parameters:** `case_study_id`, `industry`, `org_size_range`

#### 8. `pricing_page_view`
**Trigger:** Pageview on /work-with-us, /services, or /pricing
**Method:** Standard pageview + custom dimension
**Note:** High-intent signal. Create GA4 audience: "Pricing page visitor" for retargeting.

#### 9. `video_engagement`
**Trigger:** If video content is added (YouTube embed or native)
**Parameters:** `video_title`, `percent_watched` (25/50/75/100)

#### 10. `assessment_started`
**Trigger:** First question answered in assessment tool
**Purpose:** Funnel drop-off: `assessment_started` vs `assessment_completed`

---

## UTM Parameter Conventions

### Structure

```
utm_source=<where the link lives>
utm_medium=<channel type>
utm_campaign=<initiative name>
utm_content=<specific creative or link variant>
utm_term=<keyword, for paid search>
```

### Source Values — Approved List

| Source | Use Case |
|---|---|
| `linkedin` | LinkedIn posts, DMs, profile links |
| `twitter` | X/Twitter posts and threads |
| `github` | Links from GitHub README or repo |
| `newsletter` | Prediction Error Brief email sends |
| `email_outreach` | Cold outreach sequences |
| `referral_partner` | Partner referral links |
| `podcast` | Guest podcast appearances |
| `speaking` | Conference/workshop QR codes |
| `google` | Google Ads (auto-tagged, but set for manual tracking) |
| `linkedin_ads` | LinkedIn paid campaigns |

### Medium Values — Approved List

| Medium | Use Case |
|---|---|
| `organic_social` | Unpaid LinkedIn, X posts |
| `email` | All email sends (newsletter, sequences, outreach) |
| `cpc` | Paid search or paid social |
| `referral` | Human referrals from partners/clients |
| `organic` | SEO (set by GA4 automatically, but consistent) |
| `direct` | Used when source is unknown (auto) |
| `qr` | Physical or slide QR codes |

### Campaign Naming Convention

```
[initiative]-[audience]-[quarter]

Examples:
- thousand-day-window-ceo-q1-2026
- assessment-launch-techleader-q2-2026
- pilot-audit-coo-q1-2026
- 11levels-workshop-cto-q2-2026
```

### Content Values

Use content to distinguish A/B test variants or specific calls to action:
- `hero-cta-discovery-call` vs `hero-cta-work-with-us`
- `linkedin-post-three-laws-v1`
- `email-cta-assessment-bottom`

### UTM Builder Bookmark

Save this URL pattern for quick UTM generation:
```
https://ga-dev-tools.google.com/campaign-url-builder/
```

Or use a spreadsheet-based UTM builder to enforce the approved values above.

---

## Google Search Console Integration

### Connection Steps

1. Verify centaurion.me in GSC (DNS TXT record preferred for full coverage including subdomains)
2. In GA4: Admin > Property > Search Console Links > Link
3. Select GSC property > Select GA4 data stream > Link

### What GSC Unlocks in GA4

- Search query data in Reports > Acquisition > Search Console
- Landing pages by query (critical for SEO feedback loop)
- Impression vs click vs position data for target keywords

### Key GSC Reports for Centaurion

**Weekly Check (5 minutes):**
- Coverage report: Any new crawl errors or indexing failures on methodology pages?
- Performance: Which queries drove impressions this week? Any new AI-adjacent terms appearing?

**Monthly Review:**
- Top 10 queries by clicks: Are these the queries Malik wants to rank for?
- Pages with high impressions but low CTR: Likely meta title/description optimization needed
- Core Web Vitals: Site speed affects both SEO and credibility with technical audience

### Target Keyword Clusters to Monitor in GSC

| Cluster | Example Queries |
|---|---|
| Fractional CAO | "fractional chief ai officer", "fractional CAO consulting" |
| AI Readiness | "ai transformation readiness assessment", "ai organizational readiness" |
| Agentic Engineering | "agentic engineering framework", "11 levels agentic ai" |
| Human-AI Augmentation | "human ai augmentation consulting", "centaurion method" |
| Closed-Loop AI | "closed loop ai systems", "agentic ai feedback loop" |

---

## AI Referral Traffic Tracking

### Why This Matters for Centaurion

Malik's target audience (technical leaders, fractional executives) actively uses AI tools to research vendors and frameworks. When someone asks ChatGPT "who are the best fractional CAOs" or asks Perplexity "what is the Centaurion Method," and that AI cites or links to centaurion.me, that traffic shows up in GA4 as a referral from specific domains — but only if those tools provide a referrer header.

### Known AI Referral Domains to Monitor

Create a custom channel group or filter in GA4 to identify these:

```
chat.openai.com
chatgpt.com
perplexity.ai
www.perplexity.ai
claude.ai
bard.google.com
gemini.google.com
bing.com/chat
copilot.microsoft.com
you.com
phind.com
poe.com
```

### GA4 Setup for AI Traffic Segment

**Step 1: Create a custom channel group**
- GA4 Admin > Channel Groups > Create new group
- Rule: Session source matches regex: `chat\.openai\.com|chatgpt\.com|perplexity\.ai|claude\.ai|gemini\.google\.com|copilot\.microsoft\.com`
- Channel name: `AI Referral`

**Step 2: Create an audience**
- GA4 Admin > Audiences > New audience
- Condition: Session source matches [AI domain regex above]
- Use for: Retargeting in Phase 2, and as a high-value engagement indicator

**Step 3: Monthly AI traffic report**
In Looker Studio dashboard, add a dedicated tile:
- Sessions from AI Referral channel
- Conversion rate from AI referral vs organic vs social
- Top landing pages from AI referral

### The Strategic Signal

If centaurion.me receives AI referral traffic, that means Malik's content is being indexed and cited by AI knowledge bases. This is a Phase 1 strategic goal: structure methodology content (Three Laws, Fitness Equation, 11 Levels) so it is citation-worthy for AI tools. Track this as a leading indicator of brand authority.

---

## Monthly Reporting Cadence

### Report Structure: The Centaurion Monthly Analytics Brief

Deliver the first Monday of each month, covering the prior full month.

**Section 1: Conversion Scorecard (5 metrics)**
```
Discovery calls booked: [X] (vs last month: +/- Y%)
Assessment completions: [X]
Email signups: [X]
Lead magnet downloads: [X]
Methodology page engaged sessions: [X]
```

**Section 2: Traffic Sources**
- Organic search: sessions, top landing pages, top queries from GSC
- Social (LinkedIn, X): sessions, engagement rate
- Email: sessions from newsletter, click-through rate
- AI referral: sessions, top referring AI tools
- Direct/unknown: sessions (flag if unusually high)

**Section 3: Funnel Analysis**
```
Landing page visits → methodology engagement: [X]%
Methodology engagement → assessment starts: [X]%
Assessment starts → completions: [X]%
Assessment completions → email signup: [X]%
Email signup → discovery call booked: [X]%
```

**Section 4: Content Performance**
- Top 5 pages by sessions
- Top 5 pages by time-on-page (engagement quality signal)
- Blog posts or methodology pages that drove assessment starts
- LinkedIn posts that drove centaurion.me traffic

**Section 5: A/B Test Status**
- Active tests: status, sample size, current winner signal
- Completed tests: result and what was implemented

**Section 6: Month-Ahead Focus**
- One conversion rate recommendation based on data
- One SEO action based on GSC findings
- One content decision based on engagement data

### Tooling Recommendation

- **Looker Studio** (free): Connect GA4 + GSC, build the above as a persistent dashboard. Share link with Malik.
- **GA4 Exploration:** Use free-form explorations for funnel analysis (assessment start → completion).
- **No additional paid analytics tool needed in Phase 1.**

---

## Technical Implementation Notes

### Tag Manager (Optional but Recommended)

If centaurion.me is built on a platform that supports Google Tag Manager (Webflow, WordPress, custom), use GTM to manage all GA4 events without code deploys. This matters if Malik wants to iterate on event tracking without engineering support.

### Measurement Protocol (For Server-Side Events)

For events that happen outside the browser (Calendly webhook on booking confirmation, assessment tool backend), use GA4 Measurement Protocol:

```bash
POST https://www.google-analytics.com/mp/collect
?measurement_id=G-XXXXXXXXXX
&api_secret=<API_SECRET>

{
  "client_id": "555",
  "events": [{
    "name": "discovery_call_booked",
    "params": {
      "call_source": "calendly_webhook",
      "session_id": "123"
    }
  }]
}
```

This ensures call bookings are tracked even if the user closes the browser before a redirect-based thank-you page loads.

### Privacy and Consent

Centaurion.me targets B2B professionals. GDPR implications depend on EU visitor volume. In Phase 1:
- Add a cookie consent banner (Cookiebot free tier or similar)
- Configure GA4 for consent mode so analytics data is preserved even when cookies are denied (via modeled data)
- Do not use `analytics_storage=denied` to block all tracking — use consent mode v2 to maintain signal quality

---

## Phase 1 Analytics Stack Summary

| Tool | Cost | Purpose |
|---|---|---|
| GA4 | Free | Primary analytics, conversion tracking, audience building |
| Google Search Console | Free | Organic search performance, query data |
| Looker Studio | Free | Monthly reporting dashboard |
| Google Tag Manager | Free | Event management (optional) |
| GA4 Measurement Protocol | Free | Server-side event tracking |

Total Phase 1 cost: $0. The sophistication comes from configuration, not tooling spend.
