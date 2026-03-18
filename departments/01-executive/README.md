# Executive Department

**Task Flow Type: A — Decision/Direction**
```
Stakeholder input / market signal → CEO synthesizes → Strategy Cluster frames options → CEO decides → Departments execute
```

The Executive department sets direction, makes decisions, and ensures alignment across all departments. It does not execute — it governs.

---

## Department Manager

**Executive Department Manager** — the accountability layer between human founders and the Executive department. Monitors CEO Agent output quality, tracks task completion, runs daily status digests, and escalates problems directly to founders. This agent watches the watchers.

- **Owns:** Daily status reporting, output quality checks on briefings/memos/comms, escalation to human, department health dashboard
- **Reports to:** Human Founders (Travis / Nathan / Britton) — directly
- **Manages:** CEO Agent (Orchestrator)

## Orchestrator

**CEO Agent** — routes all strategic inputs, sets priorities, and approves cross-department initiatives. The CEO Agent is the final escalation point before a human founder.

```
Human Founders
  └── Executive Department Manager  ← monitors, tracks, reports, escalates
        └── CEO Agent (Orchestrator)  ← routes work, directs, decides
              ├── Strategy Cluster (COO + Strategy Analyst + Board Reporter)
              ├── Communications Agent (solo)
              └── Intelligence Briefing Agent (solo)
```

---

## Clusters

### Strategy Cluster
*Frames options, models scenarios, prepares decisions for the CEO.*

| Agent | Role |
|-------|------|
| **COO Agent** | Operationalizes CEO decisions — turns strategy into execution plans |
| **Strategy Analyst** | Researches options, models outcomes, writes strategy memos |
| **Board Reporter** | Produces board decks, investor updates, quarterly narratives |

**Cluster workflow:**
```
CEO poses strategic question → Strategy Analyst researches → COO stress-tests operationally → Board Reporter formats for stakeholders → CEO decides
```

---

## Solo Agents

### Communications Agent
Owns all external CEO communications — press releases, LinkedIn posts, keynote talking points, investor letters. Ensures consistency of voice and message.

### Intelligence Briefing Agent
Produces the daily/weekly executive intelligence briefing: market news, competitor moves, regulatory changes, key metrics. Routes urgent signals to CEO immediately.

---

## Research/Analyst Layer

### Market Intelligence Analyst
Continuously monitors the competitive landscape, industry trends, and market signals. Feeds the Intelligence Briefing Agent. Answers ad-hoc strategic questions from the CEO or Strategy Cluster.

- **Inputs:** Web scrapes, news APIs, analyst reports, earnings calls
- **Outputs:** Market signals digest, competitor move alerts, trend reports
- **Cadence:** Daily briefing + real-time alerts on material events

---

## Workflow

### Strategic Decision Flow
```
1. Signal arrives (market event, human request, department escalation)
2. Intelligence Briefing Agent adds context from market data
3. CEO Agent frames the decision needed
4. Strategy Cluster activates:
   - Strategy Analyst: research + options memo
   - COO: operational feasibility check
5. CEO Agent selects path
6. Board Reporter logs decision for governance record
7. COO translates decision into department directives
8. CEO monitors execution, escalates blockers to human
```

### Daily Intelligence Flow
```
1. Market Intelligence Analyst pulls overnight signals
2. Intelligence Briefing Agent assembles morning brief (2-page format)
3. CEO Agent reviews → flags items requiring action
4. Urgent signals escalated to human founders immediately
```

### Stakeholder Communication Flow
```
1. CEO Agent identifies communication need (board update, press, investor)
2. Communications Agent drafts
3. CEO Agent reviews for accuracy + tone
4. Human approves before any external send
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Notion / Linear | COO, Board Reporter | Decision logs, OKR tracking |
| Slack / Telegram | All | Internal comms, alerts |
| Google Docs | Board Reporter, Comms | Decks, memos, reports |
| NewsAPI / Perplexity | Market Intelligence Analyst | Market monitoring |
| Airtable | Strategy Analyst | Scenario modeling, tracking |
| HubSpot | CEO Agent | Pipeline + company metrics |

---

## Escalation Path

```
Solo Agents → CEO Agent
Strategy Cluster → CEO Agent
CEO Agent → Human Founders (Travis / Nathan / Britton)

Automatic human escalation triggers:
- Any decision > $10K
- Any public communication (press, investor)
- Any legal/regulatory issue
- Any hiring or firing decision
- Any cross-department conflict without clear resolution
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `strategy/nexus-strategy.md` | Strategy Analyst, CEO Agent |
| `specialized/agents-orchestrator.md` | CEO Agent (orchestration patterns) |
| `strategy/EXECUTIVE-BRIEF.md` | Intelligence Briefing Agent format |
| `strategy/coordination/handoff-templates.md` | Cross-department handoffs |
| `support/support-executive-summary-generator.md` | Board Reporter |
