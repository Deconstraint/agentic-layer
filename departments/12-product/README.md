# Product Department

**Task Flow Type: B — Campaign/Project**
```
Opportunity / request → PM breaks into discovery + delivery workstreams → Clusters run in parallel → Validated → Human approves roadmap → Delivery Cluster executes → Engineering hands off build
```

Creative and iterative. Discovery and delivery run in overlapping cycles. Product decisions are evidence-based — no feature makes the roadmap without research validation.

---

## Department Manager

**Product Department Manager** — the accountability layer tracking the product development lifecycle and holding the Product department accountable to roadmap commitments, research quality, and stakeholder communication.

- **Owns:** Roadmap status dashboard (features in discovery/design/development/shipped), sprint and delivery health, research output quality checks, weekly product update to founders, department KPI dashboard (roadmap predictability, feature delivery rate, user satisfaction)
- **Reports to:** Human Founders — directly
- **Manages:** Product Manager Agent (Orchestrator)

## Orchestrator

**Product Manager Agent** — translates business goals and user needs into a prioritized roadmap, directs discovery and delivery work, and makes the tradeoff decisions that define what gets built.

```
Human Founders
  └── Product Dept Manager  ← tracks roadmap, audits research, reports status, escalates
        └── Product Manager Agent (Orchestrator)  ← defines roadmap, directs clusters, decides tradeoffs
              ├── Discovery Cluster (UX Researcher + User Interviewer + Feedback Synthesizer)
              ├── Delivery Cluster (PM + Sprint Lead + Roadmap Agent)
              ├── Behavioral Analyst (solo)
              ├── Market Validator (solo)
              └── Competitive Researcher (solo)
```

---

## Clusters

### Discovery Cluster
*Generates the evidence base that drives roadmap decisions.*

| Agent | Role |
|-------|------|
| **UX Researcher** | Designs and conducts usability studies, jobs-to-be-done research, and user journey analysis |
| **User Interviewer** | Conducts structured and semi-structured user interviews; synthesizes conversation themes |
| **Feedback Synthesizer** | Aggregates feedback from all sources (support tickets, NPS, sales calls, reviews) into prioritized insight |

**Cluster workflow:**
```
Research question → UX Researcher designs study → User Interviewer conducts interviews → Feedback Synthesizer adds quantitative signal → Discovery Cluster synthesizes → PM receives evidence package → Roadmap decision made
```

### Delivery Cluster
*Manages the execution of roadmap items from spec to shipping.*

| Agent | Role |
|-------|------|
| **Delivery PM** | Owns feature specs: writes PRDs, manages stakeholder alignment, tracks feature through build |
| **Sprint Lead** | Manages sprint execution: ticket breakdown, Engineering coordination, scope management |
| **Roadmap Agent** | Maintains and publishes the roadmap: prioritization, sequencing, dependency mapping |

**Cluster workflow:**
```
Feature approved → Delivery PM writes PRD → Sprint Lead breaks into tickets → Engineering builds → Delivery PM tracks progress → Launch → Roadmap Agent updates published roadmap
```

---

## Solo Agents

### Behavioral Analyst
Analyzes in-product behavior data: feature adoption, user flows, drop-off points, session patterns. Answers "what are users actually doing?" to complement qualitative research.

### Market Validator
Tests new product concepts and positioning with target market before building. Runs landing page tests, prototype tests, and market validation experiments to reduce build risk.

### Competitive Researcher
Maintains a detailed competitive product analysis: what competitors have built, where they're headed, and where the gaps are. Feeds the PM's roadmap strategy.

---

## Research/Analyst Layer

### Product Intelligence Analyst
Synthesizes usage data, feature requests, market signals, and user research into a continuous product intelligence feed. Provides PM with the data needed to prioritize ruthlessly.

- **Inputs:** Product analytics (Mixpanel/Amplitude), support ticket themes, NPS verbatims, sales feedback, market research from Research dept
- **Outputs:** Weekly product intelligence brief, feature request prioritization data, retention/engagement cohort analysis
- **Cadence:** Weekly brief + on-demand analysis for roadmap decisions

---

## Workflow

### Feature Discovery Flow
```
1. PM identifies potential opportunity (from intelligence feed, founder input, or market signal)
2. Discovery Cluster activates:
   - UX Researcher: study design
   - User Interviewer: 5-8 interviews
   - Feedback Synthesizer: quantitative data pull
3. Discovery Cluster synthesizes findings
4. Behavioral Analyst adds product usage context
5. Market Validator tests concept if needed
6. PM produces feature brief with evidence summary
7. Product Dept Manager reviews research completeness
8. Human approves roadmap addition
```

### Feature Delivery Flow
```
1. Feature approved for roadmap
2. Delivery PM writes PRD (problem, success metrics, requirements, non-requirements)
3. Sprint Lead breaks into Engineering tickets
4. Engineering Build Cluster picks up (Engineering dept)
5. Delivery PM monitors progress, manages scope
6. QA in Engineering validates
7. PM reviews final build against PRD success metrics
8. Launch → Behavioral Analyst monitors adoption
9. Product Intelligence Analyst reports outcomes at Day 14, Day 60
```

### Roadmap Prioritization Flow
```
1. Roadmap Agent maintains full feature backlog
2. Product Intelligence Analyst produces prioritization data (impact, effort, evidence strength)
3. PM runs prioritization using scoring framework
4. Competitive Researcher validates against competitive landscape
5. PM produces proposed roadmap update
6. Product Dept Manager reviews
7. Human approves roadmap before publication
8. Roadmap Agent publishes updated roadmap to stakeholders
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Linear / Jira | Sprint Lead, Delivery PM | Ticket management |
| Notion / Confluence | Delivery PM, Roadmap Agent | PRDs, roadmap documentation |
| Maze / UserTesting | UX Researcher | Usability testing |
| Dovetail | User Interviewer, Feedback Synthesizer | Research synthesis |
| Mixpanel / Amplitude | Behavioral Analyst | Product analytics |
| Figma | UX Researcher | Prototypes for validation |
| Typeform | Market Validator | Validation surveys |
| Canny | Feedback Synthesizer | Feature request tracking |
| Productboard | Roadmap Agent | Roadmap management |

---

## Escalation Path

```
Discovery Cluster → Product Manager Agent
Delivery Cluster → Product Manager Agent
Solo Agents → Product Manager Agent
PM Agent → Product Dept Manager → Human Founders

Automatic human escalation triggers:
- Any roadmap change that affects committed Engineering work
- Any feature that requires significant scope or budget decision
- Any product pivot or strategic direction change
- Any user research finding that contradicts current product strategy
- Every roadmap update before publishing to stakeholders
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `product/product-feedback-synthesizer.md` | Feedback Synthesizer |
| `product/product-sprint-prioritizer.md` | Roadmap Agent, Sprint Lead |
| `product/product-trend-researcher.md` | Competitive Researcher, Market Validator |
| `product/product-behavioral-nudge-engine.md` | Behavioral Analyst |
| `design/design-ux-researcher.md` | UX Researcher |
| `design/design-ux-architect.md` | UX Researcher, Delivery PM |
| `project-management/project-management-experiment-tracker.md` | Market Validator |
| `testing/testing-reality-checker.md` | Product Intelligence Analyst |
