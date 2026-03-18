# Sales Department

**Task Flow Type: C — Continuous Pipeline**
```
Trigger (new lead / new day) → Revenue Cluster works pipeline → Pipeline Cluster manages data → Escalate if needed → Loop
```

Always running. Event-driven. Leads flow in, qualified opportunities flow out to close, customers flow to Customer Success.

---

## Department Manager

**Sales Department Manager** — the accountability layer that watches the pipeline and holds the Sales department to its revenue commitments. Tracks deal velocity, delivers weekly forecasts to founders, audits CRM hygiene, and escalates stalled or at-risk deals before they're lost.

- **Owns:** Daily pipeline status, weekly forecast report to founders, activity quality audits, deal escalation flags, department KPI dashboard (velocity, win rate, forecast accuracy)
- **Reports to:** Human Founders (Nathan / Travis) — directly
- **Manages:** VP Sales Agent (Orchestrator)

## Orchestrator

**VP Sales Agent** — owns the revenue number. Routes new leads, manages pipeline health, coaches cluster performance, and escalates deals that need human involvement. This agent never stops — the pipeline is always moving.

```
Human Founders
  └── Sales Department Manager  ← monitors pipeline, reports forecast, escalates
        └── VP Sales Agent (Orchestrator)  ← routes leads, manages deals, decides
              ├── Revenue Cluster (Prospector + Qualifier + AE + Follow-up)
              ├── Pipeline Cluster (CRM Ops + Forecasting)
              ├── Sales Engineer (solo)
              └── Partnerships Agent (solo)
```

---

## Clusters

### Revenue Cluster
*Runs the end-to-end selling motion from cold lead to closed deal.*

| Agent | Role |
|-------|------|
| **Prospector** | Identifies and sources qualified leads matching the ICP. Cold outreach, list building, LinkedIn, signal-based prospecting |
| **Qualifier** | Runs discovery — BANT/MEDDIC qualification. Separates real opportunities from noise |
| **Account Executive (AE)** | Owns the deal. Runs demos, handles objections, negotiates, drives to close |
| **Follow-up Agent** | Manages all nurture sequences for leads not ready to buy. Re-engages on trigger signals |

**Cluster workflow:**
```
Prospector sources lead → Qualifier runs discovery → ICP match confirmed? → AE takes ownership → Demo + proposal → Close or Follow-up hands → Customer Success intake
```

### Pipeline Cluster
*Keeps the CRM clean, forecasts accurate, and pipeline data actionable.*

| Agent | Role |
|-------|------|
| **CRM Ops Agent** | Owns CRM hygiene — stage accuracy, contact data, activity logging, deduplication |
| **Forecasting Agent** | Models pipeline to predict close rates and revenue. Weekly forecast report to VP Sales |

**Cluster workflow:**
```
Revenue Cluster logs activity → CRM Ops validates and cleans → Forecasting Agent models pipeline → VP Sales receives weekly forecast → Human reviews revenue projections
```

---

## Solo Agents

### Sales Engineer
Technical resource for complex deals. Runs technical demos, answers deep product questions, produces solution architectures for enterprise prospects. Activated by AE when deal has technical complexity.

### Partnerships Agent
Owns channel partnerships, reseller relationships, and co-sell motions. Sources and manages strategic partners that can bring qualified deals. Reports to VP Sales.

---

## Research/Analyst Layer

### Sales Intelligence Analyst
The ICP research engine. Builds and maintains ideal customer profiles, researches target accounts, surfaces buying signals, and provides account intelligence to the Revenue Cluster.

- **Inputs:** LinkedIn Sales Navigator, intent data, firmographic databases, news alerts on target accounts
- **Outputs:** ICP documents, target account profiles, buying signal alerts, market segment analyses
- **Cadence:** ICP refresh quarterly + daily account intelligence for active pipeline

---

## Workflow

### Inbound Lead Flow
```
1. Lead arrives (form fill, demo request, referral)
2. Qualifier runs immediate discovery (async or sync)
3. BANT/MEDDIC score calculated
4. Score above threshold → AE assigned, demo scheduled
5. Score below threshold → Follow-up Agent takes over nurture
6. AE runs demo → produces proposal
7. Negotiation → Close
8. Deal closed → CS Director notified for onboarding
9. CRM Ops logs all activity, Forecasting updates model
```

### Outbound Prospecting Flow
```
1. Sales Intelligence Analyst identifies target account + contact
2. Prospector crafts personalized cold outreach (email + LinkedIn)
3. Positive response → Qualifier runs discovery
4. Qualified → AE takes the deal
5. Not qualified → Follow-up Agent holds in nurture
6. No response → Prospector runs multi-touch sequence (5-7 touches)
```

### Enterprise Deal Flow
```
1. AE identifies technical complexity
2. Sales Engineer activated — technical discovery + solution design
3. SE produces technical proposal + architecture
4. AE and SE run joint demo
5. Procurement / legal negotiation → Legal dept activated
6. VP Sales approves discount beyond standard range
7. Human (Nathan/Travis) approves any unusual terms
```

### Weekly Forecast Meeting
```
1. Forecasting Agent produces pipeline analysis (Friday)
2. VP Sales reviews: commits, best-case, upside
3. CRM Ops validates data accuracy
4. VP Sales sends forecast to CEO Agent
5. Revenue gaps trigger prospecting/pipeline push
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| HubSpot / Salesforce | CRM Ops, all | CRM — pipeline, contacts, activity |
| LinkedIn Sales Navigator | Prospector, Sales Intel | Prospecting, account research |
| Apollo.io / Outreach | Prospector, Follow-up | Sequences, email automation |
| Gong / Chorus | AE, VP Sales | Call recording, deal intelligence |
| Notion / Linear | VP Sales | Deal tracking, playbooks |
| Clearbit / ZoomInfo | Sales Intelligence Analyst | Firmographic data, intent signals |
| DocuSign / PandaDoc | AE | Proposals, contracts |
| Slack | All | Deal alerts, team comms |

---

## Escalation Path

```
Revenue Cluster → VP Sales Agent
Pipeline Cluster → VP Sales Agent
VP Sales Agent → Human (Nathan/Travis)

Automatic human escalation triggers:
- Deal size above enterprise threshold (e.g., >$50K ARR)
- Non-standard contract terms
- Discount beyond standard range
- Partnership agreements (VP → Human always)
- Any deal with legal/compliance implications
- Forecast variance > 20% from prior week
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `specialized/sales-data-extraction-agent.md` | Sales Intelligence Analyst, CRM Ops |
| `specialized/data-analytics-reporter.md` | Forecasting Agent |
| `specialized/data-consolidation-agent.md` | CRM Ops Agent |
| `product/product-feedback-synthesizer.md` | Follow-up Agent (feedback capture) |
