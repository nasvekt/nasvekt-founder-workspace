# NASVEKT FOUNDER OPERATING SYSTEM
## Complete Package — All Prompts, All Pipelines, All Skills

**Version:** 1.0  
**Built by:** Abdulrahman (Nassar)  
**Purpose:** A complete AI-powered intelligence system for technical founders

---

## SYSTEM OVERVIEW

```
LAYER 1 — MARKET INTELLIGENCE      6 prompts  (P1 → P2 → P2.5 → P3 → P3.5 → P4)
LAYER 2 — FINANCIAL INTELLIGENCE   4 prompts  (F1 → F2 → F3 → F4)
LAYER 3 — COMPETITIVE INTELLIGENCE 3 prompts  (C1 → C2 → C3)
LAYER 4 — DEAL INTELLIGENCE        3 prompts  (D1 → D2 → D3)
SKILLS                             8 skills   (Claude Skills format)
```

**The integrated sequence:**
```
New idea → P1→P2→P2.5 (Market) → F1→F2→F4 (Financial) → C1 (Competitive)
→ P3→P3.5 (Build) → P4 (Launch) → C2 weekly → D1-D3 per deal
```

---

# LAYER 1 — MARKET INTELLIGENCE PIPELINE

---

## PROMPT 1 — CATEGORY SCANNER
**"What sectors are worth building in right now?"**
**Run on:** Gemini 2.5 Pro Deep Research + Perplexity Pro
**Gate:** Score ≥ 6.0 to proceed

### BUILDER PROFILE (fill once, reference everywhere)
```
Today's date: [INSERT DATE]
Name: [your name]
Skills: [your technical skills]
Geography: Egypt-based. Gulf-first. US remote secondary.
Capital: Bootstrapped
Target: AI Engineer + AI Red Teamer roles
Stack: Python, n8n, Claude API, Google Sheets, Slack
Timeline: Revenue within 90 days per project
Hard constraint: Gulf or US remote paying customers only
```

### SIGNAL HIERARCHY
```
T1 — Behavioral proof: job postings, workaround spend, freelancer hiring
T2 — Expressed desperation: Reddit/HN threads, GitHub issues
T3 — Market structure: analyst reports, VC funding data
T4 — Directional only: trend articles (never rank on T4 alone)
```

### THE PROMPT
```
Today's date: [INSERT DATE]
Search window: Last 90 days ONLY. Flag anything older as [LEGACY].

You are a venture analyst and market intelligence researcher.
Scan the global market landscape and identify the highest-value
categories worth building in — ranked by real opportunity, not hype.

Do NOT answer from memory. Run at least 15 targeted web searches
across ALL dimensions before responding.

RESEARCH DIMENSIONS:
1. VC funding flow — last 60 days, by sector
2. Talent demand — job postings with highest AI engineering demand
3. Emerging categories — new in last 12-24 months, few established players
4. MENA/Gulf underserved — global solutions that ignore Arabic/local context
5. Convergence zones — two sectors merging into something bigger
6. Regulation signals — new laws creating mandatory software spending
7. Consumer behavior — Reddit complaints, Google Trends breakouts
8. Failure signals — what's been tried and failed (and what that reveals)
9. Timing asymmetry — proven demand, no dominant player yet
10. Distribution signal — how do customers discover solutions here?

FILTERS — every category must pass ALL:
- Buildable solo by AI engineer
- Real paying customers exist NOW
- Gulf or US remote market reachable
- 3-10 funded players globally (timing sweet spot)
- Clear distribution channel exists
- Some defensibility possible

OUTPUT FORMAT:

SEARCHES RAN: [list every query — minimum 15]

TOP 8 CATEGORIES RANKED:
For each:
RANK: [1-8]
CATEGORY: [specific name]
SCORE: [1-10]
CONFIDENCE: [High/Medium/Low]
MENA GAP: [Empty/Weak incumbents/Quality gap/No gap]
SIGNAL TIER: [T1/T2/T3]
MARKET SIZE: [$XB TAM — source]
CAGR: [X% — source]
FUNDED PLAYERS: [N globally]
WHY NOW: [one specific event from last 90 days]
FIRST CUSTOMER: [specific role at specific company type]
DISTRIBUTION: [named channel]
URGENCY: [Critical/High/Medium/Low]

SUMMARY:
THE ONE CATEGORY TO ENTER NOW: [with full reasoning]
THE SLEEPING GIANT: [most underrated opportunity]
BEST GULF ANGLE: [highest local opportunity, lowest local competition]
30-DAY WINDOW: [anything time-sensitive right now]

ENTRY STRATEGY FOR #1:
- First 10 customers: [where, who, how to reach]
- Week 1 actions: [specific]
- First thing to build: [one sentence]
```

**GATE CHECK:**
- [ ] Score ≥ 6.0
- [ ] At least one T1 signal confirmed
- [ ] MENA gap is not "No gap"
- [ ] Can name first customer specifically

**HANDOFF TO PROMPT 2:**
```
SECTOR: [fill]
WHY SELECTED: [1-2 sentences]
CONFIDENCE TIER: [High/Medium/Low]
MENA GAP RATING: [fill]
FUNDED PLAYERS: [N, top 3 named]
FAILURE SIGNALS: [fill]
BUILDER PROFILE: [paste from above]
```

---

## PROMPT 2 — MARKET DEEP DIVE
**"What specific gap exists inside this sector?"**
**Run on:** Gemini 2.5 Pro + Perplexity Pro
**Gate:** Composite ≥ 6.0 to proceed

### THE PROMPT
```
Today's date: [INSERT DATE]
Search window: Last 90 days ONLY.

[PASTE HANDOFF FROM PROMPT 1]

You are a deep market research analyst and startup strategist.
Find the SPECIFIC exploitable gap inside this sector.

Do NOT answer from memory. Run at least 15 web searches across
ALL dimensions before responding.

RESEARCH PASSES:

PASS A — COMPETITIVE LANDSCAPE (run first):
Map every existing solution. For each:
- Exact pricing (visit pricing pages)
- Who they actually serve (not who they claim to)
- Primary complaint pattern in G2/Capterra reviews
- What gap they leave for our ICP

PASS B — DESPERATION SIGNALS:
Search Reddit, HackerNews, LinkedIn, X, GitHub Issues for:
"I wish there was", "nobody has built", "we built internally because",
"is there a tool that", job postings for roles that shouldn't exist,
freelancers hired repeatedly for the same manual task.
Rate every signal T1/T2/T3/T4.

PASS C — FORCED PAYMENT AUDIT:
Find mandatory payment triggers:
- New regulations creating required software spending
- Operational dependencies (business fails without this)
- Platform rules forcing specific solutions
- Certification requirements mandating tools

PASS D — MENA/GULF LENS:
Does this gap exist locally? Check:
- Arabic language support in existing tools
- Gulf-specific regulations (SAMA, CBUAE, NDMO, NCA)
- Local payment infrastructure support
- Pricing accessibility for local market
- Local incumbents and their quality

OUTPUT FORMAT:

SEARCHES RAN: [list every query]

COMPETITIVE LANDSCAPE:
| Tool | Price | Target customer | Primary complaint | Gap left |
[fill table]

THE OPPORTUNITY: [one sentence, max 25 words]
GAP TYPE: [Timing/Audience/Execution/Distribution/Pricing]
GAP REASON: [specific structural reason the gap exists NOW]

ICP:
  Role: [specific job title]
  Company type: [size + sector + stage]
  Geography: [specific country/region]
  Current workaround: [what they do today]
  Workaround cost: [hours/week or $/month]

DESPERATION EVIDENCE:
[Source | Platform | Tier | What it shows]

FORCED PAYMENT TRIGGER: [specific — not vague]
FORCED PAYMENT TYPE: [Compliance/Operational/Revenue loss/Strong preference]

MENA ANGLE: [specific local gap and why it exists]

SCORES:
  Forced payment:  [/10] | Anchor: [paste anchor used]
  Desperation:     [/10] | Evidence tier: [T1/T2/T3]
  Recurrence:      [/10] | Trigger: [daily/weekly/monthly]
  Switching cost:  [/10] | Mechanism: [what creates lock-in]
  Gap clarity:     [/10] | Gap type: [named above]
  MENA fit:        [/10] | Local gap: [named above]
  Builder fit:     [/10] | Skills that apply: [named]
  COMPOSITE:       [/10]

FIRST 10 CUSTOMERS: [where to find, what to offer]
REVENUE PATH: [$10k/month = N customers at $X/month]

GATE: [PASS/FAIL] | Reason: [why composite meets 6.0 threshold]
```

**HANDOFF TO PROMPT 2.5:**
```
OPPORTUNITY: [one sentence]
SECTOR: [from Prompt 1]
COMPOSITE SCORE: [X/10]
CONFIDENCE TIER: [High/Medium/Low]
CORE CLAIMS TO VALIDATE:
  1. [most fragile assumption]
  2. [second most fragile]
  3. [most robust]
DESPERATION EVIDENCE: [source | platform | claim]
FORCED PAYMENT TRIGGER: [specific | source | date | confidence]
CUSTOMER PROFILE: [exact ICP]
GAP CLAIM: [specific structural reason]
RED FLAGS: [any filter failures]
PROCEED: [Yes / Conditional / No]
```

---

## PROMPT 2.5 — OPPORTUNITY VALIDATOR
**"Is this opportunity actually real before I build it?"**
**Run on:** Gemini 2.5 Pro + Perplexity Pro
**Gate:** Composite ≥ 7.0, zero kill thresholds to proceed

### THE PROMPT
```
Today's date: [INSERT DATE]
Search window: Last 90 days ONLY.

[PASTE HANDOFF FROM PROMPT 2]

You are an adversarial startup validator. Your job is to find
the ONE assumption most likely to be wrong — and test it first.

Do NOT be encouraging. Run at least 15 web searches.

PHASE 0 — INSTANT KILL CHECK (before searching):
  [ ] Composite from Prompt 2 ≥ 4.0?
  [ ] Forced payment trigger is specific (not vague)?
  [ ] ICP includes role + company type + geography?
  [ ] Build timeline realistic (under 8 weeks)?
  If 2+ fail → HIGH KILL PROBABILITY

FATAL FLAW IDENTIFICATION:
  Most fragile assumption: [the claim most likely to be wrong]
  Test this first. If it fails → KILL IT immediately.

VALIDATION PASSES (run in order — stop if fatal flaw fails):

PASS A — DEMAND REALITY:
  Confirm or deny desperation evidence from Prompt 2.
  Visit actual sources — do they exist? Say what was claimed?
  Find additional T1 signals: job postings, freelance work, internal tools.
  Score: [1-10] | Kill threshold: below 5

PASS B — COMPETITION AUTOPSY:
  Find every existing solution (GitHub, Product Hunt, AppSumo, G2).
  Does any solution solve this for our ICP?
  If nothing exists → search harder (why does nothing exist?).
  Score: [1-10] | Kill threshold: below 5

PASS C — WILLINGNESS TO PAY:
  What do they currently pay for adjacent solutions?
  Are they paying for something inferior right now?
  Find AppSumo deals in this category.
  Score: [1-10] | Kill threshold: below 5

PASS D — BUILD FEASIBILITY:
  Can this be built in stated timeline at stated skill level?
  Find API documentation, rate limits, pricing at scale.
  What's the hardest single technical component?
  Score: [1-10] | Kill threshold: below 5

PASS E — DISTRIBUTION:
  Confirm the named distribution channel is active and reaches ICP.
  Visit the community — engagement rate, member count, recent posts.
  Evidence of paying customer conversions from similar launches?
  Score: [1-10] | Kill threshold: below 5

PASS F — THREAT HORIZON:
  Competitor roadmap announcements?
  OpenAI/Google/Microsoft announcements in this space?
  Platform dependency risks?
  Score: [1-10] | Kill threshold: below 5

SCORES:
  Demand reality:      [/10] | Kill threshold hit: [Y/N]
  Competition map:     [/10] | Kill threshold hit: [Y/N]
  Willingness to pay:  [/10] | Kill threshold hit: [Y/N]
  Build feasibility:   [/10] | Kill threshold hit: [Y/N]
  Distribution:        [/10] | Kill threshold hit: [Y/N]
  Threat horizon:      [/10] | Kill threshold hit: [Y/N]
  COMPOSITE:           [/10]

48-HOUR TEST:
  Method: [A-Cold outreach / B-Landing page / C-Community post / D-Manual offer]
  Exact message: [write it word for word]
  Where: [specific named platform/community]
  Success signal: [specific]
  Failure signal: [specific]

VERDICT: [BUILD IT / MODIFY IT / KILL IT]
Reason: [one clear sentence]
If MODIFY IT: [exact specific change]
Next 24-hour action: [specific]
```

**HANDOFF TO PROMPT 3 (only on BUILD IT):**
```
OPPORTUNITY (validated): [one sentence]
VALIDATOR SCORE: [X/10]
VERDICT: BUILD IT
ICP: [role | company type | geography | workaround | WTP]
DISTRIBUTION: [primary named | secondary named]
FORCED PAYMENT TRIGGER: [confirmed]
MVP SCOPE: [core function | input | output | dependencies | build estimate]
COMPETITION GAP: [tools | specific gap | why you execute better]
RISKS TO DESIGN AROUND: [from Pass F]
48-HOUR TEST RESULT: [what happened]
```

---

## PROMPT 3 — PROJECT DESIGNER
**"What exactly should I build and how?"**
**Run on:** Claude Opus 4.6

### THE PROMPT
```
Today's date: [INSERT DATE]

[PASTE HANDOFF FROM PROMPT 2.5]

You are a senior AI engineer and product architect.
Design the exact project to build — in complete technical detail.
No vague answers. Every decision justified.

DESIGN ACROSS ALL DIMENSIONS:

1. PRODUCT DEFINITION
   Name, one-sentence description, core value proposition,
   what it does that nothing else does, what it replaces.

2. MVP FEATURE SET
   Every feature in v1. For each: what it does, input, output,
   why in MVP, why not deferred.
   Deliberately excluded from v1 (with reason).
   Done definition: specific functional tests.

3. TECHNICAL ARCHITECTURE
   Data flow: TRIGGER → INGESTION → VALIDATION → PROCESSING
              → STORAGE → OUTPUT → LOGGING → ERROR PATH
   Component breakdown: technology, why this not alternatives,
   input/output connections, failure mode, cost.
   Technology decisions log: chosen vs alternatives vs reason.
   Cost model at 10/100/500 users.

4. SECURITY ARCHITECTURE
   Threat model, auth design, data handling,
   input sanitization, logging hygiene.
   (Required — targeting fintech/cybersecurity employers)

5. DAY-BY-DAY BUILD PLAN
   Each day: goal, morning tasks, afternoon tasks,
   end-state deliverable, commit message, recovery protocol.
   Week 1 ends with something demonstrable.
   Week 2 includes first customer contact.

6. TEST STRATEGY
   Component test per component, integration test,
   demo test checklist (run before every customer conversation).

7. GITHUB README (actual draft copy)
   Opening hook, problem, demo GIF description,
   quickstart (4 commands), how it works, roadmap.

8. JOB APPLICATION PARAGRAPH (fill-in draft)
   Built [name], an AI-powered [category] that [outcome]
   for [ICP]. Architected with [security decision].
   Validated through [N conversations]. [Metrics].

9. MONETIZATION
   Free tier, paid tier, price, users needed for
   $100/$1k/$10k month. Payment tool.

10. RISK MAP
    Top 3 risks: description, probability, kill or slow, mitigation.
    API dependency risk (always required for AI projects).
```

**HANDOFF TO PROMPT 3.5:**
```
PRODUCT NAME: [fill]
OPPORTUNITY: [one sentence]
FULL TECH STACK: [language | automation | AI model | storage | notification | hosting]
ARCHITECTURE SUMMARY: [data flow diagram]
COMPONENT LIST: [every component + technology]
SECURITY REQUIREMENTS: [from section 4]
DAY-BY-DAY PLAN: [paste from section 5]
TEST REQUIREMENTS: [paste from section 6]
WHAT TO GENERATE: [complete file list]
KNOWN HARD PARTS: [1-2 hardest components]
```

---

## PROMPT 3.5 — BUILDER ENGINE
**"Give me the complete technical stack and build guide"**
**Run on:** Claude Opus 4.6

### THE PROMPT
```
Today's date: [INSERT DATE]
Machine: Mac (specify Apple Silicon or Intel)

[PASTE HANDOFF FROM PROMPT 3]

You are a senior AI engineer pair-programming with a junior-mid developer.
Give me the complete technical engine — every tool, command, decision.
No vague answers. One clear path. Make the decision for me.

SECTION 1 — COMPLETE TECH STACK
For every layer:
  Tool + exact version, install command, why this not alternatives,
  cost, documentation URL, where it fits in architecture.
Layers: Language, Framework, AI/LLM, Storage, Automation,
        External APIs, Alerts, Frontend (if needed), Security, Dev Environment.

SECTION 2 — FILE STRUCTURE
Every file and folder. One-sentence purpose per file.
Adapted to this specific project — nothing generic.

SECTION 3 — SETUP COMMANDS
Every terminal command in order. Copy-pasteable. Mac-compatible.
Phase 1: System prerequisites
Phase 2: Project setup + virtual environment
Phase 3: Credentials setup (before writing any code)
Phase 4: Verify everything works (test_connections.py must pass)
Makefile shortcuts: make setup, make run, make test, make clean.

SECTION 4 — DAY-BY-DAY BUILD PLAN
Each day: goal, morning tasks, afternoon tasks,
end-state deliverable, commit message, recovery protocol.
Never move to next day until end-state passes.

SECTION 5 — CODE SKELETONS
3 most critical components. Structure only — not full implementation.
Comments explain WHY the structure exists.
Security notes inline (prompt injection defense, credential handling).

SECTION 6 — LEARNING MAP
One concept per build day, specific free resource URL,
Feynman test: "I'm ready when I can explain [X] using an analogy
that has nothing to do with computers."

SECTION 7 — TEST GATES
Every component: test command, expected output, if-it-fails fixes.
Never proceed to next component until current gate passes.
Demo test checklist for customer conversations.

SECTION 8 — GITHUB SETUP
Exact commands. .gitignore contents. First commit message.
What must NEVER be committed. Pre-commit hook setup.

SECTION 9 — COST CALCULATOR
Every API cost at 10/100/500 users. Free tier ceiling.
3 specific ways to minimize costs during development.

SECTION 10 — DANGER ZONES
5 most likely blockers for this specific project.
For each: exact error message, root cause, exact fix, prevention.

SECTION 11 — DEMO ARTIFACT
Kap setup for GIF recording. Recording script (second by second).
Outreach message template (exact words).
```

**HANDOFF TO PROMPT 4:**
```
PRODUCT NAME: [fill]
GITHUB URL: [fill when created]
DEMO GIF: [recorded/pending]
LIVE URL: [fill or "local only"]
VALIDATED ICP: [role | company | geography | pain | WTP]
DISTRIBUTION: [primary named | secondary named | outreach sent]
CAREER GOAL: [Hired/Stars/Revenue]
JOB APPLICATION PARAGRAPH: [paste draft from Prompt 3]
METRICS: [stars | beta users | revenue | outreach]
WHAT PROMPT 4 MUST PRODUCE: [list]
```

---

## PROMPT 4 — POSITIONING & LAUNCH
**"How do I present this to get hired, get stars, get users?"**
**Run on:** Claude Sonnet 4.6

### THE PROMPT
```
Today's date: [INSERT DATE]

[PASTE HANDOFF FROM PROMPT 3.5]

You are a positioning strategist for both B2B and technical hiring.
Produce copy for FOUR audiences simultaneously:
  1. Companies who might hire me
  2. Companies or people who might pay for this
  3. Developers who might star it on GitHub
  4. The broader tech community

Every output is word-for-word ready to paste. No frameworks.
Actual copy that ships.

SECTION 1 — BUSINESS POSITIONING
  Business problem statement (pitch deck opening format)
  Three value propositions (one per audience — exact language)
  Business outcome numbers (quantified, sourced)
  Competitive landscape (honest comparison table)

SECTION 2 — HIRING POSITIONING
  Job application paragraph (fill-in draft, business outcome framing)
  Cold outreach sequence (3 messages, different angle each)
    Message 1: specific observation about their company
    Message 2: progress update with new evidence (Day 6)
    Message 3: clean close with real deadline (Day 14)
  Interview story (90 seconds spoken, no jargon, Situation→Problem→Built→Learned→Impact)
  Gulf vs US market differences (separate messages for each)

SECTION 3 — PRODUCT POSITIONING
  Product pitch (one paragraph, landing page ready)
  Pricing architecture (Free/Pro/Team with upgrade triggers)
  Cold sales email (subject + 4 sentences + one CTA)
  Product Hunt launch copy (tagline + first paragraph + first comment)

SECTION 4 — COMMUNITY POSITIONING
  GitHub README opening (10 lines, optimized)
  LinkedIn launch post (hook options ranked by engagement + full post)
  Technical blog post outline (Dev.to optimized)
  Twitter/X thread (6 tweets, hook through CTA)

SECTION 5 — FOUNDER LENS
  NasVekt connection (what this teaches, what it unlocks)
  3-year startup path (Year 1 beachhead / Year 2 expansion / Year 3 category)
  Skill map (what building this gives you for future projects)

SECTION 6 — 30-DAY GROWTH PLAN
  Week 1: Launch day actions hour by hour
  Week 2: Conversation and user interviews
  Week 3: Iteration signal and v1.1
  Week 4: Retrospective + next cycle prep
  Metric targets with specific numbers.

RETROSPECTIVE (run Day 30):
  Demand signal audit, distribution audit, product audit,
  positioning audit, skill audit, NasVekt intelligence,
  Prompt 1 Round 2 inputs, one-sentence upgrade.
```

---

# LAYER 2 — FINANCIAL INTELLIGENCE PIPELINE

---

## FINANCIAL VOCABULARY
```
CAC    Customer Acquisition Cost — spend to get one paying customer
LTV    Lifetime Value = (monthly price × gross margin) ÷ churn rate
LTV:CAC  The single most important number in any subscription business
         <1:1=broken, 1:3=survival, 3:1=healthy, 5:1=exceptional
Payback  CAC ÷ monthly net revenue per customer (months)
Churn    % of customers who cancel per month (<2%=excellent, >5%=broken)
NRR      Net Revenue Retention (>100%=customers expand, <100%=shrinking)
Gross margin  Revenue minus direct cost of delivering product
Default alive  Revenue growth covers costs before cash runs out
Default dead   Needs external capital to survive
Valuation      Early SaaS: 5-15× ARR | High growth: 15-40× ARR
```

## PROMPT F1 — UNIT ECONOMICS ANALYZER
**Gate:** LTV:CAC ≥ 3:1 to proceed
**Run on:** Gemini 2.5 Pro (for benchmarks) + Claude for modeling

```
BUSINESS: [describe]
PRODUCT TYPE: [SaaS/Services/Marketplace/Physical]
PRICE: [$X/month]
ACQUISITION CHANNEL: [how you get customers]

[From Market Pipeline if available]
OPPORTUNITY: [paste] | ICP: [paste] | REVENUE PATH: [paste]

WHAT YOU KNOW:
  Estimated CAC: [$X or "unknown"]
  Average contract length: [months or "unknown"]
  Churn rate: [% monthly or "unknown"]
  Gross margin: [% or "unknown"]

TASK: Model unit economics. Find what breaks first.

Step 1 — Benchmark research (5 searches):
  Average CAC, churn, gross margin for this product type in this sector.
  Label all benchmarks [ESTIMATED — source].

Step 2 — Build the model:
  CAC = channel cost × conversion rates
  LTV = (price × gross margin) ÷ churn
  Ratios: LTV:CAC, payback period, break-even customers

Step 3 — Sensitivity analysis:
  Churn 2×, CAC 2×, Price -30%, Margin -20%
  Show LTV:CAC under each scenario.

Step 4 — Verdict:
  STRONG (≥5:1) / HEALTHY (3-5:1) / MARGINAL (1-3:1) / BROKEN (<1:1)
  The number that breaks this: [single most fragile assumption]
  What must be true: [3 specific conditions]
  Gate: PASS (≥3:1) / FAIL
```

## PROMPT F2 — BUSINESS MODEL STRESS TEST
**Gate:** Composite ≥ 6.0 to proceed | **Run on:** Claude Opus 4.6

Score 8 dimensions (1-10 each, kill signal per dimension):
Distribution risk | Churn risk | Pricing risk | Platform dependency |
Competitive moat | Cash flow timing | Scalability ceiling | Founder-market fit

Composite ≥ 6.0 = PASS

## PROMPT F3 — INVESTOR READINESS (Optional)
**Run on:** Claude Opus 4.6

Score 5 criteria (weighted):
Market (30%) | Traction (25%) | Team (20%) | Business model (15%) | Defensibility (10%)

Output: Stage assessment + honest valuation range + 3 investor questions + honest answers + 90-day milestones to raise.

## PROMPT F4 — FINANCIAL DECISION BRIEF
**Run on:** Claude Opus 4.6

Verdicts: BUILD IT / BUILD WITH MODIFICATIONS / VALIDATE FIRST / RESTRUCTURE / KILL IT

Output: Verdict + 90-day financial plan + pricing decision + bootstrapping plan + NasVekt lens.

---

# LAYER 3 — COMPETITIVE INTELLIGENCE PIPELINE

## PROMPT C1 — COMPETITOR MAP (Run once per market, refresh 90 days)
**Run on:** Gemini 2.5 Pro

For each competitor (top 5): product intelligence (pricing, features, reviews),
customer intelligence (happy customers, cancellation reasons),
hiring intelligence (new roles = next product direction),
funding intelligence, strategic signals.

Output: Competitive matrix + your position (win when/lose when) + most dangerous competitor + their likely next move.

## PROMPT C2 — WEEKLY RADAR (Every Monday, 30 minutes)
**Run on:** Gemini 2.5 Pro

Scan last 7 days: news, features, pricing changes, funding, job postings.

Flag system:
🔴 CRITICAL — respond this week
🟡 WATCH — monitor, no action yet
⚪ NOISE — noted, irrelevant

Output: Brief with flagged signals + this week's one priority action.

## PROMPT C3 — THREAT ALERT (On-demand when 🔴 appears)
**Run on:** Claude Opus 4.6

Assess: threat type, timeline, severity, affected customers.
Evaluate: Accelerate / Differentiate / Ignore.
Recommend one. Give week-by-week actions + customer talking points + what NOT to do.

---

# LAYER 4 — DEAL INTELLIGENCE PIPELINE

**The 10 things to always check:**
IP ownership | Exclusivity | Payment conditions | Termination | Post-use rights |
Liability cap | Equity terms | Decision authority | Exit mechanism | Post-deal restrictions

## PROMPT D1 — DEAL ANATOMY
**Run on:** Claude Opus 4.6

Translate agreement into:
WHAT YOU GET / WHAT YOU GIVE / WHAT THEY GET / WHAT THEY GIVE
Key terms translated (one sentence each).
Power map: your leverage vs theirs.
The deal in plain English (5 sentences max, no jargon).

## PROMPT D2 — RED FLAG SCANNER
**Run on:** Claude Opus 4.6

Scan 7 categories:
IP and ownership | Exclusivity | Payment | Termination |
Equity and dilution | Liability | Structural (partnership/co-founder)

Rate each: 🔴 CRITICAL / 🟡 SERIOUS / 🟠 MINOR / ✅ CLEAN
Overall deal health: 1-10.
Recommendation: Sign / Negotiate / Walk away.

## PROMPT D3 — NEGOTIATION BRIEF
**Run on:** Claude Opus 4.6

Output:
Opening position (exact language) | Must-have changes (with talking points) |
Negotiable items (ask/accept/offer in exchange) | Walk-away line |
Opening message (exact draft) | Pushback responses (exact) |
Post-negotiation checklist.

---

# SELF INTELLIGENCE PIPELINE

## FOUR TOOLS

**Tool 1 — Decision Log**
Log: decision + context + options + reasoning + confidence + reversibility + review date.
Review (30 days): outcome + prediction accuracy + what you missed + pattern + adjustment.

**Tool 2 — Execution Pattern Scanner**
Where do you stop in the process? (Research→Planning→Starting→Building→Finishing→Shipping→Selling)
What do you do instead of the hard thing?
What drains vs. energizes?
When is your best thinking?
What is your specific planning loop signal?

**Tool 3 — Pre-Commitment Check (5 questions, 5 minutes)**
Q1: Can I describe success in one specific sentence?
Q2: Am I deciding from excitement, fear, or clarity?
Q3: Is this reversible or irreversible?
Q4: What outcome would tell me this was wrong?
Q5: Is there a 24-hour action that gives me real information?

**Tool 4 — Growth Tracker**
Format: "After [project], I can now [capability] for [customer] through [channel] — which I couldn't do before."
Track quarterly. Find what compounds.

---

# RUNNING SCHEDULE

```
WHEN STARTING A NEW PROJECT:
  Run P1 → P2 → P2.5 (Market Intelligence)
  If BUILD IT → Run F1 → F2 → F4 (Financial Intelligence)
  Run C1 once (Competitor Map)
  Run P3 → P3.5 (Design + Build)
  Run P4 (Launch)

EVERY MONDAY (30 min):
  Run C2 (Weekly Radar)

BEFORE ANY AGREEMENT:
  Run D1 → D2 → D3 (Deal Intelligence)

ON-DEMAND:
  C3 when 🔴 competitive signal appears
  Self Intelligence tools when facing significant decisions

EVERY 30 DAYS:
  Run Retrospective (from Prompt 4)
  Update Growth Tracker
  Start next cycle with upgraded inputs
```

---

# MODEL ASSIGNMENT

| Phase | Model | Reason |
|-------|-------|--------|
| P1, P2, P2.5 | Gemini 2.5 Pro + Perplexity | Live web search required |
| P3, P3.5, P4 | Claude Opus 4.6 / Sonnet 4.6 | Synthesis + generation |
| F1 (benchmarks) | Gemini 2.5 Pro | Live search for benchmarks |
| F2, F3, F4 | Claude Opus 4.6 | Modeling + analysis |
| C1, C2 | Gemini 2.5 Pro | Live search required |
| C3 | Claude Opus 4.6 | Strategic analysis |
| D1, D2, D3 | Claude Opus 4.6 | Document analysis |
| Self Intelligence | Claude Opus 4.6 | Reflection + pattern recognition |

---

# APPLICATION PARAGRAPH — KERNEL FOR AI

**For the Kernel for AI application (adapts to any AI integration/automation role):**

```
Built the NasVekt Founder Operating System — an AI-powered business 
intelligence platform that automates the validation process before 
any AI solution is built. The system runs structured multi-phase 
pipelines across market research, financial modeling, competitive 
analysis, and deal evaluation — using Gemini 2.5 Pro for live 
market intelligence and Claude API for synthesis and decision output. 
Designed with phase gates, scoring anchors, and kill thresholds that 
prevent teams from building AI solutions that don't deliver ROI. 
Architected as 16 interconnected prompts with structured handoff 
blocks, deployed as 8 Claude Skills, managed via an Obsidian vault 
with GitHub auto-backup. This is the system I use to identify which 
business problems deserve an AI solution — and the same thinking I 
would bring to every client engagement at Kernel for AI.
GitHub: [your link]
```
