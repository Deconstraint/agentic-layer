# Deconstraint Agent OS

> The complete AI-native business operating system. Every department. Every role. Fully templatized and deployable.

---

## What This Is

A structured framework for replacing or augmenting every business function with AI agents. Agents aren't just digital employees — they're specialized workers, cluster teams, and orchestrators that together run an entire business function.

When you deploy a department, you inject:
1. The **department template** (who these agents are and how they work)
2. The **company context** (who they're working for)
3. The **credentials** (what tools they're authorized to use)

The result: a fully operational AI department that runs autonomously, escalates intelligently, and learns over time.

---

## The Layered Model

> **Not "who is this agent?" — but "what problem does this agent solve?"**

Agents inside departments come in three types:

### 1. Solo Agents
Narrow scope. One job. Fully autonomous within their lane.
- SEO Specialist, DevOps, Bookkeeper, Email Marketer
- They receive tasks, execute, report back
- Think: specialist contractor

### 2. Cluster Agents
Multiple agents working together on one function. The cluster IS the workflow.
- **Content Engine** → Researcher + Writer + Editor + Publisher
- **Revenue Engine** → Prospector + Qualifier + Closer + Follow-up
- **Build Engine** → Architect + Developer + QA + DevOps
- Think: a small team assigned to one outcome

### 3. Orchestrator Agents
Department managers. Route work to the right solo or cluster. Synthesize outputs. Escalate to humans.
- CMO, CTO, CFO, COO equivalents
- They don't do the work — they direct it
- Think: department head

```
Human
  └── Orchestrator Agent (Department Head)
        ├── Solo Agent (narrow task)
        ├── Solo Agent (narrow task)
        └── Cluster (multi-agent workflow)
              ├── Agent A
              ├── Agent B
              └── Agent C
```

---

## Architecture

```
agent-os/
├── COMPANY.md              ← Company context template (injected at onboarding)
├── ORCHESTRATOR.md         ← Master orchestrator spec (Zeus/ARES)
├── DEPARTMENT_TEMPLATE.md  ← How every department is structured
├── AGENT_TEMPLATE.md       ← How every agent role is structured
│
├── departments/
│   ├── 01-executive/
│   ├── 02-finance/
│   ├── 03-marketing/       ← IN PROGRESS (Nathan's domain)
│   ├── 04-sales/
│   ├── 05-engineering/     ← IN PROGRESS (Travis + Britton's domain)
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

| # | Department | Orchestrator | Clusters | Solos | Task Flow |
|---|---|---|---|---|---|
| 1 | **Executive** | CEO | Strategy Cluster | Board Reporter, Comms | Decisions |
| 2 | **Finance** | CFO | Reporting Cluster | Bookkeeper, AP/AR, Payroll | Request/Response |
| 3 | **Marketing** | CMO | Growth Cluster, Content Cluster | SEO, Email, Social | Campaign/Project |
| 4 | **Sales** | VP Sales | Revenue Cluster | CRM Ops, Follow-up | Continuous Pipeline |
| 5 | **Engineering** | CTO | Build Cluster | DevOps, Security | Sequential/Gated |
| 6 | **Operations** | COO | Project Cluster | Vendor, Logistics | Continuous Pipeline |
| 7 | **Customer Success** | CS Director | Support Cluster | Onboarding, NPS | Continuous Pipeline |
| 8 | **HR/People** | People Lead | Recruiting Cluster | Culture, Payroll | Request/Response |
| 9 | **Legal/Compliance** | General Counsel | Contracts Cluster | Privacy, IP | Request/Response |
| 10 | **Research/Intel** | Research Lead | Intel Cluster | Data Analyst | Intelligence/Async |
| 11 | **Content/Media** | Content Director | Production Cluster | Video, Podcast | Campaign/Project |
| 12 | **Product** | Product Manager | UX Cluster | Roadmap, User Research | Campaign/Project |

---

## Task Flow Types

Each department runs a fundamentally different type of workflow:

### Type A — Request/Response
*(Finance, Legal, HR)*
```
Human request → Orchestrator → Solo or Cluster → Output → Human review
```
Structured, compliance-sensitive. Output validated before leaving department.

### Type B — Campaign/Project
*(Marketing, Content, Product)*
```
Brief → Orchestrator breaks into workstreams → Clusters run in parallel → Orchestrator assembles → Review
```
Creative, iterative. Clusters can loop back. Orchestrator synthesizes.

### Type C — Continuous Pipeline
*(Sales, Customer Success, Operations)*
```
Trigger → Cluster executes → Logs to system → Escalates if needed → Loop
```
Always running. Event-driven. Output feeds into CRM/systems.

### Type D — Sequential/Gated
*(Engineering)*
```
Spec → Architect → Build Cluster → QA gate → DevOps ships → Monitor
```
Each stage must pass before next begins. No skipping gates.

### Type E — Intelligence/Async
*(Research, Competitive Intel)*
```
Question → Intel Cluster pulls data → Analyst synthesizes → Report → Distribution to other depts
```
Async. Output feeds other departments. Runs on schedule or on-demand.

---

## Agent File Structure

Every agent (solo or within a cluster) has these files:

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
5. Run the orchestrator agent
6. Department is operational

---

## The Master Orchestrator

Above all departments sits the **Master Orchestrator** (Zeus/ARES):
- Routes tasks to the right department
- Handles cross-department coordination  
- Runs the RSI learning loop (learns from corrections)
- Monitors department health
- Escalates to human when needed

---

## What Makes This Different

| Everyone else | Deconstraint Agent OS |
|---|---|
| Task-based agents (do one thing) | Department OS (run a whole function) |
| Requires engineering to deploy | Templatized — fill and deploy |
| No learning layer | RSI built in — agents improve over time |
| Org chart = human org chart | Layered model — solos, clusters, orchestrators |
| One agent = one tool | Agents get exactly the tools they need |

---

## Status

| Department | Orchestrator | Clusters | Solos | Status |
|---|---|---|---|---|
| Engineering | CTO ✅ | Build Cluster 🔄 | DevOps 📋 | In Progress |
| Marketing | CMO ✅ | Growth/Content Cluster 🔄 | SEO/Email 📋 | In Progress |
| All others | 📋 | 📋 | 📋 | Planned |

---

*Built by Deconstraint. The AI-native business layer.*
