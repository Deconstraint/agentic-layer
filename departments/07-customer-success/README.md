# Customer Success Department

**Task Flow Type: C — Continuous Pipeline**
```
Trigger (new customer / support ticket / NPS response) → Support Cluster handles → Retention Cluster manages health → Escalate if needed → Loop
```

Always running. Every customer interaction is a retention event. The CS department turns customers into advocates and catches churn signals before they become lost accounts.

---

## Department Manager

**Customer Success Department Manager** — the accountability layer monitoring customer health across the portfolio and holding the CS department to its response time, resolution quality, and retention commitments.

- **Owns:** Daily support queue status, customer health dashboard (at-risk flags, NPS trend), SLA adherence tracking, spot-check quality reviews on support responses, escalation to human on at-risk enterprise accounts, department KPI dashboard
- **Reports to:** Human Founders — directly
- **Manages:** CS Director Agent (Orchestrator)

## Orchestrator

**CS Director Agent** — routes incoming support tickets, manages onboarding pipelines, synthesizes customer feedback, and directs the department's retention strategy.

```
Human Founders
  └── CS Department Manager  ← monitors health, tracks SLAs, reports, escalates
        └── CS Director Agent (Orchestrator)  ← routes tickets, directs retention, decides
              ├── Support Cluster (Responder + Escalation Handler + Knowledge Base)
              ├── Retention Cluster (Onboarding + NPS + Account Manager)
              ├── Community Manager (solo)
              └── Feedback Synthesizer (solo)
```

---

## Clusters

### Support Cluster
*Handles all inbound support — fast, accurate, and empathetic.*

| Agent | Role |
|-------|------|
| **Responder** | First-line support: answers tickets, resolves common issues, routes complex ones |
| **Escalation Handler** | Owns complex or escalated tickets — deep troubleshooting, cross-dept coordination |
| **Knowledge Base Agent** | Maintains and expands the self-service knowledge base from resolved tickets |

**Cluster workflow:**
```
Ticket arrives → Responder triages → Can resolve? → Resolves + logs → Cannot resolve? → Escalation Handler takes over → Resolution → Knowledge Base captures learnable content
```

### Retention Cluster
*Proactively manages customer health to prevent churn and drive expansion.*

| Agent | Role |
|-------|------|
| **Onboarding Agent** | Guides new customers through activation milestones — time-to-value is the target |
| **NPS Agent** | Runs NPS surveys, analyzes scores, routes detractors for recovery and promoters for referrals |
| **Account Manager** | Manages ongoing relationships for key accounts — QBRs, health checks, expansion conversations |

**Cluster workflow:**
```
Customer signed → Onboarding Agent activates sequence → Milestones tracked → NPS Agent surveys at intervals → Detractor signal? → Account Manager activates recovery → CS Director notified
```

---

## Solo Agents

### Community Manager
Owns the customer community (forum, Slack, Discord, etc.). Facilitates peer-to-peer help, surfaces product feedback, highlights customer wins. Feeds insights to Feedback Synthesizer.

### Feedback Synthesizer
Aggregates customer feedback from all channels (support tickets, NPS, community, interviews) and synthesizes it into actionable product and experience insights. Feeds Product department.

---

## Research/Analyst Layer

### Customer Intelligence Analyst
Monitors churn signals, satisfaction trends, and usage patterns across the customer base. Provides CS Director and Department Manager with early warning on at-risk accounts.

- **Inputs:** Product usage data, NPS scores, support ticket volume/sentiment, billing events
- **Outputs:** Customer health scores, churn risk alerts, cohort retention analysis, satisfaction trend reports
- **Cadence:** Weekly health dashboard + real-time churn risk alerts

---

## Workflow

### Inbound Support Flow
```
1. Ticket arrives (email, chat, in-app)
2. Responder classifies: billing / technical / product question / complaint
3. Common issue: Responder resolves using knowledge base → closes ticket
4. Complex issue: Escalation Handler activated
5. Cross-department needed: CS Director routes to Engineering or Product
6. Resolution documented → Knowledge Base Agent captures learnable content
7. CSAT survey sent → scores feed Customer Intelligence Analyst
```

### Onboarding Flow
```
1. New customer confirmed (from Sales)
2. Onboarding Agent creates onboarding plan (tailored by tier)
3. Welcome sequence begins: setup guide, check-in calls scheduled, milestone tracking
4. Day 14 health check: milestones hit? → continue / at risk? → Account Manager activated
5. Day 30: NPS survey deployed
6. Onboarding complete: handoff to Account Manager for ongoing relationship
```

### Churn Recovery Flow
```
1. Customer Intelligence Analyst flags at-risk account
2. CS Director reviews and assigns Account Manager
3. Account Manager initiates outreach within 24h
4. Discovery: what's the issue?
5. Resolution path: product gap → escalate to Product; billing issue → Finance; technical → Engineering
6. Follow-up at 7 and 30 days
7. Department Manager notified on any enterprise account churn risk
8. Human escalation if account is above revenue threshold
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Intercom / Zendesk | Responder, Escalation Handler | Support ticketing |
| HubSpot | Account Manager, CS Director | CRM, customer records |
| Delighted / Typeform | NPS Agent | NPS surveys |
| Notion | Knowledge Base Agent | Internal knowledge base |
| Loom | Onboarding Agent | Onboarding video guides |
| Slack / Discord | Community Manager | Community management |
| Mixpanel / Amplitude | Customer Intelligence Analyst | Usage analytics |
| ChurnZero / Gainsight | Account Manager | Customer health scoring |

---

## Escalation Path

```
Responder → Escalation Handler → CS Director Agent
Account Manager → CS Director Agent
CS Director Agent → CS Department Manager → Human Founders

Automatic human escalation triggers:
- Enterprise account flagged at-risk (above revenue threshold)
- Customer escalation becoming public (social media, review sites)
- Any refund or credit above approval threshold
- Any product issue affecting multiple customers simultaneously
- Expansion deal above threshold (route to Sales)
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `support/support-support-responder.md` | Responder |
| `support/support-analytics-reporter.md` | Customer Intelligence Analyst |
| `product/product-feedback-synthesizer.md` | Feedback Synthesizer |
| `specialized/report-distribution-agent.md` | CS Department Manager (reporting) |
