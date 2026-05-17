# NASVEKT FINANCIAL INTELLIGENCE PIPELINE
## "Does this business actually work — and what do the numbers say?"

**Pipeline structure:** 4 phases, each phase gates the next
**Run on:** Claude Opus 4.6 (all phases — this is synthesis, not live research)
**Exception:** Phase 1 uses Gemini 2.5 Pro when benchmarking real industry numbers

---

## HOW THIS DIFFERS FROM THE MARKET INTELLIGENCE PIPELINE

```
MARKET INTELLIGENCE PIPELINE         FINANCIAL INTELLIGENCE PIPELINE
"Where should I play?"               "Does this actually work as a business?"

Input: Sector or vague idea          Input: Specific business model or idea
Output: Ranked opportunities         Output: Financial verdict + decision
Research: Live web search            Research: Structured financial modeling
Kill signal: Low market demand       Kill signal: Unit economics don't work
When to run: Before choosing         When to run: Before building OR investing
Time: 90-minute research cycle       Time: 60-minute modeling cycle
```

---

## THE FOUR PHASES

```
Phase F1 — UNIT ECONOMICS ANALYZER
"Does one customer make or lose money?"

Phase F2 — BUSINESS MODEL STRESS TEST
"Does this model survive reality?"

Phase F3 — INVESTOR READINESS SCANNER
"Would a smart investor fund this?"

Phase F4 — FINANCIAL DECISION BRIEF
"What should I actually do with this information?"
```

---

## THE FINANCIAL VOCABULARY LAYER
*Read this once. Every phase assumes you know these terms.*

```
UNIT ECONOMICS — the profit or loss from a single customer
  CAC  (Customer Acquisition Cost): what you spend to get one customer
  LTV  (Lifetime Value): total revenue one customer generates before leaving
  LTV:CAC ratio: the single most important number in any SaaS business
    < 1:1   = you lose money on every customer (death)
    1:3     = break even to slight profit (survival)
    3:1     = healthy (investable)
    5:1+    = exceptional (fundable at high valuation)

MARGINS — what's left after costs
  Gross margin: revenue minus direct cost of delivering the product
    Software: 70-90% gross margin (excellent)
    Services: 20-50% gross margin (acceptable)
    Hardware: 10-40% gross margin (hard)
  Net margin: what's left after ALL costs (target: positive before scale)

BURN & RUNWAY
  Burn rate: how much cash you spend per month
  Runway: how many months until you run out of money
    = Cash in bank ÷ Monthly burn rate
  Default alive: revenue growth will cover costs before cash runs out
  Default dead: you need external capital to survive

GROWTH METRICS
  MRR (Monthly Recurring Revenue): predictable monthly revenue
  ARR (Annual Recurring Revenue): MRR × 12
  Churn rate: % of customers who cancel per month
    < 2%/month = excellent
    2-5%/month = acceptable
    > 5%/month = the bucket has a hole — fix before scaling
  NRR (Net Revenue Retention): do existing customers pay more over time?
    > 100% = existing customers expand faster than they churn (best case)
    = 100% = flat (stable)
    < 100% = shrinking base (dangerous)

VALUATION MULTIPLES (how investors price companies)
  Early SaaS: 5-15× ARR
  High-growth SaaS (>100% YoY): 15-40× ARR
  Services/agency: 1-3× annual revenue
  Marketplace: 3-8× GMV (gross merchandise value)
  What this means practically: if you're at $100k ARR,
  a buyer might pay $500k-$1.5M for a SaaS product
```

---

# PHASE F1 — UNIT ECONOMICS ANALYZER
**"Does one customer make or lose money?"**
**Run on:** Gemini 2.5 Pro (for industry benchmarks) + Claude for modeling
**Time:** 45–60 minutes
**Gate threshold:** LTV:CAC ratio ≥ 3:1 to proceed

---

## INPUT REQUIRED

Paste this block and fill it before running:

```
BUSINESS IDEA OR MODEL: [describe in 2-3 sentences]
PRODUCT TYPE: [SaaS / Services / Marketplace / Physical / Other]
TARGET CUSTOMER: [ICP from Market Pipeline if available]
PLANNED PRICE: [$X/month or $X one-time]
HOW YOU ACQUIRE CUSTOMERS: [your planned channel]

FROM MARKET PIPELINE (if run already):
  Opportunity: [paste]
  ICP: [paste]
  Revenue path stated: [paste — e.g., "$10k/month = 35 customers at $299/month"]

WHAT YOU KNOW (fill what you can, leave blank what you don't):
  Estimated CAC: [$X or "unknown"]
  Estimated average contract length: [months or "unknown"]
  Estimated churn rate: [% per month or "unknown"]
  Estimated gross margin: [% or "unknown"]
  Estimated time to first revenue: [weeks or "unknown"]
```

---

## OPERATOR IDENTITY

You are a financial analyst and early-stage investor evaluating whether this business makes money on a per-customer basis before any growth or scale is considered. Your job is not to be encouraging — it is to find the number that doesn't work and name it clearly.

You operate on one principle: **a business that loses money on every customer cannot be fixed by getting more customers. It can only be fixed by changing the model.**

Find that number first. Everything else is secondary.

---

## PHASE F1 PROMPT

```
TODAY: [INSERT DATE]
BUSINESS: [paste input block]

TASK: Model the unit economics of this specific business.
Do not be encouraging. Find what breaks first.

STEP 1 — BENCHMARK RESEARCH (run 5 web searches):
Search for:
- Average CAC for [product type] businesses in [sector]
- Average churn rate for [product type] in [sector]
- Gross margin benchmarks for [product type]
- LTV:CAC ratio benchmarks for healthy [sector] companies
- What the top 3 direct competitors charge and their reported metrics

STEP 2 — BUILD THE UNIT ECONOMICS MODEL:

Use the inputs provided. Where inputs are missing,
use industry benchmarks found in Step 1.
State clearly which numbers are provided vs. estimated.

Calculate:

CAC CALCULATION:
  Channel: [planned acquisition channel]
  Cost per click/impression/outreach: [$X]
  Conversion rate to trial: [X%]
  Conversion rate trial to paid: [X%]
  CAC = cost to acquire one paying customer: [$X]
  Label: [PROVIDED / ESTIMATED from benchmark]

LTV CALCULATION:
  Monthly price: [$X]
  Gross margin: [X%]
  Monthly revenue per customer after direct costs: [$X]
  Average customer lifetime: [1 / churn rate in months]
  LTV = monthly net revenue × average lifetime: [$X]
  Label: [PROVIDED / ESTIMATED]

KEY RATIOS:
  LTV:CAC ratio: [X:1]
  Payback period: [CAC ÷ monthly net revenue = X months]
  Break-even customers: [fixed costs ÷ monthly net revenue per customer]
  Months to $10k MRR: [calculated from growth assumptions]

STEP 3 — SENSITIVITY ANALYSIS:
What happens to LTV:CAC if:
  - Churn is 2× your estimate?
  - CAC is 2× your estimate?
  - Price is 30% lower (customer negotiates)?
  - Gross margin drops 20% (infrastructure costs)?

Show the LTV:CAC ratio under each scenario.

STEP 4 — THE VERDICT:

UNIT ECONOMICS VERDICT:
  [ ] STRONG (LTV:CAC ≥ 5:1, payback < 12 months)
  [ ] HEALTHY (LTV:CAC 3:1–5:1, payback 12–18 months)
  [ ] MARGINAL (LTV:CAC 1:1–3:1, payback 18–36 months)
  [ ] BROKEN (LTV:CAC < 1:1 — loses money per customer)

THE NUMBER THAT BREAKS THIS:
[The single assumption that, if wrong, collapses the model]

WHAT HAS TO BE TRUE FOR THIS TO WORK:
[3 specific conditions — not general, tied to this model]

GATE CHECK:
  LTV:CAC ratio: [X:1]
  Threshold: 3:1
  Result: [PASS / FAIL / MARGINAL]
  If FAIL: [specific change that fixes it — not "improve marketing"]

Return structured output matching this exact format.
```

---

## PHASE F1 OUTPUT TEMPLATE
*Fill this in Obsidian after running*

```markdown
# Phase F1 — Unit Economics
Date: [date]
Business: [name]
Status: [ ] Complete

## The Model
| Metric | Value | Source |
|--------|-------|--------|
| Monthly price | $X | PROVIDED |
| Gross margin | X% | ESTIMATED — benchmark |
| CAC | $X | ESTIMATED — benchmark |
| Monthly churn | X% | ESTIMATED — benchmark |
| Average lifetime | X months | Derived |
| LTV | $X | Calculated |
| LTV:CAC | X:1 | Calculated |
| Payback period | X months | Calculated |

## Sensitivity Table
| Scenario | LTV:CAC | Verdict |
|----------|---------|---------|
| Base case | X:1 | |
| Churn 2× | X:1 | |
| CAC 2× | X:1 | |
| Price -30% | X:1 | |
| Margin -20% | X:1 | |

## The Number That Breaks This
[fill]

## What Has To Be True
1. [fill]
2. [fill]
3. [fill]

## Gate: [ ] PASS (≥3:1) [ ] MARGINAL [ ] FAIL
Proceed to F2: [ ] Yes [ ] No — fix first: [what to fix]
```

---

# PHASE F2 — BUSINESS MODEL STRESS TEST
**"Does this model survive reality?"**
**Run on:** Claude Opus 4.6
**Prerequisite:** Phase F1 gate PASSED
**Time:** 45 minutes
**Gate threshold:** Stress test score ≥ 6/10 to proceed

---

## OPERATOR IDENTITY

You are a first-principles business analyst. You know that most businesses that fail don't fail because of bad unit economics on paper — they fail because of things nobody modeled: a distribution channel that stops working, a platform dependency that changes, a competitor that raises $10M, a customer segment that turns out not to pay.

Your job is to find those things before they happen.

---

## PHASE F2 PROMPT

```
TODAY: [INSERT DATE]

UNIT ECONOMICS FROM F1:
  LTV:CAC: [paste]
  Payback period: [paste]
  The number that breaks this: [paste]

BUSINESS MODEL: [paste F1 input block]

TASK: Stress test this business model across 8 dimensions.
Be adversarial on every dimension. Find what breaks.

DIMENSION 1 — DISTRIBUTION RISK
  Current plan: [planned channel]
  Questions to answer:
  - What happens if this channel stops working tomorrow?
    (Platform algorithm change, price increase, saturation)
  - How many months does it take to switch channels?
  - Is there a second channel already proven?
  Score this dimension: [1-10]
  Kill signal: [what would kill this dimension]

DIMENSION 2 — CHURN RISK
  Assumed churn: [from F1]
  Questions to answer:
  - Why would a customer cancel after month 3?
  - Is there a natural "job done" moment where they no longer need this?
  - What does the best competitor offer that would make someone switch?
  - What is the switching cost — really?
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 3 — PRICING RISK
  Current price: [from F1]
  Questions to answer:
  - What happens when a competitor enters at 50% lower price?
  - Is this price defensible or is it only possible because
    no one else has built this yet?
  - What is the customer's next-best alternative and what does it cost?
  - Will the price need to drop to acquire the next 100 customers
    after the easy early adopters are gone?
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 4 — PLATFORM/DEPENDENCY RISK
  Dependencies: [APIs, platforms, suppliers this relies on]
  Questions to answer:
  - What happens if [dependency] changes its pricing or terms?
  - What happens if [API/platform] shuts down or blocks access?
  - How long to rebuild if the core dependency is removed?
  - Is there a single point of failure in the technical stack?
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 5 — COMPETITIVE MOAT
  Questions to answer:
  - What stops a well-funded team from copying this in 90 days?
  - Does the moat strengthen over time or weaken?
  - What would the moat look like after 100 customers?
    After 1,000 customers?
  - Is the moat data, network effects, switching costs,
    regulation, or just timing? (Timing is the weakest)
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 6 — CASH FLOW TIMING
  Questions to answer:
  - When does the first dollar come in?
  - Is there a gap between delivering value and getting paid?
    (Services businesses often deliver for 30-60 days before invoice)
  - Can this business be bootstrapped to $10k MRR
    without external capital?
  - At what MRR does this become default alive?
    (Revenue covers all costs including founder salary)
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 7 — SCALABILITY CEILING
  Questions to answer:
  - What breaks first when this goes from 10 to 100 customers?
  - Is growth linear (each customer requires same effort)
    or exponential (systems improve with scale)?
  - What is the first hire that becomes necessary and at what revenue?
  - Is there a ceiling on how big this can get
    given the ICP size and market?
  Score: [1-10]
  Kill signal: [what would kill this]

DIMENSION 8 — FOUNDER-MARKET FIT
  Questions to answer:
  - Does the builder understand this customer's world deeply enough
    to know what they actually need vs. what they say they need?
  - Is there a personal unfair advantage (access, domain knowledge,
    relationships, language, geography) that a well-funded
    outsider couldn't replicate quickly?
  - What happens when the first big customer asks for a custom feature
    that breaks the product for everyone else?
  Score: [1-10]
  Kill signal: [what would kill this]

STRESS TEST COMPOSITE SCORE: [average of 8 dimensions]

THE TWO DIMENSIONS MOST LIKELY TO KILL THIS:
  1. [dimension] — [specific reason]
  2. [dimension] — [specific reason]

WHAT THE MODEL NEEDS TO SURVIVE:
  [3 specific structural changes or confirmations
   that would move the weakest dimensions above 6/10]

GATE CHECK:
  Composite: [X/10]
  Threshold: 6.0
  Result: [PASS / FAIL]
  If FAIL: [which 2 dimensions to fix and how specifically]
```

---

## PHASE F2 OUTPUT TEMPLATE

```markdown
# Phase F2 — Business Model Stress Test
Date: [date]
Status: [ ] Complete

## Dimension Scores
| Dimension | Score | Kill Signal |
|-----------|-------|-------------|
| Distribution | /10 | [fill] |
| Churn | /10 | [fill] |
| Pricing | /10 | [fill] |
| Platform/Dependency | /10 | [fill] |
| Competitive Moat | /10 | [fill] |
| Cash Flow Timing | /10 | [fill] |
| Scalability | /10 | [fill] |
| Founder-Market Fit | /10 | [fill] |
| **COMPOSITE** | **/10** | |

## Two Dimensions Most Likely to Kill This
1. [fill]
2. [fill]

## What the Model Needs to Survive
1. [fill]
2. [fill]
3. [fill]

## Gate: [ ] PASS (≥6.0) [ ] FAIL
Proceed to F3: [ ] Yes [ ] No — fix first: [what]
```

---

# PHASE F3 — INVESTOR READINESS SCANNER
**"Would a smart investor fund this — and at what stage?"**
**Run on:** Claude Opus 4.6
**Prerequisite:** Phase F2 gate PASSED
**Time:** 30–45 minutes
**Note:** This phase is optional if your goal is bootstrapping only.
         Run it if: raising capital, pitching an accelerator,
         or wanting to understand what investors see when they look at you.

---

## OPERATOR IDENTITY

You are a pre-seed investor who has seen 500 pitches. You know that founders always think their business is worth more than it is and more ready than it is. Your job is to evaluate this business the way a skeptical but fair investor would — not to discourage, but to give the founder the exact feedback they would receive in a real pitch meeting, before they're in one.

The goal is not to get a yes from you. The goal is to know what a real investor would say.

---

## PHASE F3 PROMPT

```
TODAY: [INSERT DATE]
BUSINESS: [paste input block]
F1 UNIT ECONOMICS: [paste key numbers]
F2 STRESS TEST: [paste composite score + two kill dimensions]

TASK: Evaluate this business as a pre-seed investor would.
Answer every dimension the way a real investor thinks —
not the way the founder hopes.

INVESTOR EVALUATION FRAMEWORK:

CRITERION 1 — THE MARKET (30% of decision)
  What investors want: large, fast-growing, and the timing is NOW
  Questions:
  - Is the TAM genuinely large (>$1B) or are we counting
    the global market that this business will never reach?
  - Is growth driven by a real structural shift or a trend
    that could reverse?
  - Why is now the right time — what changed in the last
    12-24 months that makes this possible?
  Score: [1-10] | Investor reaction: [what they'd say]

CRITERION 2 — THE TRACTION (25% of decision)
  What investors want: evidence that customers pay and stay
  Questions:
  - What is the current MRR/ARR and growth rate?
  - What is the churn rate and NRR?
  - Is there a single customer who would be devastated
    if this product disappeared tomorrow?
  - What does the most recent customer acquisition look like —
    paid or organic? How hard was it?
  Score: [1-10] | Investor reaction: [what they'd say]

CRITERION 3 — THE TEAM (20% of decision)
  What investors want: founders who understand the problem
    better than anyone and can execute without being managed
  Questions:
  - What is the unfair insight this founder has that
    nobody else sees yet?
  - What is the evidence of execution — have they shipped?
  - What's the weakest link in the founding team
    and how does it get filled?
  Score: [1-10] | Investor reaction: [what they'd say]

CRITERION 4 — THE BUSINESS MODEL (15% of decision)
  What investors want: unit economics that get better with scale
  Questions:
  - Does CAC decrease as the company grows?
    (Content moat, word of mouth, brand — all reduce CAC over time)
  - Does LTV increase as the company grows?
    (More features, more integrations, expansion revenue)
  - Is there a natural path to 70%+ gross margins?
  From F1: LTV:CAC [X:1] | Assessment: [what investors see]
  Score: [1-10] | Investor reaction: [what they'd say]

CRITERION 5 — THE DEFENSIBILITY (10% of decision)
  What investors want: something that gets harder to compete
    with over time — not just a good idea anyone can copy
  From F2 moat score: [X/10]
  Questions:
  - What does the moat look like in 24 months?
  - Is there a data flywheel, network effect, or
    regulatory barrier that strengthens over time?
  Score: [1-10] | Investor reaction: [what they'd say]

INVESTOR READINESS COMPOSITE: [weighted average]

STAGE ASSESSMENT:
  [ ] Not yet fundable — needs [specific milestone first]
  [ ] Pre-seed ready ($50k-$500k) — what thesis this fits
  [ ] Seed ready ($500k-$2M) — what metrics are needed
  [ ] Series A ready ($2M+) — what the business looks like at this stage

VALUATION RANGE (honest):
  Pre-revenue: [methodology + range]
  At $10k MRR: [multiple + range]
  At $100k MRR: [multiple + range]

THE PITCH IN ONE MINUTE:
  Write the pitch this founder should give —
  not the pitch they want to give.
  The version that would make an investor lean forward.

THE THREE QUESTIONS AN INVESTOR WILL ASK:
  And how to answer each one honestly.
  1. [question] → [honest answer]
  2. [question] → [honest answer]
  3. [question] → [honest answer]

WHAT NEEDS TO BE TRUE IN 90 DAYS TO RAISE:
  [3 specific milestones — not "get more customers"
   — specific numbers and types of evidence]
```

---

## PHASE F3 OUTPUT TEMPLATE

```markdown
# Phase F3 — Investor Readiness
Date: [date]
Status: [ ] Complete

## Investor Scorecard
| Criterion | Weight | Score | Investor Reaction |
|-----------|--------|-------|------------------|
| Market | 30% | /10 | [fill] |
| Traction | 25% | /10 | [fill] |
| Team | 20% | /10 | [fill] |
| Business Model | 15% | /10 | [fill] |
| Defensibility | 10% | /10 | [fill] |
| **WEIGHTED COMPOSITE** | 100% | **/10** | |

## Stage Assessment
[ ] Not yet fundable — needs: [fill]
[ ] Pre-seed ready
[ ] Seed ready
[ ] Series A ready

## Valuation Range
At current stage: $[X]–$[Y]
At $10k MRR: $[X]–$[Y]

## The Pitch (honest version)
[fill]

## Three Investor Questions + Honest Answers
1. Q: [fill] → A: [fill]
2. Q: [fill] → A: [fill]
3. Q: [fill] → A: [fill]

## 90-Day Milestones to Raise
1. [specific milestone]
2. [specific milestone]
3. [specific milestone]
```

---

# PHASE F4 — FINANCIAL DECISION BRIEF
**"What should I actually do with this information?"**
**Run on:** Claude Opus 4.6
**Prerequisite:** F1 + F2 complete (F3 optional)
**Time:** 20 minutes
**Output:** One clear decision + execution steps

---

## OPERATOR IDENTITY

You are a trusted advisor — not a consultant who hedges, not an investor who wants equity, not a friend who encourages blindly. You have seen the full financial picture of this business across three phases. Your job is to give one clear recommendation and the specific steps to execute it.

The founder has already done the analysis. They don't need more analysis. They need a decision.

---

## PHASE F4 PROMPT

```
TODAY: [INSERT DATE]

FINANCIAL PICTURE SUMMARY:
  Business: [paste]
  F1 — Unit economics: LTV:CAC [X:1], payback [X months]
       The number that breaks this: [paste]
  F2 — Stress test score: [X/10]
       Two kill dimensions: [paste]
  F3 — Investor readiness: [X/10] (skip if not run)
       Stage: [paste]

TASK: Deliver the financial decision brief.
One recommendation. Specific steps. No hedging.

THE VERDICT:
  Choose exactly one:
  [ ] BUILD IT — unit economics work, model survives stress test,
      proceed with confidence
  [ ] BUILD IT WITH MODIFICATIONS — viable but needs specific
      structural changes before scaling
  [ ] VALIDATE FIRST — unit economics look good on paper but
      one critical assumption is unproven — run this test first
  [ ] RESTRUCTURE THE MODEL — current model doesn't work,
      but the idea has merit — here's the different model
  [ ] KILL IT — the numbers don't work and the fixes aren't
      realistic at this stage

THE REASONING (3 sentences maximum):
[Why this verdict, tied to the specific numbers]

IF BUILD IT or BUILD IT WITH MODIFICATIONS:
  THE 90-DAY FINANCIAL PLAN:
    Month 1 target: [$X MRR from N customers]
    Month 2 target: [$X MRR — what changes]
    Month 3 target: [$X MRR — what changes]
    The metric to watch daily: [one number]
    The alert threshold: [if this number drops below X, something is wrong]

  THE PRICING DECISION:
    Recommended price: [$X/month]
    Why not lower: [specific reason]
    Why not higher: [specific reason]
    When to raise prices: [specific trigger]

  THE BOOTSTRAPPING PLAN:
    Months to default alive: [X months at current burn]
    Cash needed before first revenue: [$X]
    First revenue milestone: [$X from N customers by date]
    Point of no return: [if you haven't reached $X by date,
                         reassess the model]

IF VALIDATE FIRST:
  THE ONE TEST TO RUN:
    What to test: [the single most critical unproven assumption]
    How to test it: [specific method — not "do more research"]
    Timeline: [X days]
    Success signal: [what counts as validation]
    Failure signal: [what means kill it]
    Cost of test: [$X or free]

IF RESTRUCTURE:
  THE DIFFERENT MODEL:
    Current model problem: [specific financial flaw]
    Alternative model: [describe the restructured version]
    Why it works better: [specific financial improvement]
    What to keep from current model: [what transfers]
    What to discard: [what changes]

IF KILL IT:
  WHAT WAS LEARNED:
    [What the financial analysis revealed that wasn't obvious before]
  WHAT TO LOOK FOR INSTEAD:
    [Specific financial characteristics to target in the next idea —
     derived from what failed here]
  RETURN TO:
    Market Intelligence Pipeline → Phase 1 with this financial lens added

THE NASVEKT LENS:
  How does this financial picture affect the NasVekt holding company?
  - Is this a business NasVekt builds and owns?
  - Is this a business NasVekt acquires later when it's proven?
  - Is this a feature of a larger platform, not a standalone business?
  - What does this business teach you about the next one?
```

---

## PHASE F4 OUTPUT TEMPLATE

```markdown
# Phase F4 — Financial Decision Brief
Date: [date]
Status: [ ] Complete

## THE VERDICT
[ ] BUILD IT
[ ] BUILD IT WITH MODIFICATIONS
[ ] VALIDATE FIRST
[ ] RESTRUCTURE THE MODEL
[ ] KILL IT

**Reasoning:** [3 sentences max]

## 90-Day Financial Plan (if building)
| Month | MRR Target | Key Action | Watch Metric |
|-------|-----------|------------|--------------|
| 1 | $X | [fill] | [fill] |
| 2 | $X | [fill] | [fill] |
| 3 | $X | [fill] | [fill] |

Alert threshold: If [metric] drops below [X], reassess.

## Pricing Decision
Recommended: $[X]/month
Not lower because: [fill]
Not higher because: [fill]
Raise price when: [fill]

## The NasVekt Lens
[fill — how this feeds the holding company architecture]
```

---

## HOW THIS PIPELINE CONNECTS TO THE MARKET INTELLIGENCE PIPELINE

```
MARKET INTELLIGENCE PIPELINE OUTPUT
         ↓
  Validated opportunity with:
  - ICP confirmed
  - Revenue path stated ($10k/month = N customers at $X)
  - Forced payment trigger confirmed
         ↓
FINANCIAL INTELLIGENCE PIPELINE INPUT
  Phase F1 takes: the ICP, the price point, the channel
  and builds the unit economics model around them

The two pipelines are designed to run in sequence:
Market Pipeline → finds the opportunity
Financial Pipeline → confirms the numbers work

If Financial Pipeline kills what Market Pipeline found:
  Return to Market Pipeline Phase 2 with a narrowed ICP
  or different pricing model — not Phase 1 from scratch.
  The sector is still valid. The specific model needs adjustment.
```

---

## OBSIDIAN VAULT ADDITIONS

Add these files to your NasVekt-Pipeline vault:

```
NasVekt-Pipeline/
├── 00-SYSTEM/
│   ├── Financial-Vocabulary.md    ← paste the vocabulary layer above
│   └── Prompts/
│       ├── Prompt-F1-Unit-Economics.md
│       ├── Prompt-F2-Stress-Test.md
│       ├── Prompt-F3-Investor-Readiness.md
│       └── Prompt-F4-Decision-Brief.md
│
└── 01-PROJECTS/
    └── Project-001/
        ├── F1-Unit-Economics.md
        ├── F2-Stress-Test.md
        ├── F3-Investor-Readiness.md
        └── F4-Decision-Brief.md
```

---

## THE COMPLETE NASVEKT OPERATING SYSTEM — UPDATED

```
INTELLIGENCE LAYER 1 — MARKET (built ✓)
  Where to play? What to build?
  Pipeline: P1 → P2 → P2.5 → P3 → P3.5 → P4

INTELLIGENCE LAYER 2 — FINANCIAL (built ✓)
  Do the numbers actually work?
  Pipeline: F1 → F2 → F3 → F4

INTELLIGENCE LAYER 3 — COMPETITIVE (next)
  What are my competitors doing right now?
  Pipeline: C1 (competitor map) → C2 (weekly scanner) → C3 (threat alert)

INTELLIGENCE LAYER 4 — DEAL (future)
  Is this agreement structured in my favor?
  Pipeline: D1 (deal anatomy) → D2 (red flag scanner) → D3 (negotiation brief)

INTELLIGENCE LAYER 5 — SELF (always running)
  Am I making decisions from clarity or fear?
  Tool: Decision log + pre-mortem protocol + energy map
```

---

## HOW TO RUN THE FINANCIAL PIPELINE IN PRACTICE

**Use case 1 — Before starting a new project:**
Take the validated opportunity from the Market Pipeline.
Run F1 to confirm the unit economics before writing code.
If F1 fails → modify the pricing or ICP, not the sector.

**Use case 2 — Evaluating any business you see:**
Read an Indie Hackers post about someone making $15k MRR.
Run F2 stress test on their model.
Ask: would this work if I built it in my market?
This builds financial pattern recognition fast.

**Use case 3 — Before any investor conversation:**
Run F3 on your current business state — honest numbers.
The three questions an investor will ask = your prep material.
Never go into a pitch without running F3 first.

**Use case 4 — When something feels off about a business:**
A client wants to pay you in equity. A partner proposes a split.
A deal sounds good but your gut says something is wrong.
Run F2 on the deal structure. The dimension that scores lowest
is what your gut was detecting.

---

## SCORING ANCHORS — FINANCIAL PIPELINE

```
UNIT ECONOMICS (F1)
  LTV:CAC ≥ 5:1    → STRONG (score 9-10)
  LTV:CAC 3:1–5:1  → HEALTHY (score 7-8)
  LTV:CAC 1:1–3:1  → MARGINAL (score 5-6)
  LTV:CAC < 1:1    → BROKEN (score 1-4)

STRESS TEST DIMENSIONS (F2)
  Score 9-10: No realistic scenario breaks this dimension
  Score 7-8: One scenario breaks it but has a clear fix
  Score 5-6: Significant risk, requires monitoring
  Score 3-4: High probability of breaking — needs structural change
  Score 1-2: Will break — not a risk, a certainty

INVESTOR READINESS (F3)
  Score 9-10: Investors compete to fund this
  Score 7-8: Strong interest, term sheet possible
  Score 5-6: Interest but needs one more milestone
  Score 3-4: Too early — specific milestone needed first
  Score 1-2: Not fundable at this stage
```
