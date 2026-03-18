# Deconstraint Agent OS

> The complete AI-native business operating system. Every department. Every role. Fully templatized and deployable.

---

## What This Is

A structured framework for replacing or augmenting every business function with AI agents. Agents aren't just digital employees — they're specialized workers, cluster teams, orchestrators, and accountability managers that together run an entire business function.

When you deploy a department, you inject:
1. The **department template** (who these agents are and how they work)
2. The **company context** (who they're working for)
3. The **credentials** (what tools they're authorized to use)

The result: a fully operational AI department that runs autonomously, escalates intelligently, and learns over time.

---

## The Layered Model

> **Not "who is this agent?" — but "what problem does this agent solve?"**

Every department has four layers:

### Layer 1 — Department Manager Agent
The **operator and accountability layer**. Monitors department health, tracks task completion, checks agent outputs for quality, runs daily/weekly status, and escalates problems directly to humans. This agent reports to humans.

- **Owns:** Reporting, KPI dashboard, output quality gates, escalation to human
- **Reports to:** Human founders — directly
- **Manages:** The Orchestrator Agent

### Layer 2 — Orchestrator Agent
The **director and routing layer**. Receives work, decides which cluster or solo handles it, synthesizes outputs, and makes technical/strategic decisions within the department.

- **Owns:** Task routing, work synthesis, within-department decisions
- **Reports to:** Department Manager

### Layer 3 — Cluster Agents
**Multi-agent workflows** that execute a complete outcome together. Clusters are small teams — 2-4 agents — built around a single outcome (e.g., Revenue Engine, Build Cluster, Content Production).

### Layer 4 — Solo Agents
**Narrow specialists** with one job. Fully autonomous within their lane. They receive tasks, execute, and report back.

```
Human Founders
  └── Department Manager Agent   ← monitors, reports, escalates
        └── Orchestrator Agent   ← routes, synthesizes, directs
              ├── Cluster A      ← multi-agent workflow
              │     ├── Agent 1
              │     └── Agent 2
              ├── Cluster B
              └── Solo Agent     ← narrow specialist
```

---

## Architecture

```
agentic-layer/
├── README.md               ← This file — full system overview
├── COMPANY.md              ← Company context template (injected at onboarding)
├── AGENT_TEMPLATE.md       ← How every agent role is structured
│
└── departments/
    ├── 01-executive/
    ├── 02-finance/
    ├── 03-marketing/
    ├── 04-sales/
    ├── 05-engineering/
    ├── 06-operations/
    ├── 07-customer-success/
    ├── 08-hr-people/
    ├── 09-legal-compliance/
    ├── 10-research-intel/
    ├── 11-content-media/
    └── 12-product/
```

Each department folder:
```
departments/XX-name/
├── README.md                     ← Department spec (flows, tools, escalation)
├── department-manager/
│   └── SOUL.md                   ← Accountability layer
├── [orchestrator]/
│   └── SOUL.md                   ← Director/routing layer
├── [cluster-agent]/
│   └── SOUL.md                   ← Cluster worker
└── [solo-agent]/
    └── SOUL.md                   ← Narrow specialist
```

---

## The 12 Departments

### 01 — Executive
**Flow:** Decision/Direction | **Orchestrator:** CEO Agent

```
Human Founders
  └── Executive Dept Manager
        └── CEO Agent
              ├── Strategy Cluster
              │     ├── COO Agent
              │     ├── Strategy Analyst
              │     └── Board Reporter
              ├── Communications Agent
              ├── Intelligence Briefing Agent
              └── [Research] Market Intelligence Analyst
```

---

### 02 — Finance
**Flow:** Request/Response | **Orchestrator:** CFO Agent

```
Human Founders
  └── Finance Dept Manager
        └── CFO Agent
              ├── Reporting Cluster
              │     ├── Controller
              │     ├── AP/AR Agent
              │     └── Payroll Agent
              ├── Financial Analyst
              ├── Tax Agent
              ├── Investor Relations
              └── [Research] Financial Intelligence Analyst
```

---

### 03 — Marketing
**Flow:** Campaign/Project | **Orchestrator:** CMO Agent

```
Human (Nathan)
  └── Marketing Dept Manager
        └── CMO Agent
              ├── Growth Cluster
              │     ├── SEO Specialist
              │     ├── Paid Media Strategist
              │     ├── Email Marketer
              │     └── Analytics Agent
              ├── Content Cluster
              │     ├── Content Writer
              │     ├── Content Editor
              │     └── Content Distributor
              ├── Brand Guardian
              ├── Social Media Strategist
              ├── [Research] Market Research Analyst
              └── [Research] Competitor Intel Agent
```

---

### 04 — Sales
**Flow:** Continuous Pipeline | **Orchestrator:** VP Sales Agent

```
Human Founders
  └── Sales Dept Manager
        └── VP Sales Agent
              ├── Revenue Cluster
              │     ├── Prospector
              │     ├── Qualifier
              │     ├── Account Executive
              │     └── Follow-up Agent
              ├── Pipeline Cluster
              │     ├── CRM Ops Agent
              │     └── Forecasting Agent
              ├── Sales Engineer
              ├── Partnerships Agent
              └── [Research] Sales Intelligence Analyst
```

---

### 05 — Engineering
**Flow:** Sequential/Gated | **Orchestrator:** CTO Agent

```
Human (Travis/Britton)
  └── Engineering Dept Manager
        └── CTO Agent
              ├── Build Cluster
              │     ├── Architect
              │     ├── Frontend Developer
              │     ├── Backend Developer
              │     └── QA Engineer
              ├── Infra Cluster
              │     ├── DevOps Engineer
              │     ├── Security Engineer
              │     └── Monitoring Agent
              ├── AI Engineer
              ├── Technical Writer
              ├── Mobile Builder
              └── [Research] Tech Research Agent
```

---

### 06 — Operations
**Flow:** Continuous Pipeline | **Orchestrator:** COO Agent

```
Human Founders
  └── Operations Dept Manager
        └── COO Agent
              ├── Execution Cluster
              │     ├── Project Manager
              │     ├── Process Analyst
              │     └── Vendor Manager
              ├── Systems Cluster
              │     ├── Workflow Architect
              │     └── Infrastructure Maintainer
              ├── Logistics Agent
              ├── Documentation Agent
              └── [Research] Operations Analyst
```

---

### 07 — Customer Success
**Flow:** Continuous Pipeline | **Orchestrator:** CS Director Agent

```
Human Founders
  └── CS Dept Manager
        └── CS Director Agent
              ├── Support Cluster
              │     ├── Responder
              │     ├── Escalation Handler
              │     └── Knowledge Base Agent
              ├── Retention Cluster
              │     ├── Onboarding Agent
              │     ├── NPS Agent
              │     └── Account Manager
              ├── Community Manager
              ├── Feedback Synthesizer
              └── [Research] Customer Intelligence Analyst
```

---

### 08 — HR / People
**Flow:** Request/Response | **Orchestrator:** People Lead Agent

```
Human Founders
  └── HR Dept Manager
        └── People Lead Agent
              ├── Recruiting Cluster
              │     ├── Sourcer
              │     ├── Screener
              │     ├── Interviewer Coordinator
              │     └── Offer Agent
              ├── Culture Cluster
              │     ├── Onboarding Agent
              │     ├── Engagement Agent
              │     └── L&D Agent
              ├── Payroll Agent
              ├── Compliance Agent
              └── [Research] Talent Market Analyst
```

---

### 09 — Legal / Compliance
**Flow:** Request/Response | **Orchestrator:** General Counsel Agent

```
Human Founders
  └── Legal Dept Manager
        └── General Counsel Agent
              ├── Contracts Cluster
              │     ├── Drafter
              │     ├── Reviewer
              │     └── Contract Tracker
              ├── Compliance Cluster
              │     ├── Policy Agent
              │     ├── Audit Agent
              │     └── Risk Agent
              ├── IP Agent
              ├── Privacy Agent
              ├── Regulatory Agent
              └── [Research] Legal Intelligence Analyst
```

---

### 10 — Research & Intelligence
**Flow:** Intelligence/Async | **Orchestrator:** Research Director Agent

```
Human Founders
  └── Research Dept Manager
        └── Research Director Agent
              ├── Market Intel Cluster
              │     ├── Market Researcher
              │     ├── Market Analyst
              │     └── Report Writer
              ├── Competitive Intel Cluster
              │     ├── Competitive Monitor
              │     ├── Competitive Analyst
              │     └── Competitive Briefer
              ├── Data Engineer
              ├── Survey Agent
              └── Trend Spotter
```

*Note: This entire department serves as the Research Layer for all other departments.*

---

### 11 — Content & Media
**Flow:** Campaign/Project | **Orchestrator:** Content Director Agent

```
Human Founders
  └── Content Dept Manager
        └── Content Director Agent
              ├── Production Cluster
              │     ├── Writer
              │     ├── Editor
              │     ├── Designer
              │     └── Publisher
              ├── Distribution Cluster
              │     ├── SEO Distribution Agent
              │     ├── Social Distribution Agent
              │     ├── Email Distribution Agent
              │     └── Syndication Agent
              ├── Video Producer
              ├── Podcast Agent
              ├── Visual Storyteller
              └── [Research] Content Intelligence Analyst
```

---

### 12 — Product
**Flow:** Campaign/Project | **Orchestrator:** Product Manager Agent

```
Human Founders
  └── Product Dept Manager
        └── Product Manager Agent
              ├── Discovery Cluster
              │     ├── UX Researcher
              │     ├── User Interviewer
              │     └── Feedback Synthesizer
              ├── Delivery Cluster
              │     ├── Delivery PM
              │     ├── Sprint Lead
              │     └── Roadmap Agent
              ├── Behavioral Analyst
              ├── Market Validator
              ├── Competitive Researcher
              └── [Research] Product Intelligence Analyst
```

---

## Task Flow Types

### Type A — Request/Response
*(Finance, Legal, HR)*
```
Human request → Dept Manager logs → Orchestrator routes → Solo or Cluster → Output reviewed → Human approves
```
Structured, compliance-sensitive. Every output validated before leaving department.

### Type B — Campaign/Project
*(Marketing, Content, Product)*
```
Brief → Dept Manager logs → Orchestrator breaks into workstreams → Clusters run in parallel → Orchestrator assembles → Human approves → Launch
```
Creative, iterative. Clusters can loop back. Human approval before any external action.

### Type C — Continuous Pipeline
*(Sales, Customer Success, Operations)*
```
Trigger → Orchestrator routes → Cluster executes → Dept Manager monitors → Logs to system → Escalates if needed → Loop
```
Always running. Event-driven. Dept Manager watches for stalls and anomalies.

### Type D — Sequential/Gated
*(Engineering)*
```
Spec → Orchestrator directs → Architect → Build Cluster → QA gate → DevOps ships → Dept Manager confirms gates cleared → Monitor
```
Each stage gates the next. Dept Manager verifies gates were actually passed.

### Type E — Intelligence/Async
*(Research & Intel)*
```
Question / schedule → Orchestrator assigns → Intel Cluster pulls data → Analyst synthesizes → Report → Dept Manager verifies delivery → Distributed to consuming depts
```
Async. Runs on schedule and on-demand. Dept Manager tracks delivery.

---

## Agent File Structure

Every agent (Department Manager, Orchestrator, cluster member, or solo) has these files:

```
departments/[DEPT]/[ROLE]/
├── SOUL.md         Who they are. Personality, voice, values.
├── IDENTITY.md     Name, title, scope, reporting line, what they own.
├── SKILLS.md       What they can do. Linked to tools in TOOLBOX.md.
├── KEYS.md         Which credentials they're authorized to access.
├── WORKFLOWS.md    Step-by-step playbooks. One workflow per task type.
├── HANDOFFS.md     Who they escalate to. Who they hand off to. When.
└── MEMORY.md       Persistent context. Learns over time.
```

*Current state: SOUL.md placeholder written for all agents. Full file expansion in progress.*

---

## Department Build Status

| # | Department | Dept Manager | Orchestrator | Clusters | Solos | Research Layer | Status |
|---|---|---|---|---|---|---|---|
| 01 | Executive | ✅ | CEO ✅ | Strategy ✅ | Comms, Intel ✅ | Mkt Intel ✅ | SOUL.md complete |
| 02 | Finance | ✅ | CFO ✅ | Reporting ✅ | Analyst, Tax, IR ✅ | Fin Intel ✅ | SOUL.md complete |
| 03 | Marketing | ✅ | CMO ✅ | Growth, Content ✅ | Brand, Social ✅ | Mkt Research, Comp Intel ✅ | SOUL.md complete |
| 04 | Sales | ✅ | VP Sales ✅ | Revenue, Pipeline ✅ | SE, Partnerships ✅ | Sales Intel ✅ | SOUL.md complete |
| 05 | Engineering | ✅ | CTO ✅ | Build, Infra ✅ | AI, TW, Mobile ✅ | Tech Research ✅ | SOUL.md complete |
| 06 | Operations | ✅ | COO ✅ | Execution, Systems ✅ | Logistics, Docs ✅ | Ops Analyst ✅ | SOUL.md complete |
| 07 | Customer Success | ✅ | CS Director ✅ | Support, Retention ✅ | Community, Feedback ✅ | Cust Intel ✅ | SOUL.md complete |
| 08 | HR / People | ✅ | People Lead ✅ | Recruiting, Culture ✅ | Payroll, Compliance ✅ | Talent Mkt ✅ | SOUL.md complete |
| 09 | Legal / Compliance | ✅ | Gen Counsel ✅ | Contracts, Compliance ✅ | IP, Privacy, Regulatory ✅ | Legal Intel ✅ | SOUL.md complete |
| 10 | Research & Intel | ✅ | Research Dir ✅ | Market Intel, Comp Intel ✅ | Data, Survey, Trend ✅ | IS the research layer ✅ | SOUL.md complete |
| 11 | Content & Media | ✅ | Content Dir ✅ | Production, Distribution ✅ | Video, Podcast, Visual ✅ | Content Intel ✅ | SOUL.md complete |
| 12 | Product | ✅ | PM Agent ✅ | Discovery, Delivery ✅ | Behavioral, Validator, Comp ✅ | Product Intel ✅ | SOUL.md complete |

**Total agents across all departments:** ~130 agent roles

**Next phase:** Expand SOUL.md stubs into full agent files (IDENTITY, SKILLS, KEYS, WORKFLOWS, HANDOFFS, MEMORY)

---

## Design Principles

### Every department has a research layer
No department operates without intelligence. Every orchestrator has access to at least one analyst/researcher whose job is to answer "what's actually true about our situation?"

### Two leadership roles per department
- **Department Manager** = operator/accountability layer (reports to humans)
- **Orchestrator** = director/routing layer (manages the work)

Smaller departments can merge these roles. Larger departments (Engineering, Marketing, Operations, Sales) keep them separate.

### Website development is a cross-department project
Not its own department. It pulls from:
- Engineering (Frontend, Backend, DevOps)
- Content/Media (Copy, SEO)
- Product (UX Researcher, UX Architect)
- Marketing (SEO, Analytics)

### Human approval gates are non-negotiable
- All external communications (emails, posts, press)
- All financial decisions above threshold
- All legal signatures
- All contract executions
- All product roadmap updates

---

## Onboarding a Department

1. Copy the department folder
2. Fill in `COMPANY.md` with client context
3. Set credentials in `KEYS.md` for each agent
4. Inject `COMPANY.md` into each agent's context
5. Configure Department Manager reporting channel (Telegram / Slack / email)
6. Run the Department Manager agent — it activates the Orchestrator
7. Department is operational

---

## What Makes This Different

| Everyone else | Deconstraint Agent OS |
|---|---|
| Task-based agents | Department OS — runs a whole function |
| Requires engineering to deploy | Templatized — fill and deploy |
| No learning layer | RSI built in |
| Single agent = single tool | Agents get exactly the tools they need |
| No oversight model | Department Manager layer — humans always informed |
| Org chart mirrors human org | Layered model: Manager → Orchestrator → Clusters → Solos |

---

*Built by Deconstraint. The AI-native business operating system.*
