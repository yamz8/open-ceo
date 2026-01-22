# SaaS Metrics Guide for Board Reporting

Comprehensive guide to calculating and presenting SaaS metrics for board meetings.

## Revenue Metrics

### ARR (Annual Recurring Revenue)

**Definition:** Annualized value of recurring subscription revenue.

**Formula:**
```
ARR = MRR × 12
```

**What to report:**
- Current ARR
- ARR at end of previous quarter
- YoY ARR growth rate
- ARR by customer segment (if applicable)

**Benchmark:** Series A companies typically have $1-3M ARR; Series B $5-15M ARR.

### MRR (Monthly Recurring Revenue)

**Definition:** Normalized monthly recurring revenue from subscriptions.

**Formula:**
```
MRR = Sum of all monthly subscription values
```

**MRR Components:**
- **New MRR**: Revenue from new customers this month
- **Expansion MRR**: Additional revenue from existing customers (upgrades, add-ons)
- **Contraction MRR**: Lost revenue from downgrades (still customers)
- **Churned MRR**: Lost revenue from cancelled customers

**Net New MRR:**
```
Net New MRR = New MRR + Expansion MRR - Contraction MRR - Churned MRR
```

### MRR Growth Rate

**Monthly Growth:**
```
MoM Growth = (Current MRR - Previous MRR) / Previous MRR × 100
```

**Annualized Growth (CMGR):**
```
CMGR = (Ending MRR / Starting MRR)^(1/months) - 1
```

**Benchmark:** 15-20% MoM growth is excellent for early-stage; 10%+ is good.

### Net Revenue Retention (NRR)

**Definition:** Revenue retained from existing customers including expansion.

**Formula:**
```
NRR = (Starting MRR + Expansion - Contraction - Churn) / Starting MRR × 100
```

**Benchmark:**
- <100% = Losing revenue from existing customers (concerning)
- 100-110% = Healthy retention
- >120% = Excellent (expansion outpaces churn)

Best-in-class SaaS companies have 120-150% NRR.

## Unit Economics

### CAC (Customer Acquisition Cost)

**Definition:** Total cost to acquire one new customer.

**Formula:**
```
CAC = (Sales + Marketing Costs) / New Customers Acquired
```

**Blended vs. Paid CAC:**
- **Blended CAC**: All customers, including organic
- **Paid CAC**: Only customers from paid channels

**What to report:**
- Blended CAC
- CAC by channel (if significant variation)
- CAC trend over time

### LTV (Lifetime Value)

**Definition:** Total revenue expected from a customer over their lifetime.

**Simple Formula:**
```
LTV = ARPU / Monthly Churn Rate
```

**More Accurate Formula:**
```
LTV = (ARPU × Gross Margin) / Monthly Churn Rate
```

Where ARPU = Average Revenue Per User (monthly).

**Example:**
- ARPU: $500/month
- Gross Margin: 80%
- Monthly Churn: 2%
- LTV = ($500 × 0.80) / 0.02 = $20,000

### LTV:CAC Ratio

**Definition:** Return on customer acquisition investment.

**Formula:**
```
LTV:CAC = LTV / CAC
```

**Benchmark:**
- <1:1 = Losing money on each customer (unsustainable)
- 1:1 to 3:1 = May be acceptable during growth phase
- 3:1 to 5:1 = Healthy ratio (target range)
- >5:1 = May be underinvesting in growth

### CAC Payback Period

**Definition:** Months to recover customer acquisition cost.

**Formula:**
```
Payback = CAC / (ARPU × Gross Margin)
```

**Benchmark:**
- <12 months = Excellent
- 12-18 months = Good
- 18-24 months = Acceptable for enterprise
- >24 months = Concerning

## Retention & Churn Metrics

### Gross Churn Rate (Revenue)

**Definition:** Revenue lost from cancellations as percentage of starting MRR.

**Formula:**
```
Gross Revenue Churn = Churned MRR / Starting MRR × 100
```

**Benchmark:**
- <2% monthly = Excellent
- 2-5% monthly = Acceptable
- >5% monthly = Concerning

### Logo Churn (Customer Churn)

**Definition:** Percentage of customers who cancel.

**Formula:**
```
Logo Churn = Churned Customers / Starting Customers × 100
```

**Note:** Logo churn is often higher than revenue churn if smaller customers churn more frequently.

### Net Churn Rate

**Definition:** Net revenue change from existing customers.

**Formula:**
```
Net Churn = (Churned MRR - Expansion MRR) / Starting MRR × 100
```

**Negative net churn** means expansion exceeds churn (ideal state).

## Cash & Runway Metrics

### Monthly Burn Rate

**Definition:** Net cash consumed per month.

**Formula:**
```
Burn Rate = Cash Outflows - Cash Inflows
```

Or simplified:
```
Burn Rate = (Starting Cash - Ending Cash) / Months
```

**Gross vs. Net Burn:**
- **Gross Burn**: Total monthly expenses
- **Net Burn**: Expenses minus revenue (actual cash consumed)

Always report **Net Burn** for runway calculations.

### Cash Runway

**Definition:** Months until cash runs out at current burn rate.

**Formula:**
```
Runway = Current Cash Balance / Monthly Net Burn
```

**What to report:**
- Current cash balance
- Monthly net burn (average of last 3 months)
- Runway in months
- Runway end date

**Benchmark:**
- <6 months = Critical, must fundraise immediately
- 6-12 months = Concerning, should be fundraising
- 12-18 months = Healthy
- >18 months = Comfortable

### Burn Multiple

**Definition:** How much cash burned to generate each dollar of new ARR.

**Formula:**
```
Burn Multiple = Net Burn / Net New ARR
```

**Benchmark:**
- <1x = Excellent efficiency
- 1-2x = Good
- 2-3x = Acceptable during scaling
- >3x = Concerning efficiency

## Presenting Metrics to the Board

### Dashboard Layout

Present metrics in a consistent dashboard format:

```
┌─────────────────┬─────────────────┬─────────────────┐
│ ARR             │ MRR Growth      │ NRR             │
│ $2.4M           │ 12% MoM         │ 115%            │
│ ▲ 18% QoQ       │ ▲ from 10%      │ ▲ from 108%     │
├─────────────────┼─────────────────┼─────────────────┤
│ CAC             │ LTV:CAC         │ Payback         │
│ $12,500         │ 3.8:1           │ 11 months       │
│ ▼ 8% QoQ        │ ▲ from 3.2:1    │ ▼ from 14 mo    │
├─────────────────┼─────────────────┼─────────────────┤
│ Gross Churn     │ Net Churn       │ Runway          │
│ 2.1%            │ -1.2%           │ 16 months       │
│ ▼ from 2.8%     │ ▼ from -0.5%    │ ▲ from 14 mo    │
└─────────────────┴─────────────────┴─────────────────┘
```

### Trend Visualization

Always show trends, not just point-in-time:
- Include 6-12 months of history
- Add trendlines to charts
- Highlight inflection points
- Compare to plan/forecast

### Cohort Analysis

For retention and revenue metrics, include cohort views:
- Monthly customer cohorts
- Revenue retention by cohort
- Identify if recent cohorts perform differently

### Segmentation

Break down key metrics by:
- Customer segment (SMB, Mid-Market, Enterprise)
- Geography (if relevant)
- Product line (if multiple products)
- Acquisition channel

## Red Flags to Address Proactively

If any of these exist, address them in the board deck before being asked:

1. **Declining MRR growth** - Explain why and recovery plan
2. **Increasing churn** - Root cause analysis and mitigation
3. **Worsening unit economics** - Path to improvement
4. **Short runway** - Fundraising timeline and plan
5. **Missed forecasts** - Why and recalibrated expectations
6. **Customer concentration** - Top 10 customers as % of ARR

## Benchmarks Summary Table

| Metric | Poor | Acceptable | Good | Excellent |
|--------|------|------------|------|-----------|
| MoM MRR Growth | <5% | 5-10% | 10-15% | >15% |
| NRR | <100% | 100-110% | 110-120% | >120% |
| LTV:CAC | <1:1 | 1-3:1 | 3-5:1 | >5:1 |
| CAC Payback | >24 mo | 18-24 mo | 12-18 mo | <12 mo |
| Gross Churn | >5% | 3-5% | 2-3% | <2% |
| Runway | <6 mo | 6-12 mo | 12-18 mo | >18 mo |
| Burn Multiple | >3x | 2-3x | 1-2x | <1x |

Note: Benchmarks vary by stage, industry, and go-to-market motion. Enterprise SaaS typically has longer payback but higher NRR.
