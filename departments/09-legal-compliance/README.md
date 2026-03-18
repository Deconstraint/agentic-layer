# Legal / Compliance Department

**Task Flow Type: A — Request/Response**
```
Request arrives (contract / compliance question / legal review) → General Counsel routes → Cluster or solo executes → Review cycle → Human approves before any action
```

Nothing leaves this department without a completed review cycle. No contract is signed, no filing submitted, and no legal position taken without human approval.

---

## Department Manager

**Legal/Compliance Department Manager** — the accountability layer tracking every active contract, compliance obligation, and regulatory deadline. Legal surprises are preventable; this agent prevents them.

- **Owns:** Active contract tracker (draft/review/signature/executed), compliance calendar with advance alerts, risk register, output quality checks (review cycles completed?), department KPI dashboard (contract cycle time, compliance adherence)
- **Reports to:** Human Founders — directly
- **Manages:** General Counsel Agent (Orchestrator)

## Orchestrator

**General Counsel Agent** — routes legal requests to the appropriate cluster or solo agent, reviews outputs for legal soundness, and manages escalation to human founders for all matters requiring signature or judgment.

```
Human Founders
  └── Legal Department Manager  ← tracks contracts, monitors compliance, reports, escalates
        └── General Counsel Agent (Orchestrator)  ← routes legal work, reviews outputs, decides
              ├── Contracts Cluster (Drafter + Reviewer + Tracker)
              ├── Compliance Cluster (Policy + Audit + Risk)
              ├── IP Agent (solo)
              ├── Privacy Agent (solo)
              └── Regulatory Agent (solo)
```

---

## Clusters

### Contracts Cluster
*Drafts, reviews, and tracks all contracts.*

| Agent | Role |
|-------|------|
| **Drafter** | Produces contract drafts from templates: NDAs, MSAs, SOWs, employment agreements, vendor contracts |
| **Reviewer** | Reviews inbound contracts (from vendors, customers, partners) and redlines for risk |
| **Contract Tracker** | Maintains the contract registry: status, key dates, renewal alerts, obligations |

**Cluster workflow:**
```
Contract request → Drafter produces draft from template → General Counsel reviews → Reviewer flags risk terms → Negotiation loop → Final version → Legal Dept Manager confirms review cycle complete → Human signs
```

### Compliance Cluster
*Manages ongoing compliance obligations across the organization.*

| Agent | Role |
|-------|------|
| **Policy Agent** | Drafts, maintains, and publishes company policies (acceptable use, data handling, code of conduct, etc.) |
| **Audit Agent** | Prepares for and manages internal/external audits (SOC 2, ISO, etc.) |
| **Risk Agent** | Maintains the risk register, assesses new risks, and tracks mitigation plans |

**Cluster workflow:**
```
Compliance obligation identified → Policy Agent confirms coverage → Audit Agent prepares documentation → Risk Agent assesses exposure → General Counsel reviews → Human approves posture
```

---

## Solo Agents

### IP Agent
Manages intellectual property: trademarks, patents, trade secrets, copyright. Monitors for infringement. Coordinates with external IP counsel for filings.

### Privacy Agent (GDPR/CCPA)
Owns data privacy compliance: privacy policies, data subject requests, consent management, breach response procedures, and regulatory compliance across jurisdictions.

### Regulatory Agent
Monitors regulatory landscape for changes affecting the business. Tracks jurisdiction-specific requirements. Flags upcoming regulatory changes with 90/60/30-day advance notice.

---

## Research/Analyst Layer

### Legal Intelligence Analyst
Monitors regulatory developments, relevant case law, and compliance landscape changes. Provides General Counsel with early warning on regulatory shifts that could affect the business.

- **Inputs:** Regulatory agency publications, legal news feeds, jurisdiction-specific alerts, industry compliance updates
- **Outputs:** Regulatory change alerts, compliance landscape reports, case law summaries relevant to business
- **Cadence:** Weekly regulatory digest + immediate alert on material changes

---

## Workflow

### Contract Review Flow
```
1. Contract request arrives (new vendor, customer agreement, partnership)
2. General Counsel classifies: standard / non-standard / high-risk
3. Standard: Drafter produces from approved template
4. Non-standard: Reviewer analyzes inbound contract, produces redline
5. Negotiation loop with counterparty
6. Final version ready → Legal Dept Manager verifies review cycle completed
7. Human founders approve and sign
8. Contract Tracker logs to registry with key dates and obligations
```

### Compliance Check Flow
```
1. New business activity proposed (new market, new product, new data type)
2. General Counsel routes to relevant solo(s): Privacy, Regulatory, IP as applicable
3. Each produces compliance assessment
4. Risk Agent adds to risk register
5. General Counsel synthesizes: proceed / modify / stop
6. Human approves decision
7. Policy Agent updates policies if needed
```

### Regulatory Alert Flow
```
1. Legal Intelligence Analyst detects material regulatory change
2. Regulatory Agent assesses impact on current business activities
3. General Counsel reviews
4. Legal Dept Manager flags to founders with: what changed, impact, required action, timeline
5. Human decides response
6. Compliance Cluster executes adaptations
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| DocuSign | Contract Tracker | E-signatures |
| Notion / Google Docs | Drafter, Policy Agent | Contract drafting, policy docs |
| Ironclad / ContractBook | Contract Tracker | Contract management system |
| OneTrust | Privacy Agent | Privacy management |
| Vanta / Drata | Audit Agent | Compliance automation (SOC 2) |
| Airtable | Risk Agent | Risk register |
| LexisNexis / Bloomberg Law | Legal Intelligence Analyst | Legal research |

---

## Escalation Path

```
Contracts Cluster → General Counsel Agent
Compliance Cluster → General Counsel Agent
Solo Agents → General Counsel Agent
General Counsel Agent → Legal Dept Manager → Human Founders

Automatic human escalation triggers (ALWAYS):
- Any contract before signature
- Any active litigation or regulatory inquiry
- Any IP dispute or infringement notice
- Any data breach or privacy incident
- Any compliance finding with material risk
- Any legal position that could affect company valuation or operations
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `support/support-legal-compliance-checker.md` | Compliance Cluster, Regulatory Agent |
| `specialized/compliance-auditor.md` | Audit Agent |
| `specialized/blockchain-security-auditor.md` | IP Agent (technical IP) |
| `specialized/data-analytics-reporter.md` | Legal Intelligence Analyst |
