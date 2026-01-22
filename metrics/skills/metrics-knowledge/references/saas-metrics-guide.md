# SaaS Metrics Complete Guide

## Revenue Metrics Deep Dive

### Monthly Recurring Revenue (MRR)

**Definition**: The predictable, recurring revenue from subscriptions normalized to a monthly amount.

**Calculation**:
```
MRR = Sum of all active subscription monthly values
```

**For annual contracts**:
```
MRR contribution = Annual Contract Value / 12
```

**MRR Components**:
- **New MRR**: First payment from new customers
- **Expansion MRR**: Additional revenue from existing customers (upgrades, add-ons, seats)
- **Contraction MRR**: Reduced revenue from downgrades
- **Churned MRR**: Lost revenue from cancellations
- **Reactivation MRR**: Revenue from returning customers

**Net New MRR Formula**:
```
Net New MRR = New MRR + Expansion MRR + Reactivation MRR - Contraction MRR - Churned MRR
```

### Annual Recurring Revenue (ARR)

**Definition**: MRR annualized, the standard metric for SaaS valuation.

**Calculation**:
```
ARR = MRR × 12
```

**When to use ARR vs MRR**:
- ARR: Investor conversations, valuation, annual planning
- MRR: Operational tracking, monthly reporting

### Average Revenue Per User (ARPU)

**Definition**: Revenue per customer, used for unit economics.

**Calculation**:
```
ARPU = MRR / Total Active Customers
```

**Variations**:
- ARPA (Per Account): For B2B with multiple users per account
- ARPU by segment: Track separately for SMB, Mid-Market, Enterprise

---

## Churn Metrics Deep Dive

### Customer Churn Rate (Logo Churn)

**Definition**: Percentage of customers lost in a period.

**Monthly Calculation**:
```
Customer Churn Rate = Customers Lost / Customers at Start of Month
```

**Annualized**:
```
Annual Churn = 1 - (1 - Monthly Churn)^12
```

**Example**:
- 5% monthly churn = 46% annual churn
- 2% monthly churn = 21% annual churn

### Revenue Churn Rate (MRR Churn)

**Definition**: Percentage of MRR lost in a period.

**Gross Revenue Churn**:
```
Gross Churn = Churned MRR / Starting MRR
```

**Net Revenue Churn** (can be negative!):
```
Net Churn = (Churned MRR + Contraction MRR - Expansion MRR) / Starting MRR
```

### Net Revenue Retention (NRR)

**Definition**: Revenue retained from a cohort including expansion. The most important retention metric.

**Calculation**:
```
NRR = (Starting MRR + Expansion - Contraction - Churn) / Starting MRR × 100
```

**Benchmarks**:
| Segment | Median | Top Quartile |
|---------|--------|--------------|
| SMB | 90-100% | 100-110% |
| Mid-Market | 100-110% | 110-120% |
| Enterprise | 110-120% | 125%+ |

**Why NRR > 100% matters**:
- Revenue grows even with zero new customers
- Indicates strong product-market fit
- Drives capital efficiency

### Gross Revenue Retention (GRR)

**Definition**: Revenue retained excluding expansion. Shows true churn.

**Calculation**:
```
GRR = (Starting MRR - Contraction - Churn) / Starting MRR × 100
```

**Maximum**: 100% (cannot exceed starting revenue)

**Benchmarks**:
- Good: 85-90%
- Great: 90-95%
- Best-in-class: 95%+

---

## Unit Economics Deep Dive

### Customer Acquisition Cost (CAC)

**Definition**: Cost to acquire one customer.

**Fully-Loaded CAC**:
```
CAC = (Sales + Marketing Spend) / New Customers Acquired
```

**Include in S&M spend**:
- Salaries (sales, marketing, SDRs)
- Advertising and paid acquisition
- Marketing tools and software
- Events and content
- Sales commissions

**CAC by Channel**:
Track separately for:
- Organic/Inbound
- Paid (by channel)
- Outbound sales
- Partnerships

### Customer Lifetime Value (LTV)

**Definition**: Total revenue expected from a customer over their lifetime.

**Simple Formula**:
```
LTV = ARPU × Gross Margin / Monthly Churn Rate
```

**With expansion**:
```
LTV = ARPU × Gross Margin / (1 - NRR)
```
Note: Only works if NRR < 100%

**Example**:
- ARPU: $500/month
- Gross Margin: 80%
- Monthly Churn: 2%
- LTV = $500 × 0.80 / 0.02 = $20,000

### LTV:CAC Ratio

**Definition**: Return on customer acquisition investment.

**Calculation**:
```
LTV:CAC = LTV / CAC
```

**Benchmarks**:
| Ratio | Interpretation |
|-------|----------------|
| <1:1 | Losing money on every customer |
| 1-2:1 | Marginal, needs improvement |
| 3:1 | Healthy, sustainable |
| 5:1+ | Very efficient (or underinvesting in growth) |

### CAC Payback Period

**Definition**: Months to recover CAC from a customer.

**Calculation**:
```
CAC Payback = CAC / (ARPU × Gross Margin)
```

**Benchmarks**:
| Stage | Target |
|-------|--------|
| Seed | <24 months |
| Series A | <18 months |
| Series B | <12 months |
| Series C+ | <12 months |

---

## Growth & Efficiency Metrics

### Burn Multiple

**Definition**: How much you burn to generate each dollar of ARR.

**Calculation**:
```
Burn Multiple = Net Burn / Net New ARR
```

**Benchmarks**:
| Multiple | Efficiency |
|----------|------------|
| <1x | Amazing (rare) |
| 1-1.5x | Great |
| 1.5-2x | Good |
| 2-3x | Acceptable (early stage) |
| >3x | Inefficient |

### Magic Number

**Definition**: Sales efficiency metric showing ARR generated per S&M dollar.

**Calculation**:
```
Magic Number = (Current Q ARR - Prior Q ARR) / Prior Q S&M Spend
```

**Benchmarks**:
| Number | Interpretation |
|--------|----------------|
| <0.5 | Inefficient, fix GTM |
| 0.5-0.75 | Needs improvement |
| 0.75-1.0 | Good efficiency |
| >1.0 | Excellent, invest more |

### Rule of 40

**Definition**: Combined growth and profitability benchmark.

**Calculation**:
```
Rule of 40 = Revenue Growth Rate + Profit Margin
```

**Example**:
- 50% growth + (-10%) margin = 40 ✓
- 30% growth + 15% margin = 45 ✓
- 20% growth + 5% margin = 25 ✗

**Benchmarks**:
| Score | Rating |
|-------|--------|
| <20 | Poor |
| 20-40 | Acceptable |
| 40-60 | Good |
| >60 | Excellent |

---

## Quick Win Metrics

### Net Promoter Score (NPS)

**Definition**: Customer satisfaction and loyalty metric.

**Calculation**:
```
NPS = % Promoters (9-10) - % Detractors (0-6)
```

**Benchmarks**:
| Score | Rating |
|-------|--------|
| <0 | Poor |
| 0-30 | Good |
| 30-50 | Great |
| >50 | Excellent |

### Monthly Active Users (MAU)

**Definition**: Unique users with meaningful activity in 30 days.

**Key variations**:
- DAU: Daily Active Users
- WAU: Weekly Active Users
- DAU/MAU Ratio: Engagement stickiness (>25% is good)

### Activation Rate

**Definition**: Percentage of signups reaching "aha moment".

**Calculation**:
```
Activation Rate = Activated Users / Total Signups
```

Define activation based on key value actions (not just login).

---

## Presenting Metrics to Investors

### What to Always Include

1. **ARR/MRR** with growth rate
2. **Net Revenue Retention**
3. **Gross Margin**
4. **Burn Rate & Runway**
5. **CAC Payback** (if positive unit economics)

### What to Include When Strong

- LTV:CAC ratio (if >3:1)
- Magic Number (if >0.75)
- Rule of 40 (if >40)
- Logo retention (if >90%)

### Common Mistakes

1. **Cherry-picking periods**: Use consistent time periods
2. **Mixing metrics**: Don't combine logo and revenue churn
3. **Ignoring seasonality**: Note seasonal patterns
4. **Gross vs Net confusion**: Always specify which
5. **Trailing vs forward**: Be clear on time basis
