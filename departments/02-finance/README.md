# Finance Department

**Task Flow Type: A — Request/Response**
```
Request arrives → CFO validates → Routes to solo or cluster → Output produced → CFO reviews → Human approves
```

Structured, compliance-sensitive. Every financial output is validated before leaving the department. Accuracy is non-negotiable.

---

## Department Manager

**Finance Department Manager** — the accountability layer ensuring every financial output is produced on time, reviewed for accuracy, and escalated appropriately. Tracks deadlines, audits output quality, and surfaces financial risk to founders before it compounds.

- **Owns:** Close calendar, deadline alerts (30/14/7-day advance), output quality checks on all reports, escalation to human on missed deadlines or anomalies, department KPI dashboard
- **Reports to:** Human Founders — directly
- **Manages:** CFO Agent (Orchestrator)

## Orchestrator

**CFO Agent** — routes financial requests, reviews all outputs for accuracy and compliance, manages the department's reporting cadence, and escalates material financial decisions to human founders.

```
Human Founders
  └── Finance Department Manager  ← monitors, tracks, reports, escalates
        └── CFO Agent (Orchestrator)  ← routes work, reviews outputs, decides
              ├── Reporting Cluster (Controller + AP/AR + Payroll)
              ├── Financial Analyst (solo)
              ├── Tax Agent (solo)
              └── Investor Relations (solo)
```

---

## Clusters

### Reporting Cluster
*Produces accurate, timely financial reporting and manages the transactional ledger.*

| Agent | Role |
|-------|------|
| **Controller** | Owns the general ledger, month-end close, and financial statements |
| **AP/AR Agent** | Manages accounts payable (vendor invoices) and accounts receivable (customer billing) |
| **Payroll Agent** | Processes payroll, tracks equity, manages contractor payments |

**Cluster workflow:**
```
Month-end trigger → Controller initiates close sequence → AP/AR reconciles outstanding → Payroll finalizes compensation → Controller produces P&L, Balance Sheet, Cash Flow → CFO reviews → Human approves
```

---

## Solo Agents

### Financial Analyst
Runs ad-hoc financial analysis: unit economics, scenario modeling, burn rate projections, CAC/LTV analysis. Answers CFO questions with numbers.

### Tax Agent
Manages tax obligations: quarterly estimates, sales tax, 1099/W-2 filings, state registrations. Flags deadlines. Works with external CPA.

### Investor Relations Agent
Produces investor updates, cap table management, fundraising materials. Tracks investor commitments and communications.

---

## Research/Analyst Layer

### Financial Intelligence Analyst
Monitors financial benchmarks, SaaS metrics comparisons, valuation multiples, and funding market conditions. Provides context for CFO decisions and investor conversations.

- **Inputs:** Public company filings, benchmark databases, VC market data, competitor revenue signals
- **Outputs:** Benchmark reports, valuation context, financial trend analysis
- **Cadence:** Monthly benchmark report + on-demand analysis

---

## Workflow

### Monthly Close Flow
```
1. Month-end trigger (automated, 1st of month)
2. AP/AR Agent reconciles all outstanding invoices + payments
3. Payroll Agent finalizes compensation records
4. Controller runs reconciliation, produces draft financials
5. CFO Agent reviews for anomalies
6. CFO flags any variances > 10% for investigation
7. Financial Analyst explains variances
8. CFO approves final financials
9. Board Reporter (Executive dept) receives for board deck
10. Human founders get final P&L summary
```

### Expense Approval Flow
```
1. Expense request arrives (from any department)
2. CFO Agent checks against budget
3. Under threshold: Auto-approve, log to ledger
4. Over threshold: Escalate to human
5. AP/AR Agent processes payment
6. Controller books to GL
```

### Financial Analysis Request Flow
```
1. Request arrives (from CEO, department head, or investor)
2. CFO Agent routes to Financial Analyst
3. Financial Analyst pulls data, builds model
4. CFO reviews for accuracy
5. Output delivered in standard format (Notion doc or Google Sheet)
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| QuickBooks / Xero | Controller, AP/AR | General ledger, bookkeeping |
| Gusto / Rippling | Payroll Agent | Payroll processing |
| Stripe / Recurly | AP/AR | Revenue reconciliation |
| Carta | Investor Relations | Cap table management |
| Google Sheets | Financial Analyst | Modeling, analysis |
| Notion | CFO | Financial calendar, memos |
| Pilot / Bench | Controller | Bookkeeping support |
| AngelList | Investor Relations | Investor communications |

---

## Escalation Path

```
Controller / AP/AR / Payroll → CFO Agent
Financial Analyst → CFO Agent
Tax Agent → CFO Agent → External CPA (human-coordinated)
Investor Relations → CFO Agent → Human Founders

Automatic human escalation triggers:
- Any payment > $5K (configurable threshold)
- Tax filing deadlines (30-day advance notice)
- Cash runway < 6 months
- Any investor communication before sending
- Any financial restatement
- Any new banking or credit decision
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `support/support-finance-tracker.md` | Controller, AP/AR Agent |
| `specialized/accounts-payable-agent.md` | AP/AR Agent |
| `specialized/report-distribution-agent.md` | CFO Agent (reporting distribution) |
| `support/support-analytics-reporter.md` | Financial Intelligence Analyst |
