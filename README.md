# Deconstraint Agent OS

> The complete AI-native business operating system. Every department. Every role. Fully templatized and deployable.

---

## What This Is

A structured framework for replacing or augmenting every business function with AI agents. Each agent has a narrow scope, a defined identity, a specific skill set, access to only the tools it needs, and clear handoff protocols to other agents.

When you deploy a department, you inject:
1. The **department template** (who these agents are and how they work)
2. The **company context** (who they're working for)
3. The **credentials** (what tools they're authorized to use)

The result: a fully operational AI department that runs autonomously, escalates intelligently, and learns over time.

---

## Architecture

```
agent-os/
├── COMPANY.md              ← Company context template (injected at onboarding)
├── ORCHESTRATOR.md         ← Zeus/ARES — master orchestrator spec
├── DEPARTMENT_TEMPLATE.md  ← How every department is structured
├── AGENT_TEMPLATE.md       ← How every agent role is structured
│
├── departments/
│   ├── 01-executive/
│   ├── 02-finance/
│   ├── 03-marketing/       ← BUILT (Nathan's domain)
│   ├── 04-sales/
│   ├── 05-engineering/     ← BUILT (Travis + Britton's domain)
│   ├── 06-operations/
│   ├── 07-customer-success/
│   ├── 08-hr-people/
│   ├── 09-legal-compliance/
│   ├── 10-research-intel/
│   ├── 11-content-media/
│   └── 12-product/
│
└── tools/
    ├── TOOLBOX.md          ← Master tool registry
    └── KEYS_TEMPLATE.md    ← Credential access patterns
```

---

## The 12 Departments

| # | Department | Manager Agent | Key Workers | Task Type |
|---|---|---|---|---|
| 1 | **Executive** | CEO Agent | COO, Strategy | Decisions, vision, board reporting |
| 2 | **Finance** | CFO Agent | Accountant, AP/AR, Analyst | Numbers, compliance, payroll |
| 3 | **Marketing** | CMO Agent | Brand, Content, SEO, Paid, Email | Campaigns, content, growth |
| 4 | **Sales** | VP Sales Agent | SDR, AE, Sales Ops | Pipeline, outreach, closing |
| 5 | **Engineering** | CTO Agent | Architect, Devs, QA, DevOps | Code, infra, deployment |
| 6 | **Operations** | COO Agent | Project Mgr, Process, Vendor | Execution, logistics, ops |
| 7 | **Customer Success** | CS Manager | Support, Onboarding, Account | Retention, tickets, NPS |
| 8 | **HR/People** | People Lead | Recruiter, Onboarding, Culture | Hiring, culture, payroll |
| 9 | **Legal/Compliance** | General Counsel | Contracts, IP, Privacy | Risk, compliance, legal |
| 10 | **Research/Intel** | Research Lead | Analyst, Competitive Intel | Market data, insights |
| 11 | **Content/Media** | Content Director | Writer, Designer, Video, Pod | Creation, production |
| 12 | **Product** | Product Manager | UX, Roadmap, User Research | Features, roadmap, UX |

---

## How Departments Work

Each department has a **unique task flow** based on what kind of work it does:

### Task Flow Types

**Type A — Request/Response** (Finance, Legal, HR)
```
Human request → Manager Agent → Worker Agent → Output → Human review
```
Structured, compliance-sensitive. Manager validates before output leaves department.

**Type B — Campaign/Project** (Marketing, Content, Product)
```
Brief → Manager breaks into tasks → Workers execute in parallel → Manager assembles → Review
```
Creative, iterative. Workers can loop back. Manager synthesizes.

**Type C — Continuous/Pipeline** (Sales, Customer Success, Operations)
```
Trigger → Worker executes → Logs to CRM/system → Escalates if needed → Loop
```
Always running. Triggered by events (new lead, new ticket, new order).

**Type D — Build/Deploy** (Engineering)
```
Spec → Architect designs → Devs build → QA tests → DevOps ships → Monitor
```
Sequential with gates. Each stage must pass before next begins.

**Type E — Intelligence/Research** (Research, Competitive Intel)
```
Question → Research Agent pulls data → Analyst synthesizes → Report → Distribution
```
Async. Output feeds other departments.

---

## Agent File Structure

Every agent in every department has these files:

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

---

## Onboarding a Department

1. Copy the department folder
2. Fill in `COMPANY.md` with client context
3. Set credentials in `KEYS.md` for each agent
4. Inject `COMPANY.md` into each agent's context
5. Run the department manager agent
6. Department is operational

---

## The Orchestrator Layer

Above all departments sits the **Orchestrator** (Zeus/ARES):
- Routes tasks to the right department
- Handles cross-department coordination
- Escalates to human when needed
- Monitors department health
- Runs the RSI learning loop

---

## Status

| Department | Status |
|---|---|
| Engineering | 🔄 In Progress |
| Marketing | 🔄 In Progress |
| All others | 📋 Planned |

---

*Built by Deconstraint. The AI-native business layer.*
