# Dashboard MVP Architecture

The dashboard version of NasVekt should work as a market opportunity engine.

```text
Founder chooses filters
  |
Market scanner runs
  |
Top gaps are ranked
  |
Founder chooses one opportunity
  |
Validation, financial, competitor, build, and launch phases run
  |
System returns verdict, numbers, evidence, and next action
```

## Core Modules

1. Market Explorer
   - Geography
   - Business category
   - Customer type
   - Date window
   - Founder goal

2. Pipeline Engine
   - Controls stage order
   - Carries handoff blocks
   - Stops progress when gates fail

3. Evidence Vault
   - Sources
   - Claims
   - Signal tiers
   - Dates
   - Confidence levels

4. Decision Engine
   - Scores
   - Gate checks
   - Kill thresholds
   - Verdicts
   - Next actions

5. Dashboard UI
   - Opportunity list
   - Stage cards
   - Evidence table
   - Financial model
   - Competitor radar
   - Launch workspace

## Suggested Stack

- Next.js and TypeScript for the dashboard
- Supabase Postgres for structured data
- Supabase Storage for source files and reports
- Trigger.dev or Inngest for long-running AI jobs
- Zod for structured output validation
- Recharts for financial and score visualizations

## MVP Rule

Start with the workflow and evidence model before building a beautiful UI. The product is valuable only if it helps a founder decide what to build, validate, modify, or kill.
