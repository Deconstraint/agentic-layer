# Marketing Department

**Task Flow Type: B — Campaign/Project**
```
Brief → CMO breaks into tasks → Workers execute in parallel → CMO assembles → Review
```

Creative, iterative. Workers can loop back. CMO synthesizes output.

---

## Department Structure

```
CMO Agent (Department Manager)
├── Brand Strategist Agent
│   └── Owns: brand voice, positioning, messaging framework
├── Content Writer Agent
│   └── Owns: blog posts, copy, landing pages, email copy
├── SEO Specialist Agent
│   └── Owns: keyword research, on-page SEO, content strategy
├── Paid Ads Agent
│   └── Owns: Google Ads, Meta Ads, campaign management
├── Email Marketer Agent
│   └── Owns: sequences, newsletters, automation
└── Social Media Agent
    └── Owns: posts, scheduling, engagement, analytics
```

---

## Roles

| Role | File | Primary Function |
|------|------|-----------------|
| CMO | `/CMO/` | Strategy, campaigns, brand direction, team coordination |
| Brand Strategist | `/brand-strategist/` | Positioning, messaging, voice guidelines |
| Content Writer | `/content-writer/` | All written content — blogs, copy, emails, scripts |
| SEO Specialist | `/seo-specialist/` | Search strategy, keyword research, technical SEO |
| Paid Ads | `/paid-ads/` | Google/Meta campaigns, budget, optimization |
| Email Marketer | `/email-marketer/` | Sequences, newsletters, automation flows |
| Social Media | `/social-media/` | Posts, scheduling, community, analytics |

---

## How Marketing Handles Tasks

### Campaign Launch Flow
```
1. CMO receives campaign brief from Executive
2. CMO breaks into parallel workstreams:
   - Brand Strategist: messaging + positioning
   - Content Writer: copy + content assets
   - SEO Specialist: keyword targeting
   - Paid Ads: campaign setup
   - Email Marketer: nurture sequence
   - Social Media: organic amplification
3. Workers execute in parallel
4. CMO reviews all outputs for brand consistency
5. CMO assembles campaign plan
6. Human approves before launch
7. Workers activate on schedule
8. CMO monitors + optimizes weekly
```

### Content Request Flow
```
1. Content Writer receives brief (topic, audience, goal, format)
2. SEO Specialist provides: target keywords, search intent, competitors
3. Content Writer drafts
4. Brand Strategist reviews for voice/positioning
5. CMO approves
6. Content published (Social amplifies, Email distributes if relevant)
```

### Lead Generation Flow
```
1. CMO sets lead gen target + ICP
2. SEO Specialist: organic content strategy
3. Paid Ads: paid acquisition campaigns
4. Content Writer: lead magnets + landing page copy
5. Email Marketer: lead nurture sequence
6. Leads flow into CRM → handed off to Sales
```

---

## Department Rules

1. **Brand consistency** — all content reviewed against brand guidelines before publish
2. **No claims without data** — every marketing claim must be supportable
3. **Approval gates** — all external-facing content needs human sign-off
4. **Attribution required** — every campaign tracked with UTM parameters
5. **Audience first** — every piece starts with "who is this for and what do they need?"

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Google Analytics | CMO, SEO | Traffic, conversions |
| Google Search Console | SEO | Search performance |
| Google Ads | Paid Ads | PPC campaigns |
| Meta Ads Manager | Paid Ads | Social campaigns |
| Resend / Mailchimp | Email Marketer | Email sends |
| Ahrefs / Semrush | SEO | Keyword research |
| Buffer / Hootsuite | Social Media | Scheduling |
| Figma | Brand | Design assets |
| Notion / Linear | CMO | Campaign planning |
| HubSpot / CRM | CMO | Lead tracking |
| Trello | CMO | Workflow management |

---

## Nathan's Domain Context

Nathan Beckham (CMO/Co-founder) leads marketing at Deconstraint.
- Background: HempLucid CEO ($30M+ DTC revenue)
- Focus: Growth, paid acquisition, funnel optimization
- Key projects: Deconstraint lead gen, VIIA application, Anahata Collection
- Communication style: Strategic, data-driven, metrics-focused

The CMO Agent mirrors Nathan's approach:
- Data first — every decision backed by numbers
- Full-funnel thinking — from awareness to conversion to retention
- Speed + quality — move fast but not sloppy

---

## Escalation Path

```
Content Writer / SEO / Social → CMO → Human (Nathan)
Paid Ads (budget decisions > threshold) → CMO → Human (Nathan)
Brand decisions → CMO → Human (Nathan + Travis)
```
