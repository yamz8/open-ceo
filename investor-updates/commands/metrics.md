---
description: Generate a metrics snapshot for investor updates
allowed-tools: Read, Write, AskUserQuestion
---

Generate a concise metrics snapshot suitable for monthly investor updates.

## Purpose

Create a lightweight metrics summary that gives investors a quick pulse on business health without overwhelming them with data.

## Context Gathering

1. Check for company configuration at `.claude/board-prep.local.md`
2. Look for any existing metrics data in the project
3. Ask user for current metrics if not available

## Metrics to Include

Focus on these key metrics (lighter than full board reporting):

### Required Metrics
| Metric | What to Show |
|--------|--------------|
| ARR or MRR | Current value + MoM change |
| Growth | MoM growth rate |
| Runway | Months remaining |

### Optional Metrics (include 1-2 if notable)
- Net Revenue Retention (if strong)
- New customers this month
- Key product metric (DAU, usage, etc.)
- Cash balance (if raising or notable change)

## Format Options

Generate the snapshot in a format suitable for embedding in an email:

### Inline Format (default)
```
📊 Quick Numbers
• ARR: $2.4M (+12% MoM)
• Runway: 16 months
• New customers: 8 (+3 from last month)
```

### Table Format
```
| Metric | Current | Change |
|--------|---------|--------|
| ARR | $2.4M | +12% MoM |
| MRR | $200K | +$22K |
| Runway | 16 mo | +2 mo |
```

## Guidance

- Keep it scannable (30 seconds to digest)
- Lead with the most important metric
- Use directional indicators (↑ ↓ →)
- Compare to previous month, not plan
- Round numbers for readability ($2.4M not $2,387,421)

## Output

Generate the metrics snapshot and offer to:
1. Copy to clipboard (for pasting into email)
2. Save to a file
3. Insert into an existing draft

Reference the monthly-investor-updates skill for metrics presentation best practices.
