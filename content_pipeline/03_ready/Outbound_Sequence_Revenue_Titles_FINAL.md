# PLAYBOOK: Outbound Sequence — Revenue Titles (50-200 SaaS)

**Role:** The Funnel Plumber
**Target:** CRO, VP RevOps, RevOps Manager
**Firmographics:** US, SaaS, 50-200 employees
**Volume:** 50+ contacts/week
**Variables:** `{{first_name}}`, `{{company}}`, `{{title}}`

---

## Sequence Map (9 Touches / 17 Days)

| Step | Day | Channel | Purpose | CTA |
|------|-----|---------|---------|-----|
| 1 | 0 | LinkedIn Profile View | Put your name on their radar | — |
| 2 | 1 | Email 1 | Pattern hook | Reply (question) |
| 3 | 3 | LinkedIn Connection Request | Peer positioning, no pitch | Accept connection |
| 4 | 5 | Email 2 | Cost quantification | Reply (confirm/deny) |
| 5 | 7 | LinkedIn Engage | Like/comment on their content | — |
| 6 | 9 | Email 3 | Proof point | Reply (curiosity) |
| 7 | 11 | LinkedIn DM | Value-add, no ask | Conversation |
| 8 | 14 | Email 4 | The offer — first time ask | Reply to book |
| 9 | 17 | Email 5 | Breakup | Reply or close |

---

## Step 1 — LinkedIn Profile View (Day 0)

No action needed beyond viewing their profile. They see your name and headline in notifications. This is priming.

---

## Step 2 — Email 1: The Pattern Hook (Day 1)

**Subject:** `{{company}} pipeline routing`

{{first_name}},

most SaaS companies between seed and series C hit the same wall. the CRM workflows that worked with a small team start silently dropping leads once headcount and integrations scale.

never broken enough to show on a dashboard, but easily costing six figures in lost pipeline annually.

has that started showing up at {{company}} yet?

---

## Step 3 — LinkedIn Connection Request (Day 3)

{{first_name}}, saw you're leading revenue ops at {{company}}. always good to connect with people building revenue infrastructure at scaling SaaS companies. no pitch, just like seeing how other teams solve the same plumbing problems.

*(Keep under 300 characters if LinkedIn enforces the limit on connection notes.)*

---

## Step 4 — Email 2: The Cost Quantification (Day 5)

**Subject:** `the math on silent leakage`

{{first_name}},

quick back-of-napkin:

if even 5% of inbound leads are stuck in bad routing logic or orphaned by a sync failure, at typical B2B deal sizes that's $150-300k/year in pipeline that never gets worked.

most ops teams don't catch it because the leads aren't "lost." they're sitting in the CRM, they just never hit a queue.

I run a diagnostic that finds it. if I don't surface at least $100k in recoverable pipeline, you don't pay.

does that sound about right for {{company}}?

---

## Step 5 — LinkedIn Engage (Day 7)

Like or comment on one of their recent posts or activity. If they haven't posted recently, like one of their comments or engage with content from {{company}}'s page.

If commenting, keep it genuine and relevant to their content. Not "Great post!" — actually add a thought. 15+ words.

**Example if they post about a RevOps challenge:**

this is one of those problems that compounds silently. we ran into the same pattern with lifecycle stage mismatches. the data looked clean in aggregate but the routing was dropping edge cases. curious what your fix looked like.

*(Only comment if you can say something real. If they have no activity, skip to a Like on a company post and move on.)*

---

## Step 6 — Email 3: The Proof Point (Day 9)

**Subject:** `how a 120-person SaaS found $400k in dead pipeline`

{{first_name}},

ran a data forensic for a SaaS company about {{company}}'s size last quarter. ~15 integrations, fast-growing sales team.

found $400k+ in leads stuck in lifecycle limbo. broken assignment rules, failed syncs between marketing and sales objects, duplicates masking real opportunities.

none of it was visible in their reporting. took 2 weeks to surface and route back to reps.

want me to send over the failure patterns? might look familiar.

---

## Step 7 — LinkedIn DM (Day 11)

*(Only send if they accepted the connection request. If they haven't, skip this step.)*

hey {{first_name}}, not trying to sell you anything. just curious, at {{company}}'s stage, what's the biggest infrastructure headache right now? routing? data hygiene? integration sprawl?

I spend most of my time inside these problems across SaaS companies so I'm always curious what's top of mind for {{title}}s right now.

*(This is a genuine conversation starter. If they reply, have a real conversation. Don't pivot to a pitch in the DM — let Email 4 do that work.)*

---

## Step 8 — Email 4: The Offer (Day 14)

**Subject:** `the diagnostic`

{{first_name}},

I run a forensic analysis on your raw CRM data to find the leads, pipeline, and revenue your system is silently dropping. takes 1-2 weeks and I pull a full manifest of orphaned records, broken syncs, and routing failures with the dollar value attached.

the guarantee: if I don't surface at least $100k in recoverable pipeline, you don't pay. full stop.

worth a 15-minute call to see if {{company}} qualifies?

---

## Step 9 — Email 5: The Breakup (Day 17)

**Subject:** `closing the loop`

{{first_name}},

last note on this.

data debt compounds. every new rep, every new integration, every migration adds entropy. what's a $5k fix today turns into a $25k project in 6 months.

if your team is spending more time cleaning data than closing deals, I'll find at least $100k in recoverable pipeline or you pay nothing.

either way, I'll stop filling your inbox.

---

## Spam-Safe Constraints

**Avoided trigger words:** "free," "guarantee," "act now," "limited time," "opportunity," "reaching out," "hope this finds you well," "I'd love to," "just following up," "just checking in," "click here," "schedule."

**Format rules:**
- Plain text only — no HTML, no images, no signature images
- Lowercase subject lines
- One link max per email (none used in this sequence)
- 50-90 words per email
- Emails 1-3 have no meeting ask — reply-optimized only
- Email 4 is the first and only meeting ask (touch 8 of 9)

---

## Narrative Arc

1. **"I know what's breaking"** — demonstrate stage-specific infrastructure pain
2. **"We think alike"** — LinkedIn connection builds peer familiarity
3. **"Here's what it's costing you"** — quantify the silent bleed
4. **"I pay attention to your world"** — LinkedIn engagement shows genuine interest
5. **"Here's proof it's fixable"** — peer company result
6. **"Here's something useful"** — LinkedIn DM delivers value with no ask
7. **"Here's what I do + let's talk"** — earned the right to ask by touch 8
8. **"Last chance"** — breakup reframes cost of inaction
