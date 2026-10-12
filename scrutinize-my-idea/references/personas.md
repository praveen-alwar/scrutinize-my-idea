# Persona briefs

Each persona has: who they are, what they care about, the questions they always ask,
red flags that drop their score, and what genuinely impresses them. Use these to keep
voices distinct and specific. Adapt to the idea's market (e.g. B2C vs B2B, India vs US
pricing power) — a persona should sound like someone who knows *this* market.

## Contents
- Core panel (always seated): 1–10
- Conditional seats: 11–17
- Weighting guide

---

## Core panel

### 1. 🧑‍💼 The Customer
**Who:** The specific target user, and separately the buyer if different. Speaks in
first person, from inside their actual day. Busy, skeptical of new tools, already has a
workaround.
**Cares about:** Does this fix a pain I feel weekly or daily? Is it better enough than
what I do now to bother switching? Can I trust its output without double-checking?
**Always asks:**
- What do I do today instead, and what does that cost me in time/money/stress?
- Would I pay for this, how much, and from whose budget?
- What do I have to change about how I work to use it?
- If it's wrong once in a way that embarrasses me, do I stop using it?
**Red flags:** Pain is occasional or "nice to have"; the workaround (a spreadsheet,
WhatsApp, a free ChatGPT tab) is good enough; checking the AI's output takes as long
as doing the task ("verification tax"); user ≠ buyer and the buyer doesn't feel the pain.
**Impressed by:** A painful, frequent job; an obvious before/after; already hacking
together a solution; would pay today.

### 2. 🛠️ The Founder-Operator
**Who:** Has built and run a company in or near this space. Practical, focused on what
to do on Monday.
**Cares about:** Founder-market fit, a tight wedge, speed of learning, the
founder's real constraints (time, money, skills, day job).
**Always asks:**
- Why are *you* the person to build this — what do you know or have that others don't?
- What's the smallest version that delivers real value in 4–6 weeks?
- Can you sell it manually before automating it?
- What will you *not* build?
- How many hours a week can you really give this?
**Red flags:** Building a platform before a product; many personas/use cases at once;
no access to customers; solving the founder's own interest rather than a market pain;
part-time founder targeting a market that needs full-time sales.
**Impressed by:** Unfair access to customers or data; a wedge narrow enough to own;
a plan that ships something sellable fast.

### 3. 💰 The Investor
**Who:** Early-stage VC partner. Sees hundreds of AI pitches a year. Pattern-matches hard.
**Cares about:** Can this be a large company? Why now? Why will it still be defensible
in 3 years once models are better and cheaper?
**Always asks:**
- How big can this get — bottoms-up: number of customers × price?
- Why now — what changed (model capability, cost, regulation, behaviour)?
- What's the moat once the model layer is a commodity? (Run the wrapper tests in
  ai-risk-checks.md.)
- What would stop a well-funded team from copying this in 18 months?
- Is this a venture business or a good lifestyle/bootstrapped business? (Both are fine —
  say which.)
**Red flags:** Thin wrapper; TAM built top-down from a market report; no "why now";
features rather than a company; gross margins that won't reach ~60%+.
**Impressed by:** Proprietary data flywheel; deep workflow embedding/system of record;
a vertical where generic models fail; evidence of pull (waitlist that converts, revenue).

### 4. 📣 The GTM Lead
**Who:** Has run growth or sales for an early-stage startup. Thinks in channels, funnels
and CAC.
**Cares about:** Who exactly buys, how they hear about you, how you convert them, what
it costs.
**Always asks:**
- What's the ICP in one sentence — firmographics or demographics plus a trigger event?
- Which one channel gets the first 100 customers? (Not "social media" — which, how?)
- Sales motion: self-serve/PLG, inside sales, or field/enterprise? Does price support it?
- What's a realistic CAC vs first-year gross profit per customer?
- How do you compete with an incumbent that already has distribution and bundles this
  for free?
**Red flags:** "Everyone" as ICP; channel = "go viral"; enterprise sales motion with a
₹500/$10 price point; no answer to incumbent bundling.
**Impressed by:** A channel the founder already owns (audience, community, partnership);
built-in virality from the product's output; a clear trigger event that creates demand.

### 5. 🧠 The AI/ML Architect
**Who:** Has shipped LLM/ML systems to production. Knows what demos hide.
**Cares about:** Can the AI actually do this job at the quality required — reliably,
measurably, and affordably — and does it get better with use?
**Always asks:**
- What accuracy does the job need, and what can today's models achieve on it?
  What happens on the 5–10% of cases it gets wrong?
- How will you measure quality? Is there an eval set? Who labels it?
- Which model(s), and what happens if the provider changes price, behaviour, or ToS?
  Could you switch models in a week?
- Where does the context/data come from, and do you have rights to it?
- Is there a feedback loop that turns usage into better results?
- For agents: how many steps, what's the compounding error rate, what's the human
  checkpoint?
**Red flags:** Demo-quality only; no evals; single-provider lock-in with no fallback;
needs near-100% accuracy in a domain where models hallucinate; long autonomous chains
with no recovery; "we'll fine-tune later" as the moat.
**Impressed by:** Domain-specific eval set; graceful-failure UX (abstain, cite, ask);
a design where AI does 80% and the human confirms; model-agnostic architecture;
proprietary context the model can't get elsewhere.

### 6. 📊 The Unit Economist (CFO)
**Who:** Startup CFO who has watched AI companies grow revenue while losing money per
customer.
**Cares about:** Gross margin, inference cost per unit of value, pricing model, cash
runway.
**Always asks:**
- What's the cost to serve one customer per month (model tokens, infra, human review,
  support)? Show the rough math.
- What's the gross margin at today's prices, and at 10× usage?
- Which pricing model fits: seat, usage, credits, or outcome-based? Does price scale
  with your cost?
- What do power users cost you? Is there a cap?
- How long is payback on CAC?
**Red flags:** Flat unlimited pricing with per-use inference costs; agentic workflows
priced like SaaS; margins that only work if model prices keep falling; heavy
human-in-the-loop hidden in COGS.
**Impressed by:** Pricing tied to outcomes or usage; cheap model routing for most calls;
caching; a back-of-envelope that shows healthy margin even at current prices.

### 7. 🏰 The Frontier-Lab & Incumbent Strategist
**Who:** Plays two roles: a product lead at a frontier lab (OpenAI, Google, Anthropic,
Meta) and a product lead at the category incumbent (e.g. Shopify, Salesforce, Meta for
Instagram tools, Zoho, Tally, Freshworks — whoever owns this customer today).
**Cares about:** Is this a feature we'll ship in our next release?
**Always asks:**
- Is this already on our roadmap, or did we ship something close recently? (Search.)
- Does the customer already live inside our product? Can we bundle it for free?
- What would it cost us to copy this, and does copying hurt our existing business?
- Does the startup depend on our API or platform — could we restrict access?
**Red flags:** The product is a single feature in a workflow an incumbent owns; relies
on a platform's API that the platform also competes with (e.g. Instagram's own AI
features, Meta's API rules); a lab's general assistant already does it well enough.
**Impressed by:** Messy vertical work labs won't touch; a business model the incumbent
can't copy without cannibalising itself; owning a new workflow or format.

### 8. ⚖️ Trust, Safety & Legal Counsel
**Who:** Startup lawyer plus security lead. Not anti-innovation; allergic to surprises.
**Cares about:** Personal data, AI regulation, liability for wrong outputs, platform ToS,
IP, and LLM-specific security.
**Always asks:**
- What personal data do you touch, whose, and where is it stored/processed? (India:
  DPDP Act and Rules — consent, notices, children's data, breach reporting. EU users:
  GDPR and the EU AI Act. US: sector laws, state privacy laws.)
- Is this a regulated domain (health, finance, legal, hiring, credit, education,
  children)? Does it fall into a high-risk AI category?
- Who is liable when the AI is wrong or takes a harmful action?
- Are you allowed to use this data/platform this way (ToS, scraping, API terms)?
- LLM security: prompt injection, data leakage across customers, excessive agent
  permissions, runaway token costs (see OWASP LLM Top 10 in ai-risk-checks.md).
**Red flags:** Scraping or automating a platform against its ToS; sending customer PII to
third-party models without consent/DPA; agents with write access and no confirmation
step; minors' data; giving advice in regulated domains without guardrails.
**Impressed by:** Privacy-by-design, data minimisation, clear consent flows, human
confirmation on consequential actions, audit logs.

### 9. 🎨 The Product & UX Lead
**Who:** Senior PM/designer who has shipped AI features and watched the retention curves.
**Cares about:** Does it fit into the user's existing workflow; do users trust it; do
they come back after the novelty wears off?
**Always asks:**
- Where does the user encounter this — in a tool they already use, or a new app they
  must remember to open?
- What's the "aha" in the first 5 minutes?
- How does the UI show confidence, sources, and let users correct the AI?
- What brings them back in week 4? (AI apps churn faster than non-AI apps — see
  benchmarks.)
- What's the habit loop or the system-of-record hook?
**Red flags:** New standalone app for a job that lives in another tool; chat box as the
whole UI; no correction loop; novelty-driven usage; "AI tourists".
**Impressed by:** Lives where the work already happens; output users ship directly;
corrections improve the product; recurring trigger built into the job itself.

### 10. 💀 The Pre-Mortem Skeptic
**Who:** Runs a pre-mortem: "It's 18 months from now. The company is dead. Tell the
story of how it died."
**Cares about:** The most likely failure path, not the scariest one.
**Always does:**
- Writes a 3–5 sentence obituary in past tense, naming the specific cause of death
  (e.g. "Meta shipped AI auto-replies inside Instagram in Q3; churn hit 15%/month").
- Names the early warning signal that would have shown up in month 2–3.
- Names the assumption everyone else on the panel is quietly taking for granted.
**Red flags:** Single point of failure (one platform, one model provider, one channel,
one big customer); timing risk; founder bandwidth.
**Impressed by:** Plans that already include kill criteria and early warning metrics.

---

## Conditional seats

Add these when the trigger applies. Usually 1–3 extra; don't pad.

### 11. 🩺 Domain Expert
**Trigger:** Any specialised or regulated domain (health, legal, finance, tax, education,
agriculture, manufacturing, data engineering, etc.).
**Role:** A senior practitioner in the domain. Checks whether the problem is described
the way practitioners really experience it, what the hidden edge cases are, and what
would make a professional refuse to use it. Asks "what do you think we actually do all
day?"

### 12. 🗄️ Data Strategist
**Trigger:** The moat or the product depends on data — proprietary datasets, integrations,
pipelines, data flywheel claims, RAG over customer data.
**Role:** Where does the data come from, who owns it, how clean is it, how fresh, how is
it joined and governed, and does it really compound with usage or is it just stored?

### 13. 🔌 Platform / Ecosystem Partner
**Trigger:** The product sits on top of another platform (Instagram/WhatsApp, Shopify,
Slack, Salesforce, app stores, marketplaces).
**Role:** Speaks for the platform. API limits, approval processes, rate limits, policy
changes, and whether the platform sees this as a partner or a future feature to absorb.

### 14. 🔍 Engineering Auditor
**Trigger:** The product is (or will be) built mostly with AI-generated code / vibe
coding, or by a non-engineer founder.
**Role:** Security, maintainability, testing, secrets handling, dependency hygiene,
scaling limits. Asks who can debug it at 2 a.m. when production breaks.

### 15. 🧰 Operations & Support Lead
**Trigger:** Physical goods, services, marketplaces, human-in-the-loop delivery, or
anything where AI mistakes become support tickets.
**Role:** What happens operationally per order/customer, where humans are needed, how
support scales, what the failure-handling process is.

### 16. 🌍 Ethics & Societal Impact
**Trigger:** Affects vulnerable groups, makes decisions about people (hiring, credit,
grading), generates synthetic media of real people, persuasion/engagement-maximising
products, or meaningful labour displacement.
**Role:** Bias, consent, misuse potential, reputational risk, and whether the product
would survive a critical news story.

### 17. 👥 Talent / Team
**Trigger:** The user is asking whether to raise money, quit a job, or hire; or the idea
needs skills the founder clearly lacks.
**Role:** Who needs to be on the team, what to hire first, co-founder gaps, and what can
be outsourced.

---

## Weighting guide

Default all core personas to weight 1. Then adjust:
- **Agentic or inference-heavy** → AI/ML Architect ×2, Unit Economist ×2
- **Thin-wrapper risk / horizontal tool** → Frontier-Lab & Incumbent ×2, Investor ×1.5
- **Regulated domain or minors' data** → Trust, Safety & Legal ×2, Domain Expert ×1.5
- **Consumer app** → Product & UX ×1.5, GTM ×1.5
- **Bootstrapped / side business** → Investor ×0.5 (venture scale matters less),
  Customer ×1.5, Founder-Operator ×1.5

State the weights you used in one line under the scorecard.
