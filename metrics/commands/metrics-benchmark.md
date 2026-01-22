---
description: Compare your metrics to stage and industry benchmarks
argument-hint: [stage]
allowed-tools: Read, Write, Grep, Glob
---

Benchmark your metrics against industry standards.

**Arguments:**
- Stage: $1 (options: seed, series-a, series-b, series-c, or leave blank to use config)

**Process:**

1. **Load current metrics:**
   - Read `.claude/metrics.local.md` for current values
   - If missing values, ask user for key metrics to benchmark

2. **Determine benchmark set:**
   - Use stage from argument or config
   - Use business model from config (SaaS vs Marketplace)
   - Select appropriate benchmark data from metrics-knowledge skill

3. **For SaaS, benchmark:**
   | Metric | Your Value | Median | Top Quartile | Status |
   |--------|------------|--------|--------------|--------|
   | ARR | | Stage-appropriate | | |
   | Growth Rate | | | | |
   | NRR | | | | |
   | GRR | | | | |
   | Gross Margin | | | | |
   | LTV:CAC | | | | |
   | CAC Payback | | | | |
   | Burn Multiple | | | | |
   | Magic Number | | | | |
   | Rule of 40 | | | | |

4. **For Marketplace, benchmark:**
   | Metric | Your Value | Median | Top Quartile | Status |
   |--------|------------|--------|--------------|--------|
   | GMV | | | | |
   | GMV Growth | | | | |
   | Take Rate | | | | |
   | Repeat Rate | | | | |
   | Search-to-Fill | | | | |
   | Contribution Margin | | | | |
   | LTV:CAC (Buyer) | | | | |
   | LTV:CAC (Seller) | | | | |

5. **Provide analysis:**
   - Identify strengths (top quartile metrics)
   - Identify areas for improvement (below median)
   - Prioritize which metrics to focus on
   - Suggest specific actions for weak areas

6. **Investor readiness assessment:**
   - Which metrics are "fundable" for next round
   - What needs to improve before fundraising
   - Estimated time to reach benchmarks

**Output format:**

```markdown
# Metrics Benchmark Analysis
## [Company] | [Stage] | [Business Model]

### Summary
- **Strengths**: [X] metrics in top quartile
- **On Track**: [X] metrics at median+
- **Needs Work**: [X] metrics below median

### Detailed Comparison

#### Revenue & Growth
| Metric | You | Median | Top 25% | Gap |
|--------|-----|--------|---------|-----|
...

#### Unit Economics
...

#### Efficiency
...

### Strengths (Top Quartile)
1. **[Metric]**: Your [value] vs top quartile [value]
   - This indicates [what it means]

### Improvement Areas
1. **[Metric]**: Your [value] vs median [value]
   - Gap: [X]%
   - To improve: [Specific suggestion]
   - Impact: [Why this matters]

### Fundraising Readiness
[Assessment of metrics readiness for next round]

### Priority Actions
1. [Most impactful improvement]
2. [Second priority]
3. [Third priority]
```
