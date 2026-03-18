# Engineering Department

**Task Flow Type: D — Build/Deploy**
```
Spec → Architect designs → Devs build → QA tests → DevOps ships → Monitor
```

Sequential with gates. Each stage must pass before next begins.

---

## Department Structure

```
CTO Agent (Department Manager)
├── Architect Agent
│   └── Owns: system design, tech decisions, code standards
├── Developer Agent(s)
│   └── Owns: feature implementation, bug fixes, code review
├── QA Engineer Agent
│   └── Owns: test coverage, regression, release sign-off
└── DevOps Agent
    └── Owns: CI/CD, infrastructure, monitoring, deployments
```

---

## Roles

| Role | File | Primary Function |
|------|------|-----------------|
| CTO | `/CTO/` | Technical strategy, architecture decisions, team coordination |
| Architect | `/architect/` | System design, tech stack, code standards, PRs |
| Developer | `/developer/` | Feature builds, bug fixes, code implementation |
| QA Engineer | `/qa-engineer/` | Test suites, regression testing, release validation |
| DevOps | `/devops/` | CI/CD pipelines, infrastructure, monitoring, deployments |

---

## How Engineering Handles Tasks

### Feature Request Flow
```
1. CTO receives spec from Executive/Product
2. CTO assigns to Architect for technical design
3. Architect produces: system design doc + ticket breakdown
4. CTO approves design → assigns tickets to Developer(s)
5. Developer builds → opens PR
6. Architect reviews PR → approves or requests changes
7. QA runs test suite → signs off
8. DevOps deploys to staging → runs smoke tests
9. CTO approves production deploy
10. DevOps deploys to production → monitors
```

### Bug Fix Flow
```
1. Bug reported (from CS Agent, monitoring, or human)
2. DevOps triages severity (P0/P1/P2/P3)
3. P0/P1: Developer assigned immediately, CTO notified
4. P2/P3: Added to sprint queue
5. Developer fixes → minimal PR
6. QA validates fix
7. DevOps hotfix deploy (P0/P1) or sprint deploy (P2/P3)
```

### Infrastructure Request Flow
```
1. Request comes in (scaling, new service, security)
2. DevOps evaluates → proposes solution
3. Architect reviews for architecture fit
4. CTO approves
5. DevOps implements with monitoring
```

---

## Department Rules

1. **No direct production deploys** — always goes through CI/CD
2. **All code reviewed** — no self-merging (except emergency hotfixes)
3. **Tests required** — no feature ships without QA sign-off
4. **Security first** — credentials never in code, always in secrets manager
5. **Document everything** — architecture decisions logged in ADR format

---

## Tools Stack

| Tool | Used By | Purpose |
|------|---------|---------|
| GitHub | All | Source control, PRs, issues |
| Vercel / Railway | DevOps | Deployment |
| GitHub Actions | DevOps | CI/CD pipelines |
| Jest / Vitest | QA | Unit + integration tests |
| Playwright | QA | E2E testing |
| Sentry | DevOps | Error monitoring |
| DataDog / Grafana | DevOps | Infrastructure monitoring |
| Linear | CTO | Sprint planning, tickets |
| Figma | Architect | Design specs |

---

## Escalation Path

```
Developer → Architect → CTO → Human (Travis/Britton)
DevOps → CTO → Human (Travis)
QA (blocker) → CTO → Human
```
