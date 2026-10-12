# scrutinize-my-idea

A Claude skill that puts your business or product idea in front of a panel of tough,
role-based critics — tuned for AI products (AI-assisted, AI-native, agentic, or built
mostly with AI).

Pitch an idea in plain words ("tear this apart", "is this worth building?", "would
investors fund this?") and the panel returns scores, the risks most likely to kill it,
a verdict, the strongest version of the idea, and a 14-day validation plan.

## The panel

**Always seated (10):**

| Seat | Cares about |
|---|---|
| 🧑‍💼 Customer | Is the pain real and frequent? Would I switch and pay? Can I trust the output? |
| 🛠️ Founder-Operator | Founder-market fit, narrow wedge, what to ship in 4–6 weeks |
| 💰 Investor | Market size, why now, moat once models are a commodity, venture vs bootstrapped |
| 📣 GTM Lead | ICP, first channel, sales motion, CAC vs gross profit, incumbent bundling |
| 🧠 AI/ML Architect | Accuracy needed vs achievable, evals, model lock-in, data flywheel, agent error rates |
| 📊 Unit Economist (CFO) | Inference cost per customer, gross margin, pricing model |
| 🏰 Frontier-Lab & Incumbent Strategist | Will OpenAI/Google/Anthropic or the incumbent ship this as a feature? |
| ⚖️ Trust, Safety & Legal | DPDP / GDPR / EU AI Act, liability, platform ToS, OWASP LLM Top 10 |
| 🎨 Product & UX Lead | Workflow fit, trust UX, week-4 retention |
| 💀 Pre-Mortem Skeptic | "It's 18 months later and the company is dead — here's how it died" |

**Added only when relevant:** Domain Expert, Data Strategist, Platform/Ecosystem Partner,
Engineering Auditor (AI-generated codebases), Operations & Support, Ethics & Societal
Impact, Talent/Team.

## What you get back

1. The idea as the panel understands it, with an AI-dependence classification and stated assumptions
2. Each critic's take, score (1–5), biggest concerns, the one question they'd ask, and what would change their mind
3. Cross-examination where critics disagree
4. A weighted scorecard
5. Kill-shots — ranked risks, each fatal or fixable, with a cheap test and a kill criterion
6. The chair's verdict: **BUILD · NARROW, THEN BUILD · VALIDATE FIRST · PIVOT · KILL**
7. The strongest version of the idea
8. A 14-day plan of validation experiments with pass/fail thresholds set in advance

Follow-up rounds re-score only the affected critics and show a score-change table.

## Install

- **Claude app:** download `scrutinize-my-idea.skill` from this repo, open it in Claude, and tap **Save skill**.
  Or zip the `scrutinize-my-idea/` folder and upload it from the Skills section of Claude's settings.
- **Claude Code:** copy the `scrutinize-my-idea/` folder into `~/.claude/skills/` (personal)
  or `.claude/skills/` in a project.

## Repo layout

```
scrutinize-my-idea/
├── SKILL.md                    # workflow, output format, follow-up rounds
├── references/
│   ├── personas.md             # each critic's lens, questions, red flags, weighting
│   └── ai-risk-checks.md       # wrapper tests, margin/retention benchmarks, OWASP LLM, regulation
└── evals/evals.json            # sample test pitches
scrutinize-my-idea.skill        # packaged skill, ready to install
```

## Notes

Benchmarks and regulation notes in `references/ai-risk-checks.md` were compiled in
October 2026. The skill tells Claude to re-check current competitors and rules on the
web before judging, since the AI landscape changes monthly.
