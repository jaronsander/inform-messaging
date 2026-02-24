# PLAYBOOK: Sales Calls & Closing

**Role:** The Funnel Plumber  
**Goal:** Navigate the sales conversation, handle objections, and close the deal.  
**Use When:** You are on a Zoom call with a prospect.

---

## 1. The Script Framework

### Phase 1: The Diagnosis (Listen & Agitate)
*Ask questions to reveal "Data Debt."*
- "Who is monitoring your data quality right now?"
- "When was the last time you found a lead that had been sitting untouched for weeks?"
- "You're hiring 3 new reps. How are you ensuring they don't corrupt the data your current team uses?"

### Phase 2: The Reframe (The "Funnel Plumber" Pitch)
*Move them from 'Marketing' to 'Engineering'.*
- **them:** "We need better dashboards."
- **You:** "Dashboards are rear-view mirrors. They show you what already broke. You need **telemetry**—alarms that go off *before* the revenue is lost."
- **Them:** "We need a cleanup."
- **You:** "Cleanups are temporary. Entropy is permanent. I don't just clean; I install 'filters' to keep the water clean forever."

### Phase 3: The Offer (The Tiers)
- **Tier 1 (Reactivation):** "Let's start with a reactivation scan. I'll surface $100K in recoverable pipeline from your existing CRM and CS data in 2 weeks or you don't pay."
- **Tier 2 (The Fix):** "Then I'll rip out the bad piping and install automated routing."
- **Tier 3 (Maintenance):** "Then I stay on to watch the gauges so you never have to do this again."

---

## 2. Objection Handling (Battle Cards)

### Pricing & Timing Objections

#### "This sounds expensive."
**Response:** "Leakage is expensive. The reactivation scan usually uncovers 10x my fee in recoverable pipeline in the first week. You aren't paying for 'hours'; you are paying for 'revenue recovery'."

#### "We're not ready yet / Talk in Q2."
**Response:** "Data debt compounds like interest. What costs $5k to fix today will cost $25k in Q2 because your new hires will have multiplied the errors. Let's just run the reactivation scan now so you know what you're sitting on."

#### "A RevOps agency quoted us less."
**Response:** "Most agencies do project work: audit, implement, hand off. The system starts degrading the moment humans start using it again. In 6 months you're back to square one, paying for another cleanup. I don't just fix it—I build observability so degradation gets caught within 24 hours. You're paying for a permanent fix, not a temporary one."

### Internal Resources Objections

#### "Can't we just hire a RevOps manager?"
**Response:** "You should! But do you want them spending $120k/year cleaning up duplicates manually? Let me fix the infrastructure first. Then hire them to do high-value strategy, not janitorial work."

#### "This sounds like what our Salesforce admin does."
**Response:** "Your admin maintains the system. I re-engineer it. There's a difference between changing a filter and re-plumbing the entire house. Your admin handles day-to-day. I'm the specialist you bring in when the foundation needs work—then your admin maintains the new, clean system."

### "We Already Have a Tool" Objections

#### "Why not just use ChatGPT/Claude with HubSpot API?" / "We could build this ourselves."
**Response (Acknowledge + Reframe):** "You're absolutely right — you could build this. Anything can be built relatively quickly now. You could rebuild HubSpot or code your own CRM if you wanted to. But people don't — because the real value isn't the tech, it's the delegation of responsibility and accountability. My engine runs deterministic statistical analysis on your CRM patterns. But the bigger point is: you don't have to think about it. You don't have to own the problem of 'is my CRM healthy?' or 'are we leaving pipeline on the table.' That's what you're buying. The moat isn't the tech. It's being the person you can point to when things go wrong."

**Template (any DIY/build-it-yourself objection):** "You could [alternative]. But [product] means you don't have to own [problem]. We're accountable for [outcome]."

**Critical Don'ts for this objection:**
- Never claim LLMs can't do statistics — they can (code interpreter exists). Argue ownership, not capability.
- Never say "you'd spend 10+ hours building this" — it insults their ability and invites an argument you'll lose.
- Never compete on features when you can compete on business model. Tool vs. tool is a race to the bottom.

#### "We already have a HubSpot Agency."
**Response:** "That's great. They are the 'decorators'—they make the emails look nice. I am the 'plumber'—I make sure the pipes (APIs/Data) actually deliver the water to the right place. You need both, but pretty emails don't matter if the data doesn't arrive."

#### "We already use Gong/Clari."
**Response:** "Those tools are excellent at what they do. But they analyze the output of your revenue system—they don't fix the input. If your lead routing drops 15% of inbound, Gong will never see those conversations because they never happened. If your lifecycle stages are misconfigured, Clari's forecast is a confident-looking lie. I fix the infrastructure those tools depend on."

#### "We use Scratchpad/WeFlow/Rattle for data hygiene."
**Response:** "Those tools make it easier for reps to update Salesforce. That's real value. But they're treating the symptom, not the disease. If your lifecycle stages are wrong, your routing logic is broken, and your schema has 200 fields nobody uses—making it easier to fill in bad fields faster doesn't help. I fix the underlying architecture so the system actually makes sense."

#### "Can't we just buy a data tool like Openprise/Syncari?"
**Response:** "You can. But a tool is only as good as the person configuring it. Openprise doesn't know why your data broke in the first place. It doesn't know which of your 47 custom fields are load-bearing and which are dead weight. I do the forensic diagnosis, then design the fix. You might use one of those tools as part of the solution—but the tool isn't the solution."

### The AI Objection

#### "These platforms have AI that cleans data now. Can't AI handle this?"

*Pick the version that matches the prospect's energy.*

**Short version:** "AI is the best thing that ever happened to my business. Every company that deploys AI on dirty data gets burned, then they call me. AI doesn't know what 'correct' looks like for your business—it just automates whatever's already there. If your plumbing is broken, AI pumps the sewage faster."

**Technical version:** "Their AI captures activity—it logs calls, fills in deal fields from transcripts, deduplicates contacts. That's the last inch of the pipe and it does it well. But your data problems aren't at the last inch. They're structural. Your lifecycle stages don't match your actual sales process. Your routing logic has dead zones. Your integrations silently drop records. Their AI cleans what reps enter. I fix the system that determines where it goes after they enter it."

**Hype Fatigue version:** "I've been hearing 'the tool will fix it' for six years. First it was 'buy Salesforce.' Then 'buy Marketo.' Then 'buy LeanData.' Now it's 'AI will fix it.' Same pitch, new label. Tools don't fix architecture. Engineers fix architecture. AI is an accelerant—if your system is clean, AI makes it incredible. If your system is broken, AI makes it incredibly broken, incredibly fast."

**The Reframe (when they push back further):** "I don't compete with AI. I make your data AI-ready so your AI investments actually pay off. You're about to pour $200K into AI tools that will run on a data foundation full of cracks. I fix the foundation."

#### Specific AI Vendor Counters
- **"Salesforce Einstein handles data quality."** → "Einstein works inside Salesforce. Your leakage is in the 14 integrations between Salesforce and everything else. Einstein can't see your Marketo sync failing."
- **"HubSpot Breeze AI cleans our data."** → "Breeze suggests field values based on patterns in your existing data. If your existing data is 60% garbage, Breeze is learning from garbage. It's autocomplete for a broken system."
- **"Gong's AI handles revenue intelligence."** → "Gong analyzes conversations that happened. It can't tell you about the leads that never made it to a conversation because your routing dropped them. I find those."
- **"Sweep's AI agents manage our Salesforce."** → "Sweep documents and monitors. It doesn't re-architect. When Sweep flags 47 unused fields and 3 conflicting automations, someone still has to decide what to do. That's me."
- **"We'll use Clay/AI enrichment to fix our data."** → "Enrichment adds data. It doesn't fix structure. You can enrich a contact with 40 data points, but if your routing sends them to the wrong rep, that enriched contact still dies in a black hole."

### "Why Now" Reinforcement
*Use any of these when a prospect is on the fence after objection handling.*
- "Every new rep you hire between now and then is multiplying the errors in your system."
- "Manual cleanup costs your RevOps team 20+ hours a month. That's $18K/year in wasted salary."
- "1 lost deal per month due to bad data = $120-300K/year."
- "You cannot deploy AI tools on dirty data. Garbage in, garbage out—at AI speed."

---

## 3. Proof Points Cheat Sheet
*Drop these numbers to build authority.*
- "I've managed **4M+ contacts**."
- "Reduced churn **40%** at Revenue Accelerator."
- "Cut costs **75%** at Sylva."
- "Increased revenue **32%** at Chief of Staff Network."
