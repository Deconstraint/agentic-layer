# Research & Intelligence Department

**Task Flow Type: E — Intelligence/Async**
```
Question / scheduled trigger → Intel Cluster pulls data → Analyst synthesizes → Report produced → Department Manager verifies delivery → Distributed to consuming departments
```

This department IS the research layer for the entire organization. It runs on schedule and on-demand, feeding intelligence to every other department. Output quality and delivery reliability are its core metrics.

---

## Department Manager

**Research & Intel Department Manager** — the accountability layer ensuring intelligence is produced on time, meets sourcing and analytical quality standards, and actually reaches the departments that need it.

- **Owns:** Research request queue (all active requests, owners, due dates, status), scheduled output calendar (weekly/monthly reports confirmed delivered), distribution verification, quality spot-checks on reports, department KPI dashboard (on-time delivery, request fulfillment, report utility)
- **Reports to:** Human Founders — directly
- **Manages:** Research Director Agent (Orchestrator)

## Orchestrator

**Research Director Agent** — routes research requests, assigns analysts, synthesizes cross-stream intelligence, and manages the department's output calendar.

```
Human Founders
  └── Research Dept Manager  ← tracks delivery, audits quality, verifies distribution, escalates
        └── Research Director Agent (Orchestrator)  ← routes requests, assigns work, synthesizes
              ├── Market Intel Cluster (Researcher + Analyst + Report Writer)
              ├── Competitive Intel Cluster (Monitor + Analyst + Briefer)
              ├── Data Engineer (solo)
              ├── Survey Agent (solo)
              └── Trend Spotter (solo)
```

---

## Clusters

### Market Intel Cluster
*Produces comprehensive market intelligence for strategic decisions.*

| Agent | Role |
|-------|------|
| **Market Researcher** | Pulls primary and secondary market data: industry reports, TAM/SAM analysis, customer segment research |
| **Market Analyst** | Synthesizes raw data into insight: what the data means, what it implies for strategy |
| **Report Writer** | Packages analysis into polished, distributable reports for each consuming department |

**Cluster workflow:**
```
Research question / scheduled brief → Market Researcher pulls data → Market Analyst synthesizes → Report Writer formats → Research Director reviews → Dept Manager verifies quality → Distributed
```

### Competitive Intel Cluster
*Tracks and synthesizes the competitive landscape in near-real-time.*

| Agent | Role |
|-------|------|
| **Competitive Monitor** | Continuously tracks competitor activity: product releases, pricing changes, marketing moves, hiring signals, press |
| **Competitive Analyst** | Synthesizes monitor data into competitive insight: what matters, what's a threat, what's an opportunity |
| **Competitive Briefer** | Produces the weekly competitive digest and ad-hoc alerts for Marketing, Sales, and Executive |

**Cluster workflow:**
```
Continuous monitoring → Material event detected → Competitive Analyst assesses → Briefer produces alert or scheduled digest → Distributed to Marketing + Sales + Executive
```

---

## Solo Agents

### Data Engineer
Builds and maintains data pipelines that feed the research department. Connects data sources, runs ETL processes, and ensures analysts have clean, structured data to work with.

### Survey Agent
Designs, deploys, and analyzes surveys for primary research: customer surveys, market surveys, expert interviews. Provides Research Director with primary data that secondary research can't provide.

### Trend Spotter
Monitors macro trends across technology, culture, regulation, and industry that could affect the business 6-24 months out. Produces the quarterly trend report for Executive and Product departments.

---

## Research/Analyst Layer

*This department IS the research layer.* Every team in this department contributes to the organization's intelligence function. The Market Analyst and Competitive Analyst are the core analytical roles.

The Research Director synthesizes across all clusters into integrated intelligence when cross-stream synthesis is needed (e.g., "here's the market opportunity + competitive gap + trend signal all pointing in the same direction").

---

## Workflow

### Scheduled Intelligence Flow
```
Weekly:
- Competitive Briefer produces competitive digest → distributed to Marketing, Sales, Executive
- Market Intel Cluster produces sector update → distributed to Executive, Product

Monthly:
- Full market analysis report → Executive, Product, Marketing
- Customer sentiment synthesis → CS, Product

Quarterly:
- Trend Spotter produces trend report → Executive, all departments
- TAM/SAM update → Executive, Finance
```

### Ad-Hoc Research Request Flow
```
1. Request arrives from any department (routed through Research Director)
2. Research Director scopes: timeline, depth, consuming audience
3. Assigns to appropriate cluster or solo
4. Research Dept Manager logs to request queue with due date
5. Researcher executes
6. Analyst synthesizes
7. Report Writer formats for audience
8. Research Director reviews for quality
9. Dept Manager verifies quality gate, confirms distribution
10. Delivered to requesting department
```

### Competitive Alert Flow
```
1. Competitive Monitor detects material competitor event
2. Competitive Analyst assesses: how significant? what's the implication?
3. If significant: Briefer produces immediate alert (< 4h turnaround)
4. Distributed to: Executive + relevant department (Marketing if messaging change, Sales if pricing change, etc.)
5. Research Dept Manager confirms delivery
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Perplexity / Tavily | Market Researcher, Competitive Monitor | Web research, news monitoring |
| Semrush / Ahrefs | Competitive Monitor | SEO and content intelligence |
| SimilarWeb | Competitive Monitor | Traffic and digital intelligence |
| Typeform / Qualtrics | Survey Agent | Survey deployment |
| dbt / Airflow | Data Engineer | Data pipelines |
| Snowflake / BigQuery | Data Engineer | Data warehouse |
| Notion | Report Writer | Research library |
| Airtable | Research Director, Dept Manager | Request tracking |
| Crunchbase | Market Researcher | Funding and company data |
| CB Insights | Market Analyst | Market intelligence platform |

---

## Escalation Path

```
All cluster agents → Research Director Agent
Solo agents → Research Director Agent
Research Director → Research Dept Manager → Human Founders

Automatic human escalation triggers:
- Intelligence finding that requires immediate strategic decision
- Competitive threat of material significance
- Research request from founders (prioritized above all else)
- Data breach or privacy concern in research data handling
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `product/product-trend-researcher.md` | Trend Spotter, Market Researcher |
| `specialized/data-analytics-reporter.md` | Market Analyst, Competitive Analyst |
| `specialized/data-consolidation-agent.md` | Data Engineer |
| `specialized/report-distribution-agent.md` | Report Writer, Competitive Briefer |
| `testing/testing-evidence-collector.md` | Market Researcher (primary research) |
