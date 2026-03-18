# HR / People Department

**Task Flow Type: A — Request/Response**
```
Request arrives (hire / onboard / compliance / question) → People Lead routes → Cluster or solo executes → Output reviewed → Human approves
```

Compliance-sensitive and human-impact-critical. Every output that touches an employee or candidate is reviewed before delivery. HR surprises are preventable; this department prevents them.

---

## Department Manager

**HR/People Department Manager** — the accountability layer ensuring hiring pipelines move, compliance obligations are met, payroll runs on time, and culture programs happen as designed.

- **Owns:** Weekly hiring pipeline status, compliance calendar (filings, trainings, policy reviews), payroll confirmation each cycle, culture program adherence tracking, department KPI dashboard (time-to-hire, onboarding completion, satisfaction)
- **Reports to:** Human Founders — directly
- **Manages:** People Lead Agent (Orchestrator)

## Orchestrator

**People Lead Agent** — routes all HR requests, manages the recruiting pipeline, oversees culture programs, and ensures compliance obligations are tracked and met.

```
Human Founders
  └── HR Department Manager  ← monitors pipeline, tracks compliance, reports, escalates
        └── People Lead Agent (Orchestrator)  ← routes requests, manages programs, decides
              ├── Recruiting Cluster (Sourcer + Screener + Interviewer + Offer)
              ├── Culture Cluster (Onboarding + Engagement + L&D)
              ├── Payroll Agent (solo)
              └── Compliance Agent (solo)
```

---

## Clusters

### Recruiting Cluster
*Runs the end-to-end hiring pipeline from sourcing to offer.*

| Agent | Role |
|-------|------|
| **Sourcer** | Finds qualified candidates through LinkedIn, job boards, referrals, and outbound recruiting |
| **Screener** | Runs initial screens — resume review, phone screens, culture fit assessment |
| **Interviewer Coordinator** | Schedules and coordinates interview loops; prepares interviewers with scorecards |
| **Offer Agent** | Prepares and manages offer letters, comp negotiation, and pre-close follow-up |

**Cluster workflow:**
```
Role opens → Sourcer builds candidate pipeline → Screener qualifies → Interview loop coordinated → Debrief → Offer Agent prepares offer → Human approves → Offer extended → Close or re-engage
```

### Culture Cluster
*Builds and sustains the people experience after the hire.*

| Agent | Role |
|-------|------|
| **Onboarding Agent** | Runs new hire onboarding: day 1 setup, role orientation, 30/60/90 plan |
| **Engagement Agent** | Runs engagement surveys, pulse checks, and monitors morale signals |
| **L&D Agent** | Manages learning and development programs: training content, skill development tracks |

**Cluster workflow:**
```
Offer accepted → Onboarding Agent activates → New hire oriented → Engagement Agent begins pulse tracking → L&D Agent identifies development needs → Ongoing culture programming
```

---

## Solo Agents

### Payroll Agent
Processes payroll on schedule, manages contractor payments, tracks equity grants, and handles payroll-adjacent compliance (tax withholding, benefits deductions). Works closely with Finance department.

### Compliance Agent (HR)
Tracks HR compliance: employment law changes, required postings, I-9 verification, EEO reporting, benefits compliance, and any jurisdiction-specific requirements. Flags deadlines early.

---

## Research/Analyst Layer

### Talent Market Analyst
Monitors the talent landscape: compensation benchmarks, hiring trends, competitor talent moves, and labor market signals. Provides People Lead with data for comp decisions, role design, and recruiting strategy.

- **Inputs:** Levels.fyi, Glassdoor, LinkedIn Talent Insights, job posting analysis, industry compensation surveys
- **Outputs:** Compensation benchmarks by role, hiring difficulty assessments, talent market reports
- **Cadence:** Quarterly comp benchmark refresh + on-demand role analysis

---

## Workflow

### Hiring Flow
```
1. Hiring need identified (from department head + approved by founders)
2. People Lead creates job description + scorecard
3. Sourcer builds candidate pipeline (target: 10 qualified candidates per role)
4. Screener runs phone screens (target: 3-5 move forward)
5. Interviewer Coordinator runs loop (3-4 interviews, structured scorecards)
6. Debrief → People Lead synthesizes → Recommendation
7. Human approves hire
8. Offer Agent prepares offer (Talent Market Analyst confirms comp is competitive)
9. Offer extended → Close or re-engage
10. Offer accepted → Onboarding Agent activates
```

### Onboarding Flow
```
1. Offer accepted → Day 1 setup initiated (accounts, equipment, access)
2. Onboarding Agent runs first week: orientation, team intros, role context
3. 30-day check-in: settling in? questions? needs?
4. 60-day: role clarity, early wins, gaps
5. 90-day: full ramp assessment → Engagement Agent begins regular pulse tracking
```

### Compliance Calendar Flow
```
1. Compliance Agent maintains calendar of all HR obligations
2. 30-day advance alert on every deadline
3. People Lead reviews and assigns execution
4. HR Department Manager confirms completion
5. Human founders notified of any filing or reporting completed
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| Greenhouse / Lever | Sourcer, Screener, Interviewer | ATS — applicant tracking |
| LinkedIn Recruiter | Sourcer | Candidate sourcing |
| Gusto / Rippling | Payroll Agent | Payroll processing |
| Lattice / Culture Amp | Engagement Agent | Engagement surveys |
| Notion | L&D Agent, Documentation | Knowledge base, training library |
| Google Calendar | Interviewer Coordinator | Interview scheduling |
| Carta | Payroll Agent | Equity management |
| Bamboo HR | People Lead | HRIS — employee records |

---

## Escalation Path

```
Recruiting Cluster → People Lead Agent
Culture Cluster → People Lead Agent
Solo Agents → People Lead Agent
People Lead Agent → HR Department Manager → Human Founders

Automatic human escalation triggers:
- Any offer letter before sending
- Any termination decision
- Any compliance filing or regulatory deadline
- Any sensitive employee situation (performance, conflict, accommodation)
- Compensation decision outside standard bands
- Any equity grant
```

---

## Reference Agents (from agency-agents)

*This department is built primarily from scratch — agency-agents has limited HR coverage.*

| File | Maps to |
|------|---------|
| `specialized/data-analytics-reporter.md` | Talent Market Analyst |
| `project-management/project-management-project-shepherd.md` | Onboarding Agent (process management) |
| `support/support-analytics-reporter.md` | Engagement Agent (survey analytics) |
