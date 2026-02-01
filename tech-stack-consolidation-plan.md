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

Build an integrated CRM on Notion as the central hub. Use n8n (self-hosted) for workflow automation. Layer AI agents (SDR, BDR, Admin) on top via API integrations.

**Flexible. Low-code. AI-powered. You own the data.**

---

## Proposal A — Architecture

**Notion (CRM & Operations Hub)**
- Contacts database with relations, rollups, and custom properties
- Pipeline tracking with Kanban boards and timeline views
- Policy lifecycle management
- Department wikis and process documentation
- Templates for repeatable workflows

**n8n (Automation Engine — Self-Hosted)**
- Replaces Zapier with unlimited executions
- Triggers workflows between Notion, SendGrid, AI agents, and external tools
- Handles lead routing, follow-up sequences, enrollment alerts, reporting

**AI Agents (via API)**
- AI SDR: Lead qualification, email/SMS outreach, follow-up, meeting booking
- AI BDR: Outbound prospecting, list building, personalized outreach
- AI Admin: Data entry, scheduling, compliance document tracking, reporting
- Built on LLM APIs (Claude, GPT) with n8n orchestrating the workflows

---

## Proposal A — What Gets Built

1. **Notion CRM** — Contacts, pipeline, policy tracking, department hubs, SOPs
2. **n8n Automation Layer** — Self-hosted on AWS; replaces Zapier; connects all systems
3. **AI SDR Agent** — n8n workflows calling LLM APIs for lead qualification and outreach
4. **AI BDR Agent** — Prospecting automation, list enrichment, personalized messaging
5. **AI Admin Agent** — Data entry automation, scheduling, compliance checks, reporting
6. **Integration Layer** — n8n connects Notion to Medicare Pro, E123, SendGrid, and retained tools

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

### Notion

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| Notion Business plan | $20/user/mo (annual) or $24/user/mo (monthly) | Per-seat; Business tier needed for SAML SSO, private teamspaces, advanced permissions |
| Estimated seats (10 users) | $200–$240/mo | Scales linearly per user added |
| Estimated seats (25 users) | $500–$600/mo | Scales linearly per user added |

*Notion pricing is per-seat. The cost scales directly with how many people need access. Free guests can view shared pages but can't edit databases.*

### n8n (Self-Hosted)

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| n8n Community Edition license | $0 | Free and open-source for self-hosting |
| AWS server for n8n (t3.medium or similar) | $30–$80/mo | EC2 instance + storage; varies by workload |
| DevOps/maintenance time | $0–$500/mo | Internal time or contractor for updates, monitoring |

*n8n self-hosted is free software. You only pay for the server it runs on. Cloud-hosted n8n would be $20–$50/mo but limits executions. Self-hosting gives unlimited executions.*

### AI Agent Development

| Line Item | Estimated Cost | Pricing Basis |
|-----------|---------------|---------------|
| AI SDR agent build (n8n workflows + LLM integration) | $8,000–$20,000 | One-time: workflow design, prompt engineering, testing, SMS/email integration |
| AI BDR agent build | $5,000–$15,000 | One-time: prospecting logic, list enrichment, outreach sequences |
| AI Admin agent build | $5,000–$15,000 | One-time: data entry automation, scheduling, compliance checks |
| Notion CRM setup & configuration | $3,000–$8,000 | One-time: database architecture, relations, views, templates, migration |
| Integration layer (n8n to Medicare Pro, E123, etc.) | $5,000–$15,000 | One-time: API connections, data sync, error handling |

### AI/LLM API Costs (Ongoing)

| Provider / Model | Cost per 1M Tokens | Estimated Monthly Usage | Est. Monthly Cost |
|-----------------|--------------------|-----------------------|-------------------|
| Claude Haiku 4.5 (fast tasks) | $1 input / $5 output | ~2M input + 500K output | $4.50 |
| Claude Sonnet 4.5 (complex tasks) | $3 input / $15 output | ~1M input + 300K output | $7.50 |
| GPT-4.1 (alternative) | $2 input / $8 output | ~1M input + 300K output | $4.40 |
| GPT-4.1-mini (high-volume) | $0.40 input / $1.60 output | ~5M input + 1M output | $3.60 |
| **Blended estimate** | | | **$50–$300/mo** |

*AI API costs depend heavily on volume. A small brokerage doing 500 outreach/day might spend $50–$100/mo. High-volume operations with complex reasoning could reach $300+/mo. Batch API discounts (50% off) and prompt caching (90% off reads) reduce this significantly.*

### AWS Infrastructure (Expanded)

| Line Item | Cost | Pricing Basis |
|-----------|------|---------------|
| EC2 for n8n | $30–$80/mo | t3.medium instance |
| EC2 for AI agent services | $50–$150/mo | t3.large or equivalent for agent runtime |
| S3 storage | $5–$20/mo | Document storage, backups |
| Data transfer | $5–$30/mo | API calls, email attachments, etc. |
| RDS (if database needed) | $15–$50/mo | Small PostgreSQL instance for agent state/logs |
| **AWS subtotal** | **$105–$330/mo** | |

*Note: This is incremental AWS cost for the new systems. Existing AWS spend for current workloads is separate and included in "retained tools."*

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
| Data migration (from Airtable, Active Campaign, etc.) | $2,000 | $5,000 |
| Training & change management | $1,000 | $3,000 |
| **TOTAL ONE-TIME** | **$29,000** | **$81,000** |

### Monthly Ongoing Costs

| Item | Low (10 seats) | High (25 seats) |
|------|----------------|-----------------|
| Notion Business | $200 | $600 |
| n8n self-hosted (AWS server) | $30 | $80 |
| AI/LLM API costs | $50 | $300 |
| AWS infrastructure (new) | $105 | $330 |
| n8n maintenance/DevOps | $0 | $500 |
| Retained tools (see above) | $354 | $1,624 |
| **TOTAL MONTHLY ONGOING** | **$739** | **$3,434** |
| **TOTAL ANNUAL ONGOING** | **$8,868** | **$41,208** |

---

## Proposal A — Timeline

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery & requirements | Weeks 1–3 | Process map complete |
| Phase 1 | Notion CRM build (databases, relations, views, templates) | Weeks 4–7 | CRM operational |
| Phase 2 | n8n setup + core automations (lead routing, notifications) | Weeks 5–8 | n8n live, replacing Zapier |
| Phase 3 | AI SDR agent (email + SMS outreach sequences via n8n) | Weeks 7–11 | SDR agent in testing |
| Phase 4 | AI BDR agent (prospecting + list building) | Weeks 9–13 | BDR agent in testing |
| Phase 5 | AI Admin agent (scheduling, data entry, compliance) | Weeks 11–15 | Admin agent in testing |
| Phase 6 | Integration layer (Medicare Pro, E123, retained tools) | Weeks 12–16 | All integrations live |
| Phase 7 | Migration & legacy tool decommission (dept by dept) | Weeks 14–20 | Redundant tools canceled |
| Phase 8 | Training, change management, stabilization | Weeks 16–22 | Full rollout |

**Total: ~5.5 months to full deployment**

---

## Proposal A — Pros & Cons

**Pros**
- Notion is familiar, flexible, and fast to configure — no custom software development for the CRM
- n8n self-hosted gives unlimited automations at near-zero marginal cost
- AI agents tuned to insurance sales workflows — competitive differentiator
- No per-seat SaaS fees for automation (n8n) — only Notion scales per seat
- You own all data — no vendor lock-in on the automation layer
- Significantly cheaper than a fully custom-coded CRM ($29K–$81K vs. $75K–$205K)

**Cons**
- Notion is not a purpose-built CRM — has limitations on relational data, reporting, and scale (10K+ records can slow down)
- n8n self-hosted requires some DevOps knowledge to maintain
- AI agents require upfront build investment and ongoing prompt tuning
- HIPAA compliance: Notion's BAA availability must be verified for PHI storage
- Not as turnkey as GoHighLevel — requires more initial configuration

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
| **One-time cost** | $29,000–$81,000 | $7,000–$20,000 |
| **Monthly ongoing (10 seats)** | $739–$1,510 | $1,018–$1,870 |
| **Monthly ongoing (25 seats)** | $1,339–$3,434 | $1,018–$2,765 |
| **Annual ongoing (10 seats)** | $8,868–$18,120 | $12,216–$22,440 |
| **Annual ongoing (25 seats)** | $16,068–$41,208 | $12,216–$33,180 |
| **Time to full deployment** | ~5.5 months | ~3.5 months |
| **Tools eliminated** | ~11 | ~11 |
| **CRM flexibility** | High (Notion is infinitely customizable) | Moderate (GHL is opinionated) |
| **Automation cost at scale** | Near-zero (n8n self-hosted) | Usage-based fees grow with volume |
| **AI capabilities** | Custom agents — full control | GHL AI Employee add-on ($97/mo) |
| **Engineering required** | Some (n8n maintenance, AI tuning) | Minimal |
| **Vendor lock-in** | Low (Notion export + open-source n8n) | High (GHL is proprietary) |
| **HIPAA compliance** | Must verify Notion BAA; HIPAA Vault for PHI | $297/mo add-on |
| **Scalability (seats)** | Notion cost grows per seat | GHL unlimited contacts, flat subscription |
| **Scalability (volume)** | n8n unlimited executions | GHL usage fees grow with volume |

---

# Cost Comparison Summary

## Year 1 (Including Setup)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| **Current state (estimated)** | $17,784–$60,996 | $17,784–$60,996 |
| **Proposal A (Notion + n8n + AI)** | $37,868–$99,120 | $45,068–$122,208 |
| **Proposal B (GoHighLevel)** | $19,216–$42,440 | $19,216–$53,180 |

## Year 2+ (Ongoing Only)

| Scenario | 10 Seats | 25 Seats |
|----------|----------|----------|
| **Current state (estimated)** | $17,784–$60,996 | $17,784–$60,996 |
| **Proposal A (Notion + n8n + AI)** | $8,868–$18,120 | $16,068–$41,208 |
| **Proposal B (GoHighLevel)** | $12,216–$22,440 | $12,216–$33,180 |

**Key insight:** Proposal A has higher Year 1 costs due to the AI agent build investment, but lower ongoing costs — especially at scale, because n8n has no per-execution fees and Notion per-seat pricing is predictable. Proposal B is cheaper to start but the HIPAA add-on ($3,564/yr) and usage-based fees make it more expensive than it first appears.

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
2. Complete Phase 0 process discovery (Weeks 1–3)
3. Audit every tool for active usage, contract terms, and renewal dates
4. Confirm seat count across departments (directly impacts Proposal A vs. B economics)
5. Verify HIPAA compliance: Notion BAA availability and GHL HIPAA add-on scope
6. Present refined proposals with validated cost projections
7. Select approach and begin department-by-department rollout
