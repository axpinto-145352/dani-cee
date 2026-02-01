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

## CRM / Sales / Outreach

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Active Campaign | Email marketing / CRM | $150–$500 | Redundant — replace |
| EZ Texting | SMS outreach | $50–$200 | Redundant — replace |
| slydial | Voicemail drops | $30–$100 | Niche — evaluate |
| GMass | Bulk email via Gmail | $20–$50 | Redundant — replace |
| Five9 | Contact center / dialer | $150–$300/seat | Core — evaluate replacement |
| Crisp | Live chat / messaging | $25–$95 | Redundant — replace |
| Quo | Sales engagement | $50–$150 | Redundant — replace |

**Category subtotal: ~$475–$1,395/mo**

---

## Marketing / Content / SEO

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Canva | Design | $13–$30 | Keep |
| Riverside | Podcast/video recording | $15–$24 | Keep if podcast continues |
| Testimonial.to | Video testimonials | $20–$50 | Evaluate ROI |
| UberSuggest | SEO research | $30–$50 | Redundant — evaluate |
| Unbounce | Landing pages | $90–$225 | Redundant — replace |
| SEO articles | Content/SEO service | $200–$500+ | Clarify vendor vs. internal |
| Liberated Syndication | Podcast hosting | $5–$20 | Keep if podcast continues |
| YouTube Premium | Video | $14 | Likely personal — remove |
| BrightFire | Insurance marketing | $100–$500 | Confirm single subscription |

**Category subtotal: ~$487–$1,413/mo**

---

## Website / Web Infrastructure

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| WordPress (main) | Primary website | $0 (open source) | Keep |
| WP Engine | WordPress hosting | $20–$60 | Keep |
| Staging environment TBI | Dev/staging | Included w/ WP Engine | Keep |
| Squarespace | Secondary site | $16–$49 | Redundant — eliminate |
| Elementor | Page builder | $5–$17 | Keep w/ WordPress |
| Gravity Forms | WordPress forms | $5–$20 | Redundant — pick one |
| Fluent Forms | WordPress forms | $5–$10 | Redundant — pick one |
| Forgravity | Gravity Forms add-ons | $10–$20 | Eliminate if Gravity goes |
| Imagify | Image optimization | $5–$10 | Keep — low cost |
| Gravatar | Profile avatars | Free | Keep |

**Category subtotal: ~$66–$186/mo**

---

## Data / Automation / Backend

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Airtable (Admin) | Database / ops | $20–$45/seat | Redundant — replace |
| Airtable | General use | $20–$45/seat | Redundant — replace |
| Airtable OTP | Unknown | $20–$45/seat | Investigate |
| Zapier | Automation | $20–$100+ | Evaluate per proposal |
| SendGrid (Twilio) | Transactional email | $15–$90 | May keep for volume |
| Amazon Web Services | Cloud infra | $50–$500+ | Evaluate what runs here |
| Couchdrop | File transfer / SFTP | $15–$50 | Evaluate necessity |
| HIPAA Vault | HIPAA hosting/storage | $50–$300 | **Keep — non-negotiable** |
| Streamlit | Data apps / dashboards | $0–$250 | Evaluate what it powers |
| Basefront | Unknown | TBD | Investigate |

**Category subtotal: ~$210–$1,425/mo** (varies heavily by seats/usage)

---

## Industry-Specific / Enrollment

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Medicare Pro | Enrollment platform | $100–$300 | **Keep — core business** |
| Medicare Pro Test | Testing environment | Included | Keep |
| E123 | Enrollment / quoting | $50–$200 | **Keep — core business** |

**Category subtotal: ~$150–$500/mo**

---

## Learning / Training

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Cloud Academy | Training platform | $40–$55/seat | Redundant — pick one |
| LearnDash | LMS (WordPress) | $13–$30 | Redundant — pick one |

**Category subtotal: ~$53–$85/mo** (single-seat estimate)

---

## Compliance / Finance / Other

| Tool | Function | Est. Monthly Cost | Status |
|------|----------|-------------------|--------|
| Tax Bandits | Tax filing | Seasonal ~$50/yr | Keep |
| Adobe Pro | PDF / e-sign | $23–$35 | Evaluate if CRM covers e-sign |
| Fathom Analytics | Privacy analytics | $14–$24 | Keep |
| AddEvent | Event scheduling | $0–$16 | Keep if used |
| Marketing inbox | Unknown | TBD | Investigate |

**Category subtotal: ~$37–$75/mo**

---

# Total Estimated Current Spend

| Category | Low Estimate | High Estimate |
|----------|-------------|---------------|
| CRM / Sales / Outreach | $475 | $1,395 |
| Marketing / Content / SEO | $487 | $1,413 |
| Website / Web Infrastructure | $66 | $186 |
| Data / Automation / Backend | $210 | $1,425 |
| Industry / Enrollment | $150 | $500 |
| Learning / Training | $53 | $85 |
| Compliance / Finance / Other | $37 | $75 |
| **TOTAL** | **~$1,478/mo** | **~$5,079/mo** |
| **Annual** | **~$17,736/yr** | **~$60,948/yr** |

*Note: These are estimates based on typical plan pricing. Actual costs require a contract/billing audit in Phase 0. Per-seat tools (Five9, Airtable, Cloud Academy) can scale significantly with headcount.*

---

# Proposal A: Custom-Built AI System + CRM

---

## Proposal A — Philosophy

Build a proprietary AI-powered sales and operations platform tailored to the insurance brokerage model.

**Maximum control. Maximum differentiation. Higher build cost.**

---

## Proposal A — Architecture

**Custom CRM (Core Platform)**
- Contact Management
- Pipeline & Policy Tracking
- HIPAA-Compliant Data Layer (HIPAA Vault / AWS)

**AI SDR/BDR Agents**
- Lead qualification
- Email, SMS, voicemail outreach
- Automated follow-up sequences
- Meeting booking

**AI Admin Agents**
- Data entry automation
- Appointment scheduling
- Compliance document tracking
- Automated reporting

---

## Proposal A — What Gets Built

1. **Custom CRM** — Contacts, pipeline, policy lifecycle, HIPAA-compliant storage
2. **AI SDR Agent** — Lead qualification, initial outreach, follow-up, meeting booking
3. **AI BDR Agent** — Outbound prospecting, list building, personalized outreach at scale
4. **AI Admin Agent** — Data entry, scheduling, compliance tracking, reporting
5. **Integration Layer** — API connections to Medicare Pro, E123, and retained tools

---

## Proposal A — Tools Eliminated

| Tool Eliminated | Replaced By |
|----------------|-------------|
| Active Campaign | Custom CRM + AI agents |
| EZ Texting | CRM SMS module |
| slydial | AI voicemail capability |
| GMass | CRM email engine |
| Crisp | CRM chat module |
| Quo | AI SDR agent |
| Airtable (all 3) | CRM database layer |
| Zapier | Custom integration layer |
| Unbounce | CRM landing pages |
| Five9 | AI dialer (or retain for complex calls) |
| Squarespace | Consolidate to WordPress |

**Estimated monthly savings from eliminated tools: $700–$2,200/mo**

---

## Proposal A — Tools Retained

| Tool | Monthly Cost | Reason |
|------|-------------|--------|
| WordPress + WP Engine + Elementor | $25–$77 | Main website |
| HIPAA Vault | $50–$300 | Compliance — non-negotiable |
| Medicare Pro + E123 | $150–$500 | Core business tools |
| SendGrid | $15–$90 | Transactional email backend |
| AWS | $50–$500+ | Infrastructure for custom platform |
| Canva | $13–$30 | Content design |
| Riverside + Libsyn | $20–$44 | Podcast production |
| Tax Bandits | ~$4 | Tax filing |
| LearnDash (or Cloud Academy) | $13–$55 | Training (pick one) |
| Fathom Analytics | $14–$24 | Privacy-compliant analytics |

**Retained tool spend: ~$354–$1,624/mo**

---

## Proposal A — New Build Costs

| Item | Estimated Cost | Type |
|------|---------------|------|
| CRM development (core platform) | $30,000–$80,000 | One-time |
| AI SDR agent build | $15,000–$40,000 | One-time |
| AI BDR agent build | $10,000–$30,000 | One-time |
| AI Admin agent build | $10,000–$30,000 | One-time |
| Integration layer (Medicare Pro, E123, etc.) | $10,000–$25,000 | One-time |
| AI/LLM API costs (OpenAI, Anthropic, etc.) | $200–$1,000/mo | Ongoing |
| AWS infrastructure (expanded) | $200–$800/mo | Ongoing |
| Ongoing engineering/maintenance | $2,000–$8,000/mo | Ongoing |
| **Total one-time build** | **$75,000–$205,000** | |
| **Total ongoing (new + retained tools)** | **$2,754–$11,424/mo** | |

---

## Proposal A — Timeline

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery & requirements | Weeks 1–3 | Process map complete |
| Phase 1 | CRM core build (contacts, pipeline, HIPAA layer) | Weeks 4–10 | CRM MVP live |
| Phase 2 | AI SDR agent (email + SMS sequences) | Weeks 8–13 | SDR agent in testing |
| Phase 3 | AI BDR agent (prospecting + list building) | Weeks 11–15 | BDR agent in testing |
| Phase 4 | AI Admin agent (scheduling, data entry, compliance) | Weeks 13–18 | Admin agent in testing |
| Phase 5 | Integration layer (Medicare Pro, E123, retained tools) | Weeks 14–19 | Integrations live |
| Phase 6 | Migration & legacy decommission (dept by dept) | Weeks 16–24 | All departments migrated |
| Phase 7 | Training, change management, stabilization | Weeks 20–26 | Full rollout |

**Total: ~6 months to full deployment**

---

## Proposal A — Pros & Cons

**Pros**
- Full control over features and data
- AI agents tuned to insurance sales workflows
- Competitive differentiator — proprietary system
- No per-seat SaaS fees at scale
- HIPAA compliance under your control

**Cons**
- Significant upfront investment ($75K–$205K)
- Requires ongoing engineering resources
- Longer time to value (~6 months)
- CRM is a solved problem — building from scratch carries risk
- Higher change management burden

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

| Tool Eliminated | GHL Feature | Est. Monthly Savings |
|----------------|-------------|---------------------|
| Active Campaign | Email marketing + automation | $150–$500 |
| EZ Texting | Built-in SMS | $50–$200 |
| slydial | Voicemail drop feature | $30–$100 |
| GMass | Email campaigns | $20–$50 |
| Crisp | Chat widget | $25–$95 |
| Quo | Pipeline + sequences | $50–$150 |
| Unbounce | Landing page builder | $90–$225 |
| Gravity Forms / Fluent Forms | Built-in forms | $10–$30 |
| Airtable (all 3) | Custom fields / database | $60–$135 |
| Five9 | Built-in dialer (evaluate) | $150–$300/seat |
| Squarespace | Funnel / site builder | $16–$49 |

**Estimated monthly savings from eliminated tools: $651–$1,834/mo**

---

## Proposal B — Tools Retained

| Tool | Monthly Cost | Reason |
|------|-------------|--------|
| WordPress + WP Engine + Elementor | $25–$77 | Main website (GHL funnels supplement) |
| HIPAA Vault | $50–$300 | Compliance — verify GHL HIPAA status |
| Medicare Pro + E123 | $150–$500 | Core business tools |
| SendGrid | $15–$90 | Transactional email volume |
| AWS | $50–$500+ | If anything critical runs here |
| Canva | $13–$30 | Content design |
| Riverside + Libsyn | $20–$44 | Podcast production |
| Tax Bandits | ~$4 | Tax filing |
| LearnDash (or Cloud Academy) | $13–$55 | Training (pick one) |
| Zapier (reduced) | $20–$50 | Only for non-GHL integrations |
| Fathom Analytics | $14–$24 | Supplement GHL reporting |

**Retained tool spend: ~$374–$1,674/mo**

---

## Proposal B — New Costs

| Item | Estimated Cost | Type |
|------|---------------|------|
| GoHighLevel subscription | $97–$497/mo | Ongoing |
| GHL setup & configuration | $2,000–$5,000 | One-time |
| Data migration (contacts, pipelines, tags) | $1,500–$4,000 | One-time |
| Automation/workflow buildout | $2,000–$6,000 | One-time |
| Training & change management | $1,000–$3,000 | One-time |
| **Total one-time** | **$6,500–$18,000** | |
| **Total ongoing (GHL + retained tools)** | **$471–$2,171/mo** | |

---

## Proposal B — Timeline

| Phase | Description | Duration | Milestone |
|-------|-------------|----------|-----------|
| Phase 0 | Process discovery & requirements | Weeks 1–3 | Process map complete |
| Phase 1 | GHL setup, HIPAA compliance verification | Week 4 | GHL account configured |
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
- Fast deployment (~3.5 months vs. ~6 months)
- Low upfront cost ($6.5K–$18K vs. $75K–$205K)
- Dramatically reduces tool count (45+ down to ~15)
- Single platform for sales, marketing, communication
- No engineering team required for maintenance

**Cons**
- Less customizable than custom build
- Vendor lock-in to GHL
- HIPAA compliance must be independently verified
- May not handle all insurance-specific workflows
- Per-seat/sub-account costs scale with headcount

---

# Side-by-Side Comparison

| Factor | Proposal A (Custom AI) | Proposal B (GHL) |
|--------|----------------------|-------------------|
| **One-time cost** | $75,000–$205,000 | $6,500–$18,000 |
| **Monthly ongoing** | $2,754–$11,424 | $471–$2,171 |
| **Time to full deployment** | ~6 months | ~3.5 months |
| **Tools eliminated** | ~11 | ~11 |
| **Final tool count** | ~12 + custom platform | ~15 |
| **Customization** | Unlimited | Platform-constrained |
| **Engineering required** | Yes — ongoing | No |
| **Competitive advantage** | High | Moderate |
| **Risk** | Higher | Lower |
| **HIPAA compliance** | You control it | Must verify with vendor |
| **Change management lift** | Higher | Lower |
| **Scalability** | No per-seat SaaS limits | Per-seat costs grow |

---

# Cost Comparison Summary

| Scenario | Year 1 Total | Year 2+ Annual |
|----------|-------------|----------------|
| **Current state (estimated)** | $17,736–$60,948 | $17,736–$60,948 |
| **Proposal A (Custom AI)** | $108,048–$342,088 | $33,048–$137,088 |
| **Proposal B (GHL)** | $12,152–$44,052 | $5,652–$26,052 |

*Proposal A breaks even vs. current high-end spend around Year 3–4. Proposal B delivers immediate savings.*

---

# The Hybrid Option

**Best of both worlds — phased approach:**

1. **Now:** Deploy GHL (Proposal B) to stop the bleeding on redundant tools
2. **Months 4–6:** Stabilize operations on GHL
3. **Months 6–12:** Begin building custom AI agents that integrate WITH GHL
4. **Year 2:** Evaluate whether to stay on GHL + AI agents or migrate to fully custom

This gives immediate consolidation wins while pursuing the strategic AI vision without betting everything on an unproven build.

---

# Recommendation

Start with **Phase 0** regardless of proposal chosen.

The process mapping will:
- Reveal which tools are truly redundant vs. serving unique needs
- Surface compliance requirements that constrain platform choices
- Give every department a voice before changes happen
- Produce the requirements needed to evaluate both proposals with real data

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
4. Verify HIPAA compliance requirements for any platform under consideration
5. Present refined proposals with validated cost projections
6. Select approach and begin department-by-department rollout
