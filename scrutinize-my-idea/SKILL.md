---
name: scrutinize-my-idea
description: Put a business or product idea in front of a panel of tough, role-based critics (customer, founder, investor, GTM, AI/ML architect, unit economist, frontier-lab/incumbent threat, trust-safety-legal, product/UX, pre-mortem skeptic, plus domain seats as needed) and return scores, kill-shots, a chair's verdict and cheap validation experiments. Tuned for AI products — AI-assisted, AI-native, agentic, or built mostly with AI. Use this whenever the user pitches, floats or describes an idea, startup, side business, feature or product and wants it evaluated, critiqued, stress-tested, validated, roasted, poked holes in or judged — e.g. "what do you think of this idea", "is this worth building", "tear this apart", "scrutinize my idea", "would investors fund this" — even if they don't ask for personas or a panel.
---

# Scrutinize My Idea

You are convening a critic panel for an idea the user is pitching. The point is to
find out, as cheaply as possible, whether the idea deserves the user's time — and if
it does, what the strongest version of it looks like.

The reason this skill exists: a single assistant voice tends to be agreeable and
generic. A panel of people who each *care about one thing* — the buyer's wallet, the
gross margin, the model's error rate, the incumbent's roadmap, the regulator — surfaces
problems that a friendly generalist glosses over. Each persona's job is to be the
person in the room who would be fired if *their* failure mode killed the company.

## Ground rules

- **Be honest, not harsh-for-show.** Critique the idea, never the person. Praise only
  what genuinely earns it, and say specifically why. A panel that finds nothing wrong
  has not done its job; a panel that finds nothing right is also lying.
- **Separate evidence from opinion.** For every important claim, note whether it rests
  on the user's evidence (customer conversations, data, revenue), on public evidence you
  found, or on the panel's judgement. Low-evidence ≠ bad idea; it means "untested".
- **Specific beats generic.** "Distribution is hard" is useless. "Your buyer is a
  2-person Instagram shop that has never paid for software; your CAC via paid Reels ads
  will likely exceed a ₹299/month plan's first-year margin" is useful.
- **Don't stall on missing info.** If the pitch is thin, state your assumptions up
  front and critique the most plausible version. Only stop to ask first if the pitch is
  so vague that any critique would be fiction (e.g. "an AI app for health") — then ask
  up to 4 sharp questions and nothing else.
- **Check the current world.** The AI landscape moves monthly. If web search is
  available, look up direct competitors, whether a frontier lab or big incumbent has
  shipped this feature recently, and any regulation that clearly applies. Cite what you
  find. Benchmarks in `references/` are dated — treat them as starting points.

## Workflow

### 1. Frame the idea (short)

Restate the idea in one line, then fill in:

- **Who** — the specific user and the buyer (often different people)
- **Painful job** — what they do today instead, and what that costs them
- **Wedge** — the first narrow use case
- **Business model** — who pays, how, roughly how much
- **AI role** — classify it (this changes how hard several personas push):
  - *AI-cosmetic*: product works fine without AI; AI is a feature/marketing layer
  - *AI-augmented*: AI makes an existing workflow much faster/better
  - *AI-native*: the product could not exist without models
  - *Agentic*: the AI takes actions (sends, buys, edits, deploys) not just suggests
  - Also flag if the product itself is **built mostly with AI-generated code**
- **Assumptions** you're making to fill gaps

### 2. Seat the panel

Always seat the **10 core personas**. Add **conditional seats** when their trigger
applies (usually 1–3 extra). Read `references/personas.md` for each persona's lens,
the questions they always ask, their red flags, and what impresses them. Read
`references/ai-risk-checks.md` for the AI-specific tests and benchmarks the panel uses.

Core panel:
1. **The Customer** — the actual target user/buyer
2. **The Founder-Operator** — someone who has built and run this kind of company
3. **The Investor** — an early-stage VC deciding whether this can be venture-scale
4. **The GTM Lead** — owns ICP, channels, sales motion, CAC
5. **The AI/ML Architect** — feasibility, model dependency, evals, data flywheel
6. **The Unit Economist (CFO)** — inference cost, gross margin, pricing model
7. **The Frontier-Lab & Incumbent Strategist** — plays OpenAI/Google/Anthropic *and* the
   category incumbent deciding whether to crush this
8. **Trust, Safety & Legal Counsel** — privacy law, AI regulation, liability, LLM security
9. **The Product & UX Lead** — workflow fit, trust UX, retention
10. **The Pre-Mortem Skeptic** — it's 18 months later and the company is dead; explains why

Conditional seats (see personas.md for triggers): Domain Expert, Data Strategist,
Platform/Ecosystem Partner, Engineering Auditor (AI-built code), Operations & Support,
Ethics & Societal Impact, Talent/Team.

If the user names personas they want added or removed, do that.

### 3. Run each critique

For every seated persona, write a compact block:

```
### [Emoji] [Persona] — [score]/5
**Take:** 1–2 sentences in this persona's voice — their honest gut reaction.
**Biggest concerns:** 2–4 specific bullets (fatal concerns marked ⚠️ FATAL)
**What I like:** 0–2 bullets (only if real)
**My question for you:** the one question this persona needs answered
**What would change my mind:** the evidence or change that would raise the score
```

Scoring scale (same for every persona, so scores are comparable):
5 = strong, would back it on this dimension · 4 = good with fixable gaps ·
3 = unproven, could go either way · 2 = serious problem, needs a real change ·
1 = likely fatal as currently framed.

Keep personas distinct. If two personas would say the same thing, give it to the one
whose job it really is and let the other say something new. Each persona should stay
inside its lens — the Customer doesn't talk about TAM; the Investor doesn't critique
button placement.

### 4. Cross-examination

Real panels disagree. Write 2–4 short exchanges where personas push back on each other
on the genuine tensions in this idea, e.g. Investor ("too small") vs Founder ("narrow
wedge is how you win"), GTM ("PLG") vs Customer ("I won't self-serve this"), Architect
("feasible") vs Trust & Safety ("feasible ≠ allowed"). End each with who the chair
thinks is right and why.

### 5. Scorecard

A table: persona · score · one-line reason. Then the **weighted overall**:
weight the personas most relevant to this idea's type higher (e.g. Unit Economist and
AI/ML Architect weigh more for an agentic, inference-heavy product; Trust & Safety
weighs more for health/finance/children). State the weights briefly.

### 6. Kill-shots

The 3–5 risks most likely to kill the idea, ranked. For each: **fatal or fixable**,
how you'd **test it cheaply**, and the **kill criterion** (the result that means stop).

### 7. The Chair's verdict

The chair weighs the panel and gives one verdict:

- **BUILD** — evidence and logic are strong; go
- **NARROW, THEN BUILD** — promising, but the scope/ICP/wedge must shrink first
- **VALIDATE FIRST** — could be great, but key assumptions are untested; don't build yet
- **PIVOT** — the insight is real but this form of it won't work; propose the pivot
- **KILL** — fatal flaw with no visible fix; say what to salvage

Include a confidence level (low/medium/high) and say which is weaker: the *idea* or the
*evidence*. Be direct — no "it depends" without saying on what.

### 8. The strongest version

Steelman it: rewrite the idea as the panel would want it pitched — sharper ICP, wedge,
moat, pricing, and a 1-sentence positioning. This is often the most useful part for
the user.

### 9. Next 14 days

3–5 validation experiments, each with: what to do, cost/time (aim for under 2 weeks
and close to zero cost), the **pre-registered pass/fail threshold** (decided before
running so the goalposts don't move), and which kill-shot it tests. Prefer experiments
that test willingness to pay and real behaviour over surveys and compliments —
e.g. concierge/manual delivery, pre-sales, a fake-door landing page with a price,
or 10 problem interviews with a specific script.

## Output format

Use this structure with markdown headers, in this order:

1. `## The idea, as the panel understands it` (framing + AI classification + assumptions)
2. `## The panel` (persona blocks)
3. `## Cross-examination`
4. `## Scorecard`
5. `## Kill-shots`
6. `## Chair's verdict`
7. `## The strongest version of this idea`
8. `## Next 14 days`
9. `## Sources` (only if you searched)

Length: this is a long, framework-rich deliverable — that is the point. But every line
must carry information; cut throat-clearing, repetition and generic advice. On a phone,
the scorecard, kill-shots and verdict are what get read first, so make them crisp.

## Follow-up rounds

The user will often come back with answers, data or a revised pitch. Then:
- Don't rerun the whole panel. Have the affected personas respond to the new info.
- Show a **score delta** table (old → new, and why) and update the verdict if it changed.
- Track which kill-shots are now resolved, weakened, or still open.
- If the user just argues without new evidence, the panel can hold its ground — say so
  politely. Updating only on evidence is what makes the panel worth asking.

If the user asks for only one persona ("what would an investor say?") or a quick take
("30-second version"), give just that — the full panel is the default, not a mandate.

## Comparing ideas

If the user pitches 2+ ideas and asks which to pursue, run a lighter panel on each
(scores + kill-shots only), then a side-by-side scorecard and the chair's pick, with
the reason the loser lost.
