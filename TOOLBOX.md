# TOOLBOX.md — Connection Registry

> The master map of every tool, connector, and credential available in the Agentic Layer.
> Morpheus reads this. Agents reference their authorized subset via KEYS.md.
> Actual credentials live in GoPass ONLY — never in this file.

---

## How This Works

1. Each tool is listed here with its GoPass path and authorized agent roles
2. An agent's `KEYS.md` lists which tools it needs (by tool ID)
3. Morpheus cross-references: does this agent have authorization for this tool?
4. If yes → Morpheus fetches credential from GoPass at runtime → passes to agent
5. If no → escalation to human for approval

---

## Connection Categories

### 📧 Communication & Email
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `email-resend` | Resend (transactional email) | `deconstraint/resend/send-only-key` | Email Marketer, CS Responder, Onboarding |
| `email-gmail-nathan` | Gmail (Nathan) | `deconstraint/gog/nathan` | CMO, Department Managers |
| `email-gmail-travis` | Gmail (Travis) | `deconstraint/gog/travis` | CEO, COO |
| `calendar-google` | Google Calendar | `deconstraint/gog/nathan` | Executive, Operations, HR |

### 📊 Analytics & Data
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `analytics-ga4` | Google Analytics 4 | `deconstraint/google/analytics` | CMO, SEO Specialist, Analytics Reporter |
| `analytics-gsc` | Google Search Console | `deconstraint/google/search-console` | SEO Specialist, Tech Research |
| `analytics-stripe` | Stripe (revenue data) | `deconstraint/stripe/secret-key` | CFO, Financial Analyst |
| `analytics-sheets` | Google Sheets | `deconstraint/gog/nathan` | Any (read), CFO/CMO (write) |

### 🔍 Research & Intelligence
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `research-brave` | Brave Search API | `deconstraint/brave/api-key` | All Research/Analyst agents |
| `research-ahrefs` | Ahrefs | `deconstraint/ahrefs/api-key` | SEO Specialist, Competitor Intel |
| `research-semrush` | SEMrush | `deconstraint/semrush/api-key` | SEO Specialist |
| `research-openai` | OpenAI API | `deconstraint/openai/api-key` | Any agent (with approval) |
| `research-anthropic` | Anthropic API | `deconstraint/anthropic/primary` | Morpheus, Orchestrators |

### 💻 Engineering & Code
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `code-github` | GitHub API | `deconstraint/github/mc-full-access` | CTO, Architect, DevOps, Developer |
| `code-vercel` | Vercel | `deconstraint/vercel/token` | DevOps, CTO |
| `code-netlify` | Netlify | `deconstraint/netlify/token` | DevOps |
| `code-railway` | Railway | `deconstraint/railway/token` | DevOps |
| `infra-do` | DigitalOcean | `deconstraint/digitalocean/token` | DevOps, Security Engineer |
| `infra-cloudflare` | Cloudflare | `deconstraint/cloudflare/token` | DevOps, Security Engineer |

### 📣 Marketing & Ads
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `ads-google` | Google Ads | `deconstraint/google/ads-api-key` | Paid Ads Agent, CMO |
| `ads-meta` | Meta Ads Manager | `deconstraint/meta/ads-token` | Paid Ads Agent, CMO |
| `social-buffer` | Buffer/Hootsuite | `deconstraint/buffer/token` | Social Media Agent |

### 🛒 Commerce & Payments
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `commerce-stripe` | Stripe (payments) | `deconstraint/stripe/secret-key` | CFO, Bookkeeper |
| `commerce-shopify` | Shopify | `deconstraint/shopify/token` | E-commerce Agent (Anahata) |

### 📋 Project Management
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `pm-trello` | Trello | `deconstraint/trello/api-token` | All Department Managers, Morpheus |
| `pm-linear` | Linear | `deconstraint/linear/token` | CTO, Engineering Manager, Product Manager |
| `pm-notion` | Notion | `deconstraint/notion/token` | Operations, Content Director |

### 🗄️ Storage & Documents
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `docs-gdrive` | Google Drive | `deconstraint/gog/nathan` | Content Director, Operations, Legal |
| `docs-gdocs` | Google Docs | `deconstraint/gog/nathan` | Content Writer, Legal, Operations |
| `docs-gsheets` | Google Sheets | `deconstraint/gog/nathan` | CFO, CMO, Operations, CRM |

### 🔊 Voice & Media
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `voice-elevenlabs` | ElevenLabs TTS | `deconstraint/elevenlabs/api-key` | Content Director, Video Producer, Morpheus |
| `voice-groq-whisper` | Groq Whisper (transcription) | `deconstraint/groq/api-key` | Content Director, Research |

### 🤖 AI Models
| Tool ID | Service | GoPass Path | Authorized Agents |
|---------|---------|-------------|------------------|
| `ai-claude` | Anthropic Claude | `deconstraint/anthropic/primary` | Orchestrators, complex reasoning |
| `ai-openai` | OpenAI GPT | `deconstraint/openai/api-key` | Content Writer, Image Gen |
| `ai-groq` | Groq (fast inference) | `deconstraint/groq/api-key` | High-frequency solos, transcription |

---

## Access Levels

| Level | Description | Who approves |
|-------|-------------|--------------|
| `READ` | Can read/query data | Department Manager |
| `WRITE` | Can read and write/create | Orchestrator + Department Manager |
| `ADMIN` | Full access including deletion/billing | Human only |
| `RESTRICTED` | Emergency use only | Human approval required each time |

---

## Adding a New Connection

When an agent requests a tool not listed here:

1. Agent submits request to Morpheus: `{ tool: "[name]", purpose: "[why]", agent: "[who]", access: "[level]" }`
2. Morpheus surfaces to human: "Agent X needs access to Tool Y for purpose Z — approve?"
3. Human approves
4. Credential is added to GoPass: `gopass insert deconstraint/[service]/[key-name]`
5. This file is updated with the new entry
6. Agent's `KEYS.md` is updated to include the tool ID
7. Agent is now authorized

**Template for new entry:**
```
| `[tool-id]` | [Service Name] | `deconstraint/[path]/[key]` | [Agent roles authorized] |
```

---

## GoPass Vault Structure

```
deconstraint/
├── anthropic/        ← AI inference
├── google/           ← Google services (ads, analytics)
├── gog/              ← Google Workspace (gmail, drive, calendar)
├── github/           ← Code repos
├── stripe/           ← Payments
├── resend/           ← Email delivery
├── elevenlabs/       ← Voice
├── groq/             ← Fast AI inference + transcription
├── openai/           ← OpenAI
├── trello/           ← Project management
├── netlify/          ← Deployment
├── vercel/           ← Deployment
├── cloudflare/       ← DNS + CDN
├── digitalocean/     ← Infrastructure
├── meta/             ← Social ads
├── shopify/          ← E-commerce
└── secrets/          ← Master keys, keyring passwords
```

---

*This file is the single source of truth for all connections. Update it when new tools are added. Never put actual credentials here — GoPass only.*
