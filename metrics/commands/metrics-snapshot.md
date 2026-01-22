---
description: Generate current metrics summary for reporting
argument-hint: [format]
allowed-tools: Read, Write, Grep, Glob
---

Generate a metrics snapshot for the current period.

**Arguments:**
- Format: $1 (options: full, summary, investor, board, or leave blank for full)

**Process:**

1. **Load configuration:**
   - Read `.claude/metrics.local.md` for metrics config and current values
   - If no config exists, run metrics-setup first or ask for key metrics

2. **Gather current metrics:**
   - Ask user for current values of tracked metrics
   - Or read from config if recently updated
   - Calculate derived metrics automatically

3. **Generate snapshot based on format:**

   **Full** (default):
   - All tracked metrics with MoM/QoQ changes
   - Benchmark comparisons
   - Commentary and insights
   - Detailed breakdowns

   **Summary**:
   - Key metrics only (5-7 most important)
   - Current values and trends
   - Quick status indicators

   **Investor**:
   - Metrics investors care about for this stage
   - Formatted for investor updates or pitch decks
   - Include positive framing with honest context

   **Board**:
   - Comprehensive metrics for board reporting
   - Comparison to plan/budget
   - Detailed commentary on variances

4. **Calculate derived metrics:**
   - Net New MRR = New + Expansion - Churned
   - LTV = ARPU × Gross Margin / Churn Rate
   - LTV:CAC = LTV / CAC
   - CAC Payback = CAC / (ARPU × Gross Margin)
   - Burn Multiple = Net Burn / Net New ARR
   - Magic Number = Net New ARR / Prior Q S&M
   - Rule of 40 = Growth Rate + Profit Margin

5. **Add status indicators:**
   - ✅ On track (at or above benchmark)
   - ⚠️ Watch (slightly below benchmark)
   - ❌ Needs attention (significantly below)

**Output format:**

```markdown
# Metrics Snapshot
## [Company Name] | [Period]

### Key Metrics
| Metric | Current | Change | Status |
|--------|---------|--------|--------|
| ARR | $X | +X% | ✅ |
...

### Detailed Breakdown
[Section by category]

### Insights
- [Key observation 1]
- [Key observation 2]

### Actions
- [Recommended action based on metrics]
```

**Tip**: Run this monthly and save snapshots to track trends over time.
