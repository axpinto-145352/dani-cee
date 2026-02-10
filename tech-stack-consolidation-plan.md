# Tech Stack Consolidation
## The Brokerage Inc. — Build-Out Plan

---

**Document Type:** Technical Implementation Plan
**Version:** 2.0
**Date:** February 2026
**Prepared For:** The Brokerage Inc. Leadership Team
**Prepared By:** VV Consulting

---

## Table of Contents

1. The Problem
2. Our Approach
3. Phase 0: Process Discovery
4. Current Tool Inventory & Cost Estimates
5. Proposal A: Notion CRM + n8n + AI Agents
6. Proposal B: GoHighLevel + Automation
7. Hours Saved & ROI Analysis
8. Side-by-Side Comparison
9. The Hybrid Option
10. Recommendation
11. Change Management Strategy
12. Next Steps

<div style="page-break-after: always;"></div>

# 1. The Problem

The Brokerage Inc. has accumulated **90+ tools** across siloed departments. The previous tech lead departed without documentation. Redundancies are costing money and creating confusion.

**Additionally:** The two core patient data systems — AgencyBlock and AgencyIntegrator — don't communicate with each other. Staff create manual workarounds to move information between systems. The data in these systems is messy, outdated, and contains records of deceased patients that have never been purged.

It's time to consolidate and integrate.

<div style="page-break-after: always;"></div>

# 2. Our Approach: Foundation First

Before selecting tools, we map the actual processes. Start analog, then rebuild the tech layer on top.

**Phase 0 comes first — regardless of which proposal is chosen.**

<div style="page-break-after: always;"></div>

# 3. Phase 0: Process Discovery

## What We Do
- Inventory every department and vertical
- Map core workflows: lead gen, enrollment, retention, marketing, compliance, training, admin
- Document who does what, when, how often, and where handoffs happen
- Identify HIPAA/compliance requirements per workflow
- Map every current tool to the process it supports
- Flag tools that are active, redundant, or orphaned

## Deliverable
A process map that becomes the single source of truth for all consolidation decisions.

## Timeline
**Weeks 1–3**

<div style="page-break-after: always;"></div>

# 4. Current Tool Inventory & Cost Estimates

All costs below are estimates based on typical published plan pricing. Actual amounts require a contract and billing audit during Phase 0.

**Total tools identified: 90+** (significant expansion from initial 46-tool estimate)

---

## Communication / Collaboration

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Zoom | Video meetings / phone system | $15–$20/user | Pro ~$15/user/mo; Business ~$20/user/mo | Keep — evaluate seat count |
| OtterAI | Meeting transcription | $10–$20/user | Pro ~$10/user/mo; Business ~$20/user/mo | Evaluate — may replace with AI |
| MS365-Teams | Team collaboration | $6–$22/user | Business Basic ~$6/user; Business Premium ~$22/user | Keep |
| Asana | Project management | $11–$25/user | Premium ~$11/user; Business ~$25/user | Redundant — replace with Notion |
| Trello | Task management | $5–$10/user | Standard ~$5/user; Premium ~$10/user | Redundant — replace with Notion |
| Grasshopper | Virtual phone | $30–$80 | Solo ~$30/mo; Small Business ~$80/mo | Evaluate — Five9 may cover |

**Category subtotal: ~$77–$177/mo** (single-seat estimate; scales significantly)

---

## CRM / Sales / Outreach

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Active Campaign | Email marketing / CRM | $150–$500 | Tiered by contact count: Starter ~$15/mo (500 contacts), Professional scales to $500+ for large lists | Redundant — replace |
| EZ Texting | SMS outreach | $50–$200 | Plans start ~$20/mo for 500 credits; scales by message volume | Redundant — replace |
| EZ Texting (ServiceLink) | SMS messaging (separate account?) | $50–$200 | Same pricing — confirm if duplicate subscription | Investigate — likely duplicate |
| slydial | Voicemail drops | $30–$100 | Per-use credits (~$0.05–$0.10/drop) or monthly subscription packs | Redundant — multiple VM tools |
| slydocast | Voicemail drops | $30–$100 | Similar to slydial — confirm if same vendor/different product | Redundant — consolidate |
| My Broadcast | Voicemail drops | $30–$100 | Another voicemail drop service | Redundant — pick one |
| GMass | Bulk email via Gmail | $20–$50 | Standard plan ~$20/mo per Gmail account; Premium ~$30; Enterprise ~$50 | Redundant — replace |
| Five9 | Contact center / dialer | $150–$300/seat | Core plan ~$149/seat/mo; per-minute telecom usage added on top | Core — evaluate replacement |
| Crisp | Live chat / messaging | $25–$95 | Free basic; Pro ~$25/mo; Unlimited ~$95/mo per workspace | Redundant — appears 3x |
| Crisp - Chatbot | Website chat | $25–$95 | Same tool, different listing | Duplicate listing |
| Quo | Sales engagement / quoting | $50–$150 | Per-seat SaaS pricing; varies by plan tier | Redundant — replace |

**Category subtotal: ~$610–$1,890/mo**

---

## Marketing / Content / SEO

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Canva | Graphic design | $13–$30 | Pro ~$13/mo (1 user); Teams ~$30/mo per 5 users | Keep |
| Riverside | Remote recording / podcast | $15–$24 | Standard ~$15/mo; Business ~$24/mo; per-seat | Keep if podcast continues |
| Testimonial.to | Video testimonials | $20–$50 | Starter ~$20/mo; Premium ~$50/mo; based on # of testimonials | Evaluate ROI |
| UberSuggest | SEO research | $30–$50 | Individual ~$29/mo; Business ~$49/mo; lifetime deals available | Redundant — evaluate |
| Unbounce | Landing pages | $90–$225 | Launch ~$90/mo; Optimize ~$225/mo; based on conversions/pages | Redundant — replace |
| BrightFire | Insurance marketing / SEO | $100–$500 | Insurance-specific marketing packages | Evaluate ROI |
| Liberated Syndication | Podcast hosting | $5–$20 | Classic plans $5–$20/mo based on storage per month | Keep if podcast continues |
| YouTube Premium | Video streaming | $14 | Fixed subscription price | Likely personal — remove |
| Link Tree | Link landing | $5–$24 | Free tier; Pro ~$5/mo; Premium ~$24/mo | Keep — low cost |
| Forgravita LLC | Marketing services | TBD | Vendor/agency — confirm scope and cost | Investigate |
| OptinMonster (crtrdp llc) | Lead capture | $14–$80 | Basic ~$14/mo; Pro ~$80/mo | Evaluate — GHL/Notion may cover |

**Category subtotal: ~$306–$1,017/mo**

---

## Website / Web Infrastructure

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| WordPress (main) | Primary website CMS | $0 | Open-source CMS — free | Keep |
| wordpress - main | Website CMS (duplicate listing) | $0 | Same as above | Duplicate listing |
| WP Engine / wpengine login | WordPress hosting | $20–$60 | Startup ~$20/mo (1 site, 25K visits); Growth ~$60/mo (10 sites) | Keep |
| Elementor | Website builder / page builder | $5–$17 | Essential ~$5/mo (1 site); Advanced ~$17/mo (25 sites); billed annually | Keep w/ WordPress |
| Gravity Forms | Form builder | $5–$20 | Basic ~$5/mo; Elite ~$20/mo; billed annually per-site license | Redundant — pick one |
| Fluent Forms (wpmanageinja) | Form builder | $5–$10 | Single site ~$5/mo; agency ~$10/mo; billed annually | Redundant — pick one |
| Forgravity (now ConnectGiant) | Gravity Forms add-ons / cloud storage | $10–$20 | Annual license divided monthly; depends on add-on bundle | Eliminate if Gravity goes |
| Imagify | Image optimization | $5–$10 | Starter free (20MB); Growth ~$5/mo (500MB); Infinite ~$10/mo | Keep — low cost |
| Gravatar | Avatar profiles | $0 | Free service | Keep |
| Metabox | WordPress fields | $5–$15 | Personal ~$5/mo; Developer ~$15/mo | Keep if used |
| perfmatters | Site performance | $3–$5 | ~$25/yr for single site | Keep — low cost |

**Category subtotal: ~$58–$157/mo**

---

## Data / Automation / Backend

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Airtable (Admin) | Database / ops | $20–$45/seat | Team ~$20/seat/mo; Business ~$45/seat/mo; scales by seats and records | Redundant — replace |
| Airtable | Database tool | $20–$45/seat | Same pricing as above — separate workspace or base | Redundant — replace |
| Airtable OTP | Secure access / unknown | $20–$45/seat | Same pricing — unknown what this base serves | Investigate |
| AirTable (Justin) | Database tool | $20–$45/seat | Personal workspace — confirm if needed | Investigate — likely consolidate |
| Zapier | App automation | $20–$100+ | Starter ~$20/mo (750 tasks); Professional ~$50/mo (2K tasks); Team ~$100/mo | Replace with n8n |
| SendGrid (Twilio) | Email delivery | $15–$90 | Free tier (100/day); Essentials ~$15/mo (50K emails); Pro ~$90/mo (100K emails) | Keep for transactional email |
| Send Grid (ServiceLink) | Email delivery (separate account?) | $15–$90 | Same pricing — confirm if duplicate subscription | Investigate — likely duplicate |
| Sendgrid | Email delivery (third listing) | $15–$90 | Same tool — multiple listings | Duplicate listing |
| Amazon Web Services | Cloud hosting | $50–$500+ | Usage-based: EC2 instances, S3 storage, data transfer — highly variable | Keep — hosts n8n + AI |
| Couchdrop | SFTP automation | $15–$50 | Starter ~$15/mo; Business ~$50/mo; based on storage and users | Evaluate necessity |
| HIPAA Vault | Secure email / HIPAA hosting | $50–$300 | Managed HIPAA hosting; pricing by server size and compliance tier | **Keep — non-negotiable** |
| Streamlit | Data apps | $0–$250 | Community Cloud free; Teams ~$250/mo for private apps | Evaluate what it powers |
| Basefront | Lead management | TBD | Cannot confirm pricing — tool needs investigation | Investigate |
| Hubsolo | Excel tools | TBD | Cannot confirm pricing — tool needs investigation | Investigate |
| FileZilla | FTP client | $0 | Free open-source software | Keep — free |

**Category subtotal: ~$260–$1,750/mo** (varies heavily by seats/usage)

---

## Industry-Specific / Enrollment / HIPAA Systems

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| **AgencyBloc** | Insurance CRM / patient records | Existing contract | HIPAA-compliant AMS; existing BAA in place | **KEEP — Core PHI system** |
| **Agency Integrator (AI)** | Data integration / workflow automation | Existing contract | HIPAA-compliant workflow platform; existing BAA in place | **KEEP — Core PHI system** |
| Agency Integrator | Data integration (duplicate listing) | Existing contract | Same tool | Duplicate listing |
| AgencyVision | Agent analytics | $50–$150 | Insurance-specific analytics platform | Evaluate — may overlap with reporting |
| HealthSherpa | ACA/Medicare enrollment | $0–$100 | Free for basic; premium features may have cost | **Keep — ACA enrollment** |
| Sunfire | Medicare enrollment | $50–$150 | Medicare-specific enrollment platform | **Keep — Medicare enrollment** |
| E123 | Medicare enrollment / commissions payouts | $50–$200 | Per-agent licensing for enrollment/quoting platform | **Keep — core business** |
| Mojo/PaperClip | Enrollment automation | $50–$150 | Enrollment workflow automation | Evaluate — may overlap with AI |
| Sircon | Licensing compliance | $25–$75 | Producer licensing management | **Keep — compliance required** |
| NIPR | Producer registry | $0–$50 | National Insurance Producer Registry; per-transaction fees | **Keep — compliance required** |
| Sunroofflex | Contracting platform | $50–$200 | Agent contracting and onboarding | Evaluate necessity |
| BrokerLink 2.0 | Agent portal | TBD | Cannot confirm pricing | Investigate |
| State Based Systems | Agent data (pulling new agent data) | $0–$50 | State-specific systems; may be free or per-transaction | **Keep — compliance required** |
| State Dept of Insurance | Agent lookup / agent data | $0 | Government systems — typically free | **Keep — compliance required** |
| DOI websites | Regulatory access | $0 | Government systems — free | **Keep — compliance required** |
| HPMS | Medicare reporting | $0 | CMS Health Plan Management System — no direct cost | **Keep — CMS compliance** |
| Workflex | Insurance admin | TBD | Cannot confirm pricing | Investigate |

**Category subtotal: ~$275–$1,125/mo** (excludes AgencyBloc/AgencyIntegrator — already in budget)

**Note:** AgencyBloc and Agency Integrator are the existing HIPAA-compliant patient data systems. They are NOT being replaced — they are being integrated via n8n and cleaned up via data hygiene services.

---

## Security / Authentication / Compliance

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| DUO | Multi-factor authentication | $3–$9/user | MFA ~$3/user; Access ~$6/user; Beyond ~$9/user | **Keep — security required** |
| Sophos | Cybersecurity / endpoint protection | $25–$50/endpoint | Intercept X ~$25–$50/endpoint/yr | **Keep — security required** |
| KnowBe4 | Security training | $18–$30/user/yr | Security awareness training; per-user annual | **Keep — compliance training** |
| Avenon | Email security | TBD | Cannot confirm pricing | Investigate |
| Alarm.com | Security monitoring | $10–$30 | Physical security monitoring | Evaluate — is this office security? |
| Checker | Background checks | Per-use | $20–$50 per background check | Keep — hiring requirement |
| ControlMap Communications | Compliance platform | TBD | Cannot confirm pricing | Investigate |
| Verify Comply | Compliance tracking | TBD | Cannot confirm pricing | Investigate |

**Category subtotal: ~$56–$119/mo** (single-user estimate; background checks variable)

---

## Finance / Accounting / HR

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Ramp | Expense management | $0–$12/user | Free tier available; Plus ~$12/user/mo | Evaluate — may overlap with accounting |
| ADP | Payroll / HR | $50–$200+ | Base platform + per-employee fees | **Keep — payroll required** |
| BILL | Bill payments | $45–$79 | Essentials ~$45/mo; Team ~$79/mo | Evaluate — may consolidate |
| Sage | Accounting software | $25–$75 | Start ~$25/mo; Accounting ~$75/mo | Redundant — pick one |
| Quickbooks | Accounting software | $30–$100 | Simple Start ~$30/mo; Plus ~$100/mo | Redundant — pick one |
| Tax Bandits | Tax filing | ~$4/mo (~$50/yr) | Per-form pricing (e.g. $3–$5 per 1099); seasonal use | Keep |

**Category subtotal: ~$154–$470/mo**

---

## Learning / Training

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Cloud Academy | Tech training | $40–$55/seat | Individual ~$40/seat/mo; Team ~$55/seat/mo; enterprise negotiated | Redundant — pick one |
| LearnDash | LMS platform | $13–$30 | 1 site ~$13/mo; 10 sites ~$30/mo; billed annually | Redundant — pick one |
| iSpring | Training software | $4–$7/user | Suite ~$4/user; Max ~$7/user (billed annually) | Redundant — pick one |
| MLN | Learning network (Medicare Learning Network) | $0 | CMS resource — free | Keep — compliance training |
| Scribe | Process documentation | $0–$29/user | Free basic; Pro ~$29/user | Evaluate — AI may replace |

**Category subtotal: ~$57–$121/mo** (single-seat estimate)

---

## AI Tools

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| ChatGPT | AI assistant | $20–$25/user | Plus ~$20/user; Team ~$25/user | Evaluate — consolidate to Bedrock |
| Co-pilot | AI assistant (Microsoft) | $30/user | Microsoft 365 Copilot ~$30/user/mo | Evaluate — consolidate to Bedrock |

**Category subtotal: ~$50–$55/mo** (single-user)

**Note:** These standalone AI subscriptions should be consolidated into AWS Bedrock for HIPAA compliance and cost efficiency. Individual ChatGPT/Copilot accounts may expose PHI to non-compliant systems.

---

## Office / Hardware / Other

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Microsoft Office | Office productivity | Included | Often bundled with MS365 | Keep |
| MS Office | Office productivity (duplicate listing) | Included | Same as above | Duplicate listing |
| Adobe Pro | PDF editing | $23–$35 | Acrobat Pro ~$23/mo; with e-sign features ~$35/mo per license | Evaluate if CRM covers e-sign |
| Zoho | Business suite / password | $3–$45/user | Varies by product; Zoho One ~$45/user/mo | Investigate scope |
| AddEvent | Calendar links | $0–$16 | Free tier available; Pro ~$16/mo for custom branding | Keep if used |
| CMS | Content management | TBD | Generic listing — clarify what this is | Investigate |
| Registration Software | Event registration | TBD | Cannot confirm — clarify vendor | Investigate |
| Brother Printers | Office printing | N/A | Hardware — not SaaS | N/A |

**Category subtotal: ~$26–$96/mo** (excluding unknown tools)

---

# Total Estimated Current Spend (UPDATED)

| Category | Low Estimate/mo | High Estimate/mo |
|----------|----------------|-----------------|
| Communication / Collaboration | $77 | $177 |
| CRM / Sales / Outreach | $610 | $1,890 |
| Marketing / Content / SEO | $306 | $1,017 |
| Website / Web Infrastructure | $58 | $157 |
| Data / Automation / Backend | $260 | $1,750 |
| Industry / Enrollment | $275 | $1,125 |
| Security / Authentication / Compliance | $56 | $119 |
| Finance / Accounting / HR | $154 | $470 |
| Learning / Training | $57 | $121 |
| AI Tools | $50 | $55 |
| Office / Hardware / Other | $26 | $96 |
| **TOTAL MONTHLY** | **~$1,929/mo** | **~$6,977/mo** |
| **TOTAL ANNUAL** | **~$23,148/yr** | **~$83,724/yr** |

*Per-seat tools (MS365, Five9, Airtable, Zoom, ADP, etc.) can multiply significantly with headcount. These estimates assume minimal seats — actual spend may be at or above the high end.*

**Key findings from expanded inventory:**
- **Multiple duplicate subscriptions** identified (SendGrid x3, Crisp x3, Airtable x4, EZ Texting x2, voicemail drops x3)
- **Three competing accounting systems** (Sage, Quickbooks, plus Ramp/BILL for payments)
- **Three competing LMS/training platforms** (Cloud Academy, LearnDash, iSpring)
- **AI tools fragmented** across ChatGPT and Copilot — consolidation to Bedrock needed for HIPAA compliance
- **Form builders duplicated** (Gravity Forms + Fluent Forms)
- **Project management duplicated** (Asana + Trello) — both replaceable by Notion

<div style="page-break-after: always;"></div>

# 5. Proposal A: Notion CRM + n8n + AI Agents

---

## Proposal A — Philosophy

**Integration-first approach:** Keep the existing HIPAA-compliant systems (AgencyBlock & AgencyIntegrator) and connect them with a modern front-end. Notion handles all non-PHI CRM operations (pipeline, tasks, contacts, SOPs). n8n bridges the systems that have never talked to each other. AI agents layer on top via n8n orchestration. Data hygiene cleans up years of accumulated mess.

**We don't replace what works — we connect it and clean it up.**

---

## Proposal A — Architecture (Integration-First)

### Layer 1: AgencyBlock + AgencyIntegrator (Existing PHI Systems — KEPT)
- **AgencyBlock:** Patient records, Medicare IDs, policy numbers, enrollment data, health plan selections — already HIPAA-compliant with existing BAA
- **AgencyIntegrator:** Workflow automation, carrier integrations, process management — already HIPAA-compliant with existing BAA
- Both systems remain the source of truth for all PHI
- **No migration of patient data** — we connect to these systems via their APIs
- **Problem solved:** n8n makes these systems communicate with each other for the first time

### Layer 2: Notion (Non-PHI CRM & Operations Hub)
- Contact records: name, email, phone, agent assignment, lead source, deal stage
- Pipeline tracking with Kanban boards and timeline views
- Task management, follow-up scheduling, activity logs
- Department wikis, SOPs, and process documentation
- Templates for repeatable workflows
- Reporting dashboards (non-PHI metrics: conversion rates, pipeline velocity, agent activity)

**What NEVER goes in Notion:** SSNs, DOBs linked to health data, Medicare/Medicaid IDs, policy numbers, health plan selections, enrollment details, medical conditions, coverage information, signed health documents

### Layer 3: n8n (Integration & Automation Hub)
- Self-hosted on AWS EC2 (automation engine)
- **Key function:** Bridges AgencyBlock and AgencyIntegrator — they finally communicate
- Syncs status information from PHI systems to Notion (sanitized — no PHI transferred)
- Orchestrates all workflows: lead routing, enrollment status updates, notifications
- Runs data hygiene workflows (duplicate detection, deceased record flagging)
- Replaces Zapier with unlimited automations at no per-use cost

### Layer 4: AI via AWS Bedrock (HIPAA-Compliant LLM Access)
- **All LLM usage routes through AWS Bedrock** — a HIPAA-eligible service covered by the AWS BAA
- No separate BAA needed with Anthropic or OpenAI — the AWS BAA covers Bedrock usage
- Available models on Bedrock: Claude (Haiku, Sonnet, Opus), Llama, Mistral, Amazon Titan, and others
- n8n calls Bedrock APIs for all AI operations

### Layer 5: AI Agents (Orchestrated by n8n via Bedrock)
- AI SDR: Lead qualification, email/SMS outreach, follow-up, meeting booking
- AI BDR: Outbound prospecting, list building, personalized outreach
- AI Admin: Data entry, scheduling, compliance document tracking, reporting
- All agent workflows call AWS Bedrock for LLM inference

### Layer 6: Data Hygiene System (AI-Powered)

**Why AI for Data Hygiene?**

Traditional rules-based cleanup tools fail when:
- Names have common variations (Jon/John, Bill/William)
- Addresses use different formats (St/Street, Apt/Unit)
- Deceased status isn't in a death registry (recent deaths, out-of-state deaths)

**AI (Claude Haiku via AWS Bedrock) provides:**
- Fuzzy matching that catches what rules miss
- Pattern recognition for deceased detection beyond death registries
- Context understanding for PHI in free-text fields
- Confidence scoring for automated vs. human-review routing

**Initial Cleanup (Phase 1):**
- **Duplicate detection:** AI compares all records using fuzzy matching on name, address, DOB, phone, Medicare ID
- **Deceased identification:** Cross-references death registries + AI pattern analysis (age, inactivity, communication failures)
- **Data standardization:** Normalizes phone (E.164), address (USPS), name (proper case)
- **Quality scoring:** Rates each record's completeness and flags critical gaps

**Ongoing Hygiene (Phase 2):**
- **New record validation:** Real-time duplicate check before save (n8n workflow + Haiku)
- **Weekly duplicate scan:** AI reviews new records for duplicates created since last scan
- **Monthly death registry check:** Automated batch query against DMF with AI pattern analysis
- **Data quality dashboard:** Notion dashboard showing health metrics in real-time

**Confidence-Based Automation:**

| Confidence | Action | Example |
|------------|--------|---------|
| **90%+** (High) | Auto-applied with audit trail | "Jon Smith" and "John Smith" at same address, same DOB |
| **70–90%** (Medium) | Queued for human review | "J. Smith" at same address — needs confirmation |
| **<70%** (Low) | Flagged only, no action | Similar names at different addresses |

**AI Cost Estimates (Claude Haiku via Bedrock):**

| Task | Volume | Cost |
|------|--------|------|
| Initial cleanup | 10,000 records | $41–$72 |
| Ongoing monthly | All new records + scans | $22–$40/mo |

*Compare to manual review: $2,500–$5,000 for initial cleanup at $25/hr*

---

## Proposal A — PHI Leakage Prevention Plan

The #1 risk in this architecture is PHI accidentally entering Notion. This section defines the technical, procedural, and organizational controls to prevent that.

### Technical Controls (Automated Enforcement)

**1. Notion Property Restrictions**
- Pre-define all allowed database properties in Notion during CRM setup
- Lock database schemas so only admins can add new properties/columns
- Use Notion's Business plan permission controls: restrict who can modify database structures
- No free-text "notes" fields on contact records — use structured dropdowns, selects, and status fields that cannot contain PHI

**2. n8n Workflow Guardrails**
- All data flowing FROM the PHI layer TO Notion passes through a sanitization workflow in n8n
- This workflow strips any PHI fields before writing to Notion — only non-PHI status fields (e.g., "stage: enrolled", "next action: renewal review") get written back
- Build a PHI detection step into the sanitization workflow: use regex patterns to flag SSN formats (XXX-XX-XXXX), Medicare ID patterns, DOB patterns, and health-related keywords before any Notion write
- If PHI is detected in a Notion-bound payload, the workflow halts and sends an alert to the compliance officer
- All n8n workflows that touch PHI are tagged and documented separately; they run only within the AWS environment

**3. n8n-Powered PHI Scanner (Scheduled)**
- Build a recurring n8n workflow (daily or weekly) that reads all Notion database records via the Notion API
- The scanner checks every text field, comment, and property for PHI patterns: SSN, Medicare ID, DOB + health keywords, policy numbers
- Uses an AI classification step (Claude Haiku via AWS Bedrock — fast, cheap, and HIPAA-compliant) to evaluate ambiguous content
- If PHI is found: immediately flag the record, notify the compliance officer, and log the incident in the AWS audit trail
- This acts as a safety net — even if a human manually enters PHI in Notion, it gets caught and remediated

**4. Notion API as the Only Write Path**
- Configure n8n as the primary mechanism for updating Notion databases programmatically
- Human users can view and update non-PHI fields manually, but all automated data flows go through n8n's sanitization layer
- Disable or restrict Notion integrations/embeds that could pull PHI from external sources without going through n8n

**5. AWS-Side Access Controls**
- PHI database (RDS) and document storage (S3) are in a private VPC subnet — no public internet access
- Access only through n8n workflows or authorized admin via VPN/bastion host
- IAM roles follow least-privilege: only the n8n service account and a small number of named admins can read/write PHI
- All access is logged via CloudTrail; anomalous access patterns trigger CloudWatch alarms
- n8n execution data saving is disabled — workflow logs do not persist PHI

### Procedural Controls (Human Behavior)

**6. Data Classification Guide**
- Create a one-page reference document (laminated desk card or Notion wiki page) that clearly defines:
  - **GREEN (Notion-safe):** Name, email, phone, mailing address, agent name, lead source, deal stage, task status, activity dates, dollar amounts, general notes about preferences
  - **RED (AWS/n8n only):** SSN, DOB linked to health info, Medicare/Medicaid ID, policy number, health plan name/selection, enrollment details, medical conditions, prescription info, signed health documents, any communication content referencing health status
- The guide includes real examples specific to the brokerage's daily work

**7. Mandatory Onboarding Training**
- Every user who accesses Notion completes a 30-minute training on the PHI boundary
- Training covers: what PHI is, where it goes (AWS), where it doesn't go (Notion), how to use the system correctly, and what to do if they accidentally enter PHI
- Training is tracked in the LMS (LearnDash) with completion certificates
- Annual refresher required — tied to compliance calendar

**8. Incident Response Procedure**
- If PHI is found in Notion (via the automated scanner or human report):
  1. Immediately delete/redact the PHI from Notion
  2. Log the incident in the AWS audit trail with timestamp, user, and data involved
  3. Notify the compliance officer within 24 hours
  4. Assess whether the exposure constitutes a HIPAA breach (was the data accessed by unauthorized parties?)
  5. If breach threshold is met, follow HIPAA Breach Notification Rule (notify affected individuals within 60 days, report to HHS)
  6. Conduct root cause analysis and update controls to prevent recurrence

### Organizational Controls (Culture)

**9. Compliance Officer Ownership**
- Designate a compliance officer (or assign the role to an existing leader) who owns the PHI boundary
- This person reviews the weekly PHI scanner reports, approves new Notion database properties, and conducts quarterly access audits

**10. Quarterly PHI Boundary Audits**
- Every quarter, review: Notion database schemas for new fields, n8n workflow configurations, AWS access logs, PHI scanner findings
- Document findings and remediation actions
- Include in board/leadership reporting

**11. "PHI-Free Zone" Branding**
- Brand Notion internally as the "PHI-Free Zone" — make it part of the culture
- Add a visible banner or callout on the Notion CRM homepage: "This workspace does not contain Protected Health Information. All PHI is stored securely in our HIPAA-compliant environment."
- Reinforce the boundary in every department meeting during rollout

### Cost of PHI Prevention Controls

| Item | Estimated Cost | Type |
|------|---------------|------|
| n8n sanitization workflow build | Included in integration layer build | One-time |
| n8n PHI scanner workflow build | $1,000–$3,000 | One-time |
| AI classification step (Claude Haiku via Bedrock) | $5–$20/mo | Ongoing (minimal token usage; HIPAA-compliant via AWS BAA) |
| Data classification guide creation | $500–$1,000 | One-time |
| Training module development (LearnDash) | $1,000–$2,000 | One-time |
| Compliance officer time (partial role) | $0–$500/mo | Ongoing (existing employee) |
| **PHI prevention total (one-time)** | **$2,500–$6,000** | |
| **PHI prevention total (ongoing)** | **$5–$520/mo** | |

---

## Proposal A — What Gets Built

1. **AgencyBlock + AgencyIntegrator Integration** — n8n connects both systems via their APIs so they finally communicate
2. **Notion CRM (Non-PHI Layer)** — Contacts, pipeline, tasks, department hubs, SOPs — no PHI
3. **n8n Automation Hub** — Self-hosted on AWS; bridges AgencyBlock, AgencyIntegrator, and Notion; orchestrates all workflows
4. **AWS Bedrock (HIPAA-Compliant AI)** — All LLM inference runs through Bedrock within AWS; covered by AWS BAA
5. **AI SDR Agent** — n8n workflows calling Bedrock (Claude Haiku/Sonnet) for lead qualification and outreach
6. **AI BDR Agent** — Prospecting automation, list enrichment, personalized messaging via Bedrock
7. **AI Admin Agent** — Data entry automation, scheduling, compliance checks, reporting via Bedrock
8. **Integration Layer** — n8n connects all systems: AgencyBlock, AgencyIntegrator, Notion, Medicare Pro, E123, SendGrid, Twilio
9. **Data Hygiene System** — Initial cleanup (deceased records, duplicates, standardization) + ongoing automated hygiene
10. **PHI Prevention System** — Sanitization workflows, scheduled PHI scanner (Bedrock-powered), incident response procedures

---

## Proposal A — Tools Eliminated

| Tool Eliminated | Replaced By | Monthly Savings |
|----------------|-------------|-----------------|
| Active Campaign | Notion CRM + n8n email sequences via SendGrid | $150–$500 |
| EZ Texting | n8n SMS workflows (via Twilio/SendGrid) | $50–$200 |
| slydial | AI agent voicemail capability via n8n | $30–$100 |
| GMass | n8n bulk email via SendGrid | $20–$50 |
| Crisp | Notion intake forms + n8n routing (or retain if chat volume is high) | $25–$95 |
| Quo | AI SDR agent via n8n | $50–$150 |
| Airtable (all 3 instances) | Notion databases | $60–$135 |
| Zapier | n8n (self-hosted — free, pay only for server) | $20–$100 |
| Unbounce | WordPress + Elementor landing pages | $90–$225 |
| Squarespace | Consolidate to WordPress | $16–$49 |
| Five9 | Evaluate: retain for complex calls or replace with AI dialer | $150–$300/seat |

**Total monthly savings from eliminated tools: ~$661–$1,904/mo**

---

## Proposal A — Tools Retained

| Tool | Monthly Cost | Why It Stays |
|------|-------------|-------------|
| WordPress + WP Engine + Elementor | $25–$77 | Main website and landing pages |
| HIPAA Vault | $50–$300 | Compliance hosting — non-negotiable |
| Medicare Pro + E123 | $150–$500 | Core enrollment and quoting tools |
| SendGrid (Twilio) | $15–$90 | Transactional + marketing email backend; SMS via Twilio |
| AWS | $50–$500+ | Infrastructure for n8n, AI agents, and any existing workloads |
| Canva | $13–$30 | Content design |
| Riverside + Libsyn | $20–$44 | Podcast production (if continuing) |
| Tax Bandits | ~$4 | Tax filing (seasonal) |
| LearnDash (or Cloud Academy) | $13–$55 | Training — pick one, eliminate the other |
| Fathom Analytics | $14–$24 | Privacy-compliant website analytics |

**Retained tool spend: ~$354–$1,624/mo**

---

## Proposal A — New Costs (Detailed Breakdown)

### Notion (Non-PHI CRM Layer)

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| Notion Business plan | $20/user/mo (annual) or $24/user/mo (monthly) | Per-seat; Business tier needed for SAML SSO, private teamspaces, advanced permissions, locked database schemas |
| Estimated seats (10 users) | $200–$240/mo | Scales linearly per user added |
| Estimated seats (25 users) | $500–$600/mo | Scales linearly per user added |

*Notion Business plan (not Enterprise) is sufficient here because PHI is not stored in Notion — no BAA required from Notion. Business tier provides the permission controls needed to lock database schemas and enforce the PHI-free boundary.*

### n8n (Self-Hosted on AWS)

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| n8n Community Edition license | $0 | Free and open-source for self-hosting |
| AWS EC2 for n8n (t3.medium or similar) | $30–$80/mo | Instance + EBS storage; handles automation workloads |
| DevOps/maintenance time | $0–$500/mo | Internal time or contractor for updates, monitoring, security patches |

*n8n self-hosted is free software with unlimited executions. You pay only for the AWS server. Execution data saving is disabled to prevent PHI persistence in workflow logs.*

### AWS PHI Environment (HIPAA-Compliant Layer)

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| AWS BAA (Business Associate Agreement) | $0 | Free — requested through AWS Artifact |
| RDS PostgreSQL (encrypted, PHI database) | $25–$75/mo | db.t3.medium with Multi-AZ for reliability; KMS encryption at rest |
| S3 (encrypted, PHI documents) | $5–$20/mo | Server-side encryption (SSE-KMS); versioning enabled; lifecycle policies |
| EC2 for AI agent services | $50–$150/mo | t3.large or equivalent; runs within private VPC subnet |
| VPC + NAT Gateway | $35–$50/mo | Private subnet isolation; NAT for outbound-only internet access |
| CloudTrail + CloudWatch | $10–$30/mo | Audit logging (required for HIPAA); alarms for anomalous access |
| KMS (Key Management Service) | $1–$5/mo | Encryption key management for RDS and S3 |
| Data transfer | $5–$30/mo | API calls between n8n, PHI database, and external services |
| **AWS PHI subtotal** | **$131–$360/mo** | |

*This is the HIPAA-compliant layer. AWS signs a BAA at no cost. The compliance burden is on configuring the environment correctly: encryption, private networking, access controls, and audit logging. This replaces the need for any third-party HIPAA add-on.*

### AI Agent Development

| Line Item | Estimated Cost | Pricing Basis |
|-----------|---------------|---------------|
| AI SDR agent build (n8n workflows + Bedrock integration) | $8,000–$20,000 | One-time: workflow design, prompt engineering, testing, SMS/email integration |
| AI BDR agent build | $5,000–$15,000 | One-time: prospecting logic, list enrichment, outreach sequences |
| AI Admin agent build | $5,000–$15,000 | One-time: data entry automation, scheduling, compliance checks |
| Notion CRM setup & configuration | $3,000–$8,000 | One-time: database architecture, relations, views, templates, migration |
| Integration layer (n8n to Medicare Pro, E123, etc.) | $5,000–$15,000 | One-time: API connections, data sync, error handling |

### PHI Prevention System

| Line Item | Estimated Cost | Pricing Basis |
|-----------|---------------|---------------|
| n8n sanitization workflows | Included in integration layer | One-time: built as part of the Notion-to-AWS data bridge |
| n8n PHI scanner workflow | $1,000–$3,000 | One-time: scheduled scan of all Notion databases for PHI patterns |
| Data classification guide | $500–$1,000 | One-time: one-page reference for all staff |
| HIPAA/PHI boundary training module | $1,000–$2,000 | One-time: built in LearnDash with completion tracking |
| **PHI prevention subtotal (one-time)** | **$2,500–$6,000** | |

### AWS Bedrock — AI/LLM Costs (Ongoing)

All AI inference runs through AWS Bedrock. This is a HIPAA-eligible service covered by the AWS BAA. PHI never leaves the AWS environment — no separate BAA with Anthropic or OpenAI is needed.

**Why Bedrock instead of direct API calls:**
- Bedrock is already covered by your AWS BAA — no additional compliance agreements
- LLM requests stay inside the same VPC as your PHI database and n8n instance
- Eliminates the risk of accidentally sending PHI to a non-compliant external API
- One access path for all AI = simpler architecture, simpler audit trail

| Model (via Bedrock) | Cost per 1M Tokens | Use Case | Est. Monthly Usage | Est. Monthly Cost |
|--------------------|--------------------|---------|--------------------|-------------------|
| Claude 3.5 Haiku | $1 input / $5 output | PHI scanning, classification, outreach drafts, simple responses | ~3M input + 800K output | $7.00 |
| Claude 3.5 Sonnet | $3 input / $15 output | Lead qualification, enrollment analysis, complex reasoning | ~1M input + 300K output | $7.50 |
| Claude 4.1 Opus | $15 input / $75 output | High-stakes decisions, compliance review (low volume) | ~100K input + 50K output | $5.25 |
| Amazon Titan (text) | $0.20 input / $0.60 output | Embeddings, lightweight text tasks | ~2M input + 500K output | $0.70 |
| **Blended estimate** | | | | **$50–$350/mo** |

**Bedrock cost optimization options:**
- **Batch inference** — 50% discount for non-time-sensitive jobs (e.g., nightly PHI scans, bulk classification)
- **Intelligent prompt routing** — Bedrock auto-routes between Sonnet and Haiku based on prompt complexity, reducing costs up to 30%
- **Provisioned throughput** — For predictable high-volume workloads, purchase dedicated model units for consistent per-token pricing
- **Prompt caching** — 90% discount on cached input tokens for repetitive workflows (e.g., same system prompt across all SDR outreach)

*Bedrock pricing is on-demand per-token with no upfront commitment. A brokerage doing 500 outreach actions/day with AI-assisted PHI processing might spend $50–$150/mo. High-volume operations with complex multi-step reasoning could reach $250–$350/mo.*

---

## Proposal A — Total Cost Summary (UPDATED)

### One-Time Costs

| Item | Low | High |
|------|-----|------|
| Notion CRM setup & config | $3,000 | $8,000 |
| AI SDR agent build | $8,000 | $20,000 |
| AI BDR agent build | $5,000 | $15,000 |
| AI Admin agent build | $5,000 | $15,000 |
| Integration layer (n8n → AgencyBlock, AgencyIntegrator, Notion, etc.) | $6,000 | $18,000 |
| PHI prevention system (scanner, training, guide) | $2,500 | $6,000 |
| **Data hygiene: initial cleanup (AI-powered)** | $4,000 | $10,000 |
| Data migration (from Airtable, Active Campaign, etc.) | $2,000 | $5,000 |
| Training & change management | $1,000 | $3,000 |
| **TOTAL ONE-TIME** | **$36,500** | **$100,000** |

*Note: AWS PHI environment setup removed — AgencyBlock and AgencyIntegrator already provide HIPAA-compliant storage. Integration layer cost increased to account for connecting to these existing systems.*

### Monthly Ongoing Costs

| Item | Low (10 seats) | High (25 seats) |
|------|----------------|-----------------|
| Notion Business | $200 | $600 |
| n8n self-hosted (AWS server) | $30 | $80 |
| AWS Bedrock AI costs (agents + data hygiene) | $55 | $350 |
| **Data hygiene automation (AI-powered)** | $50 | $100 |
| n8n maintenance/DevOps | $0 | $500 |
| Retained tools (see above) | $354 | $1,624 |
| **TOTAL MONTHLY ONGOING** | **$689** | **$3,254** |
| **TOTAL ANNUAL ONGOING** | **$8,268** | **$39,048** |

*Note: AWS PHI environment costs (RDS, S3, VPC) removed — patient data stays in AgencyBlock/AgencyIntegrator. AgencyBlock and AgencyIntegrator costs continue as-is (already in budget).*

---

## Proposal A — Timeline (UPDATED)

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery; data classification; **AgencyBlock/AgencyIntegrator API audit**; **data hygiene assessment** | Weeks 1–3 | Process map + API integration plan + data quality report |
| Phase 1 | Notion CRM build (databases, relations, views, templates, locked schemas) | Weeks 4–6 | CRM operational (non-PHI) |
| Phase 2 | n8n setup + **AgencyBlock/AgencyIntegrator integration** (the core bridge) | Weeks 4–8 | Systems communicate for the first time |
| Phase 3 | **Data hygiene Phase 1** — initial cleanup (deceased records, duplicates, standardization) | Weeks 5–8 | Critical data cleaned |
| Phase 4 | Core automations (lead routing, notifications, status sync, sanitization workflows) | Weeks 7–10 | n8n live; PHI boundary enforced |
| Phase 5 | PHI scanner workflow + incident response procedures | Weeks 8–10 | Automated PHI detection active |
| Phase 6 | AI SDR agent (email + SMS outreach sequences via n8n) | Weeks 9–13 | SDR agent in testing |
| Phase 7 | AI BDR agent (prospecting + list building) | Weeks 11–15 | BDR agent in testing |
| Phase 8 | AI Admin agent (scheduling, data entry, compliance) | Weeks 13–17 | Admin agent in testing |
| Phase 9 | **Data hygiene Phase 2** — full cleanup completed, ongoing automation enabled | Weeks 10–14 | Clean data + automated hygiene |
| Phase 10 | Integration layer (Medicare Pro, E123, retained tools) | Weeks 14–18 | All integrations live |
| Phase 11 | Migration & legacy tool decommission (dept by dept) | Weeks 16–22 | Redundant tools canceled |
| Phase 12 | Training, change management, stabilization, **data quality dashboard live** | Weeks 18–24 | Full rollout; all staff trained |

**Total: ~6 months to full deployment**

*Note: Phases 1–3 run in parallel. Key difference from previous plan: we're integrating existing systems instead of building new PHI infrastructure. Data hygiene is a major component.*

---

## Proposal A — Pros & Cons (UPDATED)

**Pros**
- **Keeps existing HIPAA-compliant systems** — AgencyBlock and AgencyIntegrator stay in place; no risky migration
- **Finally makes AgencyBlock and AgencyIntegrator communicate** — eliminates manual workarounds
- **Includes data hygiene** — cleans up years of deceased records, duplicates, and messy data
- Notion is familiar, flexible, and fast to configure — no custom software development for the CRM
- n8n self-hosted gives unlimited automations at near-zero marginal cost
- AI agents tuned to insurance sales workflows — competitive differentiator
- No per-seat SaaS fees for automation (n8n) — only Notion scales per seat
- You own all data — no vendor lock-in on the automation layer
- All AI runs through AWS Bedrock (HIPAA-eligible) — covered by AWS BAA
- PHI prevention system provides automated, continuous compliance monitoring
- Clear separation of concerns: business users work in Notion, PHI stays in AgencyBlock/AgencyIntegrator

**Cons**
- Split architecture adds complexity — multiple systems to maintain
- PHI boundary requires ongoing vigilance (mitigated by automated scanner + training)
- Notion is not a purpose-built CRM — has limitations on relational data, reporting, and scale (10K+ records can slow down)
- n8n self-hosted requires some DevOps knowledge to maintain
- AI agents require upfront build investment and ongoing prompt tuning
- Longer deployment timeline (~6 months vs. ~3.5 months for GHL)
- **AgencyBlock/AgencyIntegrator API limitations may constrain some integrations** — mitigated by thorough API audit in Phase 0

---

<div style="page-break-after: always;"></div>

# 6. Proposal B: GoHighLevel + Automation

## Proposal B — Philosophy

Use GoHighLevel (GHL) as the all-in-one platform. Strip out redundant tools. Layer basic automation on top.

**Fastest path to consolidation. Lowest ongoing complexity.**

---

## Proposal B — Architecture

**GoHighLevel (All-in-One)**
- CRM, Email, SMS, Landing Pages, Forms
- Pipeline, Calendar, Chat Widget, Reporting
- Built-in automation workflows

**Supplemented By**
- Zapier (reduced scope) / GHL native workflows
- Lead routing, follow-up triggers, enrollment alerts, reporting sync

---

## Proposal B — Tools Eliminated

| Tool Eliminated | GHL Feature That Replaces It | Est. Monthly Savings |
|----------------|------------------------------|---------------------|
| Active Campaign | Email marketing + automation workflows | $150–$500 |
| EZ Texting | Built-in SMS (usage-based: ~$0.0079/segment) | $50–$200 |
| slydial | Voicemail drop feature (built-in) | $30–$100 |
| GMass | Email campaigns via GHL | $20–$50 |
| Crisp | Chat widget (built-in) | $25–$95 |
| Quo | Pipeline + sequences (built-in) | $50–$150 |
| Unbounce | Landing page / funnel builder (built-in) | $90–$225 |
| Gravity Forms / Fluent Forms | Built-in forms | $10–$30 |
| Airtable (all 3 instances) | Custom fields / database (built-in) | $60–$135 |
| Five9 | Built-in dialer (evaluate capability vs. Five9) | $150–$300/seat |
| Squarespace | Funnel / site builder (built-in) | $16–$49 |

**Total monthly savings from eliminated tools: ~$651–$1,834/mo**

---

## Proposal B — Tools Retained

| Tool | Monthly Cost | Why It Stays |
|------|-------------|-------------|
| WordPress + WP Engine + Elementor | $25–$77 | Main website — GHL funnels supplement, not replace |
| HIPAA Vault | $50–$300 | Compliance hosting — verify GHL HIPAA status independently |
| Medicare Pro + E123 | $150–$500 | Core enrollment and quoting tools |
| SendGrid (Twilio) | $15–$90 | May still be needed for high transactional email volume |
| AWS | $50–$500+ | If anything critical currently runs here |
| Canva | $13–$30 | Content design |
| Riverside + Libsyn | $20–$44 | Podcast production (if continuing) |
| Tax Bandits | ~$4 | Tax filing (seasonal) |
| LearnDash (or Cloud Academy) | $13–$55 | Training — pick one |
| Zapier (reduced) | $20–$50 | Only for integrations GHL can't handle natively |
| Fathom Analytics | $14–$24 | Supplement GHL's built-in reporting |

**Retained tool spend: ~$374–$1,674/mo**

---

## Proposal B — New Costs (Detailed Breakdown)

### GoHighLevel Subscription

| Plan Option | Monthly Cost | What's Included | Notes |
|------------|-------------|-----------------|-------|
| **Starter** | $97/mo | Core CRM, funnels, email/SMS, 2–3 sub-accounts | Sufficient for single-location brokerage |
| **Unlimited** | $297/mo | Everything in Starter + unlimited sub-accounts, white-label desktop | Better for multi-department/multi-vertical orgs |
| **SaaS Pro** | $497/mo | Everything + SaaS mode, AI rebilling, advanced API | Overkill unless reselling GHL to sub-agents |

*Recommended: **Unlimited at $297/mo** — the multi-department structure of The Brokerage Inc. will likely need multiple sub-accounts and the advanced workflow features.*

### GHL Usage-Based Costs

| Usage Type | Cost Per Unit | Est. Monthly Volume | Est. Monthly Cost |
|-----------|--------------|--------------------|--------------------|
| SMS outbound | $0.0079/segment | 5,000 segments | $39.50 |
| MMS outbound | $0.02/message | 500 messages | $10.00 |
| Outbound calls | $0.018/minute | 2,000 minutes | $36.00 |
| Inbound calls | $0.0085/minute | 1,000 minutes | $8.50 |
| Email sending | $0.675/1,000 emails | 20,000 emails | $13.50 |
| Phone number verification | $2.50/1,000 | 500 verifications | $1.25 |
| **Usage subtotal** | | | **~$109/mo** |

*Usage costs scale with activity. A high-volume sales operation could push this to $200–$400/mo. Low activity could drop it to $30–$50/mo.*

### GHL HIPAA Compliance Add-On

| Item | Cost | What It Includes |
|------|------|-----------------|
| HIPAA compliance package | $297/mo (or $2,970/yr) | Encryption, BAA, audit logging, MFA enforcement |

**This is mandatory if any PHI (Protected Health Information) flows through GHL.** For a Medicare brokerage, this is almost certainly required. This cost is frequently overlooked in GHL proposals.

### GHL AI Employee (Optional)

| Item | Cost | What It Includes |
|------|------|-----------------|
| AI Employee bundle | $97/mo per sub-account | Conversation AI, Voice AI, Reviews AI, Content AI, Workflow AI |
| Pay-as-you-go alternative | Usage-based | Per-interaction pricing — better for low volume |

*Optional but relevant: if you want AI-powered chat, voice, or content within GHL, this is an additional cost.*

### One-Time Setup Costs

| Item | Cost | Pricing Basis |
|------|------|---------------|
| GHL account setup & configuration | $2,000–$5,000 | Consultant or agency; pipelines, automations, custom fields |
| Data migration (contacts, tags, pipelines from AC + Airtable) | $1,500–$4,000 | Volume of records, number of source systems, data cleanup |
| Automation / workflow buildout | $2,000–$6,000 | Number and complexity of workflows; lead routing, sequences, alerts |
| Landing page / form migration | $500–$2,000 | Number of pages/forms to recreate in GHL |
| Training & change management | $1,000–$3,000 | Per-department training sessions, documentation, support |

---

## Proposal B — Total Cost Summary

### One-Time Costs

| Item | Low | High |
|------|-----|------|
| GHL setup & configuration | $2,000 | $5,000 |
| Data migration | $1,500 | $4,000 |
| Automation / workflow buildout | $2,000 | $6,000 |
| Landing page / form migration | $500 | $2,000 |
| Training & change management | $1,000 | $3,000 |
| **TOTAL ONE-TIME** | **$7,000** | **$20,000** |

### Monthly Ongoing Costs

| Item | Low | High |
|------|-----|------|
| GHL Unlimited subscription | $297 | $297 |
| GHL usage-based costs (SMS, calls, email) | $50 | $400 |
| GHL HIPAA compliance add-on | $297 | $297 |
| GHL AI Employee (optional) | $0 | $97 |
| Retained tools (see above) | $374 | $1,674 |
| **TOTAL MONTHLY ONGOING** | **$1,018** | **$2,765** |
| **TOTAL ANNUAL ONGOING** | **$12,216** | **$33,180** |

*Note: Without HIPAA compliance ($297/mo), the low end drops to $721/mo / $8,652/yr. But for a Medicare brokerage this is likely non-optional.*

---

## Proposal B — Timeline

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery & requirements | Weeks 1–3 | Process map complete |
| Phase 1 | GHL setup, HIPAA compliance verification & activation | Week 4 | GHL account configured |
| Phase 2 | CRM migration (contacts, pipelines, tags) | Weeks 5–7 | Contacts & pipelines live |
| Phase 3 | Communication migration (email, SMS, chat) | Weeks 6–8 | All comms through GHL |
| Phase 4 | Landing pages & forms migration | Weeks 7–9 | Pages & forms live |
| Phase 5 | Automation buildout (GHL workflows) | Weeks 8–10 | Workflows active |
| Phase 6 | Legacy tool decommission (dept by dept) | Weeks 9–12 | Redundant tools canceled |
| Phase 7 | Training & change management | Weeks 10–14 | All departments onboarded |

**Total: ~3.5 months to full deployment**

---

## Proposal B — Pros & Cons

**Pros**
- Fast deployment (~3.5 months vs. ~5.5 months)
- Low upfront cost ($7K–$20K vs. $29K–$81K)
- Purpose-built CRM — pipelines, automations, and reporting out of the box
- Single platform for sales, marketing, and communication
- No engineering team required for maintenance
- Not contact-based pricing — unlimited contacts on all plans

**Cons**
- HIPAA add-on ($297/mo) significantly increases monthly cost
- Usage-based fees (SMS, calls, email) can be unpredictable
- Vendor lock-in — migrating off GHL later is painful
- Less customizable than Notion + n8n
- May not handle all insurance-specific workflows natively
- GHL AI features cost extra ($97/mo per sub-account)

---

<div style="page-break-after: always;"></div>

# 7. Hours Saved & ROI Analysis

## Estimated Hours Recaptured Per Week

Based on industry data for insurance brokerages (Salary.com Jan 2026, PayScale 2025) and conservative automation estimates.

**Blended hourly cost: ~$23/hr** (weighted: agents $28–31/hr at 60%, admin $15–17/hr at 30%, management $35–45/hr at 10%)

### Proposal A (Notion + n8n + AI Agents + Data Hygiene)

| Category | Current Hours/Wk | After Automation | Saved/Wk | Annual Hours Saved |
|----------|-----------------|-----------------|----------|-------------------|
| AI SDR (lead qual, outreach, follow-up) | 24–38 | 3–4.5 | 21–33.5 | 1,092–1,742 |
| AI BDR (prospecting, list building) | 11–18 | 1.5–2 | 9.5–16 | 494–832 |
| AI Admin (data entry, scheduling, compliance) | 17–28 | 3–5 | 14–23 | 728–1,196 |
| **Manual workarounds (AgencyBlock ↔ AgencyIntegrator)** | 5–10 | 0 | 5–10 | 260–520 |
| Tool consolidation (context switching, duplicate entry) | 7–13 | 1 | 6–12 | 312–624 |
| **TOTAL** | **64–107** | **8.5–12.5** | **55.5–94.5** | **2,886–4,914** |

**Equivalent to 1.4–2.4 FTEs returned to revenue-generating work.**

### Proposal B (GoHighLevel)

GHL automates tool consolidation and basic workflows but lacks custom AI agents.

| Category | Saved/Wk | Annual Hours Saved |
|----------|----------|-------------------|
| Basic workflow automation (sequences, triggers) | 10–18 | 520–936 |
| Tool consolidation (fewer platforms) | 6–12 | 312–624 |
| Built-in forms/landing pages (no switching) | 2–5 | 104–260 |
| **TOTAL** | **18–35** | **1,040–1,820** |

---

## Financial Value & ROI

### Annual Value Created (UPDATED)

| Value Source | Proposal A (Conservative) | Proposal A (Optimistic) | Proposal B (Mid-Range) |
|-------------|--------------------------|------------------------|----------------------|
| Labor value recovered (hours × $23/hr) | $66,378 | $113,022 | $32,890 |
| Tool cost savings (eliminated tools) | $8,172 | $27,648 | $14,910 |
| **Total annual value** | **$74,550** | **$140,670** | **$47,800** |

*Note: Proposal A now includes hours saved from eliminating manual workarounds between AgencyBlock and AgencyIntegrator.*

### ROI by Year (10-Seat Scenario) — UPDATED

| Period | Proposal A (Conservative) | Proposal A (Optimistic) | Proposal B |
|--------|--------------------------|------------------------|------------|
| Year 1 investment | $58,768 | $58,768 | $19,216 |
| Year 1 net value | +$15,782 | +$81,902 | +$28,584 |
| **Year 1 ROI** | **27%** | **139%** | **149%** |
| Year 2 cost (ongoing + retainer) | $26,268 | $26,268 | $12,216 |
| Year 2 net value | +$48,282 | +$114,402 | +$35,584 |
| **Year 2 ROI** | **184%** | **436%** | **291%** |
| **3-Year cumulative net value** | **+$111,564** | **+$280,104** | **+$99,752** |
| **Payback period** | **~9 months** | **~5 months** | **~5 months** |

**Key insight:** Proposal B pays back faster due to lower upfront cost, but Proposal A generates 1.1–2.8x more cumulative value by Year 3 due to AI agent automation + system integration. The gap widens every year. Option B also does NOT solve the AgencyBlock/AgencyIntegrator communication problem.

### Revenue Upside (Not Modeled)

The above ROI captures cost savings and labor efficiency only. It does not include:
- Agents spending 20+ more hours/week selling instead of admin work
- Faster lead response times (AI SDR responds in minutes vs. hours/days)
- Higher contact rates from automated multi-channel outreach
- Reduced lead leakage from centralized pipeline tracking
- Reduced AEP/OEP seasonal staffing needs

If even 10% of recovered agent hours convert to additional enrollments, the revenue impact dwarfs the cost savings.

---

<div style="page-break-after: always;"></div>

# 8. Side-by-Side Comparison

| Factor | Proposal A (Notion + n8n + AI) | Proposal B (GoHighLevel) |
|--------|-------------------------------|--------------------------|
| **One-time cost** | $33,000–$91,000 | $7,000–$20,000 |
| **Monthly ongoing (10 seats)** | $770–$1,560 | $1,018–$1,870 |
| **Monthly ongoing (25 seats)** | $1,370–$3,514 | $1,018–$2,765 |
| **Annual ongoing (10 seats)** | $9,240–$18,720 | $12,216–$22,440 |
| **Annual ongoing (25 seats)** | $16,440–$42,168 | $12,216–$33,180 |
| **Time to full deployment** | ~6 months | ~3.5 months |
| **Tools eliminated** | ~11 | ~11 |
| **CRM flexibility** | High (Notion is infinitely customizable) | Moderate (GHL is opinionated) |
| **Automation cost at scale** | Near-zero (n8n self-hosted) | Usage-based fees grow with volume |
| **AI capabilities** | Custom agents via AWS Bedrock — full control, HIPAA-compliant | GHL AI Employee add-on ($97/mo) |
| **AI HIPAA compliance** | Covered by AWS BAA — no separate AI vendor agreement | Covered by GHL HIPAA add-on ($297/mo) |
| **Engineering required** | Some (n8n + AWS maintenance, AI tuning) | Minimal |
| **Vendor lock-in** | Low (Notion export + open-source n8n) | High (GHL is proprietary) |
| **HIPAA compliance** | Split architecture: no PHI in Notion; AWS BAA (free) + self-managed encryption | $297/mo add-on (non-cancelable) |
| **HIPAA ongoing cost** | $0 (BAA free; infra cost already in AWS line) | $297/mo ($3,564/yr) |
| **PHI leakage risk** | Mitigated: automated scanner, sanitization workflows, training, incident response | Low (single platform handles PHI natively) |
| **Scalability (seats)** | Notion cost grows per seat | GHL unlimited contacts, flat subscription |
| **Scalability (volume)** | n8n unlimited executions | GHL usage fees grow with volume |

---

# Cost Comparison Summary

## Year 1 (Including Setup)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| **Current state (estimated)** | $17,784–$60,996 | $17,784–$60,996 |
| **Proposal A (Notion + n8n + AI)** | $42,240–$109,720 | $49,440–$133,168 |
| **Proposal B (GoHighLevel)** | $19,216–$42,440 | $19,216–$53,180 |

## Year 2+ (Ongoing Only)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| **Current state (estimated)** | $17,784–$60,996 | $17,784–$60,996 |
| **Proposal A (Notion + n8n + AI)** | $9,240–$18,720 | $16,440–$42,168 |
| **Proposal B (GoHighLevel)** | $12,216–$22,440 | $12,216–$33,180 |

**Key insight:** Proposal A has higher Year 1 costs due to the AI agent build + PHI infrastructure investment, but lower ongoing costs from Year 2 onward — especially at scale. The AWS BAA is free vs. GHL's non-cancelable $3,564/yr HIPAA add-on. All AI runs through AWS Bedrock (HIPAA-eligible) at per-token pricing with no platform fee — vs. GHL's $97/mo AI Employee add-on. n8n has no per-execution fees. Proposal B is cheaper to start but the mandatory HIPAA add-on and usage-based fees narrow the gap significantly over time. At the 10-seat level, Proposal A becomes cheaper than Proposal B partway through Year 2.

---

<div style="page-break-after: always;"></div>

# 9. The Hybrid Option

**Best of both worlds — phased approach:**

1. **Now:** Deploy GHL (Proposal B) to stop the bleeding on redundant tools
2. **Months 4–6:** Stabilize operations on GHL
3. **Months 6–12:** Build Notion hub for operations/documentation + n8n for custom automations alongside GHL
4. **Year 2:** Layer AI agents on top; evaluate whether GHL stays as front-end or gets replaced

This gives immediate consolidation wins while building toward the more powerful Notion + n8n + AI stack without rushing it.

---

<div style="page-break-after: always;"></div>

# 10. Recommendation

Start with **Phase 0** regardless of proposal chosen.

The process mapping will:
- Reveal which tools are truly redundant vs. serving unique needs
- Surface compliance requirements that constrain platform choices
- Give every department a voice before changes happen
- Produce the requirements needed to evaluate both proposals with real data
- Determine actual seat count and volume — which directly impacts cost comparisons

---

<div style="page-break-after: always;"></div>

# 11. Change Management Strategy

Given the number of departments and verticals, change management is critical.

- **Assign a change champion per department** — someone who owns the transition for their team
- **Communicate the "why" before the "what"** — people resist changes they don't understand
- **Run parallel systems during transition** — no cold cutovers
- **Build feedback loops into every phase** — weekly check-ins during migration
- **Document everything** — fill the gap left by the previous tech lead
- **Quick wins first** — eliminate obviously orphaned tools early to build momentum

---

<div style="page-break-after: always;"></div>

# 12. Next Steps

1. Schedule Monday discussion to review this plan
2. **Immediate:** Verify whether Active Campaign is currently on an Enterprise plan with a signed BAA — if not, there is an existing HIPAA compliance gap
3. Complete Phase 0 process discovery (Weeks 1–3), including PHI data classification across all workflows
4. Audit every tool for active usage, contract terms, and renewal dates
5. Confirm seat count across departments (directly impacts Proposal A vs. B economics)
6. If Proposal A is selected: sign AWS BAA via AWS Artifact; begin VPC + encryption setup in parallel with Notion CRM build
7. Present refined proposals with validated cost projections
8. Select approach and begin department-by-department rollout
