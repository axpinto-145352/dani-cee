# Tech Stack Consolidation — Consolidated Report
## The Brokerage Inc. — Detailed Reference Document

**Purpose:** This document is the detailed reference companion to the proposal deck. Use it to speak intelligently about every tool, cost, timeline, and architectural decision. It contains the full granular breakdowns behind every number in the presentation.

---

## Table of Contents

1. Current Tool Inventory (Full Detail)
2. Tool-by-Tool Disposition Plan
3. Proposal A: Full Architecture & Cost Breakdown
4. Proposal B: Full Architecture & Cost Breakdown
5. Side-by-Side Financial Analysis
6. Engagement Structure & Milestones
7. HIPAA Compliance Deep Dive
8. PHI Leakage Prevention Plan
9. Change Management Plan
10. Risk Register
11. Open Questions & Investigation Items

---

## 1. Current Tool Inventory (Full Detail)

### CRM / Sales / Outreach — 7 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Active Users | Status |
|------|----------|-------------------|---------------|-------------|--------|
| Active Campaign | Email marketing / CRM | $150–$500 | Tiered by contact count: Starter ~$15/mo (500 contacts), scales to $500+ for large lists. Enterprise required for BAA. | TBD (audit needed) | Redundant — replace with Notion + n8n + SendGrid |
| EZ Texting | SMS outreach | $50–$200 | Plans start ~$20/mo for 500 credits; scales by message volume per month | TBD | Redundant — replace with n8n SMS via Twilio |
| slydial | Voicemail drops | $30–$100 | Per-use credits (~$0.05–$0.10/drop) or monthly subscription packs | TBD | Niche — evaluate during Phase 0; replace with AI voicemail via n8n if feasible |
| GMass | Bulk email via Gmail | $20–$50 | Standard ~$20/mo per Gmail account; Premium ~$30; Enterprise ~$50 | TBD | Redundant — replace with n8n email via SendGrid |
| Five9 | Contact center / dialer | $150–$300/seat | Core plan ~$149/seat/mo; per-minute telecom usage added on top. This is the most expensive per-seat tool in the stack. | TBD — seat count critical | Core — evaluate replacement during Phase 0. If only 1–2 seats, retain. If 5+, explore AI dialer alternatives. |
| Crisp | Live chat / messaging | $25–$95 | Free basic; Pro ~$25/mo; Unlimited ~$95/mo per workspace | TBD | Redundant — replace with Notion intake forms + n8n routing. Retain if chat volume is high (>100 conversations/mo). |
| Quo | Sales engagement | $50–$150 | Per-seat SaaS pricing; varies by plan tier | TBD | Redundant — replace with AI SDR agent via n8n + Bedrock |

**Category subtotal: $475–$1,395/mo ($5,700–$16,740/yr)**

**Key unknowns:** Active Campaign plan tier (is there a BAA?), Five9 seat count (could be the largest single line item), Quo actual usage level.

---

### Marketing / Content / SEO — 9 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Canva | Design | $13–$30 | Pro ~$13/mo (1 user); Teams ~$30/mo per 5 users | **Keep** — low cost, high utility, used across departments |
| Riverside | Podcast/video recording | $15–$24 | Standard ~$15/mo; Business ~$24/mo; per-seat | **Keep if podcast continues** — evaluate during Phase 0 |
| Testimonial.to | Video testimonials | $20–$50 | Starter ~$20/mo; Premium ~$50/mo; based on # of testimonials collected | **Evaluate ROI** — how many testimonials collected? What's the conversion impact? |
| UberSuggest | SEO research | $30–$50 | Individual ~$29/mo; Business ~$49/mo; lifetime deals available | **Redundant** — evaluate if anyone actively uses it. May have lifetime license. |
| Unbounce | Landing pages | $90–$225 | Launch ~$90/mo; Optimize ~$225/mo; based on conversions and page count | **Redundant** — replace with WordPress + Elementor landing pages |
| SEO articles | Content/SEO service | $200–$500+ | Vendor pricing — per article or monthly retainer. Not a SaaS tool. | **Clarify** — is this a vendor/agency or an internal process? Get contract details. |
| Liberated Syndication | Podcast hosting | $5–$20 | Classic plans $5–$20/mo based on monthly storage allocation | **Keep if podcast continues** — paired with Riverside |
| YouTube Premium | Video | $14 | Fixed subscription price | **Likely personal** — verify if this is a business expense or personal subscription |
| BrightFire | Insurance marketing | $100–$500 | Insurance-specific marketing packages. Appears duplicated in the tool list — confirm single subscription. | **Confirm** — appears listed twice. Verify one subscription, eliminate duplicate billing. |

**Category subtotal: $487–$1,413/mo ($5,844–$16,956/yr)**

**Key unknowns:** BrightFire duplication, SEO articles vendor details, Testimonial.to ROI, podcast continuation decision.

---

### Website / Web Infrastructure — 10 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| WordPress (main) | Primary website | $0 | Open-source CMS — free software | **Keep** — core website platform |
| WP Engine | WordPress hosting | $20–$60 | Startup ~$20/mo (1 site, 25K visits); Growth ~$60/mo (10 sites, 100K visits) | **Keep** — managed WordPress hosting with staging |
| Staging environment TBI | Dev/staging | $0 | Included with WP Engine hosting plans | **Keep** — paired with WP Engine |
| Squarespace | Secondary site | $16–$49 | Personal ~$16/mo; Business ~$33/mo; Commerce ~$49/mo | **Eliminate** — redundant with WordPress. Migrate content, cancel. |
| Elementor | Page builder | $5–$17 | Essential ~$5/mo (1 site); Advanced ~$17/mo (25 sites); billed annually | **Keep** — WordPress page builder, also handles landing pages (replaces Unbounce) |
| Gravity Forms | WordPress forms | $5–$20 | Basic ~$5/mo; Elite ~$20/mo; billed annually per-site license | **Pick one** — redundant with Fluent Forms. Evaluate which has more active forms. |
| Fluent Forms | WordPress forms (WPManageNinja) | $5–$10 | Single site ~$5/mo; agency ~$10/mo; billed annually | **Pick one** — redundant with Gravity Forms. Likely cheaper. |
| Forgravity | Gravity Forms add-ons | $10–$20 | Annual license divided monthly; depends on which add-on bundle | **Eliminate if Gravity Forms goes** — dependent on Gravity Forms decision |
| Imagify | Image optimization | $5–$10 | Starter free (20MB/mo); Growth ~$5/mo (500MB); Infinite ~$10/mo | **Keep** — low cost, improves site performance |
| Gravatar | Profile avatars | $0 | Free service by Automattic | **Keep** — free, negligible |

**Category subtotal: $66–$186/mo ($792–$2,232/yr)**

**Key unknowns:** What is Squarespace used for? Which forms plugin has more active forms?

---

### Data / Automation / Backend — 10 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Airtable (Admin) | Database / ops tracking | $20–$45/seat | Team ~$20/seat/mo; Business ~$45/seat/mo; scales by seats and record count | **Redundant** — replace with Notion databases |
| Airtable | General use | $20–$45/seat | Same pricing — separate workspace or base from Admin | **Redundant** — replace with Notion databases |
| Airtable OTP | Unknown use case | $20–$45/seat | Same pricing — unknown what this base is used for | **Investigate** — determine purpose during Phase 0 before deciding |
| Zapier | Automation / integrations | $20–$100+ | Starter ~$20/mo (750 tasks); Professional ~$50/mo (2K tasks); Team ~$100/mo (50K tasks) | **Replace with n8n** — self-hosted n8n is free with unlimited executions |
| SendGrid (Twilio) | Transactional email | $15–$90 | Free tier (100 emails/day); Essentials ~$15/mo (50K emails); Pro ~$90/mo (100K emails) | **Keep** — transactional email backend for n8n workflows; also provides SMS via Twilio |
| Amazon Web Services | Cloud infrastructure | $50–$500+ | Usage-based: EC2 instances, S3 storage, RDS databases, data transfer — highly variable | **Keep + expand** — becomes the HIPAA-compliant backbone for PHI storage, n8n, Bedrock |
| Couchdrop | File transfer / SFTP | $15–$50 | Starter ~$15/mo; Business ~$50/mo; based on storage and concurrent users | **Evaluate** — what files are being transferred? Can S3 + n8n replace this? |
| HIPAA Vault | HIPAA-compliant hosting/storage | $50–$300 | Managed HIPAA hosting; pricing by server size and compliance tier | **Keep** — non-negotiable for compliance. Evaluate overlap with new AWS PHI environment. |
| Streamlit | Data apps / dashboards | $0–$250 | Community Cloud free for public apps; Teams ~$250/mo for private apps | **Evaluate** — what dashboards does it power? Can Notion dashboards replace them? |
| Basefront | Unknown | TBD | Cannot confirm — tool needs investigation | **Investigate** — determine what this is and whether it's actively used |

**Category subtotal: $210–$1,425/mo ($2,520–$17,100/yr)**

**Key unknowns:** Airtable OTP purpose, AWS current workloads and spend, Couchdrop use case, Streamlit dashboards, Basefront identity, HIPAA Vault overlap with new AWS PHI layer.

---

### Industry-Specific / Enrollment — 3 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Medicare Pro | Enrollment platform | $100–$300 | Industry-specific licensing; per-agent or flat monthly fee | **Keep** — core business tool, non-negotiable |
| Medicare Pro Test Account | Testing environment | $0 | Included with Medicare Pro subscription | **Keep** — paired with Medicare Pro |
| E123 | Enrollment / quoting | $50–$200 | Per-agent licensing for enrollment/quoting platform | **Keep** — core business tool, non-negotiable |

**Category subtotal: $150–$500/mo ($1,800–$6,000/yr)**

**These tools are not candidates for consolidation.** They are industry-specific platforms required for the core business of Medicare enrollment and quoting.

---

### Learning / Training — 2 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Cloud Academy | Training platform | $40–$55/seat | Individual ~$40/seat/mo; Team ~$55/seat/mo; enterprise negotiated | **Redundant** — pick one LMS, eliminate the other |
| LearnDash | LMS (WordPress-based) | $13–$30 | 1 site ~$13/mo; 10 sites ~$30/mo; billed annually | **Redundant** — pick one LMS, eliminate the other |

**Category subtotal: $53–$85/mo ($636–$1,020/yr)** (single-seat estimate)

**Recommendation:** LearnDash is cheaper and integrates with WordPress (already in the stack). Cloud Academy is better for technical training content. Decision depends on what training content exists and where.

---

### Compliance / Finance / Other — 5 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Tax Bandits | Tax filing | ~$4/mo (~$50/yr) | Per-form pricing (e.g. $3–$5 per 1099 form); seasonal use | **Keep** — seasonal, low cost |
| Adobe Pro | PDF / e-signing | $23–$35 | Acrobat Pro ~$23/mo; with e-sign features ~$35/mo per license | **Evaluate** — can n8n + a lighter e-sign solution replace this? |
| Fathom Analytics | Privacy-focused analytics | $14–$24 | $14/mo (100K page views); $24/mo (200K); scales by traffic volume | **Keep** — privacy-compliant, good for HIPAA-sensitive org |
| AddEvent | Event scheduling links | $0–$16 | Free tier available; Pro ~$16/mo for custom branding and more events | **Keep if used** — low cost, evaluate usage during Phase 0 |
| Marketing inbox | Unknown | TBD | Cannot confirm pricing — needs investigation | **Investigate** — what is this? Shared email? Separate tool? |

**Category subtotal: $41–$79/mo ($492–$948/yr)**

**Key unknowns:** Marketing inbox identity, Adobe Pro usage level and potential replacement.

---

## 2. Tool-by-Tool Disposition Plan

### Summary

| Action | Count | Tools |
|--------|-------|-------|
| **Eliminate (redundant)** | 11 | Active Campaign, EZ Texting, slydial, GMass, Crisp, Quo, Airtable (×3), Zapier, Unbounce, Squarespace |
| **Keep (core/required)** | 15 | WordPress, WP Engine, Elementor, Imagify, Gravatar, SendGrid, AWS, HIPAA Vault, Medicare Pro, Medicare Pro Test, E123, Canva, Fathom Analytics, Tax Bandits, one LMS |
| **Keep if needed** | 4 | Riverside, Libsyn, AddEvent, one forms plugin |
| **Evaluate (need data)** | 5 | Five9, Testimonial.to, UberSuggest, Adobe Pro, Couchdrop |
| **Investigate (unknown)** | 5 | Airtable OTP, Basefront, Marketing inbox, Streamlit, SEO articles |
| **Consolidate (pick one)** | 4 | Gravity/Fluent Forms (pick one), Cloud Academy/LearnDash (pick one) |
| **Verify** | 2 | BrightFire (duplicate?), YouTube Premium (personal?) |

### Estimated Monthly Savings from Eliminations

| Scenario | Monthly Savings | Annual Savings |
|----------|----------------|---------------|
| Low estimate | $661 | $7,932 |
| High estimate | $1,904 | $22,848 |

---

## 3. Proposal A: Full Architecture & Cost Breakdown

### Architecture: Split Non-PHI / PHI

**Layer 1 — Notion (Non-PHI CRM & Operations)**
- Contact records: name, email, phone, agent assignment, lead source, deal stage
- Pipeline: Kanban boards, timeline views, deal value tracking
- Tasks: follow-up scheduling, activity logs, reminders
- Operations: department wikis, SOPs, process documentation, templates
- Reporting: conversion rates, pipeline velocity, agent activity (non-PHI metrics only)

**What NEVER goes in Notion:**
- SSNs
- DOBs linked to health data
- Medicare/Medicaid IDs
- Policy numbers
- Health plan selections or enrollment details
- Medical conditions or coverage information
- Signed health documents
- Any communication content referencing health status

**Layer 2 — AWS (PHI/HIPAA-Compliant)**
- n8n self-hosted on EC2 (automation engine)
- PostgreSQL on RDS (encrypted, structured PHI storage)
- S3 (encrypted, PHI document storage)
- VPC with private subnets (network isolation)
- CloudTrail + CloudWatch (audit logging + monitoring)
- KMS (encryption key management)
- BAA signed via AWS Artifact (free)

**Layer 3 — AWS Bedrock (HIPAA-Compliant AI)**
- All LLM inference routes through Bedrock
- HIPAA-eligible service covered by the same AWS BAA
- Models available: Claude Haiku, Sonnet, Opus; Amazon Titan; Llama; Mistral
- PHI never leaves the AWS environment
- n8n calls Bedrock APIs from within the private VPC

**Layer 4 — AI Agents (Orchestrated by n8n via Bedrock)**
- AI SDR: lead qualification, outreach, follow-up, meeting booking
- AI BDR: prospecting, list building, personalized outreach
- AI Admin: data entry, scheduling, compliance tracking, reporting

---

### Proposal A — One-Time Costs (Detailed)

| Item | Low | High | What This Pays For |
|------|-----|------|-------------------|
| Notion CRM setup & config | $3,000 | $8,000 | Database architecture (contacts, deals, policies, tasks), relations and rollups, views (Kanban, table, timeline, calendar), templates, permission structure, locked schemas |
| AI SDR agent build | $8,000 | $20,000 | n8n workflow design, Bedrock integration, prompt engineering, email/SMS sequence logic, lead scoring model, follow-up triggers, meeting booking integration, testing |
| AI BDR agent build | $5,000 | $15,000 | Prospecting logic, list enrichment workflows, personalized outreach templates, Bedrock integration, data source connections, testing |
| AI Admin agent build | $5,000 | $15,000 | Data entry automation workflows, scheduling integrations, compliance document tracking, reporting dashboards, Bedrock integration, testing |
| Integration layer (n8n) | $5,000 | $15,000 | API connections to Medicare Pro, E123, SendGrid/Twilio, Notion API, Bedrock API; data sync logic; error handling; retry mechanisms |
| PHI prevention system | $2,500 | $6,000 | Sanitization workflows, PHI scanner (Bedrock-powered), data classification guide, LearnDash training module |
| AWS PHI environment setup | $1,500 | $4,000 | VPC architecture, RDS provisioning, S3 bucket config, KMS encryption, IAM policies, CloudTrail/CloudWatch setup, security group rules, BAA signing |
| Data migration | $2,000 | $5,000 | Contact export from Active Campaign + Airtable, data cleaning, Notion import, PHI data routing to AWS RDS, validation |
| Training & change management | $1,000 | $3,000 | Per-department training sessions, user guides, PHI boundary training, change champion onboarding |
| **TOTAL ONE-TIME** | **$33,000** | **$91,000** | |

---

### Proposal A — Monthly Ongoing Costs (Detailed)

| Item | Low (10 seats) | High (25 seats) | Pricing Detail |
|------|----------------|-----------------|----------------|
| Notion Business | $200 | $600 | $20/user/mo (annual) or $24/user/mo (monthly). Business tier needed for schema locking + private teamspaces. |
| n8n EC2 server | $30 | $80 | t3.medium instance ($0.0416/hr) + 50GB EBS. Handles all automation workloads. |
| RDS PostgreSQL (PHI) | $25 | $75 | db.t3.medium, encrypted (KMS), Multi-AZ at high end for reliability. |
| S3 storage (PHI docs) | $5 | $20 | SSE-KMS encryption, versioning, lifecycle policies. ~10–100GB. |
| VPC + NAT Gateway | $35 | $50 | NAT Gateway ~$32/mo + data processing. Required for private subnet internet access. |
| CloudTrail + CloudWatch | $10 | $30 | Audit logging (HIPAA requirement) + monitoring alarms. |
| KMS | $1 | $5 | $1/key/mo + $0.03/10K API calls. |
| EC2 for agent services | $50 | $150 | t3.large for AI agent runtime (if separate from n8n instance). |
| Data transfer | $5 | $30 | Inter-service API calls, Notion sync, SendGrid, external integrations. |
| **AWS Bedrock (Haiku)** | $7 | $50 | ~3M input + 800K output tokens/mo. PHI scanning, classification, drafts. |
| **AWS Bedrock (Sonnet)** | $8 | $100 | ~1M input + 300K output tokens/mo. Complex reasoning, lead qual. |
| **AWS Bedrock (Opus)** | $5 | $75 | ~100K input + 50K output tokens/mo. Compliance review (low volume). |
| **AWS Bedrock (Titan)** | $1 | $15 | ~2M input + 500K output tokens/mo. Embeddings, lightweight tasks. |
| **Bedrock subtotal** | **$21** | **$240** | |
| PHI scanner AI (Haiku) | $5 | $20 | Daily Notion scan — minimal token usage. Included in Haiku estimate above. |
| Compliance officer time | $0 | $500 | Partial role — existing employee reviewing scanner reports, approving schema changes. |
| n8n maintenance/DevOps | $0 | $500 | Internal time or contractor. Updates, monitoring, security patches. |
| **New infrastructure subtotal** | **$387** | **$2,300** | |
| Retained: WordPress + WP Engine + Elementor | $25 | $77 | WP Engine hosting + Elementor Pro license |
| Retained: HIPAA Vault | $50 | $300 | Existing compliance hosting — evaluate overlap with new AWS PHI layer |
| Retained: Medicare Pro + E123 | $150 | $500 | Core enrollment/quoting — non-negotiable |
| Retained: SendGrid (Twilio) | $15 | $90 | Email backend for n8n; SMS via Twilio |
| Retained: AWS (existing workloads) | $50 | $500 | Whatever currently runs on AWS — separate from new infrastructure |
| Retained: Canva | $13 | $30 | Design tool |
| Retained: Riverside + Libsyn | $20 | $44 | Podcast (if continuing) |
| Retained: Tax Bandits | $4 | $4 | Seasonal tax filing |
| Retained: LMS (LearnDash or Cloud Academy) | $13 | $55 | Pick one |
| Retained: Fathom Analytics | $14 | $24 | Privacy-compliant analytics |
| **Retained tools subtotal** | **$354** | **$1,624** | |
| **TOTAL MONTHLY** | **$770** | **$3,514** | |
| **TOTAL ANNUAL** | **$9,240** | **$42,168** | |

---

### Proposal A — Timeline (Detailed)

| Phase | Description | Weeks | Milestone / Deliverable | Dependencies |
|-------|-------------|-------|------------------------|-------------|
| 0 | Process discovery, PHI classification, tool audit | 1–3 | Process map + data classification guide | Access to all department leads + tool accounts |
| 1 | AWS PHI environment (VPC, RDS, S3, encryption, IAM, CloudTrail, BAA) | 4–6 | HIPAA-compliant infrastructure live and tested | Phase 0 complete; AWS account access |
| 2 | Notion CRM build (databases, relations, views, templates, locked schemas) | 4–7 | CRM operational for non-PHI workflows | Phase 0 complete; runs parallel with Phase 1 |
| 3 | n8n setup + core automations (lead routing, notifications, Notion-AWS bridge, sanitization) | 5–9 | n8n live; PHI boundary enforced | Phases 1 and 2 substantially complete |
| 4 | PHI scanner workflow + incident response procedures | 7–9 | Automated daily PHI detection active | Phase 3 complete (n8n operational) |
| 5 | AI SDR agent (email + SMS outreach sequences via Bedrock) | 8–12 | SDR agent in testing; prototype demo | Phase 3 complete; Bedrock access confirmed |
| 6 | AI BDR agent (prospecting + list building via Bedrock) | 10–14 | BDR agent in testing | Phase 5 learnings applied |
| 7 | AI Admin agent (scheduling, data entry, compliance via Bedrock) | 12–16 | Admin agent in testing | Phase 5 learnings applied |
| 8 | Integration layer (Medicare Pro, E123, retained tools) | 13–17 | All external integrations live | API access to Medicare Pro, E123 |
| 9 | Migration & legacy decommission (dept by dept) | 15–21 | All redundant tools canceled | All replacement systems tested and stable |
| 10 | Training (PHI boundary + system), change management, stabilization | 17–24 | All staff trained; system in production | All phases complete |

**Total: ~24 weeks (~6 months)**

**Critical path:** Phase 0 → Phase 1/2 (parallel) → Phase 3 → Phase 5 (SDR agent — the MVP). Everything after Phase 5 can be sequenced or parallelized based on capacity.

---

## 4. Proposal B: Full Architecture & Cost Breakdown

### Architecture: GoHighLevel All-in-One

- GHL serves as CRM, email, SMS, landing pages, forms, pipeline, calendar, chat, and reporting
- HIPAA compliance via $297/mo add-on (non-cancelable once enabled)
- Supplemented by Zapier (reduced) for integrations GHL can't handle natively
- Retained tools for website (WordPress), industry (Medicare Pro, E123), and content (Canva, etc.)

---

### Proposal B — One-Time Costs (Detailed)

| Item | Low | High | What This Pays For |
|------|-----|------|-------------------|
| GHL account setup & config | $2,000 | $5,000 | Pipelines, custom fields, automation workflows, sub-account structure, user roles |
| Data migration | $1,500 | $4,000 | Contact export from Active Campaign + Airtable, tag mapping, pipeline recreation, data cleaning |
| Automation / workflow buildout | $2,000 | $6,000 | Lead routing, follow-up sequences, enrollment alerts, reporting triggers, appointment reminders |
| Landing page / form migration | $500 | $2,000 | Recreate Unbounce pages and WordPress forms in GHL builder |
| Training & change management | $1,000 | $3,000 | Per-department training, user guides, ongoing support during transition |
| **TOTAL ONE-TIME** | **$7,000** | **$20,000** | |

---

### Proposal B — Monthly Ongoing Costs (Detailed)

| Item | Low | High | Pricing Detail |
|------|-----|------|----------------|
| GHL Unlimited subscription | $297 | $297 | Recommended tier — unlimited sub-accounts, advanced workflows. Starter ($97) may work for single-location. |
| GHL SMS outbound | $40 | $200 | $0.0079/segment × 5,000–25,000 segments |
| GHL MMS outbound | $10 | $40 | $0.02/message × 500–2,000 messages |
| GHL outbound calls | $36 | $144 | $0.018/minute × 2,000–8,000 minutes |
| GHL inbound calls | $9 | $34 | $0.0085/minute × 1,000–4,000 minutes |
| GHL email sending | $14 | $54 | $0.675/1,000 emails × 20,000–80,000 emails |
| GHL phone verification | $1 | $5 | $2.50/1,000 × 500–2,000 verifications |
| **GHL usage subtotal** | **$110** | **$477** | |
| GHL HIPAA compliance add-on | $297 | $297 | Mandatory for Medicare brokerage. Encryption, BAA, audit logging, MFA. Non-cancelable. |
| GHL AI Employee (optional) | $0 | $97 | Conversation AI, Voice AI, Content AI. Per sub-account. |
| **GHL total** | **$704** | **$1,168** | |
| Retained: WordPress + WP Engine + Elementor | $25 | $77 | |
| Retained: HIPAA Vault | $50 | $300 | |
| Retained: Medicare Pro + E123 | $150 | $500 | |
| Retained: SendGrid (Twilio) | $15 | $90 | May be redundant with GHL email — evaluate |
| Retained: AWS (existing) | $50 | $500 | |
| Retained: Canva | $13 | $30 | |
| Retained: Riverside + Libsyn | $20 | $44 | |
| Retained: Tax Bandits | $4 | $4 | |
| Retained: LMS | $13 | $55 | |
| Retained: Zapier (reduced) | $20 | $50 | Only for non-GHL integrations |
| Retained: Fathom Analytics | $14 | $24 | |
| **Retained tools subtotal** | **$374** | **$1,674** | |
| **TOTAL MONTHLY** | **$1,018** | **$2,765** | |
| **TOTAL ANNUAL** | **$12,216** | **$33,180** | |

---

## 5. Hours Saved, Labor Value Recovery & ROI Analysis

### Methodology

Hours-saved estimates are based on:
- Published industry data on insurance agent administrative burden
- Average hourly labor costs from Salary.com and PayScale (January 2026)
- Conservative assumptions — actual savings may be higher during peak enrollment periods (AEP/OEP)

### Labor Cost Assumptions

| Role | Avg. Hourly Rate (Fully Loaded) | Source |
|------|-------------------------------|--------|
| Insurance Agent / Broker | $28–$31/hr | Salary.com, ZipRecruiter (Jan 2026) |
| Administrative / Agent Assistant | $15–$17/hr | PayScale (2025) |
| Sales Manager / Team Lead | $35–$45/hr | Salary.com (Insurance Broker avg) |
| Compliance / Operations | $25–$35/hr | Industry estimate |
| **Blended weighted average** | **~$23/hr** | Weighted toward agents (60%) + admin (30%) + management (10%) |

*"Fully loaded" includes salary only. Adding benefits (20–30%) would increase the effective rate to ~$28–$30/hr, making the ROI even stronger. We use the conservative $23/hr base.*

---

### Hours Saved by Task Category

#### AI SDR Agent — Sales Outreach Automation

| Task | Current Hours/Week | Post-Automation Hours/Week | Hours Saved/Week | How It's Automated |
|------|-------------------|--------------------------|-----------------|-------------------|
| Lead qualification & scoring | 10–15 | 1–2 | **9–13** | Bedrock AI scores inbound leads based on fit criteria, demographic data, and engagement signals. Agent reviews AI recommendations rather than manually researching each lead. |
| Outreach email drafting & sending | 5–8 | 0.5–1 | **4.5–7** | n8n workflows generate personalized outreach emails via Bedrock, queue through SendGrid. Agent approves batch sends rather than writing individual emails. |
| SMS follow-up sequences | 3–5 | 0.5 | **2.5–4.5** | Automated SMS follow-up triggered by pipeline stage changes in Notion. n8n sends via Twilio based on configurable timing rules. |
| Voicemail drops | 3–5 | 0.5 | **2.5–4.5** | Automated voicemail delivery via n8n workflow replaces manual slydial usage. |
| Meeting scheduling & reminders | 3–5 | 0.5 | **2.5–4.5** | Calendar integration via n8n — AI agent proposes times, sends confirmations, handles rescheduling. |
| **SDR subtotal** | **24–38** | **3–4.5** | **21–33.5** | |

#### AI BDR Agent — Prospecting Automation

| Task | Current Hours/Week | Post-Automation Hours/Week | Hours Saved/Week | How It's Automated |
|------|-------------------|--------------------------|-----------------|-------------------|
| Prospect list building | 5–8 | 0.5–1 | **4.5–7** | Bedrock AI identifies prospects from data sources matching ideal customer profile. n8n enriches records and pushes to Notion pipeline. |
| Prospect research | 3–5 | 0.5 | **2.5–4.5** | AI agent summarizes prospect background, identifies talking points, flags relevant Medicare enrollment windows. |
| Personalized outreach at scale | 3–5 | 0.5 | **2.5–4.5** | Bedrock generates personalized messaging based on prospect data. Agent reviews and approves rather than writing from scratch. |
| **BDR subtotal** | **11–18** | **1.5–2** | **9.5–16** | |

#### AI Admin Agent — Operations Automation

| Task | Current Hours/Week | Post-Automation Hours/Week | Hours Saved/Week | How It's Automated |
|------|-------------------|--------------------------|-----------------|-------------------|
| Data entry (contacts, enrollment updates) | 6–10 | 1–2 | **5–8** | n8n workflows auto-populate Notion CRM and AWS PHI database from form submissions, email parsing, and enrollment platform data. |
| Pipeline status updates | 3–5 | 0.5 | **2.5–4.5** | Automated stage progression based on triggers (email opened, form submitted, enrollment confirmed). n8n updates Notion pipeline in real-time. |
| Compliance document tracking | 3–5 | 0.5–1 | **2.5–4** | n8n workflows monitor document submissions, flag missing items, send automated reminders. Bedrock AI classifies document types. |
| Appointment scheduling | 2–3 | 0.5 | **1.5–2.5** | Automated via calendar integration. AI Admin handles booking, confirmation, and rescheduling. |
| Report building | 3–5 | 0.5–1 | **2.5–4** | Notion dashboards auto-update. n8n aggregates data from AWS PHI layer for compliance reporting. No manual spreadsheet compilation. |
| **Admin subtotal** | **17–28** | **3–5** | **14–23** | |

#### Tool Consolidation — Reduced Context Switching

| Task | Current Hours/Week | Post-Automation Hours/Week | Hours Saved/Week | How It's Improved |
|------|-------------------|--------------------------|-----------------|-------------------|
| Switching between tools (5–10 platforms daily) | 3–5 | 0.5 | **2.5–4.5** | Notion is the single non-PHI interface. Agents work in one platform instead of 5–10. |
| Duplicate data entry across platforms | 2–5 | 0 | **2–5** | n8n syncs data between systems. Enter once, propagate everywhere. |
| Searching for information across tools | 2–3 | 0.5 | **1.5–2.5** | Centralized in Notion with linked databases. PHI accessed via controlled n8n interfaces. |
| **Context switching subtotal** | **7–13** | **1–1** | **6–12** | |

---

### Total Hours Saved — Summary

| Category | Hours Saved/Week | Hours Saved/Month | Hours Saved/Year |
|----------|-----------------|-------------------|-----------------|
| AI SDR (outreach & follow-up) | 21–33.5 | 84–134 | 1,092–1,742 |
| AI BDR (prospecting) | 9.5–16 | 38–64 | 494–832 |
| AI Admin (operations) | 14–23 | 56–92 | 728–1,196 |
| Tool consolidation (context switching) | 6–12 | 24–48 | 312–624 |
| **TOTAL** | **50.5–84.5 hrs/wk** | **202–338 hrs/mo** | **2,626–4,394 hrs/yr** |

**That's equivalent to 1.3–2.1 full-time employees** (based on 2,080 working hours/year).

*During Medicare Annual Enrollment Period (AEP) and Open Enrollment Period (OEP), agents routinely work 50–70+ hour weeks. Automation savings are amplified during these peak periods — potentially preventing burnout and reducing seasonal staffing needs.*

---

### Financial Value of Hours Saved

| Metric | Conservative | Optimistic |
|--------|-------------|-----------|
| Hours saved per year | 2,626 | 4,394 |
| Blended hourly rate | $23 | $23 |
| **Annual labor value recovered** | **$60,398** | **$101,062** |

### Annual Tool Cost Savings

| Source | Conservative | Optimistic |
|--------|-------------|-----------|
| Eliminated tools (11 tools) | $7,932 | $22,848 |
| Reduced Zapier usage (replaced by n8n) | $240 | $1,200 |
| Potential Five9 reduction (if applicable) | $0 | $3,600 |
| **Annual tool savings** | **$8,172** | **$27,648** |

### Total Annual Value Created

| Category | Conservative | Optimistic |
|----------|-------------|-----------|
| Labor value recovered | $60,398 | $101,062 |
| Tool cost savings | $8,172 | $27,648 |
| **Total annual value** | **$68,570** | **$128,710** |

---

### ROI Calculation — Proposal A (Notion + n8n + AI)

#### Year 1 ROI (10-Seat Scenario)

| Line Item | Conservative | Optimistic |
|-----------|-------------|-----------|
| Total annual value created | $68,570 | $128,710 |
| One-time build investment | ($33,000) | ($33,000) |
| VV engagement fee | ($13,000) | ($13,000) |
| Ongoing costs (10 seats, 12 months) | ($9,240) | ($9,240) |
| **Year 1 total investment** | **($55,240)** | **($55,240)** |
| **Year 1 net value** | **+$13,330** | **+$73,470** |
| **Year 1 ROI** | **24%** | **133%** |

#### Year 2 ROI (10-Seat Scenario, with retainer)

| Line Item | Conservative | Optimistic |
|-----------|-------------|-----------|
| Total annual value created | $68,570 | $128,710 |
| Ongoing costs (10 seats, 12 months) | ($9,240) | ($9,240) |
| VV retainer (12 months) | ($18,000) | ($18,000) |
| **Year 2 total cost** | **($27,240)** | **($27,240)** |
| **Year 2 net value** | **+$41,330** | **+$101,470** |
| **Year 2 ROI** | **152%** | **373%** |

#### Year 2 ROI (10-Seat Scenario, without retainer)

| Line Item | Conservative | Optimistic |
|-----------|-------------|-----------|
| Total annual value created | $68,570 | $128,710 |
| Ongoing costs only | ($9,240) | ($9,240) |
| **Year 2 net value** | **+$59,330** | **+$119,470** |
| **Year 2 ROI** | **642%** | **1,293%** |

#### Payback Period

| Scenario | Payback Period |
|----------|---------------|
| Conservative (low hours saved, low tool savings) | **~10 months** |
| Optimistic (high hours saved, high tool savings) | **~5 months** |

---

### ROI Calculation — Proposal B (GoHighLevel)

GHL automates fewer tasks than Proposal A (no custom AI agents), so hours saved are lower.

| Metric | Proposal B Estimate |
|--------|-------------------|
| Hours saved/year (tool consolidation + basic automation) | 1,040–1,820 |
| Labor value recovered | $23,920–$41,860 |
| Tool cost savings | $7,812–$22,008 |
| **Total annual value** | **$31,732–$63,868** |
| Year 1 investment (setup + ongoing) | $19,216–$42,440 |
| **Year 1 net value** | **+$12,516–$21,428** |
| Year 2 ongoing | $12,216–$33,180 |
| **Year 2 net value** | **+$19,516–$30,688** |

**Proposal B delivers positive ROI but roughly half the value of Proposal A** — because GHL doesn't include custom AI agents for lead qualification, prospecting, or admin automation. The hours saved come primarily from tool consolidation and GHL's built-in workflow automation.

---

### ROI Comparison: A vs. B

| Metric | Proposal A (Conservative) | Proposal A (Optimistic) | Proposal B (Mid-Range) |
|--------|--------------------------|------------------------|----------------------|
| Annual value created | $68,570 | $128,710 | $47,800 |
| Year 1 ROI | 24% | 133% | 35% |
| Year 2 ROI (with retainer) | 152% | 373% | 88% |
| 3-Year cumulative net value | +$95,990 | +$248,410 | +$62,216 |
| Payback period | ~10 months | ~5 months | ~6 months |

**Key insight:** Proposal A creates 1.4–2.7x more value than Proposal B annually. The higher upfront investment is recovered by Month 5–10. By Year 3, Proposal A has generated $96K–$248K in cumulative net value vs. $62K for Proposal B.

---

### Revenue Upside (Not Modeled, But Real)

The above ROI only captures cost savings and labor efficiency. It does not model the revenue upside from:
- **Agents spending 20+ more hours/week selling** instead of doing admin
- **Faster lead response times** (AI SDR responds in minutes, not hours/days)
- **Higher contact rates** from automated multi-channel outreach (email + SMS + voicemail)
- **Reduced lead leakage** — no more leads falling through cracks between 5+ disconnected tools
- **Better enrollment conversion** from more consistent, timely follow-up
- **Reduced AEP/OEP seasonal staffing needs** due to AI handling volume spikes

If even 10% of the recovered agent hours convert to additional enrollments, the revenue impact dwarfs the cost savings.

---

## 6. Side-by-Side Financial Analysis

### Monthly Comparison

| Line Item | Proposal A (10 seats) | Proposal A (25 seats) | Proposal B |
|-----------|----------------------|----------------------|------------|
| Platform (Notion / GHL) | $200 | $600 | $297 |
| Automation (n8n / Zapier) | $30 | $80 | $20–$50 |
| HIPAA compliance | $0 (AWS BAA free) | $0 (AWS BAA free) | $297 |
| AI/LLM | $55 | $350 | $0–$97 |
| Infrastructure | $131–$360 | $131–$360 | Included in GHL |
| Usage-based (SMS, calls, email) | Via SendGrid/Twilio | Via SendGrid/Twilio | $110–$477 |
| DevOps/maintenance | $0–$500 | $0–$500 | $0 |
| Retained tools | $354 | $1,624 | $374–$1,674 |
| **TOTAL** | **$770–$1,560** | **$1,370–$3,514** | **$1,018–$2,765** |

### Annual Comparison

| Scenario | Proposal A (10) | Proposal A (25) | Proposal B |
|----------|----------------|----------------|------------|
| Year 1 (setup + ongoing) | $42,240–$109,720 | $49,440–$133,168 | $19,216–$53,180 |
| Year 2 (ongoing only) | $9,240–$18,720 | $16,440–$42,168 | $12,216–$33,180 |
| Year 3 | $9,240–$18,720 | $16,440–$42,168 | $12,216–$33,180 |
| **3-Year Total** | **$60,720–$147,160** | **$82,320–$217,504** | **$43,648–$119,540** |

### Break-Even Analysis (Proposal A vs. B)

At 10 seats:
- Proposal A Year 2+ saves $2,976–$3,720/yr vs. Proposal B
- Break-even on the upfront investment: **Year 3–4** (depending on actual costs)

At 25 seats:
- Proposal A Year 2+ costs are comparable to Proposal B at the high end
- The value proposition shifts to **customization, AI agents, and vendor independence** rather than pure cost savings

### Break-Even vs. Current State

| Proposal | Breaks even vs. current high-end ($61K/yr) by: |
|----------|------------------------------------------------|
| Proposal A (10 seats) | Year 2 (ongoing costs well below current) |
| Proposal A (25 seats) | Year 2 (ongoing costs below current high-end) |
| Proposal B | Year 1 (lower than current in most scenarios) |

---

## 6. Engagement Structure & Milestones

### VV Consulting Fee Structure

| Component | Amount | Timing |
|-----------|--------|--------|
| Base engagement fee | $10,000 | Due at kickoff (covers Months 1–2) |
| Monthly retainer (15%) | $1,500/mo | Begins Month 3 |
| Month 1 | Covered by base | Discovery + architecture |
| Month 2 | Covered by base | MVP build + first AI agent prototype |
| Month 3 | $1,500 | AI expansion + migration |
| Month 4 | $1,500 | Full rollout + handoff |
| **Total 4-month engagement** | **$13,000** | |
| Post-engagement retainer | $1,500/mo | Optional — cancelable with 30 days notice |

### Milestone Schedule

**Milestone 1: Foundation — End of Month 1 (Week 3)**
| Deliverable | Status Criteria |
|-------------|----------------|
| Process map (all departments) | Complete and reviewed by stakeholders |
| PHI data classification guide | GREEN/RED list finalized |
| Tool audit (all 46 tools) | Active/redundant/orphaned status, contract terms, renewal dates |
| Architecture plan | Approved by client |
| **Go/no-go decision point** | Client approves full build OR stops here with discovery artifacts |

**Milestone 2: MVP / Prototype — End of Month 2 (Week 8)**
| Deliverable | Status Criteria |
|-------------|----------------|
| Notion CRM | Live with core databases, pipeline, locked schemas |
| n8n automation engine | Self-hosted on AWS, operational |
| AWS PHI environment | VPC, RDS, S3, encryption, IAM, CloudTrail — all configured |
| AWS BAA | Signed via AWS Artifact |
| Core automations | Lead routing, notifications, Notion-AWS bridge active |
| PHI sanitization workflows | Active and tested |
| AI SDR agent (prototype) | In testing — demonstrable lead qualification + outreach |
| **Go/no-go decision point** | Client approves AI expansion. **Retainer ($1,500/mo) begins.** |

**Milestone 3: AI Expansion — End of Month 3 (Week 14)**
| Deliverable | Status Criteria |
|-------------|----------------|
| AI SDR agent | In production |
| AI BDR agent | Built and in testing |
| AI Admin agent | Built and in testing |
| PHI scanner | Active — daily Notion scans via Bedrock |
| Integrations | Medicare Pro + E123 connected |
| First migration | At least one department migrated off legacy tools |

**Milestone 4: Full Rollout — End of Month 4 (Week 18)**
| Deliverable | Status Criteria |
|-------------|----------------|
| All AI agents | In production |
| All departments | Migrated and trained (including PHI boundary) |
| Legacy tools | Fully decommissioned |
| Audit process | Quarterly review cadence established |
| Documentation | Complete handoff docs for ongoing operations |
| **Engagement transitions to retainer-only** | |

---

## 7. HIPAA Compliance Deep Dive

### What Is PHI in This Context?

For a Medicare insurance brokerage, PHI includes:
- SSNs
- Dates of birth linked to health information
- Medicare/Medicaid beneficiary numbers
- Health plan enrollment selections
- Policy numbers and coverage details
- Medical conditions, diagnoses, prescriptions
- Signed enrollment applications and health documents
- Communication content referencing health status or treatment

### What Is NOT PHI (Notion-Safe)?

- Names, email addresses, phone numbers (without health context)
- Mailing addresses
- Agent assignments
- Lead sources and referral information
- Deal stages and pipeline positions
- Task statuses and activity dates
- Dollar amounts (commissions, deal values)
- General preference notes (preferred call times, language)

### Compliance Architecture

| Layer | HIPAA Status | BAA | PHI Allowed? |
|-------|-------------|-----|-------------|
| Notion | No BAA (Business plan) | No | **No — PHI-free zone** |
| AWS (RDS, S3, EC2) | HIPAA-eligible services | Yes (free via AWS Artifact) | **Yes — all PHI lives here** |
| AWS Bedrock | HIPAA-eligible service | Yes (same AWS BAA) | **Yes — AI processes PHI here** |
| n8n (self-hosted on AWS) | Runs within AWS HIPAA perimeter | Covered by AWS BAA | **Yes — workflows process PHI within AWS** |
| SendGrid/Twilio | Signs BAA on certain plans | Verify plan tier | **Only if BAA is in place** |
| Medicare Pro / E123 | Industry-regulated platforms | Verify with vendor | **Yes — inherent to their function** |

### Active Campaign — Immediate Compliance Question

Active Campaign only signs BAAs on their Enterprise plan. If The Brokerage Inc. is on a lower tier, **there is an existing HIPAA compliance gap today** — regardless of which proposal is selected. This should be verified immediately.

---

## 8. PHI Leakage Prevention Plan

### Technical Controls (5)

1. **Locked Notion schemas** — Only admins can add database properties. No free-text "notes" fields on contact records. Structured dropdowns and selects only.

2. **n8n sanitization workflows** — All data flowing from AWS → Notion passes through a sanitization step. PHI fields are stripped. Only non-PHI status values ("enrolled", "pending review") write to Notion. If PHI is detected in a Notion-bound payload, the workflow halts and alerts the compliance officer.

3. **Automated PHI scanner** — Daily n8n workflow scans all Notion database records via the Notion API. Checks for SSN patterns (XXX-XX-XXXX), Medicare ID formats, DOB+health keyword combinations, policy number patterns. Uses Claude Haiku via Bedrock for ambiguous content classification. Flags records and notifies compliance officer if PHI found.

4. **n8n as only automated write path** — All programmatic Notion updates route through n8n (and its sanitization layer). Third-party Notion integrations/embeds that could pull PHI are disabled.

5. **AWS-side access controls** — RDS and S3 in private VPC subnet. Access via n8n workflows or admin VPN/bastion only. Least-privilege IAM roles. CloudTrail logging for all access. CloudWatch alarms for anomalous patterns. n8n execution data saving disabled.

### Procedural Controls (3)

6. **Data classification guide** — One-page reference: GREEN (Notion-safe) vs. RED (AWS-only). Real examples from daily brokerage work. Laminated desk cards + Notion wiki page.

7. **Mandatory training** — 30-minute onboarding module in LearnDash. Covers: what PHI is, the boundary, correct system usage, what to do if you make a mistake. Completion tracked with certificates. Annual refresher required.

8. **Incident response** — If PHI is found in Notion: (1) Immediately delete/redact, (2) Log in AWS audit trail, (3) Notify compliance officer within 24 hours, (4) Assess breach threshold, (5) If breach: follow HIPAA Breach Notification Rule (60-day notice to affected individuals, report to HHS), (6) Root cause analysis + control update.

### Organizational Controls (3)

9. **Compliance officer** — Designated owner of the PHI boundary. Reviews scanner reports, approves schema changes, conducts quarterly audits.

10. **Quarterly audits** — Review Notion schemas, n8n workflows, AWS access logs, scanner findings. Document findings. Include in leadership reporting.

11. **"PHI-Free Zone" branding** — Notion homepage banner: "This workspace does not contain Protected Health Information." Reinforced in department meetings during rollout.

---

## 9. Change Management Plan

### Principles
- **Analog first:** Understand the human process before automating
- **Communicate the "why" before the "what":** People resist changes they don't understand
- **No cold cutovers:** Parallel systems during every transition
- **Department-by-department:** Don't migrate everyone at once
- **Quick wins first:** Eliminate obviously orphaned tools early to build momentum
- **Document everything:** Fill the gap left by the previous tech lead

### Roles

| Role | Responsibility | Who |
|------|---------------|-----|
| Executive sponsor | Approves budget, removes organizational blockers, signals priority | Senior leadership |
| Project lead (VV) | Architecture, build, migration, training delivery | VV consultant |
| Change champion (per dept) | Owns transition for their team, collects feedback, escalates issues | Department lead or senior team member |
| Compliance officer | PHI boundary ownership, scanner review, audit process | Designated internal role |

### Communication Cadence

| Event | Frequency | Audience |
|-------|----------|----------|
| Kickoff presentation | Once (Week 1) | All staff |
| Department check-ins | Weekly during migration | Per department |
| Milestone reviews | Monthly (×4) | Leadership + change champions |
| PHI scanner reports | Weekly | Compliance officer |
| Quarterly audits | Quarterly (post-launch) | Leadership |

---

## 10. Risk Assessment & Mitigation Plan

### Risk Scoring

- **Likelihood:** Low (unlikely, <20%), Medium (possible, 20–60%), High (probable, >60%)
- **Impact:** Low (minor inconvenience), Medium (delays or added cost), High (significant disruption), Critical (compliance violation, data breach, or project failure)
- **Risk Level:** Likelihood × Impact → color-coded priority

---

### Category 1: Compliance & HIPAA Risks

| # | Risk | Likelihood | Impact | Risk Level | Detailed Mitigation |
|---|------|-----------|--------|-----------|-------------------|
| C1 | **PHI leaks into Notion** — A user manually enters PHI (Medicare ID, SSN, health plan info) into a Notion database field | Medium | Critical | **HIGH** | **11-control prevention plan:** (1) Locked database schemas — only admins add properties, (2) No free-text notes fields — structured dropdowns only, (3) n8n sanitization workflows strip PHI from all automated Notion writes, (4) PHI detection regex halts workflows if PHI detected in Notion-bound payloads, (5) Daily automated PHI scanner via Bedrock AI scans all Notion records, (6) n8n as only automated write path, (7) Data classification guide (GREEN/RED) distributed to all staff, (8) Mandatory 30-min onboarding training with annual refresher, (9) Documented incident response procedure, (10) Compliance officer reviews scanner reports weekly, (11) "PHI-Free Zone" branding on Notion. **If PHI is found:** immediate deletion, incident logging, breach assessment, HHS notification if threshold met. |
| C2 | **Active Campaign currently has no BAA** — If the current plan is not Enterprise tier, PHI may already be flowing through a non-compliant platform | Medium | Critical | **HIGH** | **Verify immediately** — this is an existing compliance gap that predates this project. Check plan tier and BAA status with Active Campaign account admin. If no BAA: (1) stop sending PHI through AC immediately, (2) escalate to compliance/legal, (3) accelerate migration off AC as part of this project. |
| C3 | **SendGrid/Twilio BAA not configured** — If email/SMS workflows route PHI-adjacent content through SendGrid without a BAA | Medium | High | **HIGH** | Verify SendGrid plan tier supports BAA (Pro plan and above). Sign BAA before any PHI-adjacent communications route through SendGrid. If lower tier, upgrade or evaluate alternative transactional email provider with BAA. |
| C4 | **AWS PHI environment misconfigured** — Encryption not enabled, public subnet exposure, IAM over-permissioned, CloudTrail not active | Low | Critical | **MEDIUM** | Infrastructure-as-code (IaC) templates for reproducible, auditable setup. Security review gate at Milestone 2 before any PHI enters the environment. CloudTrail enabled from day one. Quarterly security audits post-launch. VPC configuration reviewed by AWS-certified professional. |
| C5 | **HIPAA breach notification failure** — PHI breach occurs but incident response is not followed correctly | Low | Critical | **MEDIUM** | Documented incident response procedure included in training. Compliance officer designated before go-live. Procedure tested with tabletop exercise during Milestone 4 training phase. Clear escalation path: detect → delete → log → assess → notify (60-day window for affected individuals per HIPAA Breach Notification Rule). |

---

### Category 2: Operational & Technical Risks

| # | Risk | Likelihood | Impact | Risk Level | Detailed Mitigation |
|---|------|-----------|--------|-----------|-------------------|
| O1 | **Staff resistance to new systems** — Departments push back on changing tools they're familiar with | High | Medium | **HIGH** | Change champions assigned per department — someone who owns the transition for their team. "Why" communicated before "what" in kickoff presentation. Parallel systems during every migration — no cold cutovers. Department-by-department rollout (not all at once). Quick wins first — eliminate obviously orphaned/unused tools early to build momentum and credibility. Weekly check-ins during active migration phases. |
| O2 | **n8n self-hosted goes down** — Server crash, out-of-memory, or failed update takes automation offline | Low | High | **MEDIUM** | AWS Auto Scaling Group or auto-recovery on the n8n EC2 instance. CloudWatch alarms trigger on CPU, memory, disk, and process health — notify admin immediately. Documented restart/recovery playbook. n8n Docker deployment for clean restarts. If extended downtime: manual fallback procedures documented for critical workflows (lead routing, enrollment notifications). |
| O3 | **Notion performance degrades at scale** — Databases with 10K+ records become slow to load and filter | Medium | Medium | **MEDIUM** | Proactive mitigation: archive records older than 12–18 months to a separate "archive" database. Use filtered views (not full-database views) for daily operations. Split large databases by year, department, or pipeline if needed. Notion's API performance is unaffected by database size — only the UI slows down. Monitor during Phase 9 migration as data volume increases. |
| O4 | **Five9 replacement doesn't match capability** — AI dialer or Twilio-based solution can't handle complex call center scenarios (transfers, queues, supervisor monitoring) | Medium | Medium | **MEDIUM** | Evaluate Five9 usage thoroughly during Phase 0. If Five9 handles complex multi-agent call routing, supervisor barge/whisper, or regulatory call recording — retain it. Only replace if usage is simple outbound dialing. Phase 0 deliverable includes Five9 capability assessment. |
| O5 | **AI agent output quality issues** — Bedrock-powered agents produce inaccurate, inappropriate, or off-brand communications | Medium | Medium | **MEDIUM** | All agent outputs go through approval workflows during initial deployment (human-in-the-loop). Prompt engineering includes brand voice guidelines, compliance guardrails, and output validation rules. Agent performance reviewed weekly during Months 2–4. Gradual autonomy — start with AI-assisted (human reviews), move to AI-automated only after confidence is established. |
| O6 | **Integration failures with Medicare Pro / E123** — APIs are limited, undocumented, or require vendor cooperation | Medium | Medium | **MEDIUM** | Research API availability during Phase 0. If no API exists: evaluate CSV export/import via n8n scheduled workflows, or screen scraping as last resort. Engage Medicare Pro / E123 vendor support early. Integration layer build (Phase 8) has 4-week window to accommodate complexity. Worst case: manual processes continue for these tools with Notion as the coordination layer. |
| O7 | **Data migration errors** — Contacts, tags, pipeline data lost or corrupted during migration from Active Campaign / Airtable | Low | High | **MEDIUM** | Full export backups before any migration begins. Migration runs in staging/test environment first. Validation checks: record counts, field mapping spot checks, duplicate detection. Parallel systems — old tools stay active until new system is validated. Rollback plan: restore from backup if critical issues found within 7 days of migration. |

---

### Category 3: Project & Engagement Risks

| # | Risk | Likelihood | Impact | Risk Level | Detailed Mitigation |
|---|------|-----------|--------|-----------|-------------------|
| P1 | **Scope creep during build** — New requirements surface after Phase 0, expanding the build beyond original estimate | Medium | Medium | **MEDIUM** | Fixed 4-milestone structure with go/no-go gates. Scope is locked at Milestone 1 (end of discovery). New requests after scope lock go into a backlog for retainer phase or a separate engagement. VV engagement fee is fixed — scope creep doesn't change the base fee, but may extend the retainer. |
| P2 | **Key person dependency (VV consultant)** — If VV becomes unavailable, institutional knowledge is lost | Medium | Medium | **MEDIUM** | All architecture decisions documented in Notion (meta: the CRM documents its own build). Complete handoff documentation delivered at Milestone 4. n8n workflows are self-documenting (visual flowcharts). Retainer provides ongoing access. If VV is unavailable: another n8n/Notion specialist can pick up from documentation. |
| P3 | **Longer timeline than estimated** — Build takes 5–6 months instead of 4 | Medium | Medium | **MEDIUM** | MVP at Milestone 2 (Month 2) delivers functional value even if later phases delay. Team can use Notion CRM + basic automations while AI agents are still in development. Go/no-go gates prevent sunk cost spiral — if Milestone 1 reveals the project is larger than expected, scope is adjusted before major build investment. |
| P4 | **Budget overrun on one-time costs** — Build costs exceed the $33K–$91K range | Low | Medium | **LOW** | VV engagement is fixed fee ($13K for 4 months). Infrastructure costs (AWS) are usage-based and monitored monthly. Agent build costs are the main variable — mitigated by building SDR first (Milestone 2) and validating cost/effort before committing to BDR and Admin agents. Go/no-go gate at Milestone 2 specifically addresses this. |
| P5 | **Stakeholder alignment breaks down** — Different departments have conflicting requirements that can't be reconciled | Medium | Medium | **MEDIUM** | Phase 0 gives every department a voice before any changes happen. Process map is reviewed and approved by all department leads at Milestone 1. Change champions serve as feedback conduits throughout the build. Executive sponsor resolves conflicts that change champions can't. |

---

### Category 4: Strategic & External Risks

| # | Risk | Likelihood | Impact | Risk Level | Detailed Mitigation |
|---|------|-----------|--------|-----------|-------------------|
| S1 | **AWS Bedrock model availability or pricing changes** — Anthropic or Amazon changes pricing, deprecates a model, or limits availability | Low | Medium | **LOW** | Architecture supports model switching — n8n workflows reference model IDs that can be changed without rebuilding. Bedrock offers Claude, Llama, Mistral, Titan — not locked to one provider. Intelligent prompt routing already routes between models. Pricing changes are gradual and announced in advance. |
| S2 | **Notion changes pricing or feature set** — Notion raises prices, removes features, or changes API limits | Low | Medium | **LOW** | Notion data is fully exportable (CSV, API, Markdown). n8n is open-source and portable. The architecture has low vendor lock-in by design. If Notion becomes unviable: CRM layer can migrate to another database (Airtable, custom app) while n8n and AWS layers remain unchanged. |
| S3 | **Competitor adopts similar AI stack** — Another brokerage builds comparable AI agents | Medium | Low | **LOW** | First-mover advantage. Custom agent training on brokerage-specific data, workflows, and compliance requirements creates differentiation that generic tools can't replicate. The institutional knowledge embedded in the prompts, workflows, and PHI handling is proprietary. |
| S4 | **Regulatory changes to HIPAA requirements** — New rules expand the definition of PHI or add compliance requirements | Low | High | **MEDIUM** | Split architecture is inherently conservative — PHI is already isolated in the most controlled environment possible (encrypted AWS with BAA, private VPC, audit logging). Easier to adapt than a single-vendor platform where compliance is a black box. Compliance officer role includes regulatory monitoring. |
| S5 | **AWS region outage** — US-East-1 or selected region experiences extended downtime | Low | High | **MEDIUM** | Multi-AZ deployment for RDS (high-end configuration). S3 has 99.999999999% durability by design. n8n can be redeployed to alternate region from Docker image + database backup. For critical workflows: document manual fallback procedures. AWS region outages >1 hour are rare but have occurred historically. |

---

### Risk Summary Matrix

| Risk Level | Count | Examples |
|-----------|-------|---------|
| **HIGH** (address immediately) | 3 | PHI in Notion (C1), Active Campaign BAA gap (C2), staff resistance (O1) |
| **MEDIUM** (active mitigation plan) | 11 | AWS misconfiguration (C4), n8n downtime (O2), Notion scale (O3), AI quality (O5), scope creep (P1), timeline (P3), regulatory change (S4) |
| **LOW** (monitor) | 4 | Bedrock pricing (S1), Notion pricing (S2), competitor (S3), budget overrun (P4) |

### Key Takeaway

The three HIGH risks all have concrete mitigation plans:
1. **PHI in Notion** → 11-control prevention plan (the most detailed mitigation in this project)
2. **Active Campaign BAA** → Verify this week, before the project even starts
3. **Staff resistance** → Change management plan with champions, parallel systems, and department-by-department rollout

The architecture itself is designed to contain risk: the split design means a failure in one layer (Notion) doesn't compromise the other (AWS/PHI). Go/no-go gates at Milestones 1 and 2 limit financial exposure if the project proves unfeasible.

---

## 11. Open Questions & Investigation Items

These must be resolved during Phase 0:

| Question | Impact | Who Answers |
|----------|--------|-------------|
| Is Active Campaign on Enterprise plan with a signed BAA? | Critical — existing compliance gap | Account admin / billing |
| How many Five9 seats are active? | Major cost variable ($150–$300/seat/mo) | IT / sales leadership |
| What is Airtable OTP used for? | Determines if it can be eliminated | Department that uses it |
| What is Basefront? | Unknown tool — needs identification | Previous tech lead contacts / billing records |
| What is the Marketing inbox? | Unknown — shared email? Tool? | Marketing team |
| What does Streamlit power? | Determines replacement path | Data / analytics team |
| Is SEO articles a vendor or internal? | Cost and contract implications | Marketing team |
| Is BrightFire billed twice? | Potential immediate savings | Billing records |
| Is YouTube Premium a business or personal expense? | Potential immediate savings | Account holder |
| What is the actual AWS bill breakdown? | Determines true infrastructure baseline | AWS billing console |
| How many total Notion seats are needed? | Directly impacts Proposal A monthly cost | All departments |
| Does the podcast continue? (Riverside + Libsyn) | Determines if these tools stay | Leadership decision |
| What is Couchdrop used for? | Determines replacement path | IT / operations |
| What does HIPAA Vault currently host? | Determines overlap with new AWS PHI layer | IT |
