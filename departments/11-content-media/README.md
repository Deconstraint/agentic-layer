# Content & Media Department

**Task Flow Type: B — Campaign/Project**
```
Brief → Content Director breaks into production + distribution workstreams → Clusters run in parallel → Review cycle → Human approves → Publish + distribute
```

Creative, pipeline-driven. Production and distribution run in parallel. Nothing publishes without human approval — the Content Department Manager enforces this gate.

---

## Department Manager

**Content & Media Department Manager** — the accountability layer keeping the content pipeline moving and ensuring every piece that publishes has cleared the proper approval gates.

- **Owns:** Content pipeline dashboard (production/review/approved/scheduled/published), approval gate verification (nothing goes live without confirmed human sign-off), content calendar health, post-publish performance routing, department KPI dashboard (output volume, on-schedule rate, engagement per piece)
- **Reports to:** Human Founders — directly
- **Manages:** Content Director Agent (Orchestrator)

## Orchestrator

**Content Director Agent** — directs the full content operation: briefs the Production Cluster, manages the distribution strategy, enforces editorial standards, and synthesizes performance data into content strategy adjustments.

```
Human Founders
  └── Content Dept Manager  ← tracks pipeline, enforces approvals, reports performance, escalates
        └── Content Director Agent (Orchestrator)  ← briefs, directs, reviews, strategy decisions
              ├── Production Cluster (Writer + Editor + Designer + Publisher)
              ├── Distribution Cluster (SEO + Social + Email + Syndication)
              ├── Video Producer (solo)
              ├── Podcast Agent (solo)
              └── Visual Storyteller (solo)
```

---

## Clusters

### Production Cluster
*Creates all content from brief to publish-ready asset.*

| Agent | Role |
|-------|------|
| **Writer** | Produces long-form and short-form written content: articles, guides, case studies, scripts |
| **Editor** | Reviews all written content for clarity, brand voice, accuracy, and SEO optimization |
| **Designer** | Produces visual assets: graphics, infographics, social images, presentation slides |
| **Publisher** | Formats and publishes content to all channels (CMS, social, email platform) |

**Cluster workflow:**
```
Brief → Writer drafts → Editor refines → Designer produces visuals → Content Director reviews → Human approves → Publisher schedules and publishes
```

### Distribution Cluster
*Maximizes reach and impact of every piece of content produced.*

| Agent | Role |
|-------|------|
| **SEO Distribution Agent** | Optimizes content for search, handles technical publishing requirements (schema, meta, canonicals) |
| **Social Distribution Agent** | Adapts content for each social platform and schedules organic posts |
| **Email Distribution Agent** | Packages content into newsletter/digest format and sends to appropriate lists |
| **Syndication Agent** | Identifies and manages content syndication opportunities: Medium, industry publications, partner channels |

**Cluster workflow:**
```
Content approved → Distribution Cluster adapts for each channel → SEO handles technical → Social schedules posts → Email prepares digest → Syndication identifies placement → All launch on coordinated schedule
```

---

## Solo Agents

### Video Producer
Owns video content end-to-end: scripting, production coordination, editing direction, and platform publishing (YouTube, LinkedIn Video, social clips). Works with Writer for scripts and Designer for graphics.

### Podcast Agent
Manages podcast production: episode planning, guest coordination, recording logistics, editing coordination, show notes, and distribution to podcast platforms.

### Visual Storyteller
Creates narrative-driven visual content: data visualizations, visual essays, interactive graphics, and brand storytelling assets that go beyond standard design work.

---

## Research/Analyst Layer

### Content Intelligence Analyst
Monitors content performance across all channels and provides the Content Director with data on what's working, what gaps exist, and where the biggest opportunities lie.

- **Inputs:** Google Analytics, Search Console, social analytics, email metrics, video performance data, competitive content analysis
- **Outputs:** Weekly content performance report, top-performing content digest, content gap analysis, SEO opportunity reports
- **Cadence:** Weekly performance report + on-demand analysis

---

## Workflow

### Content Production Flow
```
1. Content brief arrives (from Marketing, Executive, or Content Director's editorial plan)
2. Content Director assigns to Production Cluster
3. Writer drafts (SEO Distribution Agent provides keyword targets)
4. Editor reviews: voice, clarity, accuracy, SEO
5. Designer produces visuals
6. Content Director reviews complete package
7. Content Dept Manager verifies approval gate
8. Human approves
9. Publisher + Distribution Cluster execute coordinated publish
10. Content Intelligence Analyst instruments tracking
11. Performance data routed back to Content Director at Day 7, Day 30
```

### Video/Podcast Flow
```
1. Episode/video concept approved by Content Director
2. Video Producer / Podcast Agent activates production workflow
3. Script produced by Writer, reviewed by Editor
4. Production coordinated (recording, editing, assets)
5. Final review by Content Director
6. Human approves before publish
7. Distribution Cluster handles multi-channel distribution
```

### Distribution Optimization Flow
```
1. Content Intelligence Analyst identifies high-performing content
2. Content Director decides: repurpose / amplify / update
3. Production Cluster produces derivative assets (e.g., article → video script → infographic)
4. Distribution Cluster pushes to additional channels
5. Performance tracked across all derivative versions
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| WordPress / Webflow | Publisher, SEO Agent | CMS publishing |
| Figma / Canva | Designer, Visual Storyteller | Design and visual assets |
| Buffer / Later | Social Distribution | Social scheduling |
| Resend / Klaviyo | Email Distribution | Email distribution |
| YouTube Studio | Video Producer | Video platform management |
| Buzzsprout / Transistor | Podcast Agent | Podcast hosting |
| Descript | Video Producer, Podcast Agent | Audio/video editing |
| Google Search Console | SEO Distribution | Search performance |
| Ahrefs | Content Intelligence Analyst | SEO + content gap analysis |
| Google Analytics | Content Intelligence Analyst | Performance tracking |

---

## Escalation Path

```
Production Cluster → Content Director Agent
Distribution Cluster → Content Director Agent
Solo Agents → Content Director Agent
Content Director → Content Dept Manager → Human Founders

Automatic human escalation triggers:
- Every piece of content before publish (approval required)
- Any content touching sensitive topics, competitors by name, or legal claims
- Any partnership content or co-branded material
- Any content budget above threshold
- Any PR or reputation-adjacent content
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `design/design-visual-storyteller.md` | Visual Storyteller |
| `design/design-brand-guardian.md` | Editor (brand voice enforcement) |
| `marketing/marketing-content-creator.md` | Writer |
| `marketing/marketing-social-media-strategist.md` | Social Distribution Agent |
| `design/design-image-prompt-engineer.md` | Designer |
| `marketing/marketing-seo-specialist.md` | SEO Distribution Agent |
