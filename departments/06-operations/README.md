# Operations Department

**Task Flow Type: C — Continuous Pipeline**
```
Trigger (project, request, recurring task) → Execution Cluster manages → Systems Cluster supports → Log + escalate → Loop
```

Operations never stops. Every cross-department project, vendor relationship, and business process flows through here.

---

## Department Manager

**Operations Department Manager** — the accountability layer tracking every active project, vendor commitment, and operational process. Monitors project health, surfaces blockers to founders, verifies vendor renewals are handled, and ensures the COO's plans are executing — not just planned.

- **Owns:** Project health dashboard (green/yellow/red), vendor renewal calendar with advance alerts, cross-department coordination status, weekly ops digest to founders, department KPI reporting (on-time rate, SLA compliance)
- **Reports to:** Human Founders — directly
- **Manages:** COO Agent (Orchestrator)

## Orchestrator

**COO Agent** — runs the operational backbone of the organization. Translates CEO strategy into executable plans, manages cross-department coordination, and ensures nothing falls through the cracks.

```
Human Founders
  └── Operations Department Manager  ← monitors projects, tracks vendors, reports, escalates
        └── COO Agent (Orchestrator)  ← plans, routes, coordinates, decides
              ├── Execution Cluster (Project Manager + Process Analyst + Vendor Manager)
              ├── Systems Cluster (Workflow Architect + Infrastructure Maintainer)
              ├── Logistics Agent (solo)
              └── Documentation Agent (solo)
```

---

## Clusters

### Execution Cluster
*Manages all active projects, vendor relationships, and process execution.*

| Agent | Role |
|-------|------|
| **Project Manager** | Owns active project timelines, milestones, blockers, and cross-department dependencies |
| **Process Analyst** | Documents, analyzes, and improves business processes. Finds bottlenecks and inefficiencies |
| **Vendor Manager** | Manages vendor relationships, contracts, renewals, and performance |

**Cluster workflow:**
```
New project/initiative → Project Manager creates plan + assigns owners → Process Analyst checks for process fit → Vendor Manager confirms required vendor capacity → Execution begins → PM monitors + escalates blockers
```

### Systems Cluster
*Designs and maintains the operational infrastructure that keeps the business running.*

| Agent | Role |
|-------|------|
| **Workflow Architect** | Designs automation workflows, system integrations, and operational playbooks |
| **Infrastructure Maintainer** | Keeps operational tools running: SaaS subscriptions, accounts, permissions, integrations |

**Cluster workflow:**
```
Process gap or tool request → Workflow Architect designs solution → Infrastructure Maintainer implements + maintains → Process Analyst validates improvement
```

---

## Solo Agents

### Logistics Agent
Handles physical and digital logistics: shipping, vendor procurement, office operations (if applicable), event coordination, and any operational task with external dependencies.

### Documentation Agent
Owns the company's operational knowledge base. Ensures every process, runbook, and standard operating procedure is written, current, and accessible.

---

## Research/Analyst Layer

### Operations Analyst
Monitors operational efficiency across the organization. Tracks key operational metrics, identifies bottlenecks, and provides the COO with data-driven insight for process improvement.

- **Inputs:** Project completion rates, cycle times, vendor SLAs, tool usage, department feedback
- **Outputs:** Weekly operations dashboard, bottleneck reports, efficiency improvement recommendations
- **Cadence:** Weekly ops review + on-demand analysis

---

## Workflow

### New Project Flow
```
1. Initiative arrives from CEO/Executive (or any department head)
2. COO Agent scopes: objectives, timeline, resources, departments involved
3. Project Manager creates project plan in Linear/Notion
4. Cross-department dependencies mapped and owners assigned
5. Process Analyst reviews for process fit
6. Execution begins — PM tracks daily
7. Weekly status to COO → COO to CEO
8. Blockers escalated immediately
9. Project close: lessons captured by Documentation Agent
```

### Process Improvement Flow
```
1. Operations Analyst identifies inefficiency or bottleneck
2. Process Analyst documents current state
3. Workflow Architect designs improved process
4. COO approves change
5. Infrastructure Maintainer implements (if tool change needed)
6. Process Analyst monitors adoption and impact
7. Documentation Agent updates runbooks
```

### Vendor Management Flow
```
1. Vendor Manager tracks renewal dates and SLAs
2. 60 days before renewal: evaluation triggered
3. Vendor Manager assesses value vs. alternatives
4. Recommendation to COO: renew / renegotiate / replace
5. Human approves any contract > threshold
6. Vendor Manager executes
```

### Cross-Department Coordination Flow
```
1. Multi-department initiative arrives
2. COO maps which departments are involved and who owns what
3. Project Manager sets up shared project space
4. Each department head gets their workstream
5. COO runs weekly cross-dept sync (async digest or live)
6. Blockers escalated through department heads to COO
7. COO resolves or escalates to CEO
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Linear / Asana | Project Manager | Project tracking |
| Notion | Documentation Agent, COO | Knowledge base, runbooks |
| Slack / Telegram | All | Communication, alerts |
| Zapier / Make | Workflow Architect | Automation workflows |
| Google Workspace | All | Docs, sheets, calendar |
| Airtable | Vendor Manager, Process Analyst | Vendor tracking, process docs |
| Loom | Documentation Agent | Process walkthroughs |
| 1Password | Infrastructure Maintainer | Credential management |
| Stripe / Recurly | Vendor Manager | Subscription tracking |

---

## Escalation Path

```
Execution Cluster → COO Agent
Systems Cluster → COO Agent
Solo Agents → COO Agent
COO Agent → CEO Agent → Human Founders

Automatic human escalation triggers:
- Vendor contract > $X threshold
- Project significantly off-track (>20% timeline slip)
- Cross-department conflict unresolvable at department level
- Budget overrun on any project
- Any new tool/SaaS procurement > $500/month
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `specialized/specialized-workflow-architect.md` | Workflow Architect |
| `support/support-infrastructure-maintainer.md` | Infrastructure Maintainer |
| `project-management/project-manager-senior.md` | Project Manager |
| `project-management/project-management-project-shepherd.md` | Project Manager |
| `project-management/project-management-studio-operations.md` | COO Agent |
| `testing/testing-workflow-optimizer.md` | Process Analyst |
| `specialized/data-analytics-reporter.md` | Operations Analyst |
