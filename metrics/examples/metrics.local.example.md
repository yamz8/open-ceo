# Metrics Configuration Example

Copy this file to `.claude/metrics.local.md` and fill in your company details.

```markdown
---
# Company Profile
company_name: "TechFlow"
business_model: "saas"  # saas, marketplace
stage: "series-a"  # pre-seed, seed, series-a, series-b, series-c
industry: "b2b"  # b2b, b2c, fintech, etc.

# Revenue Metrics (SaaS)
mrr: 185000
arr: 2220000
new_mrr: 22000
expansion_mrr: 8000
churned_mrr: 13000
net_new_mrr: 17000

# Growth Metrics
mrr_growth_mom: 10.1  # percentage
arr_growth_yoy: 219  # percentage
nrr: 112  # percentage
grr: 91  # percentage

# Unit Economics
cac: 8500
ltv: 42000
ltv_cac_ratio: 4.9
cac_payback_months: 11
arpu: 1850
gross_margin: 78  # percentage

# Efficiency Metrics
burn_multiple: 1.8
magic_number: 0.82
rule_of_40: 52

# Burn & Runway
cash_balance: 4200000
monthly_burn: 150000
monthly_revenue: 185000
net_burn: -35000  # negative means cash flow positive
runway_months: 24

# Customer Metrics
total_customers: 100
new_customers: 8
churned_customers: 3
logo_churn_rate: 3  # percentage

# Last Updated
last_updated: "2025-01-15"
---

## Notes

### Metric Definitions
- MRR: Monthly Recurring Revenue from all active subscriptions
- NRR: Net Revenue Retention (including expansion)
- GRR: Gross Revenue Retention (excluding expansion)
- CAC: Fully-loaded Customer Acquisition Cost
- LTV: Customer Lifetime Value using (ARPU × Gross Margin / Churn)

### Customer Segments
- SMB (<$1K MRR): 65 customers, $45K MRR
- Mid-Market ($1-5K MRR): 30 customers, $85K MRR
- Enterprise (>$5K MRR): 5 customers, $55K MRR

### Key Observations
- Strong expansion driving NRR > 100%
- Mid-market churn elevated this month
- Approaching cash flow positive

### Benchmarks for Series A SaaS
| Metric | Minimum | Good | Our Value |
|--------|---------|------|-----------|
| ARR | $1M | $2-3M | $2.2M ✅ |
| NRR | 100% | 110%+ | 112% ✅ |
| Gross Margin | 70% | 75%+ | 78% ✅ |
| Burn Multiple | <2.5x | <1.5x | 1.8x ✅ |
```

---

## For Marketplace Businesses

Use these fields instead:

```yaml
# Volume Metrics
gmv: 500000  # monthly
net_revenue: 75000
take_rate: 15  # percentage
aov: 85  # average order value

# Liquidity Metrics
search_to_fill_rate: 28  # percentage
time_to_fill_hours: 4
utilization_rate: 45  # percentage

# Supply & Demand
active_buyers: 5000
active_sellers: 250
buyer_seller_ratio: 20

# Retention
buyer_repeat_rate: 35  # percentage
seller_retention: 88  # percentage

# Economics
buyer_cac: 25
buyer_ltv: 150
seller_cac: 500
seller_ltv: 2500
contribution_margin: 45  # percentage
```
