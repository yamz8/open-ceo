---
description: Draft board deck sections in markdown
argument-hint: [section-name]
allowed-tools: Read, Write, Edit, AskUserQuestion, Glob
---

Draft board deck content in markdown format for a VC-backed startup.

## Available Sections

If a specific section is provided ($1), draft only that section. Otherwise, offer to draft sections in order:

1. `summary` - Executive summary (highlights, challenges, asks)
2. `metrics` - Metrics dashboard (ARR, MRR, growth, unit economics, runway)
3. `business` - Business update (progress on strategic priorities)
4. `financial` - Financial review (P&L, cash position, forecast)
5. `gtm` - Go-to-market (sales pipeline, marketing, customer success)
6. `product` - Product & engineering (releases, roadmap, tech health)
7. `team` - Team & organization (headcount, hiring, changes)
8. `strategic` - Strategic discussion (deep-dive topic)
9. `asks` - Board asks (decisions needed, introductions, help)
10. `all` - Draft complete deck outline

## Context Gathering

Before drafting any section:

1. Check for company configuration at `.claude/board-prep.local.md`
2. Ask user for current metrics and data needed for the section
3. Review any existing board materials in the project

## Section-Specific Guidance

### Executive Summary (`summary`)
Request from user:
- 3-5 key highlights from the period
- 1-2 key challenges or concerns
- Specific decisions needed from board

Draft: Concise bullets with specific metrics, not vague statements.

### Metrics Dashboard (`metrics`)
Request from user (or locate in files):
- ARR/MRR current and previous
- Growth rates (MoM, QoQ, YoY)
- Churn rates (gross and net)
- CAC and LTV figures
- Cash balance and burn rate

Draft: Dashboard format with current value, change, and trend indicator.

### Financial Review (`financial`)
Request from user:
- P&L actual vs. plan
- Significant variances to explain
- Runway scenarios

Draft: Formatted P&L table with variance analysis.

### Go-to-Market (`gtm`)
Request from user:
- Pipeline by stage
- Notable wins/losses
- Marketing performance

Draft: Pipeline table, win/loss analysis, channel performance.

### Strategic Discussion (`strategic`)
Request from user:
- Topic for deep-dive
- Options being considered
- Management recommendation

Draft: Context, options with pros/cons, recommendation, discussion questions.

## Output Format

Generate markdown formatted for easy conversion to slides:
- One main message per section
- Use tables for data
- Include placeholders for charts: `[CHART: Description]`
- Add speaker notes where helpful

## Output Location

Ask user for preferred location, default: `docs/board-deck-[date].md`

Reference the deck structure guide in the startup-board-prep skill for detailed section guidance.
