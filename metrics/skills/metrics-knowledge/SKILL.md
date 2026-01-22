---
name: Metrics Knowledge
description: This skill should be used when the user asks to "track metrics", "calculate ARR", "what metrics should I track", "benchmark my metrics", "understand churn", "calculate LTV", "what is burn multiple", "GMV calculation", "marketplace metrics", or mentions specific metrics like ARR, MRR, NRR, churn, CAC, LTV, burn rate, runway, GMV, take rate, or cohort analysis.
version: 0.1.0
---

# Startup Metrics Knowledge

## Overview

This skill provides comprehensive guidance on startup metrics for SaaS and marketplace businesses. It covers metric definitions, calculation formulas, stage-appropriate benchmarks, and best practices for tracking and reporting.

## SaaS Metrics Fundamentals

### Revenue Metrics

| Metric | Formula | Description |
|--------|---------|-------------|
| MRR | Sum of monthly recurring revenue | Core subscription revenue |
| ARR | MRR × 12 | Annualized recurring revenue |
| New MRR | MRR from new customers | Growth driver |
| Expansion MRR | MRR from upgrades/upsells | Land-and-expand signal |
| Churned MRR | MRR lost from cancellations | Retention indicator |
| Net New MRR | New + Expansion - Churned | Overall momentum |

### Growth Metrics

| Metric | Formula | Good | Great |
|--------|---------|------|-------|
| MoM Growth | (MRR₁ - MRR₀) / MRR₀ | 10-15% | 20%+ |
| YoY Growth | (ARR₁ - ARR₀) / ARR₀ | 2x | 3x |
| Net Revenue Retention | (Starting MRR + Expansion - Churn) / Starting MRR | 100-110% | 120%+ |
| Gross Revenue Retention | (Starting MRR - Churn) / Starting MRR | 85-90% | 95%+ |
| Logo Retention | Customers retained / Starting customers | 85-90% | 95%+ |

### Unit Economics

| Metric | Formula | Target |
|--------|---------|--------|
| CAC | Sales & Marketing spend / New customers | Varies by ACV |
| LTV | ARPU × Gross Margin × (1/Churn Rate) | 3x+ CAC |
| LTV:CAC Ratio | LTV / CAC | 3:1 to 5:1 |
| CAC Payback | CAC / (ARPU × Gross Margin) | <18 months |
| Gross Margin | (Revenue - COGS) / Revenue | 70-80%+ |

### Efficiency Metrics

| Metric | Formula | Target |
|--------|---------|--------|
| Burn Multiple | Net Burn / Net New ARR | <2x |
| Magic Number | Net New ARR / Prior Q S&M Spend | >0.75 |
| Rule of 40 | Growth Rate + Profit Margin | >40% |
| Hype Ratio | Implied ARR Multiple / Growth Rate | <1x |

## Marketplace Metrics Fundamentals

### Volume Metrics

| Metric | Formula | Description |
|--------|---------|-------------|
| GMV | Total transaction value | Gross Merchandise Value |
| Net Revenue | GMV × Take Rate | Actual revenue |
| Take Rate | Net Revenue / GMV | Platform fee % |
| AOV | GMV / Orders | Average Order Value |

### Liquidity Metrics

| Metric | Formula | Description |
|--------|---------|-------------|
| Search-to-Fill Rate | Filled requests / Total searches | Demand satisfaction |
| Time-to-Fill | Avg time from request to fulfillment | Efficiency |
| Buyer-to-Seller Ratio | Active buyers / Active sellers | Balance indicator |
| Repeat Rate | Repeat transactions / Total | Stickiness |

### Marketplace Health

| Metric | Description | Target |
|--------|-------------|--------|
| Supply Liquidity | % of listings with transactions | >30% |
| Demand Liquidity | % of searches resulting in purchase | >20% |
| Supplier Concentration | Top 10% supplier revenue share | <40% |
| Cross-Side Network Effects | Growth correlation between sides | Positive |

## Burn & Runway

### Burn Calculations

| Metric | Formula |
|--------|---------|
| Gross Burn | Total monthly operating expenses |
| Net Burn | Gross Burn - Revenue |
| Runway | Cash Balance / Net Burn |
| Zero Cash Date | Today + (Runway months) |

### Burn Benchmarks by Stage

| Stage | Acceptable Burn Multiple | Target Runway |
|-------|-------------------------|---------------|
| Pre-seed | N/A | 18-24 months |
| Seed | <3x | 18-24 months |
| Series A | <2x | 18-24 months |
| Series B | <1.5x | 24+ months |
| Series C+ | <1x | 24+ months |

## Stage-Appropriate Metrics

### Pre-Seed / Seed
Focus on product-market fit signals:
- Engagement metrics (DAU/MAU, retention curves)
- Organic growth / word-of-mouth
- Early revenue or intent signals
- User feedback quality

### Series A
Prove repeatable revenue:
- ARR: $1-3M
- Growth: 2-3x YoY
- Retention: >100% NRR
- Unit economics trending positive

### Series B
Scale efficiently:
- ARR: $5-15M
- Growth: 2x+ YoY
- Burn multiple: <1.5x
- Clear path to profitability

### Series C+
Efficient growth at scale:
- ARR: $20M+
- Rule of 40: >40%
- Strong unit economics
- Market leadership indicators

## Cohort Analysis

### Revenue Cohorts
Track how revenue from each customer cohort evolves over time:
- Month 0: Initial MRR
- Month 3, 6, 12: Retention %
- Expansion curve: Upsell trajectory

### User Cohorts
Track engagement by signup cohort:
- Day 1, 7, 30 retention
- Feature adoption rates
- Conversion milestones

## Additional Resources

### Reference Files

For detailed guidance, consult:
- **`references/saas-metrics-guide.md`** - Complete SaaS metrics with formulas and examples
- **`references/marketplace-metrics-guide.md`** - Marketplace-specific metrics and benchmarks
- **`references/benchmarks-by-stage.md`** - Stage and industry benchmarks

### Example Files

Working examples in `examples/`:
- **`example-metrics-snapshot.md`** - Sample metrics report format
- **`example-cohort-analysis.md`** - Cohort analysis template
