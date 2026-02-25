# Outbound Email Guideline Sheet

**Author:** Jaron Sander, Inform Growth
**Purpose:** Founder-led reference for filtering targets, selecting messaging angles, and running value-first outbound that starts conversations.
**Tool-agnostic** — works with Apollo, Instantly, Smartlead, or manual sends.

---

## 0. Outbound Philosophy

**Selling is helping.**

If someone has a problem I can solve, telling them about my offer IS the valuable thing. A $1,500 diagnostic that surfaces $100K in hidden pipeline with a money-back guarantee — that's not a pitch, that's a gift. Withholding it isn't "being respectful," it's leaving them stuck.

The goal of every touch is to:
1. **Demonstrate pattern recognition** — show them you understand their stage-specific pain
2. **Deliver genuine value** — an insight, a number, an offer that helps them
3. **Gauge interest** — find out if the pain is real and what kind of help they actually need

The offer belongs in the sequence. It's not something I "earn the right" to mention — it's the most valuable thing I can put in front of them. If the diagnostic isn't the right fit, I want to understand what is. The goal is to help, and the conversation is how I figure out the best way to do that.

---

## 1. Target Filtering (Who Gets an Email)

### Company Filters

| Filter | Criteria | Why |
|--------|----------|-----|
| **Stage** | Series B, C, or growth-stage | Complex enough to have real data debt |
| **Revenue** | $5M+ ARR | Budget exists, ROI is provable |
| **Headcount** | 50-300 employees | Scaling pain without a massive internal ops team |
| **Growth** | 40-100%+ YoY | Fast growth = fast data degradation |
| **Revenue Model** | B2B SaaS, Platform + Services hybrid, or tech-enabled service with subscription component | Multi-stage funnels with high leakage risk |
| **Contract Value** | $25K-500K+ ACV | Deal sizes where 1 lost deal/month = $120-300K/year |
| **Tech Stack** | Salesforce, HubSpot, or Attio + 5-10 other GTM tools (Outreach, Salesloft, Gong, 6sense, ZoomInfo, etc.) | Integration sprawl = sync failures = silent leakage |

### Buying Signal Filters (Prioritize companies showing these)

| Signal | Where to Find It | What It Means |
|--------|-------------------|---------------|
| **Hiring RevOps / CRM Admin / Sales Ops** | LinkedIn Jobs, Indeed, company careers page | They know their data is broken — the "Trojan Horse" trigger |
| **Recently raised Series B/C** | Crunchbase, LinkedIn announcements | Budget and scaling pressure simultaneously |
| **Using expensive-tier tools** | Job postings mention Salesforce Enterprise, HubSpot Enterprise, Clari, 6sense | Spending big on tools that depend on clean data they probably don't have |
| **High headcount in data-entry or "Sales Ops" roles** | LinkedIn org chart | Manual cleanup = infrastructure hasn't been engineered |
| **Recent CRM migration or consolidation** | Job postings, press releases, LinkedIn posts from ops team | Migrations always leave data debt behind |
| **Rapid rep hiring** | LinkedIn hiring activity | New reps = new data corruption vectors |

### Job Posting Keywords (Trojan Horse Triggers)

Search LinkedIn Jobs and Indeed for these in the JD body:

- "Clean up" / "Data cleanup"
- "Migration" / "CRM migration" / "Implementation"
- "Data hygiene" / "Data quality"
- "Messy CRM" / "Technical debt"
- "Salesforce admin" / "HubSpot admin"
- "RevOps manager" / "Revenue operations"
- "Lifecycle stages" / "Lead routing"

### Person Filters

| Filter | Criteria | Notes |
|--------|----------|-------|
| **Titles (Primary)** | CRO, VP RevOps, VP Revenue Operations, Head of RevOps, RevOps Manager | Own the infrastructure and feel the pain daily |
| **Titles (Secondary)** | VP Sales, VP Sales Ops, Head of GTM, Director of Operations | Feel the downstream effects — slow routing, bad reports, lost deals |
| **Titles (Executive)** | CEO, COO, CFO | Only at 50-150 employee companies where execs still feel ops pain directly |
| **Seniority** | Director+ at 100-300 employees; Manager+ at 50-100 employees | Smaller company = lower title still has decision authority |

### Anti-Targets (Skip These)

| Signal | Why |
|--------|-----|
| <$5M ARR or <50 employees | Too early for the complexity we solve |
| No CRM or basic tools only (spreadsheets, Notion-as-CRM) | No plumbing to fix |
| "Strategy consultant" signals | We build, we don't advise-and-leave |
| Custom app development requests | Infrastructure engineers, not a dev shop |
| E-commerce, local business, traditional manufacturing | Wrong model — no multi-stage B2B funnels |

---

## 2. Messaging Points by Persona

### The North Star: RevOps Observability

Every messaging angle should ladder up to this:

> We work with clients to put systems in place so you catch mistakes and errors **while they happen** in your revenue operations system — not weeks or quarters later when the damage is done.

This is the long-term value prop. The Reactivation Diagnostic is the door-opener. Observability is the destination.

### CRO / VP RevOps (Primary Buyer)

**Their world:** They own pipeline accuracy, forecasting, and cross-functional data flow. Accountable when numbers don't add up.

| Messaging Angle | Example Line |
|----------------|--------------|
| **Silent leakage** | "Most ops teams don't catch it because the leads aren't 'lost' — they're sitting in the CRM, they just never hit a queue." |
| **Dashboard distrust** | "If your lifecycle stages are misconfigured, every forecast is a confident-looking lie." |
| **Post-cleanup decay** | "Cleanups are temporary. Entropy is permanent. The question is whether you catch the decay in 24 hours or 6 months." |
| **Integration sprawl** | "Your leakage is in the 14 integrations between Salesforce and everything else." |
| **Observability gap** | "Who's watching the pipes between your systems right now? If a sync fails tonight, when does someone notice?" |
| **AI readiness** | "You can't deploy AI tools on a data foundation full of cracks. AI just automates the problems faster." |

### VP Sales / Head of GTM (Feels the Symptoms)

**Their world:** Reps complaining about lead quality, slow routing, ghost leads. Pipeline looks thin but they can't pinpoint why.

| Messaging Angle | Example Line |
|----------------|--------------|
| **Speed-to-lead** | "If your routing drops 15% of inbound, your reps never see those conversations because they never happened." |
| **Ghost leads** | "Leads aren't disappearing — they're stuck in lifecycle limbo. Dead zones your reporting can't see." |
| **New rep onboarding** | "Every new rep you hire is multiplying the errors in your system." |
| **Rep time waste** | "Sales reps wasting 20% of time on admin/cleanup instead of selling." |
| **Cost of 1 lost deal** | "1 lost deal per month due to bad routing = $120-300K/year in missed revenue." |

### CEO / COO / CFO (50-150 Employee Companies)

**Their world:** Scaling fast, scared systems will break, need to look buttoned-up for board/investors.

| Messaging Angle | Example Line |
|----------------|--------------|
| **Fundraise/exit readiness** | "Investors are going to look at your data room. What they'll see is 7 systems that don't agree on revenue numbers." |
| **Specialist vs. hire** | "A RevOps manager costs $120k/year. They'll spend their first quarter drowning in cleanup. Let me hand them a clean stack." |
| **Blocked AI deployment** | "You cannot deploy AI tools on dirty data. Garbage in, garbage out — at AI speed." |
| **Compounding data debt** | "What costs $5k to fix today will cost $25k in Q2 because every new hire multiplies the errors." |
| **Hard cost savings** | "I consolidated 7 CRMs into 1 and cut tooling costs 75%. How many redundant subscriptions are you carrying?" |

---

## 3. Brand Messaging Rules

### Identity in One Line

> "Your RevOps Funnel Plumbers. We refactor your revenue stack with engineering-grade plumbing to recover lost pipeline and ensure scale."

### What We're Really Building Toward

**RevOps Observability** — putting monitoring and alerting systems in place so your revenue infrastructure catches its own errors in real-time. Not one-time fixes. Continuous awareness.

### The Entry Point: Reactivation Diagnostic

| Detail | Value |
|--------|-------|
| **What** | Forensic scan of CRM + CS data to surface hidden pipeline buried in sales and customer success systems |
| **Promise** | Find $100K+ in recoverable pipeline, or your money back |
| **Price** | $1,500 |
| **ROI** | 66x return ($100K found on a $1,500 investment) |
| **Timeline** | 1-2 weeks |
| **Why it works** | Risk-reversed, absurdly high ROI, immediate tangible output |

> **Pricing note:** Considering $1,000 price point for a clean 100x ROI story. Either way, the ratio is the anchor — not the dollar amount.

### The Full Stack (Context for Conversations)

The diagnostic is the entry point. These come up naturally once you're in conversation and understand what they actually need:

- **Stage 2 — Re-Architecture:** Rip out broken infrastructure, install automated routing and clean data models ($12K-$30K project)
- **Stage 3 — Flow Assurance (RevOps Observability):** Ongoing monitoring, telemetry, schema protection, anomaly alerts ($3K-$5K/mo retainer)

Outbound leads with the diagnostic because it's the most concrete, risk-free offer. But if the conversation reveals they need something different, follow the help — don't force the funnel.

### Language Rules

**Use these words:**
Refactor, Latency, Throughput, Telemetry, Leakage, Schema, Orphaned Leads, Zombie Leads, AI-Ready Data, Revenue Trenches, Stop the Leak, Funnel Plumbing, RevOps Infrastructure, Data Debt, Entropy, Observability, Forensic, Diagnostic.

**Never use these words:**
Synergy, Holistic, Ideate, Paradigm, Best-in-class, Leverage (as a verb), Game-changer, Disruptive, "Reaching out," "Hope this finds you well," "I'd love to."

### Email Tone & Format

- **Conversational, lowercase subject lines, plain text only**
- 4 sentences max (50-90 words per email)
- No self-introductions ("I'm a Computer Engineer who...")
- No internal jargon dumped on the prospect ("reactivation scan," "orphaned leads")
- No dashes breaking up sentences
- CTA is casual ("Worth a quick look?" not "Open to a 15-minute strategic call?")
- **Every email should give them something** — an insight, a pattern, a number, or the offer itself. The diagnostic IS value. Mentioning it is helping, not pitching.

### Spam-Safe Rules

- Plain text only — no HTML, no images, no signature images, no tracking pixels if possible
- Lowercase subject lines
- One link max per email (prefer zero)
- Avoid trigger words: "free," "guarantee" (reword as "you don't pay"), "act now," "limited time," "opportunity," "click here," "schedule"
- Early emails are reply-optimized — but the offer IS value, so don't hide it
- The $1,500 diagnostic with money-back guarantee can appear as early as it's natural — it's not a hard sell, it's the help

---

## 4. Key Metrics & Proof Points

### The Headline Numbers

| Metric | Client | The Hook |
|--------|--------|----------|
| **+32% revenue** | Chief of Staff Network | "Interviewed 50% fewer people, made 32% more money." (intelligent routing logic) |
| **-75% costs** | Sylva | "Consolidated 7 CRMs into 1. Stopped paying for redundant tools." |
| **-40% churn** | Revenue Accelerator | "Gave clients a login to see the work. Trust went up, churn went down." |

### The Diagnostic ROI Story

> "$1,500 diagnostic. $100K+ in recovered pipeline. 66x ROI. If we don't find it, you get your money back."

This IS the value. Don't hide it behind a conversation gate. Putting this offer in front of someone who has the problem is helping them. Use it in the sequence — it's the most concrete, risk-free thing you can say.

### Cost-of-Inaction Numbers (The "Why Now")

| Stat | Context |
|------|---------|
| RevOps spends 20 hrs/month fixing data manually = **$18K/year wasted salary** | The invisible cost nobody budgets for |
| 1 lost deal/month due to bad data = **$120K-$300K/year** | Based on typical B2B ACV at target companies |
| 5% of inbound leads stuck in bad routing = **$150-300K/year in unworked pipeline** | The leads aren't lost — they're sitting in the CRM in dead zones |
| Every new rep hired multiplies data errors | Compounding — not a fixed cost |
| AI deployed on dirty data = "Garbage in, garbage out — at AI speed" | Resonates with every exec evaluating AI tools right now |

### Detailed ROI by Category (For Follow-Up Conversations)

**Revenue Velocity:**
- Chief of Staff Network: 32% revenue increase (auto-accept logic for high-quality leads)
- Women Travel Abroad: 27% ROI improvement (killed low-performing ad partners via better tracking)

**Cost Reduction:**
- Sylva: 75% hosting/tooling costs, 50% operational headcount
- Outbound Agency: 30% reduction in data purchasing (stopped buying the same lead twice)
- Tech Ladies: 70% reduction in manual job posting (ATS integrations)

**Efficiency:**
- Outbound Agency: 50 hours/week saved across 5 Account Managers
- CoS Network: 50% fewer interviews (removed humans from filtering)
- Howdy Sales: 50% reduction in client status meetings (self-service dashboard)
- Revenue Accelerator Support: 2 hours/day per support rep saved (triage automation)

**Retention:**
- Revenue Accelerator: 40% churn reduction (client visibility portal)
- PreSales Collective: 20% churn reduction (automated renewal defense)
- Outbound Agency: 30% churn reduction (better reporting transparency)

### The Engineer's Resume (Credibility Anchor)

- **4M+ contacts** managed across 7 major CRM consolidations
- **400,000+ records** consolidated across 7 CRM systems in a single engagement
- **20-person distributed ops team** managed
- **6+ years** in end-to-end customer journey architecture
- **Platform depth:** HubSpot, Salesforce, Attio + 15 other platforms
- **Stack:** SQL, Python, dbt, BigQuery, Make.com, Zapier, REST APIs

---

## 5. Competitive Counter-Messaging

When a prospect mentions any of these in conversation, reframe — don't attack.

| They Mention | Your Angle |
|-------------|------------|
| **Gong / Clari / People.ai** | "Those tools analyze conversations and forecast deals. They sit on top of CRM data and assume it's accurate. I fix the data underneath so their output is actually trustworthy." |
| **WeFlow / Scratchpad / Rattle** | "Those solve the last inch — making it easier for reps to update Salesforce. Your problems are structural: lifecycle stages, routing logic, integration failures. Different layer." |
| **Openprise / Syncari / LeanData** | "Tools don't diagnose problems. Engineers do. You might end up using one of those, but someone has to figure out what's actually broken first." |
| **RevOps agency (RevPartners, Go Nimbly)** | "Most agencies do project work and hand off. Systems degrade in 6 months. I build observability so it stays fixed." |
| **"AI handles data quality now"** | "AI cleans what reps enter — activity capture, field updates, dedup. It doesn't fix structural problems: broken lifecycle stages, dead routing queues, silent sync failures. AI on broken architecture automates the problems faster." |
| **"Salesforce Einstein / HubSpot Breeze"** | "Einstein works inside Salesforce. Your leakage is in the integrations between systems. Breeze learns patterns from your existing data — if that data is 60% garbage, it's autocomplete for a broken system." |
| **"We'll use Clay / enrichment"** | "Enrichment adds data. It doesn't fix structure. Enrich a contact with 40 data points, but if routing sends them to the wrong rep, that contact still dies in a black hole." |
| **Internal hire** | "You should hire. But let me fix the infrastructure first so they do high-value strategy, not $120k/year janitorial work." |

---

## 6. Sequence Structure Cheat Sheet

### Philosophy Reminder

Selling is helping. Every touch delivers value — an insight, a pattern, a number, or the offer itself. The $1,500 money-back diagnostic is one of the most valuable things you can put in someone's inbox. No touch exists just to "follow up." If they need a different kind of help, the conversation will reveal that.

### Narrative Arc (9 Touches / 17 Days)

| Touch | Day | Channel | Purpose |
|-------|-----|---------|---------|
| 1 | 0 | LinkedIn Profile View | Priming — name in their notifications |
| 2 | 1 | Email 1 | Pattern hook — show you know their stage-specific pain |
| 3 | 3 | LinkedIn Connection | Peer positioning, no pitch |
| 4 | 5 | Email 2 | Cost quantification — put a dollar figure on the bleed |
| 5 | 7 | LinkedIn Engage | Like/comment on their content (genuine, 15+ words) |
| 6 | 9 | Email 3 | Proof point — peer company result, offer to share failure patterns |
| 7 | 11 | LinkedIn DM | Value-add conversation starter, no ask |
| 8 | 14 | Email 4 | The offer — first and only meeting ask |
| 9 | 17 | Email 5 | Breakup — reframe cost of inaction, close the loop |

### Rules

- **Every touch delivers value.** Pattern insight, cost quantification, proof point, or the offer itself.
- **The offer is value.** $1,500 with a money-back guarantee is not a hard sell — it's the most helpful thing you can say. Use it when it's natural.
- **LinkedIn touches are genuine engagement.** Build familiarity through real interaction, not pitch DMs.
- **If they reply at any point:** Drop the sequence, have a real conversation. Understand what they actually need — if the diagnostic isn't the right fit, figure out what is.
- **Multi-thread:** If primary doesn't respond, start a parallel sequence to a second person at the same company after Day 10.
