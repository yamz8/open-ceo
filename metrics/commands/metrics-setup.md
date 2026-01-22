---
description: Configure which metrics to track based on business model and stage
argument-hint: [model] [stage]
allowed-tools: Read, Write, Edit, Grep, Glob
---

Set up metrics tracking configuration for the company.

**Arguments:**
- Model: $1 (options: saas, marketplace, or leave blank to ask)
- Stage: $2 (options: pre-seed, seed, series-a, series-b, or leave blank to ask)

**Process:**

1. **Determine business model and stage:**
   - Check `.claude/metrics.local.md` for existing config
   - If not specified, ask user for business model and stage

2. **For SaaS companies, configure:**
   - Revenue metrics: MRR, ARR, New/Expansion/Churned MRR
   - Growth metrics: MoM growth, NRR, GRR
   - Unit economics: CAC, LTV, CAC Payback, Gross Margin
   - Efficiency: Burn Multiple, Magic Number, Rule of 40
   - Customer metrics: Logo count, churn rate

3. **For Marketplace companies, configure:**
   - Volume metrics: GMV, Net Revenue, Take Rate, AOV
   - Liquidity metrics: Search-to-Fill, Time-to-Fill, Utilization
   - Supply/Demand: Active buyers, Active sellers, B:S ratio
   - Retention: Buyer repeat rate, Seller retention
   - Economics: Buyer LTV:CAC, Seller LTV:CAC, Contribution margin

4. **Customize for stage:**
   - Pre-seed: Focus on engagement, activation, early signals
   - Seed: Add revenue metrics, basic unit economics
   - Series A: Full unit economics, efficiency metrics
   - Series B+: All metrics plus Rule of 40, FCF

5. **Create or update `.claude/metrics.local.md`:**
   - Store business model and stage
   - List metrics to track with current values (to be filled)
   - Include relevant benchmarks for reference
   - Document calculation methods

**Output format:**

```markdown
# Metrics Configuration

## Company Profile
- Business Model: [SaaS/Marketplace]
- Stage: [Stage]
- Industry: [If specified]

## Metrics to Track

### Primary Metrics (Report Monthly)
| Metric | Current | Target | Benchmark |
|--------|---------|--------|-----------|
| [Metric 1] | [Value] | [Target] | [Benchmark] |
...

### Secondary Metrics (Review Quarterly)
...

### Formulas
[Key calculation formulas for this business]
```

**Integration note:**
This config file (`.claude/metrics.local.md`) can be read by other Open CEO plugins (fundraising, board-prep, investor-updates) to provide consistent metrics across all communications.
