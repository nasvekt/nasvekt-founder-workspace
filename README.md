# NasVekt Founder Operating System

> **An AI-powered intelligence system that validates whether a business problem deserves an AI solution — before a single line of code is written.**

Built by Abdulrahman (Nassar) · Cairo, Egypt · AI Engineer

---

## The Problem This Solves

Most AI projects fail not because they were built wrong — because they were built for the wrong problem.

Teams spend weeks building AI automation for workflows that don't have real demand, don't have paying customers, or have unit economics that don't work. The NasVekt Founder OS is the validation layer that runs before the build starts.

## What It Is

A system of 4 interconnected intelligence pipelines — 16 structured prompts total — that evaluate any business problem across market demand, financial viability, competitive positioning, and deal structure. Each pipeline produces scored, evidence-based outputs with phase gates that prevent bad decisions from reaching the next stage.

```
Market Intelligence     → Does this problem have real, paying customers?
Financial Intelligence  → Do the unit economics actually work?
Competitive Intelligence → What are existing solutions missing?
Deal Intelligence       → Is this agreement structured correctly?
```

## Why This Matters for AI Integration Work

When integrating AI into a business, the most expensive mistake is automating the wrong thing. This system answers three questions before any AI solution is scoped:

1. **Is the pain real?** (Not assumed — validated through behavioral signals)
2. **Will it deliver ROI?** (Unit economics modeled before build)
3. **Is the timing right?** (Competitive landscape mapped)

## System Architecture

```
New problem identified
        ↓
MARKET LAYER  P1→P2→P2.5  "Is this worth solving?"
        ↓ BUILD IT verdict
FINANCIAL LAYER  F1→F2→F4  "Will it make economic sense?"
        ↓ Confirmed
COMPETITIVE LAYER  C1  "How do we position against alternatives?"
        ↓
BUILD & LAUNCH  P3→P3.5→P4
        ↓
CONTINUOUS  C2 weekly radar · D1-D3 per agreement
```

## The Phase Gate System

Every phase produces a score. Below the threshold → stop and fix before proceeding.

| Phase | Gate | Kill Signal |
|-------|------|------------|
| Market P1 | Score ≥ 6.0 | No T1/T2 demand signal found |
| Market P2 | Composite ≥ 6.0 | Forced payment trigger absent |
| Market P2.5 | Score ≥ 7.0 | Any validation dimension < 5 |
| Financial F1 | LTV:CAC ≥ 3:1 | LTV:CAC < 1:1 |
| Financial F2 | Stress score ≥ 6.0 | Two+ dimensions < 4 |

## Signal Hierarchy

Evidence is weighted — not all signals are equal:

```
T1 — Behavioral proof    Job postings for manual roles, freelancer hiring,
                         internal tools built because nothing existed
T2 — Expressed pain      Reddit/HN "is there a tool for X", GitHub issues  
T3 — Market structure    Analyst reports, VC funding, review patterns
T4 — Directional only    Trend articles (never rank an opportunity on T4 alone)
```

## Repository Structure

```
├── 01-market-intelligence.md       # P1-P4 prompts
├── 02-financial-intelligence.md    # F1-F4 prompts  
├── 03-competitive-intelligence.md  # C1-C3 prompts
├── 04-deal-intelligence.md         # D1-D3 prompts
├── 05-self-intelligence.md         # Decision tracking + pattern recognition
├── 06-skills/                      # 8 Claude Skills (.skill files)
├── docs/                           # Future product architecture
├── examples/                       # Templates and profiles
├── COMPLETE-SYSTEM.md              # All 16 prompts in one document
├── MVP-ROADMAP.md                  # Evolution into a runnable dashboard
├── NEXT_STEPS.md                   # Current action plan
├── CONTRIBUTING.md                 # How to participate
└── LICENSE                         # MIT License
```

## How to Use

### Quick Start
1. Open `COMPLETE-SYSTEM.md` — all prompts are there
2. Fill the Builder Profile at the top with your context
3. Run Phase 1 on Gemini 2.5 Pro with Deep Research enabled
4. Follow the handoff blocks between phases

### Install Claude Skills
```bash
claude skills install 06-skills/market-research.skill
claude skills install 06-skills/unit-economics.skill
claude skills install 06-skills/competitive-intelligence.skill
claude skills install 06-skills/deal-analysis.skill
claude skills install 06-skills/systems-architecture.skill
claude skills install 06-skills/prompt-engineering.skill
claude skills install 06-skills/decision-quality.skill
claude skills install 06-skills/self-intelligence.skill
```

Once installed, Claude automatically applies the right methodology based on your question.

### Model Assignment
| Research phases (P1, P2, P2.5, C1, C2) | Gemini 2.5 Pro + Perplexity |
| Synthesis phases (P3, P3.5, P4, F2-F4, D1-D3) | Claude Opus 4.6 |

## The Compounding Logic

Each project cycle produces better outputs than the last — because you accumulate:

- **ICP intelligence** — which customer types actually pay
- **Channel intelligence** — which distribution channels work in your market  
- **Technical intelligence** — what you can now build that you couldn't before
- **Market intelligence** — patterns about where real demand lives

By Project 3, you're not researching blind. You're applying proprietary knowledge from three real validation cycles.

## Built With

- Prompt engineering (multi-phase pipeline architecture)
- Claude API (synthesis and analysis phases)
- Gemini 2.5 Pro (live market research phases)
- Obsidian (personal intelligence dashboard)
- Python / n8n (for project builds validated by this system)

## License

MIT — use it, fork it, improve it.

---

*"Get paid to learn, learn to build, build to found."*
