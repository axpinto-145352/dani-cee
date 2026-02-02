# Tech Stack Consolidation
## The Brokerage Inc. — Presented by VV

---

# What This Presentation Covers

We looked at every tool your company uses — all 46 of them.

This deck explains:
- What's broken and what it's costing you
- How we fix it (two options)
- What it costs and what you save
- How we keep patient data safe
- The timeline and what happens each month
- How to get started

---

# The Problem in One Sentence

Your company pays for 46 different software tools, many of them do the same thing, and nobody knows which ones are actually needed.

---

# How Did We Get Here?

- The previous tech lead left without any documentation
- Different departments bought their own tools independently
- Nobody has a complete picture of what's active, what's redundant, or what's safe
- There's no single place where all your contacts, leads, and deals live
- Some of these tools may not meet healthcare privacy requirements

**This isn't unusual — but it needs to be fixed before it gets more expensive.**

---

# What "46 Tools" Actually Looks Like

Your teams use tools across every part of the business:

| Area | How Many Tools | What They Do |
|------|---------------|-------------|
| Sales & Outreach | 7 tools | CRM, email campaigns, texting, calls |
| Marketing & Content | 9 tools | SEO, social media, content creation |
| Websites | 10 tools | Hosting, landing pages, forms, analytics |
| Data & Automation | 10 tools | Databases, integrations, workflow tools |
| Insurance-Specific | 3 tools | Medicare enrollment, carrier platforms |
| Training | 2 tools | Online courses for agents |
| Finance & Compliance | 5 tools | Billing, compliance tracking |

**Total estimated spend: $17,784–$60,996/year** — and that grows as you add people.

---

# The Real Cost Isn't Just the Software

Beyond the subscription fees, you're paying in:

- **Wasted time** — staff switching between tools, re-entering the same data in multiple places
- **Missed leads** — no single view of your pipeline means things fall through the cracks
- **Compliance risk** — patient health data may be sitting in tools that aren't designed to protect it
- **Training overhead** — new hires have to learn a dozen tools instead of one system

**The hidden costs are bigger than the software bills.**

---

# Where the Overlap Is

You're paying for multiple tools that do the same job:

| Job to Be Done | Tools You're Paying For | How Many |
|----------------|------------------------|----------|
| Send emails | Active Campaign, GMass, SendGrid | 3 |
| Send texts | EZ Texting, slydial | 2 |
| Store data | Airtable (3 separate accounts) | 3 |
| Collect form responses | Gravity Forms, Fluent Forms, Forgravity | 3 |
| Host websites | WordPress, Squarespace | 2 |
| Train agents | Cloud Academy, LearnDash | 2 |
| Build landing pages | Unbounce, Elementor | 2 |
| Track analytics | Fathom, BrightFire | 2 |

**At least 11 tools can be cut right away.**

---

# Two Options to Fix This

We're presenting two approaches. Both solve the problem — they differ in how much control you get.

| | **Option A: Custom Build** | **Option B: All-in-One Platform** |
|--|---------------------------|----------------------------------|
| What it is | We build your system using best-in-class pieces | We move everything into GoHighLevel |
| Best for | Maximum flexibility and long-term savings | Speed and simplicity |
| Analogy | Building a custom home | Buying a condo |

**Let's walk through each one.**

---

# Option A: The Custom Build

## The Recommended Approach

We combine three proven platforms into one integrated system:

- **Notion** — Your new CRM and operations hub (think: the command center where your team lives every day)
- **n8n** — The automation engine that connects everything behind the scenes (replaces Zapier and manual data entry)
- **AI Assistants** — Digital workers that handle lead outreach, follow-ups, and admin tasks 24/7

---

# What Notion Replaces

Notion becomes the one place your team goes for everything non-medical:

| Currently Using | Notion Replaces It With |
|----------------|------------------------|
| Active Campaign (CRM features) | Contact database + pipeline view |
| Airtable (3 accounts) | Structured databases with views |
| Scattered Google Docs / wikis | Department wikis and SOPs |
| Manual spreadsheet reports | Auto-updating dashboards |
| Crisp (chat/support) | Intake forms + automated routing |

**One login. One system. Everyone on the same page.**

---

# What the Automation Engine Does

n8n is the "invisible assistant" that runs behind the scenes:

- When a new lead comes in → it automatically gets scored and routed to the right agent
- When an appointment is booked → it sends confirmation texts and calendar invites
- When a form is submitted → the data flows to the right database without anyone typing it in
- When a deal moves to a new stage → the next follow-up sequence starts automatically

**This replaces Zapier (which charges per task) with unlimited automations at no per-use cost.**

---

# What the AI Assistants Do

Think of these as digital employees that handle repetitive work so your people can focus on selling:

**AI Sales Development Rep (SDR)**
- Reaches out to new leads via email and text
- Follows up automatically if someone doesn't respond
- Qualifies leads and books meetings for your human agents

**AI Business Development Rep (BDR)**
- Builds prospecting lists from your target markets
- Sends personalized outreach at scale
- Enriches lead records with relevant data

**AI Admin Assistant**
- Enters data into your systems automatically
- Manages appointment scheduling and reminders
- Tracks compliance documents and flags what's missing

---

# How Much Time This Saves

Here's where your team's hours currently go — and what gets automated:

| Task | Hours/Week Today | Hours/Week After | Time Saved |
|------|-----------------|-----------------|------------|
| Qualifying and scoring leads | 10–15 hrs | 1–2 hrs | **9–13 hrs** |
| Sending outreach emails & texts | 8–12 hrs | 1–2 hrs | **7–10 hrs** |
| Data entry (contacts, pipeline) | 10–15 hrs | 2–3 hrs | **8–12 hrs** |
| Scheduling appointments | 5–8 hrs | 0.5–1 hr | **4.5–7 hrs** |
| Building reports | 5–8 hrs | 1–2 hrs | **4–6 hrs** |
| Switching between tools | 5–10 hrs | 0.5–1 hr | **4.5–9 hrs** |
| Compliance tracking | 3–5 hrs | 0.5–1 hr | **2.5–4 hrs** |
| Voicemail drops & call logging | 3–5 hrs | 0.5 hr | **2.5–4.5 hrs** |
| **TOTAL** | **49–78 hrs/wk** | **7–12.5 hrs/wk** | **42–65.5 hrs/wk** |

**That's 1 to 1.6 full-time employees' worth of time — returned to revenue-generating work every single week.**

---

# The Healthcare Privacy Question

As a Medicare brokerage, you handle protected health information (PHI) — things like Medicare IDs, policy numbers, and enrollment data.

**Federal law (HIPAA) requires this data to be stored and processed in specific, secure ways.**

This is the single biggest consideration in choosing your tech stack.

Here's how we handle it →

---

# How We Keep Patient Data Safe

We use a "split" design — think of it like having two filing cabinets:

**Filing Cabinet #1 — Notion (Day-to-Day Work)**
- Contact names, phone numbers, email addresses
- Deal stages, task lists, meeting notes
- Department wikis and training materials
- **No patient health data ever goes here**

**Filing Cabinet #2 — AWS Secure Environment (Patient Data Only)**
- Medicare IDs, policy numbers, enrollment records
- Signed documents and health-related forms
- All data encrypted and access-controlled
- Covered by a free federal compliance agreement (BAA)

**The automation engine (n8n) is the only bridge between the two — and it strips out any sensitive data before updating Notion.**

---

# What About the AI? Is That Safe?

Great question. All AI processing runs through **AWS Bedrock** — Amazon's enterprise AI service.

Why this matters:

| Concern | How It's Addressed |
|---------|-------------------|
| Does patient data leave our systems? | **No.** All AI processing happens inside your secure AWS environment. |
| Do we need a separate privacy agreement with the AI company? | **No.** It's covered by your existing AWS agreement. |
| Can the AI "learn" from our patient data? | **No.** AWS Bedrock does not use your data to train models. |
| What AI models are available? | Claude (Anthropic), Amazon Titan, and others — you're not locked into one. |

**Bottom line: the AI never sees data outside your secure environment.**

---

# 11 Safeguards to Prevent Data Leaks

We don't just separate the data — we build a system of checks:

**Automated Protections (Always Running)**
1. Database fields in Notion are locked — only admins can change the structure
2. Automation workflows automatically strip patient data before updating Notion
3. An AI scanner checks Notion every night for any patient data that shouldn't be there
4. Only the automation engine can write data to Notion (no manual copy-paste gaps)
5. The patient data environment is in a private network — not accessible from the internet

**Team Rules & Training**
6. Simple color-coded guide: GREEN data goes to Notion, RED data stays in AWS
7. Every employee gets privacy training at onboarding and annually
8. Written plan for what to do if patient data ends up in the wrong place

**Organizational Accountability**
9. A designated compliance officer owns the data boundary
10. Quarterly audits to verify the separation is holding
11. Notion workspace is branded "PHI-Free Zone" so nobody forgets

---

# What Gets Cut (11 Tools)

| Tool Being Removed | What Replaces It | Monthly Savings |
|-------------------|-----------------|----------------|
| Active Campaign | Notion + automations + SendGrid | $150–$500 |
| EZ Texting | Automated texting via Twilio | $50–$200 |
| slydial | AI voicemail via automation | $30–$100 |
| GMass | Automated bulk email | $20–$50 |
| Crisp | Notion intake + routing | $25–$95 |
| Quo | AI sales assistant | $50–$150 |
| Airtable (×3 accounts) | Notion databases | $60–$135 |
| Zapier | n8n (free, unlimited) | $20–$100 |
| Unbounce | WordPress + Elementor | $90–$225 |
| Squarespace | WordPress (consolidate to one site platform) | $16–$49 |

**Total tool savings: $7,932–$22,848/year**

---

# Option A: What It Costs to Build

## One-Time Investment

| What You're Paying For | Cost Range |
|-----------------------|-----------|
| Setting up Notion as your CRM | $3,000–$8,000 |
| Building the AI Sales Rep | $8,000–$20,000 |
| Building the AI Business Dev Rep | $5,000–$15,000 |
| Building the AI Admin Assistant | $5,000–$15,000 |
| Connecting everything (automation workflows) | $5,000–$15,000 |
| Patient data protection system | $2,500–$6,000 |
| Secure AWS environment setup | $1,500–$4,000 |
| Moving your data + training your team | $3,000–$8,000 |
| **TOTAL ONE-TIME** | **$33,000–$91,000** |

*The range depends on complexity discovered during Phase 0 and how many custom workflows are needed.*

---

# Option A: What It Costs Monthly

## Ongoing After Build is Complete

| Item | Small Team (10 people) | Larger Team (25 people) |
|------|----------------------|------------------------|
| Notion Business plan | $200/mo | $600/mo |
| Automation engine hosting (AWS) | $30/mo | $80/mo |
| Secure patient data environment | $131/mo | $360/mo |
| AI processing costs | $55/mo | $350/mo |
| Maintenance & updates | $0–$500/mo | $0–$500/mo |
| Tools you keep (SendGrid, Twilio, etc.) | $354/mo | $1,624/mo |
| **TOTAL MONTHLY** | **$770–$1,560** | **$1,414–$3,514** |
| **TOTAL ANNUAL** | **$9,240–$18,720** | **$16,968–$42,168** |

**Compare to current spend: $17,784–$60,996/year**

---

# Return on Investment

## When Does Option A Pay for Itself?

| | Conservative | Optimistic |
|--|-------------|-----------|
| Value of time saved per year | $50,232 | $78,338 |
| Tool cost savings per year | $7,932 | $22,848 |
| **Total annual value** | **$58,164** | **$101,186** |
| Year 1 total cost (build + consulting + monthly) | $55,240 | $55,240 |
| **Year 1 net return** | **+$2,924 (5%)** | **+$45,946 (83%)** |
| Year 2 cost (monthly + retainer only) | $27,240 | $27,240 |
| **Year 2 net return** | **+$30,924 (114%)** | **+$73,946 (271%)** |

**Payback period: 7–12 months**

*This does not include the revenue upside from your agents spending more time actually selling — which is the real multiplier.*

---

# Option B: The All-in-One Platform

## GoHighLevel — For Comparison

Instead of building custom, you move everything into one vendor platform:

| | Detail |
|--|--------|
| **What it is** | GoHighLevel — an all-in-one CRM and marketing platform |
| **One-time setup cost** | $7,000–$20,000 |
| **Monthly cost** | $1,018–$2,765 (includes $297/mo HIPAA add-on) |
| **Annual cost** | $12,216–$33,180 |
| **Timeline** | ~3.5 months |
| **AI features** | Basic — $97/mo add-on per account |
| **Customization** | Limited to what the platform offers |
| **Switching later** | Difficult — high vendor lock-in |

**GoHighLevel is simpler and faster to deploy, but you're renting — not owning.**

---

# Side-by-Side: Option A vs Option B

| | **Option A (Custom Build)** | **Option B (GoHighLevel)** |
|--|---------------------------|--------------------------|
| **Upfront cost** | $33K–$91K | $7K–$20K |
| **Monthly cost (10 people)** | $770–$1,560 | $1,018–$1,870 |
| **Annual cost (10 people)** | $9,240–$18,720 | $12,216–$22,440 |
| **HIPAA compliance cost** | $0 (included in AWS) | $297/mo ($3,564/yr) |
| **AI capabilities** | Full custom AI assistants | Basic platform AI |
| **Hours saved/week** | 42–65.5 hrs | ~21–33 hrs |
| **Customization** | Unlimited | Platform-limited |
| **Vendor lock-in** | Low (you own it) | High (you're renting) |
| **Payback period** | 7–12 months | ~6 months |
| **Best for** | Long-term competitive advantage | Quick wins, simpler needs |

---

# Three-Year Cost Comparison

## What Each Path Costs Over Time

| | Year 1 | Year 2 | Year 3 | **3-Year Total** |
|--|--------|--------|--------|-----------------|
| **Do nothing** (current state) | $18K–$61K | $18K–$61K | $18K–$61K | **$53K–$183K** |
| **Option A** (10 seats + VV engagement) | $55K–$123K | $27K–$37K | $27K–$37K | **$109K–$197K** |
| **Option A value created** | $58K–$101K | $58K–$101K | $58K–$101K | **$174K–$303K** |
| **Option A net gain (3-year)** | | | | **+$65K–$106K** |
| **Option B** | $19K–$42K | $12K–$22K | $12K–$22K | **$43K–$86K** |
| **Option B value created** | $36K–$61K | $36K–$61K | $36K–$61K | **$108K–$183K** |
| **Option B net gain (3-year)** | | | | **+$65K–$97K** |

**Option A costs more upfront but creates more value. By Year 3, both options are net positive — but Option A pulls ahead on capabilities and savings.**

---

# What Could Go Wrong (And How We Prevent It)

## Compliance Risks

| What Could Happen | How Likely | How Bad | How We Prevent It |
|-------------------|-----------|---------|------------------|
| Patient data accidentally gets into Notion | Medium | Very Bad | 11-layer protection system (automated scanners, locked fields, training, audits) |
| Current tools already have a compliance gap | Medium | Very Bad | We check this in the very first week — before building anything |
| Secure environment set up incorrectly | Low | Very Bad | We use pre-built security templates, review at every milestone, and log everything |

---

# What Could Go Wrong (Continued)

## Operational Risks

| What Could Happen | How Likely | How Bad | How We Prevent It |
|-------------------|-----------|---------|------------------|
| Staff resist the change | High | Medium | We assign change champions per department, roll out gradually, and show quick wins early |
| Automation system goes down | Low | High | Automatic recovery, monitoring alerts, restart procedures documented |
| Notion slows down with lots of data | Medium | Medium | We archive old records quarterly and structure databases to stay fast |
| Current phone system (Five9) is hard to replace | Medium | Medium | We evaluate this during discovery — we may keep Five9 if the replacement isn't ready |

---

# What Could Go Wrong (Continued)

## Project & Strategic Risks

| What Could Happen | How Likely | How Bad | How We Prevent It |
|-------------------|-----------|---------|------------------|
| Project scope grows beyond budget | Medium | Medium | Fixed milestones with approval gates — scope is locked after Month 1 |
| Too dependent on VV | Medium | Medium | Full documentation and training at handoff. Everything is yours. |
| Data gets lost during migration | Low | High | We back everything up, run systems in parallel, and validate before cutting over |
| AI pricing goes up | Low | Medium | We're not locked into one AI provider — the system can switch models |
| Notion changes their pricing | Low | Medium | Your data is exportable. Low lock-in by design. |
| Regulations change | Low | High | The split architecture is built to be conservative — easier to adapt than a single-vendor system |

**Every risk has a mitigation. And the go/no-go gates at Milestones 1 and 2 mean you're never over-committed.**

---

# The VV Engagement

## What You Pay Us

| | Detail |
|--|--------|
| **Base fee** | $10,000 |
| **Duration** | 4 months |
| **Months 1–2** | Covered by the base fee (discovery + build kickoff) |
| **Month 3 retainer** | $1,500 |
| **Month 4 retainer** | $1,500 |
| **Total engagement** | **$13,000** |

## What's Included

- Full discovery of every process and tool across all departments
- Classification of all data (what's sensitive, what's not)
- Complete Notion CRM build and configuration
- Automation setup and workflow building
- Secure AWS environment for patient data
- AI assistant design, building, and testing
- Data migration from old tools
- Training for every department
- Full handoff documentation

**After the engagement:** Retainer continues at $1,500/mo for optimization and support — cancelable with 30 days notice.

---

# The 4-Month Roadmap

## Month 1 → Discovery & Planning

**What happens:**
- We map every department's workflows
- We classify all data (sensitive vs. non-sensitive)
- We audit every tool (who uses it, what it costs, when the contract renews)
- We deliver the architecture plan

**What you get:** A complete picture of your current state and an approved plan to move forward

**Decision point: Go or no-go.** You've spent $10K. If you don't like the plan, you stop here with a full process map in hand.

---

# The 4-Month Roadmap

## Month 2 → Build the Foundation (MVP)

**What happens:**
- Notion CRM goes live with your contacts, pipeline, and dashboards
- Automation engine is running on AWS
- Secure patient data environment is configured
- Core automations are active (lead routing, notifications, data syncing)
- Patient data safeguards are in place
- **First AI assistant (Sales Rep) is in prototype**

**What you get:** A working system your team can start using for daily operations

**Decision point: Go or no-go.** If the MVP is working, you approve continued build. Retainer ($1,500/mo) begins.

---

# The 4-Month Roadmap

## Month 3 → Expand the AI

**What happens:**
- AI Sales Rep goes live in production
- AI Business Dev Rep built and in testing
- AI Admin Assistant built and in testing
- Nightly data scanner is active (checking for patient data leaks)
- Insurance platform integrations go live
- First department migrated off old tools

**What you get:** Full AI assistant suite in testing; legacy tools starting to shut down

---

# The 4-Month Roadmap

## Month 4 → Full Rollout & Handoff

**What happens:**
- All AI assistants live in production
- All departments migrated and trained
- Old tools fully decommissioned
- Quarterly audit process established
- Complete handoff documentation delivered

**What you get:** A fully operational system that you own. VV transitions to optional retainer support.

---

# The Hybrid Option

**You don't have to choose one path forever.**

A phased approach:

1. **Months 1–4:** Build Option A (Notion + AI) with VV
2. **If you need something working immediately:** Deploy GoHighLevel in parallel for basic CRM consolidation
3. **Months 5–8:** Stabilize the custom build; evaluate if GoHighLevel adds value or is redundant
4. **Year 2:** Full AI optimization; GoHighLevel either stays as a supplement or gets cut

**This gives you the speed of Option B with the long-term upside of Option A.**

---

# Our Recommendation

**Start with Phase 0 — no matter which direction you choose.**

The discovery phase will:
- Show you exactly which tools are needed and which aren't
- Uncover any existing compliance gaps (before they become a problem)
- Give every department input before changes happen
- Replace estimates with real numbers

**You can't make a confident decision without this information. Phase 0 gives it to you.**

---

# What Happens Next

1. **This week** → Approve the engagement and schedule kickoff
2. **Immediately** → We check your current tools for compliance gaps
3. **Weeks 1–3** → Full discovery across every department
4. **End of Week 3** → Milestone 1 review — you decide if we proceed
5. **Weeks 4–8** → Build the MVP (Notion CRM + automations + first AI assistant)
6. **End of Week 8** → Milestone 2 review — you decide if we expand
7. **Weeks 9–18** → Full AI rollout, migration, training, and stabilization

**Every major decision point requires your approval. You're never locked in past the next milestone.**

---

# Thank You

## VV — The Brokerage Inc. Tech Stack Consolidation

**Total engagement: $13,000 over 4 months**
**Projected annual value: $58,000–$101,000**
**Payback period: 7–12 months**

Ready to get started? Let's schedule Phase 0.
