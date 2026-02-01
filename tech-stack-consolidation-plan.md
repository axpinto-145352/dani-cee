# Tech Stack Consolidation — Build-Out Plan

## Context

The Brokerage Inc. has accumulated significant tech redundancy across siloed departments. The previous tech lead departed without documentation. This plan takes a foundation-first approach: define the root processes, then rebuild the tooling layer on top.

---

## Phase 0: Process Discovery (Analog First)

Before selecting any tools, map the actual workflows across every department and vertical.

### Steps
1. **Department inventory** — List every department/vertical and their primary functions
2. **Process mapping** — For each department, document:
   - Core workflows (lead gen, enrollment, retention, marketing, compliance, training, admin)
   - Who does what, when, and how often
   - Handoff points between departments
   - Compliance/HIPAA requirements per workflow
3. **Current tool-to-process mapping** — For each tool below, identify:
   - Which department uses it
   - What process it supports
   - Whether it is actively used, redundant, or orphaned
4. **Gap and overlap analysis** — Identify processes that are duplicated across tools and processes that have no tool support

### Deliverable
A process map document that becomes the single source of truth for all consolidation decisions.

---

## Current Tech Inventory (Categorized)

### CRM / Sales / Outreach
| Tool | Function | Notes |
|------|----------|-------|
| Active Campaign | Email marketing / CRM | Overlap with SendGrid, GMass |
| EZ Texting | SMS outreach | Overlap with potential GHL SMS |
| slydial | Voicemail drops | Niche — evaluate usage |
| GMass | Bulk email via Gmail | Redundant if CRM handles email |
| Five9 | Contact center / dialer | Core sales infrastructure — evaluate |
| Crisp | Live chat / messaging | Evaluate volume and necessity |
| Quo | Sales engagement | Evaluate overlap with CRM |

### Marketing / Content / SEO
| Tool | Function | Notes |
|------|----------|-------|
| Canva | Design | Keep — low cost, high utility |
| Riverside | Podcast/video recording | Keep if podcast continues |
| Testimonial.to | Video testimonials | Evaluate ROI |
| UberSuggest | SEO research | Redundant if consolidating SEO |
| Unbounce | Landing pages | Redundant with GHL or WordPress |
| SEO articles | Content/SEO service | Clarify — vendor or internal? |
| Liberated Syndication | Podcast hosting | Keep if podcast continues |
| YouTube Premium | Video | Likely personal — evaluate |
| BrightFire | Insurance marketing | Appears duplicated in list — confirm one subscription |

### Website / Web Infrastructure
| Tool | Function | Notes |
|------|----------|-------|
| WordPress (main) | Primary website | Core — keep or migrate |
| WP Engine | WordPress hosting | Core if WordPress stays |
| Staging environment TBI | Dev/staging | Keep with WordPress |
| Squarespace | Secondary site? | Redundant with WordPress — consolidate |
| Elementor | WordPress page builder | Keep if WordPress stays |
| Gravity Forms | WordPress forms | Redundant with Fluent Forms |
| Fluent Forms | WordPress forms | Pick one — eliminate the other |
| Forgravity | Gravity Forms add-ons | Eliminate if Gravity Forms goes |
| Imagify | Image optimization | Low cost — keep with WordPress |
| Gravatar | Profile avatars | Free — negligible |

### Data / Automation / Backend
| Tool | Function | Notes |
|------|----------|-------|
| Airtable (Admin) | Database / ops | Redundant with CRM if consolidated |
| Airtable | General use | Same platform — consolidate bases |
| Airtable OTP | Unknown use case | Investigate |
| Zapier | Automation / integrations | Core glue — evaluate in both proposals |
| SendGrid (Twilio) | Transactional email | May be needed for programmatic email |
| Amazon Web Services | Cloud infrastructure | Evaluate what runs here |
| Couchdrop | File transfer / SFTP | Evaluate necessity |
| HIPAA Vault | HIPAA-compliant hosting/storage | **Critical for compliance — keep** |
| Streamlit | Data apps / dashboards | Evaluate what it powers |
| Basefront | Unknown | Investigate |

### Industry-Specific / Enrollment
| Tool | Function | Notes |
|------|----------|-------|
| Medicare Pro | Enrollment platform | Core business tool |
| Medicare Pro Test Account | Testing environment | Keep with Medicare Pro |
| E123 | Enrollment / quoting | Core business tool |

### Learning / Training
| Tool | Function | Notes |
|------|----------|-------|
| Cloud Academy | Training platform | Redundant with LearnDash? |
| LearnDash | LMS (WordPress-based) | Pick one — eliminate the other |

### Compliance / Finance
| Tool | Function | Notes |
|------|----------|-------|
| Tax Bandits | Tax filing | Seasonal — keep |
| Adobe Pro | PDF / document signing | Evaluate if CRM covers e-sign |
| HIPAA Vault | Compliance hosting | **Non-negotiable — keep** |

### Email / Communication
| Tool | Function | Notes |
|------|----------|-------|
| Marketing inbox | Unknown | Investigate |
| Fathom Analytics | Privacy-focused analytics | Good — keep or evaluate vs. GHL analytics |
| AddEvent | Event scheduling links | Low cost — keep if used |

---

## Proposal A: Custom-Built AI System + CRM

### Philosophy
Build a proprietary AI-powered sales and operations platform tailored to the insurance brokerage model. Maximum control, maximum differentiation, higher build cost.

### Architecture

```
┌─────────────────────────────────────────────────┐
│              CUSTOM CRM (Core Platform)          │
│                                                  │
│  Contact Management · Pipeline · Policy Tracking │
│  HIPAA-Compliant Data Layer (HIPAA Vault / AWS)  │
└──────────────┬───────────────┬──────────────────┘
               │               │
       ┌───────▼──────┐ ┌─────▼────────┐
       │  AI SDR/BDR  │ │  AI Admin    │
       │  Agents      │ │  Agents      │
       │              │ │              │
       │ - Lead qual  │ │ - Data entry │
       │ - Outreach   │ │ - Scheduling │
       │ - Follow-up  │ │ - Reporting  │
       │ - SMS/Email  │ │ - Compliance │
       │ - Voicemail  │ │   checks     │
       └──────────────┘ └──────────────┘
```

### What Gets Built
1. **Custom CRM** — Contact management, pipeline, policy lifecycle tracking, HIPAA-compliant storage
2. **AI SDR Agent** — Handles lead qualification, initial outreach (email, SMS, voicemail drop), follow-up sequences, meeting booking
3. **AI BDR Agent** — Manages outbound prospecting, list building, personalized outreach at scale
4. **AI Admin Agent** — Data entry automation, appointment scheduling, compliance document tracking, reporting
5. **Integration layer** — Connects to Medicare Pro, E123, and other industry platforms via APIs

### What Gets Eliminated
- Active Campaign (replaced by CRM + AI agents)
- EZ Texting (replaced by CRM SMS)
- slydial (replaced by AI voicemail capability)
- GMass (replaced by CRM email)
- Crisp (replaced by CRM chat)
- Quo (replaced by AI SDR)
- Airtable (all instances — replaced by CRM database)
- Zapier (replaced by custom integration layer)
- Unbounce (replaced by CRM landing pages)
- Five9 (evaluate — may be replaced by AI dialer or retained for complex calls)
- Squarespace (consolidate to WordPress or CRM pages)

### What Stays
- WordPress + WP Engine + Elementor (website)
- HIPAA Vault (compliance)
- Medicare Pro + E123 (industry tools)
- SendGrid (transactional email backend)
- AWS (infrastructure for custom platform)
- Canva, Riverside, Libsyn (content creation)
- Tax Bandits (finance)
- One LMS (LearnDash or Cloud Academy — pick one)
- Fathom Analytics (privacy-compliant analytics)

### Pros
- Full control over feature set and data
- AI agents can be tuned specifically to insurance sales workflows
- Competitive differentiator — proprietary system
- No per-seat SaaS fees at scale

### Cons
- Significant upfront build investment
- Requires ongoing engineering resources to maintain
- Longer time to full deployment
- CRM is a solved problem — building from scratch carries risk

### Build Phases
1. Process mapping and requirements (Phase 0)
2. CRM core: contacts, pipeline, HIPAA-compliant data layer
3. AI SDR agent: email + SMS outreach sequences
4. AI BDR agent: prospecting and list building
5. AI Admin agent: scheduling, data entry, compliance
6. Integration with Medicare Pro, E123, and remaining tools
7. Migration from legacy tools, department-by-department

---

## Proposal B: GoHighLevel + Automation (Streamlined)

### Philosophy
Use GoHighLevel (GHL) as the all-in-one platform. Strip out redundant tools. Layer basic automation on top. Fastest path to consolidation with lowest ongoing complexity.

### Architecture

```
┌─────────────────────────────────────────────────┐
│            GoHighLevel (All-in-One)              │
│                                                  │
│  CRM · Email · SMS · Landing Pages · Forms ·     │
│  Pipeline · Calendar · Chat Widget · Reporting   │
└──────────────┬──────────────────────────────────┘
               │
       ┌───────▼──────────────┐
       │  Zapier / GHL        │
       │  Workflows           │
       │                      │
       │ - Lead routing       │
       │ - Follow-up triggers │
       │ - Enrollment alerts  │
       │ - Reporting sync     │
       └─────────────────────┘
```

### What GHL Replaces
| Eliminated Tool | GHL Feature |
|----------------|-------------|
| Active Campaign | Email marketing + automation |
| EZ Texting | Built-in SMS |
| slydial | Voicemail drop feature |
| GMass | Email campaigns |
| Crisp | Chat widget |
| Quo | Pipeline + sequences |
| Unbounce | Landing page builder |
| Gravity Forms / Fluent Forms | Built-in forms |
| Airtable (all) | Built-in database / custom fields |
| Five9 | Built-in dialer (evaluate capability) |
| Squarespace | Funnel / site builder |

### What Stays
- WordPress + WP Engine + Elementor (main website — GHL funnels supplement, not replace)
- HIPAA Vault (compliance — **verify GHL HIPAA compliance for your use case**)
- Medicare Pro + E123 (industry tools)
- SendGrid (may still be needed for transactional email volume)
- AWS (if anything critical runs there)
- Canva, Riverside, Libsyn (content creation)
- Tax Bandits (finance)
- One LMS (LearnDash or Cloud Academy)
- Zapier (reduced — GHL handles most automations natively)
- Fathom Analytics (supplement GHL reporting)

### Pros
- Fast deployment — GHL is ready out of the box
- Dramatically reduces tool count and cost
- Single platform for sales, marketing, and communication
- Built-in automation reduces Zapier dependency
- Lower ongoing maintenance — no custom engineering required

### Cons
- Less customizable than a custom build
- Vendor lock-in to GHL platform
- GHL HIPAA compliance must be independently verified for insurance use
- May not handle all insurance-specific workflows natively
- Per-seat/sub-account costs at scale

### Rollout Phases
1. Process mapping and requirements (Phase 0)
2. GHL account setup, HIPAA compliance verification
3. CRM migration: contacts, pipelines, tags from Active Campaign + Airtable
4. Communication migration: email, SMS, chat into GHL
5. Landing page and form migration
6. Automation buildout in GHL workflows (replace Zapier where possible)
7. Legacy tool decommissioning, department-by-department
8. Training and change management across all verticals

---

## Recommendation

Start with **Phase 0** regardless of which proposal is selected. The process mapping will:
- Reveal which tools are truly redundant vs. serving unique needs
- Surface compliance requirements that constrain platform choices
- Give every department a voice before changes happen (critical for change management)
- Produce the requirements document needed to evaluate both proposals fairly

### Decision Framework

| Factor | Proposal A (Custom AI) | Proposal B (GHL) |
|--------|----------------------|-------------------|
| Speed to value | Slower | Faster |
| Upfront cost | Higher | Lower |
| Long-term cost at scale | Potentially lower | Predictable SaaS fees |
| Customization | Unlimited | Platform-constrained |
| Maintenance burden | High (need engineering) | Low (vendor-managed) |
| Competitive advantage | High | Moderate |
| Risk | Higher (building unproven) | Lower (proven platform) |
| HIPAA compliance | You control it | Must verify with GHL |
| Change management lift | Higher | Lower |

### Hybrid Option
Consider a phased approach: deploy GHL now (Proposal B) to stop the bleeding on redundant tools, then build custom AI agents (elements of Proposal A) that integrate with GHL over time. This gives immediate consolidation wins while pursuing the strategic AI vision.

---

## Next Steps

1. Complete Phase 0 process discovery
2. Audit every tool for active usage, contract terms, and renewal dates
3. Verify HIPAA compliance requirements for any platform under consideration
4. Present both proposals with cost projections
5. Select approach and begin department-by-department rollout with change management plan

---

## Change Management Notes

Given the number of departments and verticals:
- Assign a change champion per department
- Communicate the "why" before the "what"
- Run parallel systems during transition — no cold cutover
- Build feedback loops into every phase
- Document everything the previous tech lead did not
