# Tech Stack Consolidation
## The Brokerage Inc. — Proposal Deck

---

# The Challenge

The Brokerage Inc. operates 45+ tools across siloed departments. The previous tech lead departed without documentation. The result:

- Redundant tools doing the same job across different teams
- Estimated current spend: **$17,784–$60,996/year** (before headcount scaling)
- No single source of truth for contacts, pipelines, or processes
- Unknown HIPAA compliance gaps across multiple platforms
- No documentation of what tools are active, orphaned, or redundant

**It's time to consolidate.**

---

# The Approach: Foundation First

We don't start with tools. We start with process.

**Phase 0: Process Discovery (Weeks 1–3)**
- Map every department's core workflows
- Classify all data as PHI or non-PHI
- Audit every tool for active usage, contracts, and renewal dates
- Deliver a process map that becomes the single source of truth

**Then we build back up — on a solid foundation.**

---

# Current Tool Landscape

**45+ tools across 7 categories:**

| Category | Tool Count | Est. Monthly Spend |
|----------|-----------|-------------------|
| CRM / Sales / Outreach | 7 tools | $475–$1,395 |
| Marketing / Content / SEO | 9 tools | $487–$1,413 |
| Website / Web Infrastructure | 10 tools | $66–$186 |
| Data / Automation / Backend | 10 tools | $210–$1,425 |
| Industry / Enrollment | 3 tools | $150–$500 |
| Learning / Training | 2 tools | $53–$85 |
| Compliance / Finance / Other | 5 tools | $41–$79 |
| **TOTAL** | **46 tools** | **$1,482–$5,083/mo** |

**Annual: $17,784–$60,996** — and that's before per-seat scaling.

---

# Where the Redundancies Are

**Multiple tools doing the same job:**

- **Email:** Active Campaign + GMass + SendGrid (3 tools)
- **SMS:** EZ Texting + slydial (2 tools)
- **Databases:** Airtable Admin + Airtable + Airtable OTP (3 instances)
- **Forms:** Gravity Forms + Fluent Forms + Forgravity (3 tools)
- **Websites:** WordPress + Squarespace (2 platforms)
- **LMS:** Cloud Academy + LearnDash (2 platforms)
- **Landing Pages:** Unbounce + Elementor (2 tools)
- **Analytics:** Fathom + BrightFire (2 tools)

**~11 tools can be eliminated immediately.**

---

# Proposal A: Notion + n8n + AI Agents

## The Recommended Approach

Build a split-architecture system purpose-designed for a HIPAA-regulated insurance brokerage:

- **Notion** — Non-PHI CRM & operations hub
- **n8n (self-hosted on AWS)** — Automation engine with unlimited workflows
- **AWS Bedrock** — HIPAA-compliant AI (Claude, Titan) — PHI never leaves AWS
- **AI Agents** — SDR, BDR, and Admin agents for sales and ops automation

---

# How It Works: Split Architecture

## Two layers. Clear boundary. Full compliance.

**Layer 1 — Notion (Non-PHI)**
- Contacts, pipeline stages, tasks, agent assignments
- Department wikis, SOPs, reporting dashboards
- No PHI ever touches Notion

**Layer 2 — AWS (PHI/HIPAA)**
- Encrypted database (RDS) for enrollment, Medicare IDs, policy data
- Encrypted document storage (S3) for signed forms
- n8n automation engine + AI agents via AWS Bedrock
- Covered by free AWS BAA — no $297/mo HIPAA add-on

**n8n bridges both layers** — reads non-PHI from Notion, processes PHI on AWS, writes back only sanitized status updates.

---

# AI Agents: What They Do

All AI runs through **AWS Bedrock** (HIPAA-eligible, covered by AWS BAA).

**AI SDR Agent**
- Lead qualification and scoring
- Email/SMS outreach sequences
- Automated follow-up and meeting booking

**AI BDR Agent**
- Outbound prospecting and list building
- Personalized outreach at scale
- Lead enrichment

**AI Admin Agent**
- Data entry automation
- Appointment scheduling
- Compliance document tracking and reporting

---

# PHI Protection: 11 Controls

## Technical (Automated)
1. Locked Notion database schemas — admin-only changes
2. n8n sanitization workflows strip PHI before any Notion write
3. Automated PHI scanner — daily scan of all Notion records via Bedrock AI
4. n8n as the only automated write path to Notion
5. AWS private VPC — PHI database not publicly accessible

## Procedural (Human)
6. Data classification guide — GREEN (Notion) vs RED (AWS)
7. Mandatory onboarding training + annual refresher
8. Documented incident response procedure

## Organizational (Culture)
9. Designated compliance officer owns the PHI boundary
10. Quarterly PHI boundary audits
11. "PHI-Free Zone" branding on Notion workspace

---

# What Gets Eliminated (11 Tools)

| Eliminated | Replaced By | Monthly Savings |
|-----------|-------------|-----------------|
| Active Campaign | Notion + n8n + SendGrid | $150–$500 |
| EZ Texting | n8n SMS via Twilio | $50–$200 |
| slydial | AI voicemail via n8n | $30–$100 |
| GMass | n8n bulk email | $20–$50 |
| Crisp | Notion intake + n8n | $25–$95 |
| Quo | AI SDR agent | $50–$150 |
| Airtable (×3) | Notion databases | $60–$135 |
| Zapier | n8n (free self-hosted) | $20–$100 |
| Unbounce | WordPress + Elementor | $90–$225 |
| Squarespace | WordPress | $16–$49 |

**Total savings: $661–$1,904/mo ($7,932–$22,848/yr)**

---

# Investment & Cost Structure

## One-Time Build

| Item | Investment |
|------|-----------|
| Notion CRM setup & configuration | $3,000–$8,000 |
| AI SDR agent build | $8,000–$20,000 |
| AI BDR agent build | $5,000–$15,000 |
| AI Admin agent build | $5,000–$15,000 |
| Integration layer (n8n workflows) | $5,000–$15,000 |
| PHI prevention system | $2,500–$6,000 |
| AWS PHI environment setup | $1,500–$4,000 |
| Data migration + training | $3,000–$8,000 |
| **TOTAL** | **$33,000–$91,000** |

---

# Ongoing Monthly Costs

| Item | Low (10 seats) | High (25 seats) |
|------|----------------|-----------------|
| Notion Business | $200 | $600 |
| n8n self-hosted (AWS) | $30 | $80 |
| AWS PHI environment | $131 | $360 |
| AWS Bedrock AI | $55 | $350 |
| DevOps/maintenance | $0 | $500 |
| Retained tools | $354 | $1,624 |
| **TOTAL MONTHLY** | **$770** | **$3,514** |
| **TOTAL ANNUAL** | **$9,240** | **$42,168** |

---

# Engagement Structure

## VV Consulting Fee

| Component | Detail |
|-----------|--------|
| **Base engagement fee** | $10,000 |
| **Engagement duration** | 4 months |
| **Retainer (begins Month 3)** | 15% of base ($1,500/mo) |
| **Month 1–2 total** | $10,000 (base fee covers full discovery + build kickoff) |
| **Month 3** | $1,500 (retainer) |
| **Month 4** | $1,500 (retainer) |
| **Total 4-month engagement** | **$13,000** |

**What the engagement covers:**
- Phase 0 process discovery and PHI data classification
- Notion CRM architecture and build
- n8n automation setup and core workflow buildout
- AWS PHI environment configuration
- AI agent design, prompt engineering, and testing
- PHI prevention system implementation
- Migration planning and execution support
- Training and change management across all departments

**Post-engagement:** Retainer continues at $1,500/mo for ongoing optimization, AI agent tuning, and support — cancelable with 30 days notice.

---

# Project Milestones

## 4-Month Engagement Roadmap

### Milestone 1: Foundation (Weeks 1–3) — End of Month 1
- Process discovery complete across all departments
- PHI vs. non-PHI data classification finalized
- Tool audit with contract terms and renewal dates
- Architecture plan approved

**Deliverable:** Process map + data classification guide
**Go/no-go decision point**

### Milestone 2: MVP / Prototype (Weeks 4–8) — End of Month 2
- Notion CRM live with core databases, pipeline, and locked schemas
- n8n self-hosted and operational on AWS
- AWS PHI environment configured (VPC, RDS, S3, encryption, BAA signed)
- Core automations running: lead routing, notifications, Notion-AWS bridge
- PHI sanitization workflows active
- **One AI agent (SDR) in prototype/testing**

**Deliverable:** Working MVP — team can begin using Notion CRM + n8n for daily operations
**Go/no-go decision point — retainer begins**

### Milestone 3: AI Expansion (Weeks 9–14) — End of Month 3
- AI SDR agent live in production
- AI BDR agent built and in testing
- AI Admin agent built and in testing
- PHI scanner workflow active (daily Notion scans via Bedrock)
- Medicare Pro + E123 integrations live
- First department migrated off legacy tools

**Deliverable:** Full AI agent suite in testing; first legacy tools decommissioned

### Milestone 4: Full Rollout (Weeks 15–18) — End of Month 4
- All AI agents in production
- All departments migrated and trained (including PHI boundary training)
- Legacy tools fully decommissioned
- Quarterly audit process established
- Handoff documentation complete

**Deliverable:** Fully operational system; engagement transitions to retainer-only

---

# Risk Assessment: What Could Go Wrong

## Compliance Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| PHI leaks into Notion | Medium | **Critical** | 11-control prevention plan: locked schemas, sanitization workflows, daily AI-powered PHI scanner, mandatory training, incident response, compliance officer |
| Active Campaign currently has no BAA | Medium | **Critical** | Verify immediately — existing gap that predates this project. Remediate before or during migration. |
| SendGrid/Twilio BAA not in place | Medium | High | Verify plan tier supports BAA before routing PHI-adjacent communications through it |
| AWS environment misconfigured | Low | **Critical** | Infrastructure-as-code templates, security review at Milestone 2, CloudTrail audit logging from day one |

## Operational Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Staff resistance to new systems | **High** | Medium | Change champions per department, parallel systems (no cold cutovers), department-by-department rollout, quick wins first |
| n8n self-hosted goes down | Low | High | AWS auto-recovery groups, CloudWatch alarms, documented restart procedures, failover playbook |
| Notion performance at scale (10K+ records) | Medium | Medium | Archive old records quarterly, use filtered views, split databases by year/department if needed |
| Five9 replacement doesn't match capability | Medium | Medium | Evaluate during Phase 0 — retain Five9 for complex calls if AI dialer falls short |

---

# Risk Assessment: Project & Strategic Risks

## Project Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| Scope creep during build | Medium | Medium | Fixed 4-milestone structure with go/no-go gates. Scope locked at Milestone 1. |
| Key person dependency (VV) | Medium | Medium | Full handoff documentation at Milestone 4. Retainer for ongoing support. All architecture decisions documented. |
| Migration data loss or corruption | Low | High | Pre-migration backups, parallel systems during transition, validation checks before legacy tool decommission |
| Longer timeline than estimated | Medium | Medium | MVP at Milestone 2 delivers value even if later phases delay. Go/no-go gates prevent sunk cost spiral. |

## Strategic Risks

| Risk | Likelihood | Impact | Mitigation |
|------|-----------|--------|------------|
| AWS Bedrock model changes or pricing increases | Low | Medium | Architecture supports model switching — not locked to one provider. Bedrock offers multiple model families. |
| Notion changes pricing or feature set | Low | Medium | Notion data is exportable (CSV, API). n8n is open-source. Low vendor lock-in by design. |
| Competitor adopts similar AI stack | Medium | Low | First-mover advantage. Custom agent training on brokerage-specific data creates defensible differentiation. |
| Regulatory changes to HIPAA requirements | Low | High | Split architecture is inherently conservative — PHI is isolated in a controlled environment. Easier to adapt than a single-vendor platform. |

**Risk mitigation is built into the architecture and engagement structure. Go/no-go gates at Milestones 1 and 2 limit downside exposure.**

---

# Proposal B: GoHighLevel (Alternative)

For comparison — the faster, simpler path:

| Factor | Detail |
|--------|--------|
| Platform | GoHighLevel (all-in-one CRM) |
| One-time cost | $7,000–$20,000 |
| Monthly ongoing | $1,018–$2,765 |
| HIPAA add-on | $297/mo (non-cancelable) |
| AI features | $97/mo extra per sub-account |
| Deployment | ~3.5 months |
| Customization | Platform-constrained |
| Vendor lock-in | High |

**GHL is a good choice if speed matters most and you want a vendor-managed HIPAA solution. But it costs more monthly and gives you less control.**

---

# Hours Saved: Where Time Goes Back

## Estimated Weekly Hours Recaptured by Role

| Task Currently Done Manually | Hours/Week (Current) | Hours/Week (After) | Hours Saved/Week | Who Benefits |
|------------------------------|---------------------|-------------------|-----------------|-------------|
| Lead qualification & scoring | 10–15 hrs | 1–2 hrs | **9–13 hrs** | Sales agents |
| Outreach emails & SMS follow-ups | 8–12 hrs | 1–2 hrs | **7–10 hrs** | Sales agents |
| Data entry (contacts, enrollment, pipeline updates) | 10–15 hrs | 2–3 hrs | **8–12 hrs** | Admin staff |
| Appointment scheduling & reminders | 5–8 hrs | 0.5–1 hr | **4.5–7 hrs** | Admin staff |
| Report building & pipeline tracking | 5–8 hrs | 1–2 hrs | **4–6 hrs** | Managers |
| Tool switching & duplicate data across platforms | 5–10 hrs | 0.5–1 hr | **4.5–9 hrs** | Everyone |
| Compliance document tracking | 3–5 hrs | 0.5–1 hr | **2.5–4 hrs** | Compliance / Admin |
| Manual voicemail drops & call logging | 3–5 hrs | 0.5 hr | **2.5–4.5 hrs** | Sales agents |
| **TOTAL** | **49–78 hrs/wk** | **7–12.5 hrs/wk** | **42–65.5 hrs/wk** | |

That's **1–1.6 FTEs returned to revenue-generating work every week.**

---

# ROI: Return on Investment

## Proposal A — Payback Analysis

**Assumptions:**
- Blended hourly cost: $28/hr (agents) to $16/hr (admin) → weighted average **~$23/hr**
- Hours saved: 42–65.5 hrs/week → **~2,184–3,406 hrs/year**
- Value of recovered hours: **$50,232–$78,338/year**
- Tool savings from eliminations: **$7,932–$22,848/year**

| Metric | Conservative | Optimistic |
|--------|-------------|-----------|
| Annual labor value recovered | $50,232 | $78,338 |
| Annual tool cost savings | $7,932 | $22,848 |
| **Total annual value** | **$58,164** | **$101,186** |
| Year 1 investment (build + engagement + ongoing) | $55,240 | $55,240 |
| **Year 1 net ROI** | **+$2,924 (5%)** | **+$45,946 (83%)** |
| Year 2 ongoing cost (10 seats + retainer) | $27,240 | $27,240 |
| **Year 2 net ROI** | **+$30,924 (114%)** | **+$73,946 (271%)** |

**Payback period: 7–12 months** (depending on actual hours saved and tool costs confirmed in Phase 0)

*Note: This does not include revenue upside from agents spending more time selling instead of doing admin work — which is the real multiplier.*

---

# Side-by-Side: Proposal A vs. B

| Factor | Proposal A (Notion + n8n) | Proposal B (GHL) |
|--------|--------------------------|-------------------|
| **One-time cost** | $33K–$91K | $7K–$20K |
| **Monthly (10 seats)** | $770–$1,560 | $1,018–$1,870 |
| **Annual (10 seats)** | $9,240–$18,720 | $12,216–$22,440 |
| **HIPAA cost** | $0 (AWS BAA free) | $297/mo ($3,564/yr) |
| **AI HIPAA** | Bedrock (covered by BAA) | $97/mo add-on |
| **Customization** | Unlimited | Platform-limited |
| **Vendor lock-in** | Low | High |
| **Deployment** | ~6 months (4-mo engagement) | ~3.5 months |

---

# Year-Over-Year Cost Comparison

## Year 1 (Including Setup + Engagement)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| Current state | $17,784–$60,996 | $17,784–$60,996 |
| Proposal A + VV engagement | $55,240–$122,720 | $62,440–$146,168 |
| Proposal B | $19,216–$42,440 | $19,216–$53,180 |

## Year 2+ (Ongoing Only)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| Current state | $17,784–$60,996 | $17,784–$60,996 |
| Proposal A + retainer | $27,240–$36,720 | $34,440–$60,168 |
| Proposal B | $12,216–$22,440 | $12,216–$33,180 |

*Proposal A Year 2+ includes $18,000/yr retainer. Without retainer: $9,240–$18,720 (10 seats).*

---

# The Hybrid Option

**Don't choose — phase it:**

1. **Now (Months 1–4):** Build Proposal A (Notion + n8n + AI) via VV engagement
2. **If timeline pressure exists:** Deploy GHL in parallel for immediate tool consolidation
3. **Months 5–8:** Stabilize on Notion + n8n; evaluate if GHL adds value or creates redundancy
4. **Year 2:** Full AI agent optimization; GHL either supplements or gets decommissioned

---

# Recommendation

**Start with Phase 0 — regardless of direction.**

The process discovery will:
- Reveal which tools are truly redundant vs. serving unique needs
- Surface HIPAA compliance gaps (starting with Active Campaign's BAA status)
- Give every department a voice before changes happen
- Produce the requirements to validate cost projections with real data

**Proposed next step:** Approve VV engagement and begin Phase 0 discovery.

---

# Next Steps

1. **This week:** Approve engagement and schedule kickoff
2. **Immediate:** Verify Active Campaign BAA status (potential existing compliance gap)
3. **Weeks 1–3:** Phase 0 process discovery + PHI classification
4. **Week 3:** Milestone 1 review — go/no-go on full build
5. **Weeks 4–8:** MVP build — Notion CRM + n8n + AWS + first AI agent
6. **Week 8:** Milestone 2 review — go/no-go on AI expansion (retainer begins)
7. **Weeks 9–18:** Full AI rollout, migration, training, and stabilization
