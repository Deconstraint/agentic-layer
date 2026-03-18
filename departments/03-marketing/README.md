# Marketing Department

**Task Flow Type: B — Campaign/Project**
```
Brief → CMO breaks into workstreams → Clusters run in parallel → CMO assembles → Human approves → Launch
```

Creative, iterative. Clusters can loop back. CMO synthesizes all outputs into coherent campaigns.

---

## Department Manager

**Marketing Department Manager** — the accountability layer ensuring campaigns launch on schedule, content clears all approval gates, and performance numbers reach founders on time. Tracks the content pipeline, verifies external approvals, and delivers weekly marketing metrics.

- **Owns:** Campaign status dashboard, content pipeline tracking, approval gate verification (nothing external without sign-off), weekly metrics delivery to founders, department KPI reporting
- **Reports to:** Human (Nathan Beckham) — directly
- **Manages:** CMO Agent (Orchestrator)

## Orchestrator

**CMO Agent** — translates business goals into marketing strategy, manages campaigns, enforces brand consistency, and reports on performance. Nathan Beckham's domain; CMO Agent mirrors his DTC-founder mindset.

```
Human (Nathan)
  └── Marketing Department Manager  ← monitors, tracks, reports, escalates
        └── CMO Agent (Orchestrator)  ← strategy, routing, synthesis, decisions
              ├── Growth Cluster (SEO + Paid + Email + Analytics)
              ├── Content Cluster (Writer + Editor + Distributor)
              ├── Brand Guardian (solo)
              └── Social Media Strategist (solo)
```

---

## Clusters

### Growth Cluster
*Drives measurable audience and revenue growth through owned, paid, and earned channels.*

| Agent | Role |
|-------|------|
| **SEO Specialist** | Keyword strategy, technical SEO, content gap analysis, search performance |
| **Paid Media Strategist** | Google Ads, Meta Ads, paid social — campaign setup, optimization, budget management |
| **Email Marketer** | Sequences, newsletters, automation flows, list segmentation |
| **Analytics Agent** | Attribution, reporting, conversion tracking, growth dashboards |

**Cluster workflow:**
```
Growth brief → SEO provides organic angle → Paid provides acquisition angle → Email provides nurture angle → Analytics instruments tracking → CMO synthesizes into unified growth plan
```

### Content Cluster
*Produces, refines, and distributes all written and visual content.*

| Agent | Role |
|-------|------|
| **Content Writer** | Blog posts, landing pages, email copy, ad copy, thought leadership |
| **Content Editor** | Quality, voice, brand consistency, SEO optimization of drafts |
| **Content Distributor** | Schedules and publishes across channels, manages content calendar |

**Cluster workflow:**
```
Content brief → Writer drafts → Editor refines (brand voice + SEO) → CMO approves → Distributor publishes on schedule
```

---

## Solo Agents

### Brand Guardian
Owns the brand: voice guidelines, visual standards, messaging framework, positioning. Reviews all external content for brand consistency. Final check before CMO approval on brand-sensitive pieces.

### Social Media Strategist
Owns organic social presence across all platforms. Posts, community engagement, influencer coordination, social listening. Feeds insights back to CMO and Analytics Agent.

---

## Research/Analyst Layer

### Market Research Analyst
Studies target audiences, conducts ICP research, monitors industry trends, and provides customer insight. Feeds the CMO's campaign strategy with data on who we're talking to and what they care about.

- **Inputs:** Surveys, social listening, market reports, customer interviews (from CS dept)
- **Outputs:** ICP profiles, audience reports, trend memos
- **Cadence:** Quarterly deep-dive + monthly trend update

### Competitor Intel Agent
Tracks competitor marketing: ad creative, messaging changes, SEO moves, content strategy, pricing. Delivers weekly competitor intelligence to CMO.

- **Inputs:** SpyFu/Semrush, ad libraries, RSS feeds, social monitoring
- **Outputs:** Weekly competitive digest, alert on major competitor moves
- **Cadence:** Weekly digest + real-time alerts on material changes

---

## Workflow

### Campaign Launch Flow
```
1. CMO receives campaign brief from Executive
2. CMO routes to Research layer for audience + competitive context
3. CMO breaks into parallel workstreams:
   - Growth Cluster: acquisition + nurture strategy
   - Content Cluster: assets + copy
   - Brand Guardian: positioning check
4. All clusters execute in parallel
5. CMO assembles into unified campaign plan
6. Human approves before launch
7. Analytics Agent instruments tracking
8. CMO monitors performance weekly, optimizes
```

### Content Request Flow
```
1. Brief arrives (topic, audience, goal, format)
2. Market Research Analyst confirms audience angle
3. SEO Specialist provides keyword targeting
4. Content Cluster executes (Write → Edit → Distribute)
5. Brand Guardian reviews for consistency
6. CMO approves → Distributor publishes
```

### Paid Campaign Flow
```
1. Paid Media Strategist receives budget + goals
2. Analytics Agent confirms tracking infrastructure
3. Paid Strategist builds campaigns
4. Content Writer produces ad creative
5. CMO approves creative + budget allocation
6. Launch → Analytics monitors daily
7. Paid Strategist optimizes weekly; CMO reviews
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Ahrefs / Semrush | SEO Specialist, Competitor Intel | Keyword research, competitive SEO |
| Google Ads | Paid Media Strategist | Search campaigns |
| Meta Ads Manager | Paid Media Strategist | Social campaigns |
| Resend / Klaviyo | Email Marketer | Email sends + automation |
| Buffer / Hootsuite | Social Media Strategist, Distributor | Scheduling |
| Google Analytics 4 | Analytics Agent | Traffic + conversion tracking |
| Figma | Brand Guardian | Visual asset review |
| Notion | CMO | Campaign planning, editorial calendar |
| HubSpot | CMO, Analytics | Lead tracking, attribution |
| SpyFu / AdSpy | Competitor Intel Agent | Paid ad monitoring |

---

## Escalation Path

```
Growth Cluster / Content Cluster → CMO Agent
Solo Agents → CMO Agent
CMO Agent → Human (Nathan Beckham)

Automatic human escalation triggers:
- Any campaign launch (external content requires approval)
- Budget decisions > configured threshold
- Brand direction changes
- Crisis communications
- Any influencer partnership or paid collaboration
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `marketing/marketing-seo-specialist.md` | SEO Specialist |
| `marketing/marketing-growth-hacker.md` | CMO Agent, Analytics Agent |
| `marketing/marketing-content-creator.md` | Content Writer |
| `marketing/marketing-social-media-strategist.md` | Social Media Strategist |
| `paid-media/paid-media-ppc-strategist.md` | Paid Media Strategist (search) |
| `paid-media/paid-media-paid-social-strategist.md` | Paid Media Strategist (social) |
| `paid-media/paid-media-creative-strategist.md` | Content Writer (ad creative) |
| `paid-media/paid-media-auditor.md` | Analytics Agent |
| `paid-media/paid-media-search-query-analyst.md` | SEO Specialist, Analytics Agent |
| `paid-media/paid-media-tracking-specialist.md` | Analytics Agent |
| `paid-media/paid-media-programmatic-buyer.md` | Paid Media Strategist |
