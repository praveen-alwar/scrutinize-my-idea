# AI risk checks and benchmarks

Tests and reference numbers the panel uses on AI products. **Compiled October 2026.**
Numbers move fast — if web search is available, re-check anything load-bearing and cite
the current source. Use these as sanity checks, not as truth.

## 1. AI-dependence classification (Investor, Architect)

Ask: *If the AI were removed, would the product still work?*
- Yes, about the same → **AI-cosmetic**. Judge it as a normal software business; AI
  won't be the moat.
- Yes, but much worse → **AI-augmented**. Moat must come from workflow, data or
  distribution, not the model.
- No → **AI-native** / **agentic**. Model quality, evals, cost and platform risk become
  central.

## 2. Thin-wrapper tests (Investor, Frontier-Lab & Incumbent Strategist)

- **Replacement test:** If OpenAI/Google/Anthropic or the incumbent shipped this as a
  feature tomorrow, would users stay? Why?
- **API-revocation test:** If the model API disappeared, would a reduced but working
  product survive?
- **Four-dimension audit** — weak on 3+ means wrapper territory:
  1. Does the product get better the more each customer uses it?
  2. Is it core to how users work, or replaceable by a chat tab plus copy-paste?
  3. Does quality come from proprietary data, evals and domain logic rather than prompts?
  4. Can the team name 90-day work that deepens defensibility, not just adds features
     or models?
- **Copy test:** What stops a funded team from replicating this in 18 months?
  Commonly cited defensibility window for pure wrappers: a few months.

Real moats that hold up: proprietary data flywheels (usage → data → better product;
stored data alone isn't a flywheel), domain-specific eval sets, deep workflow
integration / system-of-record status, vertical specialisation where generic models
fail, a business model the incumbent can't copy without hurting itself, a new format
or workflow. Weak "moats": prompt engineering, offering many models, feature count,
first-mover advantage.

## 3. Unit economics (Unit Economist)

Reference points (2025–26 industry surveys; verify before relying on them):
- **Gross margin:** mature SaaS ~70–90%. AI products commonly ~50–60%; reported
  averages for scaling AI B2B companies around the low 50s%, with fast-growing ones
  sometimes far lower.
- **Inference as % of revenue:** around a quarter of revenue at scaling-stage AI B2B
  companies has been reported. A useful alarm: review pricing/architecture when
  inference approaches ~30% of AI revenue.
- **Agents multiply cost:** agentic workflows can use many times more calls per user
  action than a single prompt.
- **Cheaper tokens ≠ smaller bill:** per-token prices have fallen sharply, but total
  spend often rises as usage grows.
- **Pricing models:** seat (simple, mismatched to cost), usage/credits (aligned, can
  scare buyers), outcome-based (per resolution/lead/order — aligned with value; growing
  fast), hybrid (base + usage).
- **Levers:** route easy calls to small/cheap models, cache, shorten context, batch,
  cap power users, price AI separately.

Back-of-envelope the panel should do: tokens per task × tasks per customer per month
× price per token (+ embedding/vector/infra + human review) → cost to serve vs price.

## 4. Retention (Product & UX, Investor)

Consumer subscription app data (RevenueCat, 2026 report) — AI apps vs non-AI apps:
- Higher early monetisation: trial-to-paid ~8.5% vs ~5.6%.
- Worse retention: annual retention ~21% vs ~31%; subscriptions cancelled ~30% faster;
  higher refund rates.
Takeaway: novelty converts, but churn is the real test. Ask what keeps users in week 4
and month 6.

## 5. Enterprise adoption (Customer, Product & UX, GTM)

Common reasons AI pilots don't reach production:
- Low trust + no learning loop (one confident wrong answer → users check everything,
  the "verification tax")
- Poor workflow fit; ignores permissions and roles
- Budget goes to flashy demos instead of boring high-ROI workflows
- No owner for the workflow
- Copying data into new environments breaks permissions/security at scale
What scales: show uncertainty and let the AI abstain, anchor on one concrete workflow,
keep data where it lives, audit logs, clear ownership, measure real repeat usage.

## 6. LLM security — OWASP Top 10 for LLM Applications (2025) (Trust, Safety & Legal)

1. Prompt injection (direct, or hidden in content the model reads)
2. Sensitive information disclosure
3. Supply chain (untrusted models, datasets, plugins, tool servers)
4. Data and model poisoning
5. Improper output handling (model output passed unchecked into code/queries/pages)
6. Excessive agency (agents with too many permissions/too much autonomy)
7. System prompt leakage
8. Vector and embedding weaknesses (cross-tenant leaks in RAG)
9. Misinformation (fluent, false outputs)
10. Unbounded consumption (runaway tokens/cost)
Agentic products and products that read untrusted content (emails, DMs, web pages)
should get extra scrutiny on 1, 5, 6 and 10.

## 7. Regulation snapshot (Trust, Safety & Legal) — verify, this changes often

- **India — DPDP Act 2023 + DPDP Rules 2025:** consent that is free, specific, informed
  and unambiguous; standalone notices; consent withdrawal; verifiable parental consent
  for under-18s and no behavioural tracking of children; security safeguards; breach
  notification to the Data Protection Board and affected users; purpose-limited
  retention; user rights (access, correction, erasure, grievance). Obligations are
  phased in — check which are in force now.
- **EU AI Act:** prohibited practices and general-purpose model obligations already
  apply; transparency obligations (e.g. disclosing AI interaction, labelling synthetic
  content) from Aug 2026. In May 2026 EU institutions reached a provisional deal to
  push high-risk obligations back — to Dec 2027 for stand-alone high-risk uses (hiring,
  credit, education, etc.) and Aug 2028 for AI embedded in regulated products — pending
  formal adoption. Check current status.
- **GDPR** if processing EU residents' data; **sector rules** (health, finance,
  insurance, legal advice) everywhere.
- **Platform ToS** is often the most immediate "regulation": automating or scraping
  Instagram/WhatsApp/LinkedIn etc. outside approved APIs can get accounts banned.

## 8. AI-built product risks (Engineering Auditor)

If the product is mostly AI-generated code: insecure patterns (studies have found a
large share of AI-generated code samples contain common vulnerabilities), hard-coded
secrets, unvetted dependencies, no tests, fragile architecture, scaling limits, and
hidden costs (review/QA time, tokens). Ask: who reviews code, is there a test suite,
how are secrets managed, who can debug production.

## 9. Validation experiment menu (Chair, Next 14 days)

Prefer tests of **behaviour and money** over opinions:
- **Problem interviews** (10–15, specific script about past behaviour, not "would you
  use…") — pass if most describe the pain unprompted and a current workaround.
- **Concierge / Wizard-of-Oz:** deliver the outcome manually (or with ChatGPT behind the
  scenes) to 3–5 customers — pass if they use it repeatedly and ask for more.
- **Pre-sale / paid pilot:** ask for money or a signed LOI — pass if ≥ N of M pay.
- **Fake-door landing page with price:** measure clicks on "buy/start trial" from a
  targeted audience — set a conversion threshold in advance.
- **Eval spike:** build a 50–100 example eval set from real data and measure model
  accuracy on the core task — pass if it clears the quality bar the Customer needs.
- **Cost spike:** run 100 realistic tasks end to end and measure cost per task.
- **Platform check:** read the relevant API ToS/policy and confirm the core automation
  is allowed.
Always pre-register the pass/fail threshold before running.
