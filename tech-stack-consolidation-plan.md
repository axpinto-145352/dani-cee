# Tech Stack Consolidation
## The Brokerage Inc. — Build-Out Plan

---

# The Problem

The Brokerage Inc. has accumulated 45+ tools across siloed departments. The previous tech lead departed without documentation. Redundancies are costing money and creating confusion. It's time to consolidate.

---

# Our Approach: Foundation First

Before selecting tools, we map the actual processes. Start analog, then rebuild the tech layer on top.

**Phase 0 comes first — regardless of which proposal is chosen.**

---

# Phase 0: Process Discovery

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

---

# Current Tool Inventory & Cost Estimates

All costs below are estimates based on typical published plan pricing. Actual amounts require a contract and billing audit during Phase 0.

---

## CRM / Sales / Outreach

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Active Campaign | Email marketing / CRM | $150–$500 | Tiered by contact count: Starter ~$15/mo (500 contacts), Professional scales to $500+ for large lists | Redundant — replace |
| EZ Texting | SMS outreach | $50–$200 | Plans start ~$20/mo for 500 credits; scales by message volume | Redundant — replace |
| slydial | Voicemail drops | $30–$100 | Per-use credits (~$0.05–$0.10/drop) or monthly subscription packs | Niche — evaluate |
| GMass | Bulk email via Gmail | $20–$50 | Standard plan ~$20/mo per Gmail account; Premium ~$30; Enterprise ~$50 | Redundant — replace |
| Five9 | Contact center / dialer | $150–$300/seat | Core plan ~$149/seat/mo; per-minute telecom usage added on top | Core — evaluate replacement |
| Crisp | Live chat / messaging | $25–$95 | Free basic; Pro ~$25/mo; Unlimited ~$95/mo per workspace | Redundant — replace |
| Quo | Sales engagement | $50–$150 | Per-seat SaaS pricing; varies by plan tier | Redundant — replace |

**Category subtotal: ~$475–$1,395/mo**

---

## Marketing / Content / SEO

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Canva | Design | $13–$30 | Pro ~$13/mo (1 user); Teams ~$30/mo per 5 users | Keep |
| Riverside | Podcast/video recording | $15–$24 | Standard ~$15/mo; Business ~$24/mo; per-seat | Keep if podcast continues |
| Testimonial.to | Video testimonials | $20–$50 | Starter ~$20/mo; Premium ~$50/mo; based on # of testimonials | Evaluate ROI |
| UberSuggest | SEO research | $30–$50 | Individual ~$29/mo; Business ~$49/mo; lifetime deals available | Redundant — evaluate |
| Unbounce | Landing pages | $90–$225 | Launch ~$90/mo; Optimize ~$225/mo; based on conversions/pages | Redundant — replace |
| SEO articles | Content/SEO service | $200–$500+ | Vendor pricing — per article or monthly retainer | Clarify vendor vs. internal |
| Liberated Syndication | Podcast hosting | $5–$20 | Classic plans $5–$20/mo based on storage per month | Keep if podcast continues |
| YouTube Premium | Video | $14 | Fixed subscription price | Likely personal — remove |
| BrightFire | Insurance marketing | $100–$500 | Insurance-specific marketing packages; appears duplicated in inventory — confirm one sub | Confirm single subscription |

**Category subtotal: ~$487–$1,413/mo**

---

## Website / Web Infrastructure

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| WordPress (main) | Primary website | $0 | Open-source CMS — free | Keep |
| WP Engine | WordPress hosting | $20–$60 | Startup ~$20/mo (1 site, 25K visits); Growth ~$60/mo (10 sites) | Keep |
| Staging environment TBI | Dev/staging | $0 | Included with WP Engine hosting plans | Keep |
| Squarespace | Secondary site | $16–$49 | Personal ~$16/mo; Business ~$33/mo; Commerce ~$49/mo | Redundant — eliminate |
| Elementor | Page builder | $5–$17 | Essential ~$5/mo (1 site); Advanced ~$17/mo (25 sites); billed annually | Keep w/ WordPress |
| Gravity Forms | WordPress forms | $5–$20 | Basic ~$5/mo; Elite ~$20/mo; billed annually per-site license | Redundant — pick one |
| Fluent Forms | WordPress forms | $5–$10 | Single site ~$5/mo; agency ~$10/mo; billed annually | Redundant — pick one |
| Forgravity | Gravity Forms add-ons | $10–$20 | Annual license divided monthly; depends on add-on bundle | Eliminate if Gravity goes |
| Imagify | Image optimization | $5–$10 | Starter free (20MB); Growth ~$5/mo (500MB); Infinite ~$10/mo | Keep — low cost |
| Gravatar | Profile avatars | $0 | Free service | Keep |

**Category subtotal: ~$66–$186/mo**

---

## Data / Automation / Backend

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Airtable (Admin) | Database / ops | $20–$45/seat | Team ~$20/seat/mo; Business ~$45/seat/mo; scales by seats and records | Redundant — replace |
| Airtable | General use | $20–$45/seat | Same pricing as above — separate workspace or base | Redundant — replace |
| Airtable OTP | Unknown use case | $20–$45/seat | Same pricing — unknown what this base serves | Investigate |
| Zapier | Automation | $20–$100+ | Starter ~$20/mo (750 tasks); Professional ~$50/mo (2K tasks); Team ~$100/mo | Evaluate per proposal |
| SendGrid (Twilio) | Transactional email | $15–$90 | Free tier (100/day); Essentials ~$15/mo (50K emails); Pro ~$90/mo (100K emails) | May keep for volume |
| Amazon Web Services | Cloud infra | $50–$500+ | Usage-based: EC2 instances, S3 storage, data transfer — highly variable | Evaluate what runs here |
| Couchdrop | File transfer / SFTP | $15–$50 | Starter ~$15/mo; Business ~$50/mo; based on storage and users | Evaluate necessity |
| HIPAA Vault | HIPAA hosting/storage | $50–$300 | Managed HIPAA hosting; pricing by server size and compliance tier | **Keep — non-negotiable** |
| Streamlit | Data apps / dashboards | $0–$250 | Community Cloud free; Teams ~$250/mo for private apps | Evaluate what it powers |
| Basefront | Unknown | TBD | Cannot confirm pricing — tool needs investigation | Investigate |

**Category subtotal: ~$210–$1,425/mo** (varies heavily by seats/usage)

---

## Industry-Specific / Enrollment

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Medicare Pro | Enrollment platform | $100–$300 | Industry-specific licensing; per-agent or flat monthly | **Keep — core business** |
| Medicare Pro Test | Testing environment | $0 | Included with Medicare Pro subscription | Keep |
| E123 | Enrollment / quoting | $50–$200 | Per-agent licensing for enrollment/quoting platform | **Keep — core business** |

**Category subtotal: ~$150–$500/mo**

---

## Learning / Training

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Cloud Academy | Training platform | $40–$55/seat | Individual ~$40/seat/mo; Team ~$55/seat/mo; enterprise negotiated | Redundant — pick one |
| LearnDash | LMS (WordPress) | $13–$30 | 1 site ~$13/mo; 10 sites ~$30/mo; billed annually | Redundant — pick one |

**Category subtotal: ~$53–$85/mo** (single-seat estimate)

---

## Compliance / Finance / Other

| Tool | Function | Est. Monthly Cost | Where the Cost Comes From | Status |
|------|----------|-------------------|--------------------------|--------|
| Tax Bandits | Tax filing | ~$4/mo (~$50/yr) | Per-form pricing (e.g. $3–$5 per 1099); seasonal use | Keep |
| Adobe Pro | PDF / e-sign | $23–$35 | Acrobat Pro ~$23/mo; with e-sign features ~$35/mo per license | Evaluate if CRM covers e-sign |
| Fathom Analytics | Privacy analytics | $14–$24 | $14/mo (100K page views); $24/mo (200K); scales by traffic | Keep |
| AddEvent | Event scheduling | $0–$16 | Free tier available; Pro ~$16/mo for custom branding and more events | Keep if used |
| Marketing inbox | Unknown | TBD | Cannot confirm — needs investigation | Investigate |

**Category subtotal: ~$41–$79/mo**

---

# Total Estimated Current Spend

| Category | Low Estimate/mo | High Estimate/mo |
|----------|----------------|-----------------|
| CRM / Sales / Outreach | $475 | $1,395 |
| Marketing / Content / SEO | $487 | $1,413 |
| Website / Web Infrastructure | $66 | $186 |
| Data / Automation / Backend | $210 | $1,425 |
| Industry / Enrollment | $150 | $500 |
| Learning / Training | $53 | $85 |
| Compliance / Finance / Other | $41 | $79 |
| **TOTAL MONTHLY** | **~$1,482/mo** | **~$5,083/mo** |
| **TOTAL ANNUAL** | **~$17,784/yr** | **~$60,996/yr** |

*Per-seat tools (Five9, Airtable, Cloud Academy) can multiply significantly with headcount. These estimates assume minimal seats — actual spend may be at or above the high end.*

---

# Proposal A: Notion CRM + n8n + AI Agents

---

## Proposal A — Philosophy

Build a split-architecture system: Notion handles all non-PHI CRM operations (pipeline, tasks, contacts, SOPs). Self-hosted n8n on AWS handles all HIPAA/PHI workflows in an encrypted, BAA-covered environment. AI agents layer on top of both via n8n orchestration.

**Two layers. Clear boundary. No PHI in Notion. Full compliance on AWS.**

---

## Proposal A — Architecture (Split: Non-PHI / PHI)

### Layer 1: Notion (Non-PHI CRM & Operations Hub)
- Contact records: name, email, phone, agent assignment, lead source, deal stage
- Pipeline tracking with Kanban boards and timeline views
- Task management, follow-up scheduling, activity logs
- Department wikis, SOPs, and process documentation
- Templates for repeatable workflows
- Reporting dashboards (non-PHI metrics: conversion rates, pipeline velocity, agent activity)

**What NEVER goes in Notion:** SSNs, DOBs linked to health data, Medicare/Medicaid IDs, policy numbers, health plan selections, enrollment details, medical conditions, coverage information, signed health documents

### Layer 2: n8n + AWS (PHI/HIPAA-Compliant Environment)
- Self-hosted n8n on AWS (standard regions — not GovCloud; BAA signed with AWS)
- Encrypted PostgreSQL (RDS) for structured PHI: enrollment data, policy details, Medicare IDs, health plan selections
- Encrypted S3 for PHI documents: signed enrollment forms, compliance paperwork, health-related correspondence
- All PHI processing happens exclusively in this layer
- n8n workflows bridge Notion and the PHI layer — reading non-PHI context from Notion, processing PHI on AWS, writing back only non-PHI status updates (e.g., "enrollment complete" without enrollment details)

### Layer 3: AI Agents (Orchestrated by n8n)
- AI SDR: Lead qualification, email/SMS outreach, follow-up, meeting booking
- AI BDR: Outbound prospecting, list building, personalized outreach
- AI Admin: Data entry, scheduling, compliance document tracking, reporting
- Built on LLM APIs (Claude, GPT) — all PHI-touching agent workflows execute within the AWS environment
- Non-PHI agent tasks (outreach copy, scheduling) can reference Notion data directly

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
- Uses an AI classification step (Claude Haiku — fast and cheap) to evaluate ambiguous content
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
| AI classification step (Claude Haiku API) | $5–$20/mo | Ongoing (minimal token usage) |
| Data classification guide creation | $500–$1,000 | One-time |
| Training module development (LearnDash) | $1,000–$2,000 | One-time |
| Compliance officer time (partial role) | $0–$500/mo | Ongoing (existing employee) |
| **PHI prevention total (one-time)** | **$2,500–$6,000** | |
| **PHI prevention total (ongoing)** | **$5–$520/mo** | |

---

## Proposal A — What Gets Built

1. **Notion CRM (Non-PHI Layer)** — Contacts, pipeline, tasks, department hubs, SOPs — no PHI
2. **AWS PHI Environment** — Encrypted RDS + S3 with BAA, private VPC, audit logging — all PHI lives here
3. **n8n Automation Layer** — Self-hosted on AWS; bridges Notion and PHI layer; includes sanitization and PHI scanning workflows
4. **AI SDR Agent** — n8n workflows calling LLM APIs for lead qualification and outreach
5. **AI BDR Agent** — Prospecting automation, list enrichment, personalized messaging
6. **AI Admin Agent** — Data entry automation, scheduling, compliance checks, reporting
7. **Integration Layer** — n8n connects Notion, AWS PHI layer, Medicare Pro, E123, SendGrid, and retained tools
8. **PHI Prevention System** — Sanitization workflows, scheduled PHI scanner, incident response procedures

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
| AI SDR agent build (n8n workflows + LLM integration) | $8,000–$20,000 | One-time: workflow design, prompt engineering, testing, SMS/email integration |
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

### AI/LLM API Costs (Ongoing)

| Provider / Model | Cost per 1M Tokens | Estimated Monthly Usage | Est. Monthly Cost |
|-----------------|--------------------|-----------------------|-------------------|
| Claude Haiku 4.5 (fast tasks: PHI scanning, classification, outreach drafts) | $1 input / $5 output | ~2M input + 500K output | $4.50 |
| Claude Sonnet 4.5 (complex tasks: lead qualification, enrollment analysis) | $3 input / $15 output | ~1M input + 300K output | $7.50 |
| GPT-4.1 (alternative for variety/redundancy) | $2 input / $8 output | ~1M input + 300K output | $4.40 |
| GPT-4.1-mini (high-volume: bulk classification, simple responses) | $0.40 input / $1.60 output | ~5M input + 1M output | $3.60 |
| **Blended estimate** | | | **$50–$300/mo** |

*AI API costs depend heavily on volume. The PHI scanner adds minimal cost (~$5–$20/mo using Haiku). Batch API discounts (50% off) and prompt caching (90% off cached reads) reduce costs significantly for repetitive workflows.*

---

## Proposal A — Total Cost Summary

### One-Time Costs

| Item | Low | High |
|------|-----|------|
| Notion CRM setup & config | $3,000 | $8,000 |
| AI SDR agent build | $8,000 | $20,000 |
| AI BDR agent build | $5,000 | $15,000 |
| AI Admin agent build | $5,000 | $15,000 |
| Integration layer (n8n workflows) | $5,000 | $15,000 |
| PHI prevention system (scanner, training, guide) | $2,500 | $6,000 |
| Data migration (from Airtable, Active Campaign, etc.) | $2,000 | $5,000 |
| AWS PHI environment setup (VPC, encryption, IAM, logging) | $1,500 | $4,000 |
| Training & change management | $1,000 | $3,000 |
| **TOTAL ONE-TIME** | **$33,000** | **$91,000** |

### Monthly Ongoing Costs

| Item | Low (10 seats) | High (25 seats) |
|------|----------------|-----------------|
| Notion Business | $200 | $600 |
| n8n self-hosted (AWS server) | $30 | $80 |
| AWS PHI environment (RDS, S3, VPC, logging) | $131 | $360 |
| AI/LLM API costs (agents + PHI scanner) | $55 | $320 |
| n8n maintenance/DevOps | $0 | $500 |
| Retained tools (see above) | $354 | $1,624 |
| **TOTAL MONTHLY ONGOING** | **$770** | **$3,484** |
| **TOTAL ANNUAL ONGOING** | **$9,240** | **$41,808** |

---

## Proposal A — Timeline

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery & requirements; data classification (PHI vs. non-PHI) | Weeks 1–3 | Process map + data classification guide complete |
| Phase 1 | AWS PHI environment setup (VPC, RDS, S3, encryption, IAM, CloudTrail, BAA) | Weeks 4–6 | HIPAA-compliant infrastructure live |
| Phase 2 | Notion CRM build (databases, relations, views, templates, locked schemas) | Weeks 4–7 | CRM operational (non-PHI) |
| Phase 3 | n8n setup + core automations (lead routing, notifications, Notion-AWS bridge, sanitization workflows) | Weeks 5–9 | n8n live; PHI boundary enforced |
| Phase 4 | PHI scanner workflow + incident response procedures | Weeks 7–9 | Automated PHI detection active |
| Phase 5 | AI SDR agent (email + SMS outreach sequences via n8n) | Weeks 8–12 | SDR agent in testing |
| Phase 6 | AI BDR agent (prospecting + list building) | Weeks 10–14 | BDR agent in testing |
| Phase 7 | AI Admin agent (scheduling, data entry, compliance) | Weeks 12–16 | Admin agent in testing |
| Phase 8 | Integration layer (Medicare Pro, E123, retained tools) | Weeks 13–17 | All integrations live |
| Phase 9 | Migration & legacy tool decommission (dept by dept) | Weeks 15–21 | Redundant tools canceled |
| Phase 10 | Training (including PHI boundary training), change management, stabilization | Weeks 17–24 | Full rollout; all staff trained |

**Total: ~6 months to full deployment**

*Note: Phases 1 and 2 run in parallel (AWS setup + Notion CRM build). The extra time vs. the previous estimate accounts for the PHI prevention system build and mandatory compliance training.*

---

## Proposal A — Pros & Cons

**Pros**
- Notion is familiar, flexible, and fast to configure — no custom software development for the CRM
- n8n self-hosted gives unlimited automations at near-zero marginal cost
- AI agents tuned to insurance sales workflows — competitive differentiator
- No per-seat SaaS fees for automation (n8n) — only Notion scales per seat
- You own all data — no vendor lock-in on the automation layer
- HIPAA compliance handled via AWS BAA (free) + self-managed encryption — no $297/mo add-on fee
- PHI prevention system provides automated, continuous compliance monitoring
- Clear separation of concerns: business users work in Notion, PHI stays locked in AWS

**Cons**
- Split architecture adds complexity — two systems to maintain instead of one
- PHI boundary requires ongoing vigilance (mitigated by automated scanner + training)
- Notion is not a purpose-built CRM — has limitations on relational data, reporting, and scale (10K+ records can slow down)
- n8n self-hosted requires some DevOps knowledge to maintain
- AI agents require upfront build investment and ongoing prompt tuning
- Longer deployment timeline (~6 months vs. ~3.5 months for GHL)
- Compliance responsibility is on the organization, not a vendor

---

# Proposal B: GoHighLevel + Automation

---

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

# Side-by-Side Comparison

| Factor | Proposal A (Notion + n8n + AI) | Proposal B (GoHighLevel) |
|--------|-------------------------------|--------------------------|
| **One-time cost** | $33,000–$91,000 | $7,000–$20,000 |
| **Monthly ongoing (10 seats)** | $770–$1,560 | $1,018–$1,870 |
| **Monthly ongoing (25 seats)** | $1,370–$3,484 | $1,018–$2,765 |
| **Annual ongoing (10 seats)** | $9,240–$18,720 | $12,216–$22,440 |
| **Annual ongoing (25 seats)** | $16,440–$41,808 | $12,216–$33,180 |
| **Time to full deployment** | ~6 months | ~3.5 months |
| **Tools eliminated** | ~11 | ~11 |
| **CRM flexibility** | High (Notion is infinitely customizable) | Moderate (GHL is opinionated) |
| **Automation cost at scale** | Near-zero (n8n self-hosted) | Usage-based fees grow with volume |
| **AI capabilities** | Custom agents — full control | GHL AI Employee add-on ($97/mo) |
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
| **Proposal A (Notion + n8n + AI)** | $42,240–$109,720 | $49,440–$132,808 |
| **Proposal B (GoHighLevel)** | $19,216–$42,440 | $19,216–$53,180 |

## Year 2+ (Ongoing Only)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| **Current state (estimated)** | $17,784–$60,996 | $17,784–$60,996 |
| **Proposal A (Notion + n8n + AI)** | $9,240–$18,720 | $16,440–$41,808 |
| **Proposal B (GoHighLevel)** | $12,216–$22,440 | $12,216–$33,180 |

**Key insight:** Proposal A has higher Year 1 costs due to the AI agent build + PHI infrastructure investment, but lower ongoing costs from Year 2 onward — especially at scale. The AWS BAA is free vs. GHL's non-cancelable $3,564/yr HIPAA add-on. n8n has no per-execution fees. Proposal B is cheaper to start but the mandatory HIPAA add-on and usage-based fees narrow the gap significantly over time. At the 10-seat level, Proposal A becomes cheaper than Proposal B partway through Year 2.

---

# The Hybrid Option

**Best of both worlds — phased approach:**

1. **Now:** Deploy GHL (Proposal B) to stop the bleeding on redundant tools
2. **Months 4–6:** Stabilize operations on GHL
3. **Months 6–12:** Build Notion hub for operations/documentation + n8n for custom automations alongside GHL
4. **Year 2:** Layer AI agents on top; evaluate whether GHL stays as front-end or gets replaced

This gives immediate consolidation wins while building toward the more powerful Notion + n8n + AI stack without rushing it.

---

# Recommendation

Start with **Phase 0** regardless of proposal chosen.

The process mapping will:
- Reveal which tools are truly redundant vs. serving unique needs
- Surface compliance requirements that constrain platform choices
- Give every department a voice before changes happen
- Produce the requirements needed to evaluate both proposals with real data
- Determine actual seat count and volume — which directly impacts cost comparisons

---

# Change Management Strategy

Given the number of departments and verticals, change management is critical.

- **Assign a change champion per department** — someone who owns the transition for their team
- **Communicate the "why" before the "what"** — people resist changes they don't understand
- **Run parallel systems during transition** — no cold cutovers
- **Build feedback loops into every phase** — weekly check-ins during migration
- **Document everything** — fill the gap left by the previous tech lead
- **Quick wins first** — eliminate obviously orphaned tools early to build momentum

---

# Next Steps

1. Schedule Monday discussion to review this plan
2. **Immediate:** Verify whether Active Campaign is currently on an Enterprise plan with a signed BAA — if not, there is an existing HIPAA compliance gap
3. Complete Phase 0 process discovery (Weeks 1–3), including PHI data classification across all workflows
4. Audit every tool for active usage, contract terms, and renewal dates
5. Confirm seat count across departments (directly impacts Proposal A vs. B economics)
6. If Proposal A is selected: sign AWS BAA via AWS Artifact; begin VPC + encryption setup in parallel with Notion CRM build
7. Present refined proposals with validated cost projections
8. Select approach and begin department-by-department rollout
