# Engineering Department

**Task Flow Type: D — Sequential/Gated**
```
Spec → Architect designs → Build Cluster executes → QA gate → Infra Cluster ships → Monitor
```

Each stage must pass before the next begins. No skipping gates. Reliability and security are non-negotiable.

---

## Department Manager

**Engineering Department Manager** — the accountability layer tracking what's shipping, what's blocked, and what's broken. Monitors sprint health, verifies QA and Security gates were actually cleared, delivers incident alerts immediately to founders, and confirms the department is delivering against commitments.

- **Owns:** Daily engineering status (PRs, tickets, deploys), incident reporting (immediate human notification for P0/P1), sprint health monitoring, gate compliance verification, post-mortem tracking, department KPI dashboard (velocity, deploy frequency, MTTR)
- **Reports to:** Human Founders (Travis / Britton) — directly
- **Manages:** CTO Agent (Orchestrator)

## Orchestrator

**CTO Agent** — technical authority. Translates business needs into technical direction, approves architecture decisions, manages the engineering pipeline, and escalates blockers. Travis and Britton's domain.

```
Human Founders (Travis / Britton)
  └── Engineering Department Manager  ← monitors sprints, reports status, escalates incidents
        └── CTO Agent (Orchestrator)  ← technical direction, routing, architecture decisions
              ├── Build Cluster (Architect + Frontend + Backend + QA)
              ├── Infra Cluster (DevOps + Security + Monitoring)
              ├── AI Engineer (solo)
              ├── Technical Writer (solo)
              └── Mobile Builder (solo)
```

---

## Clusters

### Build Cluster
*Designs and builds all product features.*

| Agent | Role |
|-------|------|
| **Architect** | System design, tech stack decisions, API contracts, code standards, PR reviews |
| **Frontend Developer** | UI implementation, component library, web performance, accessibility |
| **Backend Developer** | APIs, business logic, database design, service integration |
| **QA Engineer** | Test coverage, regression testing, release sign-off, bug triage |

**Cluster workflow:**
```
Spec arrives → Architect designs → Frontend + Backend build in parallel → QA validates → Gate passed → Infra ships
```

### Infra Cluster
*Ships, secures, and monitors everything in production.*

| Agent | Role |
|-------|------|
| **DevOps Engineer** | CI/CD pipelines, infrastructure provisioning, deployment automation |
| **Security Engineer** | Vulnerability scanning, secrets management, security reviews, incident response |
| **Monitoring Agent** | Uptime, performance, error rates, alerting — production health at all times |

**Cluster workflow:**
```
Build Cluster produces release → DevOps runs deployment pipeline → Security validates → Monitoring instruments → Production live → Monitoring watches continuously
```

---

## Solo Agents

### AI Engineer
Specializes in AI/ML integration: LLM APIs, embedding pipelines, fine-tuning, AI agent infrastructure. Activated when features require AI capability. Reports to CTO.

### Technical Writer
Owns all technical documentation: API docs, developer guides, architecture decision records (ADRs), runbooks, and changelogs. Works across Build and Infra clusters.

### Mobile Builder
Owns mobile app development (iOS/Android). Works within Build Cluster patterns but specialized for mobile-specific concerns: app store compliance, native performance, push notifications.

---

## Research/Analyst Layer

### Tech Research Agent
Evaluates new tools, frameworks, libraries, and architectural patterns before the team adopts them. Prevents the team from building on shaky foundations or missing better options.

- **Inputs:** Framework releases, security advisories, engineering blogs, CTO requests
- **Outputs:** Tech evaluation reports (pros/cons/recommendation), migration assessments, security advisories
- **Cadence:** On-demand evaluation + weekly tech radar update

---

## Workflow

### Feature Build Flow
```
1. CTO receives spec (from Product or Executive)
2. CTO assigns to Architect for technical design
3. Architect produces: system design doc + ticket breakdown
4. CTO approves design
5. Frontend + Backend build in parallel
6. Each opens PR → Architect reviews
7. QA runs full test suite → signs off (GATE)
8. DevOps deploys to staging → smoke tests
9. Security validates (GATE)
10. CTO approves production deploy
11. DevOps deploys → Monitoring watches
```

### Bug Fix Flow
```
1. Bug reported (CS, Monitoring alert, or human)
2. DevOps triages: P0 / P1 / P2 / P3
3. P0/P1: Developer assigned immediately, CTO notified
4. P2/P3: Sprint queue
5. Developer fixes → minimal PR
6. QA validates fix
7. DevOps hotfix deploy (P0/P1) or sprint deploy (P2/P3)
8. Monitoring confirms resolution
```

### Security Incident Flow
```
1. Security Engineer or Monitoring detects incident
2. CTO and Security Engineer assess scope immediately
3. P0: human founders notified immediately
4. Infra Cluster activates incident response
5. Build Cluster produces fix
6. Security Engineer validates remediation
7. Post-mortem written by Technical Writer
```

### Tech Evaluation Flow
```
1. Tech Research Agent receives evaluation request (from CTO or team)
2. Researches: capabilities, maturity, security posture, community, license
3. Produces evaluation report with clear recommendation
4. CTO reviews → adopts, defers, or rejects
5. If adopted: Technical Writer documents onboarding guide
```

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| GitHub | All | Source control, PRs, CI |
| Vercel / Railway / Fly.io | DevOps | Deployment |
| GitHub Actions | DevOps | CI/CD automation |
| Jest / Vitest | QA | Unit + integration tests |
| Playwright / Cypress | QA | E2E testing |
| Sentry | Monitoring | Error tracking |
| Datadog / Grafana | Monitoring | Infrastructure monitoring |
| Snyk / Semgrep | Security | Vulnerability scanning |
| Linear | CTO | Sprint management |
| Figma | Architect | Design specs |
| AWS / GCP / DigitalOcean | DevOps | Cloud infrastructure |

---

## Escalation Path

```
Frontend / Backend → Architect → CTO Agent
QA (blocker) → CTO Agent
DevOps → CTO Agent
Security (P0/P1 incident) → CTO Agent → Human (Travis/Britton) immediately
Tech Research → CTO Agent

Automatic human escalation triggers:
- Any P0 incident (production down or data breach)
- Any security vulnerability in production
- Architecture decisions with significant cost implications
- Any infrastructure change > $500/month impact
- Any third-party service contract or commitment
```

---

## Reference Agents (from agency-agents)

| File | Maps to |
|------|---------|
| `engineering/engineering-backend-architect.md` | Architect, Backend Developer |
| `engineering/engineering-frontend-developer.md` | Frontend Developer |
| `engineering/engineering-devops-automator.md` | DevOps Engineer |
| `engineering/engineering-security-engineer.md` | Security Engineer |
| `engineering/engineering-ai-engineer.md` | AI Engineer |
| `engineering/engineering-technical-writer.md` | Technical Writer |
| `engineering/engineering-mobile-app-builder.md` | Mobile Builder |
| `engineering/engineering-senior-developer.md` | Backend + Frontend Developer |
| `engineering/engineering-rapid-prototyper.md` | Build Cluster (early-stage) |
| `engineering/engineering-data-engineer.md` | Backend Developer (data) |
| `engineering/engineering-incident-response-commander.md` | Security Engineer (incidents) |
| `engineering/engineering-threat-detection-engineer.md` | Security Engineer |
| `engineering/engineering-autonomous-optimization-architect.md` | Tech Research Agent |
| `testing/testing-api-tester.md` | QA Engineer |
| `testing/testing-performance-benchmarker.md` | QA Engineer, Monitoring Agent |
| `testing/testing-tool-evaluator.md` | Tech Research Agent |
