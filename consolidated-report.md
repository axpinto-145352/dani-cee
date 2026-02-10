# Tech Stack Consolidation — Consolidated Report
## The Brokerage Inc.

---

**Document Type:** Technical Reference Document
**Version:** 2.0
**Date:** February 2026
**Prepared For:** The Brokerage Inc. Leadership Team
**Prepared By:** Veteran Vectors

---

**Purpose:** This document is the detailed reference companion to the proposal deck. Use it to speak intelligently about every tool, cost, timeline, and architectural decision. It contains the full granular breakdowns behind every number in the presentation.

<div style="page-break-after: always;"></div>

## Table of Contents

1. Current Tool Inventory (Full Detail)
2. AgencyBlock & AgencyIntegrator: The Core Patient Data Systems
3. API Capabilities Report: Full Tool Analysis
4. Data Hygiene Problem & Solution
5. Tool-by-Tool Disposition Plan
6. Proposal A: Full Architecture & Cost Breakdown
7. Proposal B: Full Architecture & Cost Breakdown
8. Hours Saved, Labor Value Recovery & ROI Analysis
9. Side-by-Side Financial Analysis
10. Engagement Structure & Milestones
11. HIPAA Compliance Deep Dive
12. PHI Leakage Prevention Plan
13. Change Management Plan
14. Risk Register
15. Open Questions & Investigation Items

<div style="page-break-after: always;"></div>

## 1. Current Tool Inventory (Full Detail)

**UPDATED: 90+ tools identified** (expanded from initial 46-tool estimate based on new inventory data)

### CRM / Sales / Outreach — 11 Tools

| Tool | Function | Est. Monthly Cost | Pricing Model | Active Users | Status |
|------|----------|-------------------|---------------|-------------|--------|
| Active Campaign | Email marketing / CRM | $150–$500 | Tiered by contact count: Starter ~$15/mo (500 contacts), scales to $500+ for large lists. Enterprise required for BAA. | TBD (audit needed) | Redundant — replace with Notion + n8n + SendGrid |
| EZ Texting | SMS outreach | $50–$200 | Plans start ~$20/mo for 500 credits; scales by message volume per month | TBD | Redundant — replace with n8n SMS via Twilio |
| slydial | Voicemail drops | $30–$100 | Per-use credits (~$0.05–$0.10/drop) or monthly subscription packs | TBD | Niche — evaluate during Phase 0; replace with AI voicemail via n8n if feasible |
| GMass | Bulk email via Gmail | $20–$50 | Standard ~$20/mo per Gmail account; Premium ~$30; Enterprise ~$50 | TBD | Redundant — replace with n8n email via SendGrid |
| Five9 | Contact center / dialer | $150–$300/seat | Core plan ~$149/seat/mo; per-minute telecom usage added on top. This is the most expensive per-seat tool in the stack. | TBD — seat count critical | Core — evaluate replacement during Phase 0. If only 1–2 seats, retain. If 5+, explore AI dialer alternatives. |
| Crisp | Live chat / messaging | $25–$95 | Free basic; Pro ~$25/mo; Unlimited ~$95/mo per workspace | TBD | Redundant — replace with Notion intake forms + n8n routing. Retain if chat volume is high (>100 conversations/mo). |
| Quo | Sales engagement | $50–$150 | Per-seat SaaS pricing; varies by plan tier | TBD | Redundant — replace with AI SDR agent via n8n + Bedrock |
| EZ Texting (ServiceLink) | SMS messaging (possible duplicate) | $50–$200 | Same as EZ Texting — confirm if separate subscription | TBD | Investigate — likely duplicate billing |
| slydocast | Voicemail drops | $30–$100 | Similar to slydial | TBD | Redundant — consolidate voicemail tools |
| My Broadcast | Voicemail drops | $30–$100 | Another voicemail drop service | TBD | Redundant — pick one voicemail tool |
| Grasshopper | Virtual phone | $30–$80 | Solo ~$30/mo; Small Business ~$80/mo | TBD | Evaluate — Five9 may cover this |

**Category subtotal: $610–$1,890/mo ($7,320–$22,680/yr)**

**Key unknowns:** Active Campaign plan tier (is there a BAA?), Five9 seat count (could be the largest single line item), Quo actual usage level, multiple voicemail drop subscriptions (slydial, slydocast, My Broadcast — consolidate to one).

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

### Communication / Collaboration — 6 Tools (NEW CATEGORY)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Zoom | Video meetings / phone system | $15–$20/user | Pro ~$15/user/mo; Business ~$20/user/mo | **Keep** — evaluate seat count during Phase 0 |
| OtterAI | Meeting transcription | $10–$20/user | Pro ~$10/user/mo; Business ~$20/user/mo | **Evaluate** — may replace with AI agent via Bedrock |
| MS365-Teams | Team collaboration | $6–$22/user | Business Basic ~$6/user; Business Premium ~$22/user | **Keep** — core collaboration platform |
| Asana | Project management | $11–$25/user | Premium ~$11/user; Business ~$25/user | **Redundant** — replace with Notion |
| Trello | Task management | $5–$10/user | Standard ~$5/user; Premium ~$10/user | **Redundant** — replace with Notion |

**Category subtotal: $47–$97/mo per user ($564–$1,164/yr per user)**

**Key unknowns:** Seat counts for Zoom, MS365, Asana, Trello — costs scale significantly.

---

### Data / Automation / Backend — 15 Tools (EXPANDED)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Airtable (Admin) | Database / ops tracking | $20–$45/seat | Team ~$20/seat/mo; Business ~$45/seat/mo; scales by seats and record count | **Redundant** — replace with Notion databases |
| Airtable | General use | $20–$45/seat | Same pricing — separate workspace or base from Admin | **Redundant** — replace with Notion databases |
| Airtable OTP | Secure access / unknown | $20–$45/seat | Same pricing — unknown what this base is used for | **Investigate** — determine purpose during Phase 0 |
| AirTable (Justin) | Personal workspace | $20–$45/seat | Personal workspace — additional subscription | **Investigate** — consolidate if possible |
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

### Learning / Training — 5 Tools (EXPANDED)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Cloud Academy | Tech training platform | $40–$55/seat | Individual ~$40/seat/mo; Team ~$55/seat/mo; enterprise negotiated | **Redundant** — pick one LMS |
| LearnDash | LMS (WordPress-based) | $13–$30 | 1 site ~$13/mo; 10 sites ~$30/mo; billed annually | **Redundant** — pick one LMS |
| iSpring | Training software | $4–$7/user | Suite ~$4/user; Max ~$7/user (billed annually) | **Redundant** — third competing LMS |
| MLN | Medicare Learning Network | $0 | CMS resource — free | **Keep** — compliance training resource |
| Scribe | Process documentation | $0–$29/user | Free basic; Pro ~$29/user | **Evaluate** — AI may replace |

**Category subtotal: $57–$121/mo ($684–$1,452/yr)** (single-seat estimate)

**Recommendation:** Three competing LMS platforms is excessive. LearnDash is cheapest and integrates with WordPress. Consolidate to one.

---

### Security / Authentication — 8 Tools (NEW CATEGORY)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| DUO | Multi-factor authentication | $3–$9/user | MFA ~$3/user; Access ~$6/user; Beyond ~$9/user | **Keep** — security required |
| Sophos | Endpoint protection / cybersecurity | $25–$50/endpoint/yr | Intercept X ~$25–$50/endpoint/yr | **Keep** — security required |
| KnowBe4 | Security awareness training | $18–$30/user/yr | Per-user annual licensing | **Keep** — compliance training |
| Avenon | Email security | TBD | Cannot confirm pricing | **Investigate** — clarify during Phase 0 |
| Alarm.com | Security monitoring | $10–$30 | Physical security monitoring | **Evaluate** — is this office security? |
| Checker | Background checks | Per-use | $20–$50 per background check | **Keep** — hiring requirement |
| ControlMap Communications | Compliance platform | TBD | Cannot confirm pricing | **Investigate** |
| Verify Comply | Compliance tracking | TBD | Cannot confirm pricing | **Investigate** |

**Category subtotal: ~$56–$119/mo ($672–$1,428/yr)** (plus per-use background check fees)

---

### Finance / Accounting / HR — 6 Tools (NEW CATEGORY)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Ramp | Expense management | $0–$12/user | Free tier available; Plus ~$12/user/mo | **Evaluate** — may overlap with accounting |
| ADP | Payroll / HR | $50–$200+ | Base platform + per-employee fees | **Keep** — payroll is non-negotiable |
| BILL | Bill payments | $45–$79 | Essentials ~$45/mo; Team ~$79/mo | **Evaluate** — may consolidate with accounting |
| Sage | Accounting software | $25–$75 | Start ~$25/mo; Accounting ~$75/mo | **Redundant** — pick one accounting system |
| Quickbooks | Accounting software | $30–$100 | Simple Start ~$30/mo; Plus ~$100/mo | **Redundant** — pick one accounting system |
| Tax Bandits | Tax filing | ~$4/mo (~$50/yr) | Per-form pricing (e.g. $3–$5 per 1099 form); seasonal use | **Keep** — seasonal, low cost |

**Category subtotal: $154–$470/mo ($1,848–$5,640/yr)**

**Key issue:** Two competing accounting systems (Sage and Quickbooks) is wasteful. Pick one and migrate.

---

### AI Tools — 2 Tools (NEW CATEGORY)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| ChatGPT | AI assistant | $20–$25/user | Plus ~$20/user; Team ~$25/user | **Consolidate to Bedrock** — HIPAA compliance risk |
| Co-pilot | AI assistant (Microsoft) | $30/user | Microsoft 365 Copilot ~$30/user/mo | **Consolidate to Bedrock** — HIPAA compliance risk |

**Category subtotal: $50–$55/mo per user ($600–$660/yr per user)**

**CRITICAL:** Standalone AI subscriptions (ChatGPT, Copilot) are a **HIPAA compliance risk**. Staff may inadvertently paste PHI into these tools. Consolidate all AI usage to AWS Bedrock, which is covered by the AWS BAA.

---

### Office / Other — 5 Tools (NEW CATEGORY)

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Adobe Pro | PDF / e-signing | $23–$35 | Acrobat Pro ~$23/mo; with e-sign features ~$35/mo per license | **Evaluate** — can CRM handle e-sign? |
| Zoho | Business suite / password manager | $3–$45/user | Varies by product; Zoho One ~$45/user/mo | **Investigate** — clarify what Zoho products are in use |
| AddEvent | Event scheduling links | $0–$16 | Free tier available; Pro ~$16/mo for custom branding | **Keep if used** — low cost |
| Fathom Analytics | Privacy-focused analytics | $14–$24 | $14/mo (100K page views); $24/mo (200K) | **Keep** — privacy-compliant analytics |
| Marketing inbox | Unknown | TBD | Cannot confirm — needs investigation | **Investigate** — what is this? |

**Category subtotal: $40–$120/mo ($480–$1,440/yr)**

| Tool | Function | Est. Monthly Cost | Pricing Model | Status |
|------|----------|-------------------|---------------|--------|
| Tax Bandits | Tax filing | ~$4/mo (~$50/yr) | Per-form pricing (e.g. $3–$5 per 1099 form); seasonal use | **Keep** — seasonal, low cost |
| Adobe Pro | PDF / e-signing | $23–$35 | Acrobat Pro ~$23/mo; with e-sign features ~$35/mo per license | **Evaluate** — can n8n + a lighter e-sign solution replace this? |
| Fathom Analytics | Privacy-focused analytics | $14–$24 | $14/mo (100K page views); $24/mo (200K); scales by traffic volume | **Keep** — privacy-compliant, good for HIPAA-sensitive org |
| AddEvent | Event scheduling links | $0–$16 | Free tier available; Pro ~$16/mo for custom branding and more events | **Keep if used** — low cost, evaluate usage during Phase 0 |
| Marketing inbox | Unknown | TBD | Cannot confirm pricing — needs investigation | **Investigate** — what is this? Shared email? Separate tool? |

**Category subtotal: $41–$79/mo ($492–$948/yr)**

**Key unknowns:** Marketing inbox identity, Adobe Pro usage level and potential replacement.

<div style="page-break-after: always;"></div>

## 2. AgencyBlock & AgencyIntegrator: The Core Patient Data Systems

### Overview

The Brokerage Inc. already has two HIPAA-compliant systems for patient data management. These systems are not being replaced — they are being integrated and optimized.

| System | Primary Function | HIPAA Status |
|--------|-----------------|-------------|
| **AgencyBlock** | Patient records, policies, enrollment data, Medicare IDs | HIPAA-compliant (existing BAA) |
| **AgencyIntegrator** | Workflow automation, integrations, process management | HIPAA-compliant (existing BAA) |

### Current Problems

Based on management feedback, both systems share these issues:

| Problem | Impact | Severity |
|---------|--------|----------|
| **Data is messy, old, and redundant** | Inconsistent records, conflicting information, wasted time searching | High |
| **Deceased patient records still active** | Compliance risk, wasted outreach, inaccurate reporting | High |
| **No time to review and purge records** | Problems compound monthly, staff too busy with daily operations | Medium |
| **No regular data hygiene process** | One-time cleanups don't stick; data degrades over time | High |
| **AgencyBlock and AgencyIntegrator don't communicate** | Manual workarounds, duplicate data entry, errors in sync | Critical |
| **Departments create workarounds** | Shadow processes, inconsistent data, frustrated staff | High |

### Why We Keep These Systems

| Reason | Detail |
|--------|--------|
| **Already HIPAA-compliant** | BAAs in place, encryption configured, audit logging active |
| **Contains years of patient data** | Migration would be costly, risky, and time-consuming |
| **Staff already trained** | Learning curve for a replacement would be significant |
| **Industry-specific features** | Built for insurance/Medicare workflows |
| **Cost** | Already paying for these — replacement would add cost, not reduce it |

**The solution is not replacement — it's integration and cleanup.**

### Integration Architecture

We solve the communication problem by adding n8n as a middle layer:

```
┌─────────────────────┐
│     AgencyBlock     │
│   (Patient Records) │
└──────────┬──────────┘
           │ API
           ▼
┌─────────────────────┐     ┌─────────────────────┐
│        n8n          │◄───►│       Notion        │
│  (Integration Hub)  │     │    (Daily CRM)      │
└──────────┬──────────┘     └─────────────────────┘
           │ API
           ▼
┌─────────────────────┐
│  AgencyIntegrator   │
│    (Workflows)      │
└─────────────────────┘
```

**How it works:**
- n8n connects to both AgencyBlock and AgencyIntegrator via their APIs
- When data changes in one system, n8n propagates the change to others
- Notion receives only non-PHI data (names, status, stages) — never patient health information
- Staff work primarily in Notion; AgencyBlock/AgencyIntegrator are accessed only when needed for PHI

<div style="page-break-after: always;"></div>

## 3. API Capabilities Report: Full Tool Analysis

This section documents the API capabilities of every tool in the current tech stack, assessing integration potential with n8n and the proposed architecture.

### API Strength Rating Scale

| Rating | Meaning | Integration Potential |
|--------|---------|----------------------|
| **Excellent** | Full REST/GraphQL API, well-documented, webhooks, all CRUD operations | Full automation possible |
| **Good** | REST API with most needed operations, decent documentation | Most automation possible |
| **Moderate** | Limited API or webhook-only, partial documentation | Some automation, manual gaps |
| **Basic** | Simple endpoints only (send/receive), poor documentation | Limited automation |
| **None** | No API available | Manual only, cannot integrate |

---

### Core Patient Data Systems (HIPAA)

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **AgencyBlock** | REST API | Good | Read/write patient records, enrollment data, policy info, search, webhooks for updates | Rate limits, some bulk operations require pagination | Native n8n node available; custom HTTP requests for advanced operations |
| **AgencyIntegrator** | REST API | Good | Trigger workflows, status updates, data sync, event webhooks | Complex workflow triggers may require custom configuration | HTTP Request node + webhooks; may need custom integration work |

### CRM / Sales / Outreach — 7 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Active Campaign** | REST API v3 | Good | Contacts, lists, tags, campaigns, automations, deals, notes, custom fields, webhooks | Complex automation logic must be built in AC, not just API | Native n8n node; full contact management, campaign triggers |
| **EZ Texting** | REST API | Basic | Send SMS, check delivery status, manage contacts | No advanced workflows, limited webhook support | HTTP Request node; basic send/receive only |
| **slydial** | None | None | N/A | No API exists; voicemail drops are manual or via their interface only | Cannot integrate — replaced by Twilio/n8n |
| **GMass** | Limited | Basic | Send campaigns, track opens/clicks via Google Sheets | Gmail-based, no direct API; relies on Google Sheets integration | Not practical to integrate — replaced by SendGrid |
| **Five9** | REST API + SOAP | Limited | Call data, agent status, campaign management | Real-time call events difficult; complex authentication; SOAP legacy | Partial integration possible; may need to keep Five9 separate for complex call center features |
| **Crisp** | REST API | Moderate | Conversations, contacts, send messages, webhooks | Limited CRM features; best for chat widget only | Native n8n node available; webhook triggers for new conversations |
| **Quo** | REST API | Moderate | Contacts, sequences, activities, tasks | Limited documentation; may require vendor support | HTTP Request node; being replaced by AI SDR agent |

### Marketing / Content / SEO — 9 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Canva** | REST API | Moderate | Export designs, access brand kit, create designs from templates | Cannot programmatically edit complex designs; template-based only | HTTP Request node; useful for automated design exports |
| **Riverside** | Limited | Basic | Export recordings, manage guests | No real-time integration; mostly manual workflow | Webhook for recording completion; manual download |
| **Testimonial.to** | REST API | Moderate | Retrieve testimonials, embed codes, submission webhooks | Limited write operations | Webhook for new testimonials; display automation |
| **UberSuggest** | None | None | N/A | No public API; data must be exported manually | Cannot integrate — manual SEO research tool |
| **Unbounce** | REST API + Webhooks | Moderate | Page stats, lead capture webhooks, A/B test data | Cannot programmatically create/edit pages | Webhook for lead capture; being replaced by WordPress |
| **SEO articles** | N/A | N/A | Vendor service, not a tool | N/A | N/A — human vendor relationship |
| **Libsyn** | REST API | Basic | Episode data, download stats | Cannot upload via API on all plans | Limited integration; mostly manual |
| **YouTube Premium** | N/A | N/A | Consumer subscription, not a tool | N/A | N/A — likely personal expense |
| **BrightFire** | Unknown | Unknown | Insurance marketing platform | Requires vendor confirmation | TBD — investigate during Phase 0 |

### Website / Web Infrastructure — 10 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **WordPress** | REST API | Good | Posts, pages, users, media, custom post types, custom fields (with plugins) | Plugin-dependent for advanced features; authentication can be complex | Native n8n node; full content management |
| **WP Engine** | REST API | Moderate | Environment management, backups, cache clearing | Hosting-level operations only; not content | HTTP Request node; useful for deployment automation |
| **Squarespace** | REST API | Limited | Pages, products, orders, inventory | Cannot fully manage site design via API | Limited integration; being consolidated to WordPress |
| **Elementor** | None | None | N/A | Page builder with no API; changes require WP admin | Cannot integrate — visual editing only |
| **Gravity Forms** | REST API | Good | Entries, forms, fields, notifications | Requires WordPress REST API access | Native n8n node via WordPress; form submission webhooks |
| **Fluent Forms** | REST API | Good | Similar to Gravity Forms | Requires WordPress REST API access | HTTP Request node; webhook triggers |
| **Forgravity** | N/A | N/A | Gravity Forms add-on | Depends on Gravity Forms | N/A — plugin, not standalone tool |
| **Imagify** | REST API | Basic | Optimize images, check usage | Simple operations only | HTTP Request node; batch optimization possible |
| **Gravatar** | REST API | Basic | Retrieve avatars by email hash | Read-only; cannot modify profiles | HTTP Request node; avatar lookup |

### Data / Automation / Backend — 10 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Airtable** | REST API | Excellent | Full CRUD on all records, views, attachments, webhooks, formula fields | 5 requests/second rate limit; large bases can be slow | Native n8n node; full database automation |
| **Zapier** | REST API + Webhooks | Excellent | 5,000+ app integrations, webhook triggers | Being replaced by n8n | N/A — competitor being replaced |
| **SendGrid** | REST API | Excellent | Send email, templates, contacts, analytics, webhooks for events | Deliverability requires proper domain setup | Native n8n node; full email automation |
| **Twilio** | REST API | Excellent | SMS, voice, WhatsApp, verify, webhooks | Usage-based pricing can add up | Native n8n node; SMS/voice automation |
| **Amazon Web Services** | Multiple APIs | Excellent | S3, RDS, EC2, Bedrock, SES, SNS, Lambda — full infrastructure | Complexity; requires AWS expertise | Native n8n nodes for most services; Bedrock via HTTP |
| **Couchdrop** | REST API | Moderate | File transfer, SFTP, cloud storage sync | Limited to file operations | HTTP Request node; file transfer automation |
| **HIPAA Vault** | Basic | Basic | File storage, basic management | Limited API; mostly portal access | Limited integration; may need manual processes |
| **Streamlit** | None | None | N/A | Python app framework; no management API | Cannot integrate — application runtime, not service |
| **Basefront** | Unknown | Unknown | Unidentified tool | Requires investigation | TBD — investigate during Phase 0 |

### Industry-Specific / Enrollment — 3 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Medicare Pro** | REST API | Good | Enrollment status, quotes, carrier data, agent assignments | Rate limits; requires vendor partnership | HTTP Request node; enrollment pipeline sync |
| **Medicare Pro Test** | Same as Medicare Pro | Good | Test environment | Same as production | Same integration approach |
| **E123** | REST API | Moderate | Quoting, enrollment submission, status tracking | Documentation may be limited | HTTP Request node; quote-to-enrollment automation |

### Learning / Training — 2 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Cloud Academy** | REST API | Moderate | User management, course assignments, completion tracking | Limited content creation via API | HTTP Request node; training completion triggers |
| **LearnDash** | REST API (WordPress) | Moderate | Courses, lessons, quizzes, user progress | Requires WordPress REST API | WordPress node + custom endpoints |

### Compliance / Finance / Other — 5 Tools

| Tool | API Type | Strength | Key Capabilities | Limitations | n8n Integration |
|------|----------|----------|------------------|-------------|-----------------|
| **Tax Bandits** | REST API | Moderate | 1099 generation, filing status | Seasonal use; mostly batch operations | HTTP Request node; year-end automation |
| **Adobe Pro** | Limited | Basic | PDF operations via Adobe Document Services | Complex authentication; per-document pricing | Limited; may be replaced by simpler PDF tools |
| **Fathom Analytics** | REST API | Moderate | Site stats, custom events | Read-only; no data push | HTTP Request node; dashboard data pull |
| **AddEvent** | REST API | Moderate | Create events, RSVPs, calendar sync | Simple event management | HTTP Request node; event creation automation |
| **Marketing inbox** | Unknown | Unknown | Unidentified | Requires investigation | TBD — investigate during Phase 0 |

---

### API Integration Architecture Summary

**Tools with Excellent/Good APIs (Full Integration Possible):**
- AgencyBlock, AgencyIntegrator, Active Campaign, Airtable, SendGrid, Twilio, AWS, WordPress, Gravity Forms, Medicare Pro

**Tools with Moderate APIs (Partial Integration):**
- Canva, Testimonial.to, Unbounce (webhooks), WP Engine, E123, Cloud Academy, LearnDash, Fathom, AddEvent

**Tools with Basic/No APIs (Manual or Replaced):**
- slydial (None — replaced), GMass (Limited — replaced), EZ Texting (Basic — replaced), Squarespace (Limited — migrated), Elementor (None — visual tool), HIPAA Vault (Basic), Streamlit (None)

**Tools Requiring Investigation:**
- BrightFire, Basefront, Marketing inbox, Five9 (complex)

<div style="page-break-after: always;"></div>

## 4. Data Hygiene Problem & Solution

### The Current State of Patient Data

Based on management feedback, AgencyBlock and AgencyIntegrator contain:

| Data Quality Issue | Estimated Prevalence | Impact |
|-------------------|---------------------|--------|
| **Deceased patient records** | Unknown — common in systems 5+ years old | Compliance risk, wasted marketing spend, inaccurate metrics |
| **Duplicate records** | Typically 10–30% of records in unmanaged systems | Conflicting information, split history, reporting errors |
| **Outdated contact information** | Degrades 2–3% per month naturally | Failed outreach, returned mail, frustrated staff |
| **Incomplete records** | Varies by data entry discipline | Missing critical fields for compliance, enrollment |
| **Inconsistent formatting** | Common without validation rules | Phone numbers, addresses, names in different formats |
| **Orphaned records** | Agents who left, abandoned leads | Database bloat, confusion about ownership |

### Why Manual Cleanup Doesn't Work

| Approach | Problem |
|----------|---------|
| "We'll clean it up when we have time" | Time never comes; daily operations take priority |
| One-time cleanup project | Data degrades immediately after; no lasting improvement |
| Individual staff responsibility | Inconsistent, no accountability, no standardization |
| Annual cleanup | Too infrequent; problems compound for 11 months |

### The Data Hygiene Solution

#### Phase 1: Initial Cleanup (One-Time)

| Task | Method | Deliverable |
|------|--------|-------------|
| **Deceased record identification** | Cross-reference against SSDI (Social Security Death Index), state death registries, DMF (Death Master File) | Flagged records for human review; no auto-deletion |
| **Duplicate detection** | AI-powered fuzzy matching across both systems (name, DOB, SSN, address, phone) | Merge candidates with confidence scores |
| **Duplicate resolution** | High-confidence: auto-merge with audit trail. Low-confidence: human review queue | Single "golden record" per patient |
| **Data standardization** | Normalize phone (E.164), address (USPS), name (proper case) | Consistent formatting across all records |
| **Missing data audit** | Identify records missing critical fields (DOB, Medicare ID, contact info) | Report + action items by agent/department |
| **Archive inactive records** | Flag records with no activity in 3+ years | Archived status (retained but hidden from active views) |

**Estimated one-time cost: $4,000–$10,000** (depends on record volume and data quality)

#### Phase 2: Ongoing Hygiene (Automated)

| Task | Frequency | Method |
|------|-----------|--------|
| **New record validation** | Real-time (every new entry) | n8n workflow checks for duplicates, validates required fields, standardizes format before save |
| **Death registry check** | Monthly | Automated batch query against DMF; flagged records sent to compliance for review |
| **Duplicate monitoring** | Weekly | AI scan for new duplicates created since last check |
| **Data decay detection** | Monthly | Flag records with bounced emails, disconnected phones, returned mail |
| **Compliance completeness** | Weekly | Audit records approaching renewal for missing required fields |
| **Data quality dashboard** | Real-time | Notion dashboard showing health metrics: duplicate rate, completeness %, decay rate |

**Estimated ongoing cost: $50–$100/month** (n8n workflows + AI processing + registry access)

### Data Hygiene Cost Breakdown

| Item | One-Time | Monthly | Pricing Basis |
|------|----------|---------|---------------|
| Death registry access (DMF/SSDI) | $500–$1,000 | $50–$100 | Per-query or subscription; volume-dependent |
| AI duplicate detection (Bedrock) | $200–$500 | $10–$30 | Token usage for fuzzy matching |
| n8n workflow development | $2,000–$5,000 | $0 | One-time build; included in integration layer |
| Manual review labor (internal) | $500–$2,000 | $0–$200 | Staff time for edge cases; may be internal |
| Data standardization scripts | $500–$1,000 | $0 | One-time build |
| Quality dashboard (Notion) | $300–$500 | $0 | Included in Notion CRM build |
| **TOTAL** | **$4,000–$10,000** | **$50–$100** | |

### Expected Outcomes

| Metric | Before | After (3 months) | After (12 months) |
|--------|--------|-----------------|-------------------|
| Duplicate rate | 10–30% (est.) | <5% | <2% |
| Deceased records in active status | Unknown | 0 (flagged for review) | 0 (ongoing monitoring) |
| Records with missing critical fields | Unknown | Identified, action plan | <5% |
| Data format consistency | Low | 80%+ | 95%+ |
| Staff time on data issues | 3–5 hrs/week | 1 hr/week | <30 min/week |

---

### AI-Powered Data Hygiene: Technical Implementation

#### Why AI Instead of Rules-Based Matching?

Traditional data cleanup tools rely on exact matches or simple fuzzy rules. They fail when:
- Names have common variations (Jon/John, Bill/William, Cathy/Catherine)
- Addresses use different formats (St/Street, Apt/Unit/#)
- Records are incomplete (missing DOB, partial phone numbers)
- Deceased status isn't in a death registry (recent deaths, out-of-state deaths)

**AI-powered hygiene using Claude Haiku via AWS Bedrock provides:**

| Capability | Technical Implementation | Advantage Over Rules |
|-----------|------------------------|---------------------|
| **Fuzzy name matching** | Embedding similarity + LLM verification | Catches variations rules miss (Jon/John) |
| **Address normalization** | USPS standardization + LLM interpretation | Handles "123 Main" vs "123 Main Street Apt 2" |
| **Deceased pattern detection** | Multi-factor scoring via LLM | Finds deceased records not in death registries |
| **Context-aware PHI detection** | LLM classification of free-text fields | Catches Medicare IDs in notes fields |
| **Confidence scoring** | LLM probability assessment | Enables automated vs. human-review routing |

#### Confidence-Based Automation Workflow

All AI decisions are routed based on confidence level:

```
┌─────────────────┐
│  Record Pair    │
│  for Analysis   │
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│   AI Analysis   │
│  (Claude Haiku) │
└────────┬────────┘
         │
    ┌────┴────┐
    │Confidence│
    │  Score   │
    └────┬────┘
         │
    ┌────┼────────────────┐
    │    │                │
    ▼    ▼                ▼
┌──────┐ ┌──────┐    ┌──────┐
│ 90%+ │ │70-90%│    │ <70% │
│ HIGH │ │MEDIUM│    │ LOW  │
└──┬───┘ └──┬───┘    └──┬───┘
   │        │           │
   ▼        ▼           ▼
┌──────┐ ┌──────┐    ┌──────┐
│ Auto │ │Human │    │ Flag │
│Apply │ │Review│    │ Only │
│+Audit│ │Queue │    │      │
└──────┘ └──────┘    └──────┘
```

**Routing rules:**
- **High confidence (90%+):** Auto-applied with full audit trail. Human notified but no action required.
- **Medium confidence (70–90%):** Queued for human review. AI provides recommendation + reasoning.
- **Low confidence (<70%):** Flagged for awareness. No action taken. Available for manual investigation.

#### Sample Prompts: Duplicate Detection

**System prompt for duplicate detection:**

```
You are a data quality analyst for a Medicare insurance brokerage. Your task is to
determine if two patient records represent the same person.

Consider these factors:
1. Name similarity (account for common nicknames: Bill/William, Jon/John, etc.)
2. Address similarity (normalize: St=Street, Apt=Unit, etc.)
3. Phone number (ignore formatting differences)
4. Date of birth (exact match is strong signal)
5. Medicare ID (if available, even partial matches are significant)
6. Last contact date and activity patterns

Return a JSON response with:
- match_confidence: 0-100 (probability these are the same person)
- reasoning: Brief explanation of your assessment
- recommended_action: "merge", "review", or "flag_only"
- primary_record: Which record should be kept as primary (more complete/recent)
```

**Example input:**

```
Record A:
- Name: Jon Smith
- Address: 123 Main St, Springfield, IL 62701
- Phone: 217-555-1234
- DOB: 05/15/1945
- Medicare ID: 1EG4-TE5-MK72
- Last contact: 2023-06-15

Record B:
- Name: John Smith
- Address: 123 Main Street, Apt 2, Springfield, IL 62701
- Phone: (217) 555-1234
- DOB: 5/15/1945
- Medicare ID: [not recorded]
- Last contact: 2024-02-20
```

**Example AI response:**

```json
{
  "match_confidence": 94,
  "reasoning": "Strong match based on: (1) Name 'Jon' is common variant of 'John' - 95% name similarity, (2) Same base address with unit added - likely moved within building or data entry variation, (3) Identical phone number after normalization, (4) Identical DOB, (5) Activity in both records suggests same active enrollee. The only uncertainty is the apartment number difference, which could indicate a move or data entry inconsistency.",
  "recommended_action": "merge",
  "primary_record": "B",
  "merge_notes": "Keep Record B as primary (more recent contact, has apartment number). Archive Record A. Copy Medicare ID from A to B."
}
```

#### Sample Prompts: Deceased Detection

**System prompt for deceased detection:**

```
You are a compliance analyst for a Medicare insurance brokerage. Your task is to
assess whether a patient record may represent a deceased individual, even if no
death record is available.

Consider these signals:
1. Age (patients 85+ have higher mortality rates)
2. Last contact date (no activity in 2+ years is unusual for Medicare enrollees)
3. Communication failures (disconnected phones, returned mail)
4. Policy status (no renewal, lapsed coverage)
5. Activity patterns in AgencyIntegrator (no claims, no inquiries)

Be conservative: false positives (flagging living patients) are more harmful than
false negatives (missing deceased patients).

Return a JSON response with:
- deceased_probability: 0-100
- signals_present: List of signals that suggest deceased status
- signals_absent: List of signals that suggest the patient is still living
- recommended_action: "flag_for_review", "attempt_contact", or "no_action"
- reasoning: Brief explanation
```

**Example input:**

```
Record:
- Name: Mary Johnson
- DOB: 03/12/1932
- Age: 93
- Last contact: 2021-01-15
- Phone status: Disconnected (last 2 outreach attempts failed)
- Address: 456 Oak Lane, Springfield, IL 62702
- Policy status: Not renewed since 2021
- AgencyIntegrator activity: No claims since December 2020
- Death registry match: None found
```

**Example AI response:**

```json
{
  "deceased_probability": 78,
  "signals_present": [
    "Age 93 - high mortality probability for Medicare population",
    "No contact in 3+ years - unusual for active enrollee",
    "Phone disconnected - communication channel lost",
    "Policy not renewed since 2021",
    "No claims activity in 3+ years"
  ],
  "signals_absent": [
    "No death registry match found",
    "No returned mail indicator",
    "Address still valid (no forwarding notice)"
  ],
  "recommended_action": "flag_for_review",
  "reasoning": "Multiple signals are consistent with deceased status (age, inactivity, disconnected phone, no claims). However, absence of death registry match and valid address suggest some uncertainty. Recommend: (1) Attempt one certified mail contact, (2) Check with local Social Security office if no response, (3) Add to compliance review queue. Do NOT auto-archive without human confirmation.",
  "next_steps": [
    "Send certified letter to address on file",
    "Wait 30 days for response",
    "If no response, escalate to compliance officer for final determination"
  ]
}
```

#### AI Data Hygiene: Detailed Cost Model

**Token usage estimates based on record complexity:**

| Operation | Tokens per Record | Records | Total Tokens | Cost (Haiku) |
|-----------|------------------|---------|--------------|--------------|
| **Duplicate comparison** | 800–1,200 | 10,000 comparisons | 10M | $15–$25 |
| **Deceased detection** | 600–900 | 10,000 records | 8M | $12–$20 |
| **Data standardization** | 300–500 | 10,000 records | 4M | $6–$12 |
| **Quality scoring** | 400–600 | 10,000 records | 5M | $8–$15 |
| **Initial cleanup total** | | | ~27M tokens | **$41–$72** |

*Note: Haiku pricing is $0.25/1M input tokens + $1.25/1M output tokens. Estimates assume 70% input, 30% output.*

**Ongoing monthly costs:**

| Operation | Frequency | Records/Month | Tokens | Monthly Cost |
|-----------|-----------|---------------|--------|--------------|
| New record validation | Real-time | 500 new records | 500K | $2–$4 |
| Duplicate scan | Weekly | 2,000 scans | 2M | $5–$10 |
| Deceased check | Monthly | 10,000 records | 8M | $12–$20 |
| Quality monitoring | Weekly | 1,000 samples | 800K | $3–$6 |
| **Monthly total** | | | ~11M tokens | **$22–$40** |

**Cost comparison:**

| Method | Initial Cleanup (10K records) | Ongoing (monthly) |
|--------|------------------------------|-------------------|
| Manual review ($25/hr) | $2,500–$5,000 | $500–$1,000 |
| Traditional dedup software | $500–$2,000 + license | $100–$300 |
| **AI-powered (Haiku)** | **$41–$72** | **$22–$40** |

AI-powered hygiene is 10–50x cheaper than manual review and provides better accuracy than rules-based tools.

<div style="page-break-after: always;"></div>

## 5. Tool-by-Tool Disposition Plan

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

## 6. Proposal A: Full Architecture & Cost Breakdown

### Architecture: Integration-First Approach (Updated)

**Key Change:** We keep AgencyBlock and AgencyIntegrator as the HIPAA-compliant patient data systems. We do NOT build a new AWS PHI database. Instead, n8n integrates existing systems and Notion provides the modern front-end.

**Layer 1 — AgencyBlock + AgencyIntegrator (Existing PHI Systems — KEPT)**
- **AgencyBlock:** Patient records, Medicare IDs, policy numbers, enrollment data, health plan selections
- **AgencyIntegrator:** Workflow automation, carrier integrations, process management
- Both systems remain the source of truth for all PHI
- Existing BAAs remain in place — no new compliance agreements needed
- n8n connects to these systems via their APIs

**Layer 2 — Notion (Non-PHI CRM & Operations)**
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

**Layer 3 — n8n (Integration & Automation Hub)**
- Self-hosted on AWS EC2 (automation engine)
- **Solves the core problem:** Bridges AgencyBlock and AgencyIntegrator so they finally communicate
- Syncs status information from PHI systems to Notion (sanitized — no PHI transferred)
- Orchestrates all workflows: lead routing, enrollment status updates, notifications
- Runs data hygiene workflows (duplicate detection, deceased record flagging)

**Layer 4 — AWS Bedrock (HIPAA-Compliant AI)**
- All LLM inference routes through Bedrock
- HIPAA-eligible service covered by AWS BAA
- Models available: Claude Haiku, Sonnet, Opus; Amazon Titan; Llama; Mistral
- n8n calls Bedrock APIs for AI agent operations and data hygiene

**Layer 5 — AI Agents (Orchestrated by n8n via Bedrock)**
- AI SDR: lead qualification, outreach, follow-up, meeting booking
- AI BDR: prospecting, list building, personalized outreach
- AI Admin: data entry, scheduling, compliance tracking, reporting

**Layer 6 — Data Hygiene System**
- Initial cleanup: deceased record identification, duplicate detection, standardization
- Ongoing hygiene: new record validation, monthly death registry checks, weekly duplicate scans
- Quality dashboard in Notion showing data health metrics

---

### Proposal A — One-Time Costs (Detailed) — UPDATED

| Item | Low | High | What This Pays For |
|------|-----|------|-------------------|
| Notion CRM setup & config | $3,000 | $8,000 | Database architecture (contacts, deals, policies, tasks), relations and rollups, views (Kanban, table, timeline, calendar), templates, permission structure, locked schemas |
| AI SDR agent build | $8,000 | $20,000 | n8n workflow design, Bedrock integration, prompt engineering, email/SMS sequence logic, lead scoring model, follow-up triggers, meeting booking integration, testing |
| AI BDR agent build | $5,000 | $15,000 | Prospecting logic, list enrichment workflows, personalized outreach templates, Bedrock integration, data source connections, testing |
| AI Admin agent build | $5,000 | $15,000 | Data entry automation workflows, scheduling integrations, compliance document tracking, reporting dashboards, Bedrock integration, testing |
| Integration layer (n8n) | $6,000 | $18,000 | **API connections to AgencyBlock, AgencyIntegrator**, Medicare Pro, E123, SendGrid/Twilio, Notion API, Bedrock API; data sync logic; error handling; retry mechanisms. **Increased** to account for AgencyBlock/AgencyIntegrator integration complexity. |
| PHI prevention system | $2,500 | $6,000 | Sanitization workflows, PHI scanner (Bedrock-powered), data classification guide, LearnDash training module |
| **Data hygiene: initial cleanup** | $4,000 | $10,000 | **NEW:** Deceased record identification (death registry cross-reference), duplicate detection/resolution, data standardization, missing data audit, archive inactive records |
| Data migration | $2,000 | $5,000 | Contact export from Active Campaign + Airtable, data cleaning, Notion import, validation |
| Training & change management | $1,000 | $3,000 | Per-department training sessions, user guides, PHI boundary training, change champion onboarding |
| **TOTAL ONE-TIME** | **$36,500** | **$100,000** | |

*Note: AWS PHI environment setup removed — we are keeping AgencyBlock/AgencyIntegrator instead of building new PHI infrastructure. Integration layer cost increased to account for connecting to these existing systems.*

---

### Proposal A — Monthly Ongoing Costs (Detailed) — UPDATED

| Item | Low (10 seats) | High (25 seats) | Pricing Detail |
|------|----------------|-----------------|----------------|
| Notion Business | $200 | $600 | $20/user/mo (annual) or $24/user/mo (monthly). Business tier needed for schema locking + private teamspaces. |
| n8n EC2 server | $30 | $80 | t3.medium instance ($0.0416/hr) + 50GB EBS. Handles all automation workloads + AgencyBlock/AgencyIntegrator integrations. |
| **Data hygiene automation** | $50 | $100 | **NEW:** Death registry access, AI duplicate detection, quality monitoring. Ongoing after initial cleanup. |
| Data transfer | $5 | $30 | Inter-service API calls, Notion sync, SendGrid, AgencyBlock/AgencyIntegrator API calls. |

*Note: RDS, S3, VPC, KMS costs removed — patient data remains in AgencyBlock/AgencyIntegrator. AgencyBlock and AgencyIntegrator costs continue as-is (already in budget).*
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
| Veteran Vectors engagement fee | ($13,000) | ($13,000) |
| Ongoing costs (10 seats, 12 months) | ($9,240) | ($9,240) |
| **Year 1 total investment** | **($55,240)** | **($55,240)** |
| **Year 1 net value** | **+$13,330** | **+$73,470** |
| **Year 1 ROI** | **24%** | **133%** |

#### Year 2 ROI (10-Seat Scenario, with retainer)

| Line Item | Conservative | Optimistic |
|-----------|-------------|-----------|
| Total annual value created | $68,570 | $128,710 |
| Ongoing costs (10 seats, 12 months) | ($9,240) | ($9,240) |
| Veteran Vectors retainer (12 months) | ($18,000) | ($18,000) |
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

### Veteran Vectors Fee Structure

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
| Project lead (Veteran Vectors) | Architecture, build, migration, training delivery | Veteran Vectors consultant |
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
| P1 | **Scope creep during build** — New requirements surface after Phase 0, expanding the build beyond original estimate | Medium | Medium | **MEDIUM** | Fixed 4-milestone structure with go/no-go gates. Scope is locked at Milestone 1 (end of discovery). New requests after scope lock go into a backlog for retainer phase or a separate engagement. Veteran Vectors engagement fee is fixed — scope creep doesn't change the base fee, but may extend the retainer. |
| P2 | **Key person dependency (Veteran Vectors consultant)** — If Veteran Vectors becomes unavailable, institutional knowledge is lost | Medium | Medium | **MEDIUM** | All architecture decisions documented in Notion (meta: the CRM documents its own build). Complete handoff documentation delivered at Milestone 4. n8n workflows are self-documenting (visual flowcharts). Retainer provides ongoing access. If Veteran Vectors is unavailable: another n8n/Notion specialist can pick up from documentation. |
| P3 | **Longer timeline than estimated** — Build takes 5–6 months instead of 4 | Medium | Medium | **MEDIUM** | MVP at Milestone 2 (Month 2) delivers functional value even if later phases delay. Team can use Notion CRM + basic automations while AI agents are still in development. Go/no-go gates prevent sunk cost spiral — if Milestone 1 reveals the project is larger than expected, scope is adjusted before major build investment. |
| P4 | **Budget overrun on one-time costs** — Build costs exceed the $33K–$91K range | Low | Medium | **LOW** | Veteran Vectors engagement is fixed fee ($13K for 4 months). Infrastructure costs (AWS) are usage-based and monitored monthly. Agent build costs are the main variable — mitigated by building SDR first (Milestone 2) and validating cost/effort before committing to BDR and Admin agents. Go/no-go gate at Milestone 2 specifically addresses this. |
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
