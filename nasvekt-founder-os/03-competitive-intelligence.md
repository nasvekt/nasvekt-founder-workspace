# NASVEKT COMPETITIVE INTELLIGENCE PIPELINE
## "What are my competitors doing right now — before they do it to me?"

**Nature:** Continuous — runs weekly while you operate
**Run on:** Gemini 2.5 Pro + Perplexity (live search required)
**Trigger:** Every Monday morning, 30 minutes
**Output:** Weekly competitor brief + alert flags

---

## HOW THIS DIFFERS FROM MARKET INTELLIGENCE

```
MARKET INTELLIGENCE PIPELINE        COMPETITIVE INTELLIGENCE PIPELINE
Runs once before you build           Runs every week while you operate
"What sectors are worth building?"   "What are my specific competitors doing?"
Broad market scan                    Narrow competitor surveillance
Output: opportunity to pursue        Output: moves to respond to
Looks at the whole market            Looks at named companies only
```

---

## THE THREE PHASES

```
Phase C1 — COMPETITOR MAP
"Who exactly am I competing with and what are their positions?"
Run once when you enter a market. Update every 90 days.

Phase C2 — WEEKLY RADAR
"What did my competitors do in the last 7 days?"
Run every Monday. Takes 30 minutes.

Phase C3 — THREAT ALERT
"Is something happening that requires an immediate response?"
Run when C2 flags a critical signal. On-demand.
```

---

# PHASE C1 — COMPETITOR MAP
**"Who exactly am I competing with and what are their real positions?"**
**Run:** Once when entering a market. Refresh every 90 days.
**Run on:** Gemini 2.5 Pro Deep Research
**Time:** 60–90 minutes
**Output:** Complete competitor intelligence dossier

---

## INPUT REQUIRED

```
YOUR PRODUCT/OPPORTUNITY: [one sentence from Market Pipeline P2]
YOUR ICP: [from Market Pipeline P2]
YOUR GEOGRAPHY: Gulf-first, US remote secondary
YOUR PRICE POINT: [$X/month — from Financial Pipeline F4]
YOUR CORE DIFFERENTIATOR: [what you do that they don't]

COMPETITORS TO MAP: [list any you already know — leave blank
                     for full discovery]
```

---

## OPERATOR IDENTITY

You are a competitive intelligence analyst embedded in a startup.
Your job is not to find out that competitors exist — the founder already knows that. Your job is to find out what they are **actually doing** versus what they say they are doing, where their customers are unhappy, where their product is weak, and what they are building next based on observable signals.

Everything you find must be observable — job postings, GitHub commits, pricing page changes, review patterns, hiring patterns, content output. No speculation. Only signals.

---

## PHASE C1 PROMPT

```
TODAY: [INSERT DATE]
MY PRODUCT: [paste input block]

TASK: Build a complete competitor intelligence map.
Run minimum 12 web searches. Every claim must have a source.

FOR EACH COMPETITOR FOUND (aim for top 5):

SEARCH DIMENSIONS:

1. PRODUCT INTELLIGENCE
   - Current pricing page (screenshot or exact prices)
   - Features listed vs. features users actually use
     (check G2/Capterra reviews for "I don't use X feature")
   - Recent product changelog or release notes
   - What their free tier includes vs. paid
   - What their reviews say they're missing

2. CUSTOMER INTELLIGENCE
   - Who their happiest customers are
     (look at case studies, testimonials, LinkedIn mentions)
   - Who their unhappiest customers are
     (1-3 star G2/Capterra reviews in last 90 days)
   - What customers say when they cancel
     (search "[competitor] alternatives" and "[competitor] vs"
      — cancellation reasons appear in comparison searches)
   - Which customer segments they're losing

3. GROWTH INTELLIGENCE
   - Estimated traffic (use SimilarWeb estimates or
     SEO tools if available)
   - Their content strategy — what keywords they target
   - Their distribution channels (where they acquire customers)
   - Their partnership announcements in last 90 days

4. HIRING INTELLIGENCE (strongest signal of future direction)
   Search LinkedIn Jobs and their careers page for:
   - New roles posted in last 30 days
   - Which departments are they hiring in?
     (Engineering = building features,
      Sales = going upmarket,
      Marketing = scaling acquisition,
      Customer Success = fixing churn,
      Partnerships = channel strategy)
   - What skills appear in their engineering job postings?
     (New tech stack = new product direction)

5. FUNDING INTELLIGENCE
   - Last funding round (Crunchbase)
   - Total raised to date
   - Investors (tell you the strategic direction — YC vs.
     enterprise VC vs. strategic investor = different paths)
   - Burn rate estimate if public

6. STRATEGIC SIGNALS
   - Any acquisitions or partnership announcements
   - Any pricing changes in last 90 days
   - Any new market or geography expansion
   - Any rebrand or messaging shift
   - Key executives who joined or left

OUTPUT FORMAT — for each competitor:

COMPETITOR: [name]
WEBSITE: [URL]
FOUNDED: [year]
TOTAL RAISED: [$X]
LAST ROUND: [$X, date, stage]

PRODUCT POSITION:
  Price: [$X/month for what]
  Target customer: [who they actually serve]
  Core strength: [what they do better than anyone]
  Core weakness: [what their customers consistently complain about]
  Free tier: [yes/no — what's included]

CUSTOMER SENTIMENT (from reviews):
  Average rating: [X/5 on G2 or Capterra]
  Most common praise: [what happy customers say]
  Most common complaint: [pattern in negative reviews]
  Cancellation reason: [why people leave]

GROWTH SIGNALS:
  Estimated monthly traffic: [X visitors]
  Primary acquisition channel: [SEO / paid / community / sales]
  Content focus: [what topics they publish about]

HIRING SIGNALS (last 30 days):
  Roles posted: [list]
  What this signals: [your interpretation]

STRATEGIC SIGNALS (last 90 days):
  [Any significant moves — funding, partnerships, pivots, pricing]

YOUR OPPORTUNITY AGAINST THEM:
  Where their weakness creates your opening: [specific]
  Which of their unhappy customers match your ICP: [specific]
  What you can say that they can't: [specific positioning claim]

---

COMPETITIVE MATRIX (after all competitors mapped):

| Dimension          | You | Comp 1 | Comp 2 | Comp 3 |
|--------------------|-----|--------|--------|--------|
| Price              |     |        |        |        |
| Target customer    |     |        |        |        |
| Gulf/MENA support  |     |        |        |        |
| Arabic language    |     |        |        |        |
| Setup complexity   |     |        |        |        |
| AI-native          |     |        |        |        |
| Open source option |     |        |        |        |

YOUR COMPETITIVE POSITION:
  You win when: [specific scenario]
  You lose when: [specific scenario]
  Your defensible angle: [the one thing they can't easily copy]

THE MOST DANGEROUS COMPETITOR:
  [Name] — because [specific reason tied to your model]
  Their most likely move in next 90 days: [based on hiring signals]
  How to prepare: [specific action]

THE WEAKEST COMPETITOR:
  [Name] — their customers are most likely to switch to you because:
  [specific complaint pattern that you solve]
```

---

## PHASE C1 OUTPUT TEMPLATE

```markdown
# Phase C1 — Competitor Map
Date: [date] | Refresh due: [date + 90 days]
My product: [name]

## Competitor Dossiers
[paste structured output for each competitor]

## Competitive Matrix
[paste matrix]

## My Position
Win when: [fill]
Lose when: [fill]
Defensible angle: [fill]

## Most Dangerous: [name]
Their next move: [fill]
My preparation: [fill]

## Weakest (best acquisition target): [name]
Why their customers will switch: [fill]
```

---

# PHASE C2 — WEEKLY RADAR
**"What did my competitors do in the last 7 days?"**
**Run:** Every Monday morning
**Run on:** Gemini 2.5 Pro + Perplexity
**Time:** 30 minutes maximum
**Output:** Weekly brief + flag any critical signals

---

## OPERATOR IDENTITY

You are a reconnaissance analyst giving a Monday morning briefing. Fast, specific, actionable. No background context — the founder already has the competitor map from C1. This is the update layer only. What changed in the last 7 days. What requires a response. What can be ignored.

---

## PHASE C2 PROMPT

```
TODAY: [INSERT DATE — Monday]
LAST WEEK: [INSERT DATE — previous Monday]
MY COMPETITORS: [list from C1 — names only]
MY PRODUCT: [one sentence]

TASK: Scan for competitor activity in the last 7 days only.
Run 8 targeted searches. Fast and specific.

SEARCH FOR EACH COMPETITOR:
  - "[competitor name]" site:twitter.com last week
  - "[competitor name]" new feature OR update OR launch
  - "[competitor name]" pricing OR plan change
  - "[competitor name]" funding OR raised OR investment
  - "[competitor name]" partnership OR integration
  - Google Alerts equivalent: any news in last 7 days

FLAG SYSTEM — rate every signal:
  🔴 CRITICAL — requires response this week
       (competitor launched feature that directly competes with
        your core value prop, major funding announced,
        pricing dropped to undercut you)
  🟡 WATCH — monitor but no action yet
       (new hire in a relevant area, content shift,
        new integration announced)
  ⚪ NOISE — noted, irrelevant
       (general company news, unrelated features)

WEEKLY BRIEF FORMAT:

WEEK OF: [date]

COMPETITOR UPDATES:
  [Competitor 1]:
    Signal: [what happened]
    Flag: 🔴 / 🟡 / ⚪
    What it means: [one sentence]
    Response needed: [yes/no — if yes, what]

  [Competitor 2]: [same format]
  [Competitor 3]: [same format]

MARKET SIGNALS (anything affecting the whole category):
  [New entrant, regulation change, platform update
   that affects all players]
  Flag: 🔴 / 🟡 / ⚪

THIS WEEK'S PRIORITY:
  [The one thing from this scan that requires action]
  Action: [exactly what to do]
  By when: [Friday of this week]

NOTHING TO WORRY ABOUT:
  [What looks significant but isn't — and why]
```

---

## PHASE C2 OUTPUT TEMPLATE

```markdown
# Weekly Radar — [Date]
Time to run: 30 min | Next radar: [next Monday]

## Competitor Updates
| Competitor | Signal | Flag | Action needed |
|------------|--------|------|---------------|
| [name] | [what] | 🔴/🟡/⚪ | [yes/no] |

## This Week's Priority
[fill — one action, one deadline]

## Noise (ignored)
[fill — what you deliberately decided to ignore]
```

---

# PHASE C3 — THREAT ALERT
**"A competitor just made a major move — how do I respond?"**
**Run:** On-demand when C2 flags a 🔴 CRITICAL signal
**Run on:** Claude Opus 4.6
**Time:** 45 minutes
**Output:** Specific response strategy

---

## PHASE C3 PROMPT

```
TODAY: [INSERT DATE]
THE THREAT: [describe exactly what the competitor did]
MY CURRENT POSITION: [one sentence on where you are]
MY RESOURCES: [time available, capital available]

TASK: Design a specific response to this competitive threat.

THREAT ASSESSMENT:
  Type: [Feature parity / Price undercut / New entrant /
         Funding event / Market expansion / Customer poaching]
  Timeline: [How long until this threatens your customers?]
  Severity: [Existential / Serious / Manageable / Overstated]
  Affected customers: [which of your ICP segments are most at risk]

RESPONSE OPTIONS (evaluate all three, recommend one):

OPTION 1 — ACCELERATE:
  What: [what to build or ship faster in response]
  Cost: [time and money]
  Risk: [what could go wrong]
  Best if: [when this is the right choice]

OPTION 2 — DIFFERENTIATE:
  What: [how to make the comparison irrelevant]
  Cost: [time and money]
  Risk: [what could go wrong]
  Best if: [when this is the right choice]

OPTION 3 — IGNORE:
  Reasoning: [why this threat is actually less serious than it appears]
  Risk: [what happens if you're wrong]
  Best if: [when ignoring is actually the smart move]

RECOMMENDED RESPONSE: [Option 1/2/3]
Why: [specific reasoning tied to your position and resources]

THIS WEEK'S ACTIONS:
  Day 1-2: [specific action]
  Day 3-5: [specific action]
  By end of week: [what should be different]

WHAT TO TELL YOUR CUSTOMERS:
  [If existing customers ask about the competitor's move —
   exact talking points. Honest, not defensive.]

WHAT NOT TO DO:
  [The reactive move that feels right but is wrong]
```

---

## PHASE C3 OUTPUT TEMPLATE

```markdown
# Threat Alert — [Date]
Threat: [competitor] did [what]
Severity: Existential / Serious / Manageable / Overstated

## Assessment
Type: [fill]
Timeline to impact: [fill]
Customers at risk: [fill]

## Recommended Response
Option chosen: [1/2/3 — name]
Reasoning: [fill]

## This Week
Day 1-2: [fill]
Day 3-5: [fill]
End of week: [fill]

## Customer Talking Points
[fill]

## What NOT to do
[fill]
```

---

## RUNNING SCHEDULE

```
WEEKLY (every Monday, 30 min):
  Run Phase C2 — Weekly Radar
  Flag any 🔴 signals

QUARTERLY (every 90 days, 90 min):
  Refresh Phase C1 — Competitor Map
  Update the competitive matrix
  Add any new entrants discovered in weekly radars

ON-DEMAND (when 🔴 flag appears):
  Run Phase C3 — Threat Alert
  Within 24 hours of the signal appearing

FIRST TIME IN A NEW MARKET:
  Run Phase C1 first
  Then start weekly C2 cadence
```
