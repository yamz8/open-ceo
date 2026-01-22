# Marketplace Metrics Complete Guide

## Core Marketplace Metrics

### Gross Merchandise Value (GMV)

**Definition**: Total value of transactions processed through the marketplace.

**Calculation**:
```
GMV = Sum of all transaction values
```

**Key considerations**:
- Include or exclude shipping/fees consistently
- Handle refunds and cancellations
- Track gross vs net GMV

### Net Revenue (Take Rate Revenue)

**Definition**: The marketplace's actual revenue from GMV.

**Calculation**:
```
Net Revenue = GMV × Take Rate
```

### Take Rate

**Definition**: Percentage of GMV captured as revenue.

**Calculation**:
```
Take Rate = Net Revenue / GMV × 100
```

**Benchmarks by category**:
| Category | Typical Take Rate |
|----------|-------------------|
| E-commerce | 10-20% |
| Food delivery | 15-30% |
| Ride-sharing | 20-30% |
| Professional services | 10-20% |
| Real estate | 2-6% |
| B2B marketplaces | 5-15% |

**Take rate components**:
- Transaction fee (% of GMV)
- Service fees (flat or %)
- Subscription fees (for sellers)
- Advertising/promotion revenue
- Fulfillment/logistics fees

---

## Liquidity Metrics

Liquidity is the most critical marketplace metric - it measures whether supply meets demand.

### Search-to-Fill Rate

**Definition**: Percentage of searches/requests that result in a transaction.

**Calculation**:
```
Search-to-Fill = Completed Transactions / Total Searches
```

**Benchmarks**:
| Rate | Quality |
|------|---------|
| <10% | Poor liquidity |
| 10-20% | Developing |
| 20-40% | Good |
| >40% | Excellent |

### Time-to-Fill

**Definition**: Average time from search/request to completed transaction.

**Calculation**:
```
Time-to-Fill = Avg(Transaction Time - Request Time)
```

**Target**: Depends on category
- Ride-sharing: <5 minutes
- Food delivery: <45 minutes
- Professional services: <24-48 hours
- E-commerce: <3-5 days (delivery)

### Match Rate

**Definition**: Percentage of listings that receive at least one inquiry/order.

**Calculation**:
```
Match Rate = Listings with Activity / Total Active Listings
```

**Healthy benchmark**: >30% of listings should have activity

### Utilization Rate (Supply-side)

**Definition**: How much of available supply is being used.

**Calculation**:
```
Utilization = Used Supply / Available Supply
```

**Examples**:
- Airbnb: Nights booked / Nights available
- Uber: Hours driving / Hours online
- Freelance: Hours billed / Hours available

---

## Supply & Demand Metrics

### Supply Metrics

| Metric | Definition |
|--------|------------|
| Active Sellers | Sellers with activity in 30 days |
| Listings | Total active product/service listings |
| Inventory Depth | Avg listings per seller |
| New Seller Adds | New sellers joining per period |
| Seller Churn | Sellers becoming inactive |
| Seller Activation | % of signups becoming active sellers |

### Demand Metrics

| Metric | Definition |
|--------|------------|
| Active Buyers | Buyers with activity in 30 days |
| Purchase Frequency | Orders per buyer per period |
| Buyer Churn | Buyers becoming inactive |
| New Buyer Adds | New buyers per period |
| Conversion Rate | Visitors → Purchasers |

### Supply-Demand Balance

**Buyer-to-Seller Ratio**:
```
B:S Ratio = Active Buyers / Active Sellers
```

Optimal ratio varies by marketplace type:
- E-commerce: 50-100+ buyers per seller
- Services: 5-20 buyers per provider
- C2C: 1-5 buyers per seller

---

## Engagement & Retention

### Buyer Metrics

| Metric | Formula | Target |
|--------|---------|--------|
| Repeat Purchase Rate | Buyers with 2+ orders / Total buyers | >30% |
| Purchase Frequency | Orders / Active buyers / Period | Category-dependent |
| Time Between Purchases | Avg days between orders | Decreasing |
| Basket Size | GMV / Orders | Stable or growing |
| Buyer NPS | Standard NPS methodology | >30 |

### Seller Metrics

| Metric | Formula | Target |
|--------|---------|--------|
| Seller Retention | Sellers active M2 / Sellers active M1 | >80% |
| Revenue per Seller | GMV / Active sellers | Growing |
| Seller NPS | Standard NPS methodology | >30 |
| Time to First Sale | Days from signup to first transaction | Decreasing |
| Seller Activation | Sellers with sale / Total signups | >20% |

### Cohort Retention

Track by signup cohort:
- Month 1, 3, 6, 12 retention
- GMV per cohort over time
- Purchase frequency evolution

---

## Network Effects Metrics

### Cross-Side Network Effects

**Definition**: How growth on one side drives growth on the other.

**Measurement**:
```
Track correlation between:
- Seller growth → Buyer growth
- Buyer growth → Seller growth
```

**Healthy sign**: Both correlations positive and significant

### Same-Side Effects

**Can be positive or negative**:
- Positive: Buyers attract buyers (social proof, reviews)
- Negative: Sellers compete (price pressure, attention)

### Network Effect Strength

**Indirect measurement**:
- Organic growth rate (word of mouth)
- CAC trend over time (should decrease with scale)
- Conversion rate vs marketplace size

---

## Marketplace Health Scorecard

### Concentration Risk

| Metric | Formula | Target |
|--------|---------|--------|
| Top 10 Seller % | Top 10 seller GMV / Total GMV | <30% |
| Top 10 Buyer % | Top 10 buyer GMV / Total GMV | <20% |
| Category Concentration | Largest category % | <50% |
| Geographic Concentration | Largest geo % | <40% |

### Quality Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Review Rate | % of orders with reviews | >20% |
| Avg Rating | Mean seller/product rating | >4.0 |
| Dispute Rate | Orders with disputes / Total | <2% |
| Refund Rate | Refunded GMV / Total GMV | <5% |
| Fraud Rate | Fraudulent transactions / Total | <0.5% |

### Platform Health

| Metric | Description | Target |
|--------|-------------|--------|
| Support Tickets | Tickets per 100 orders | <5 |
| Resolution Time | Avg time to resolve issues | <24 hours |
| Platform Uptime | % time available | >99.9% |
| Mobile % | Mobile transactions / Total | Benchmark category |

---

## Marketplace Unit Economics

### Buyer Economics

```
Buyer LTV = Avg Orders × Avg Order Value × Take Rate × Gross Margin × Avg Lifetime

Buyer CAC = (Marketing + Incentives) / New Buyers

Buyer LTV:CAC = Target 3:1+
```

### Seller Economics

```
Seller LTV = Avg Monthly GMV × Take Rate × Gross Margin × Avg Lifetime Months

Seller CAC = (Sales + Onboarding + Incentives) / New Sellers

Seller LTV:CAC = Target 3:1+
```

### Blended CAC

```
Blended CAC = (Buyer CAC + Seller CAC) / 2
```

Or weight by which side is harder to acquire.

### Contribution Margin

```
Contribution Margin = Net Revenue - Variable Costs
                    = (GMV × Take Rate) - (Payment processing + Support + Incentives)
```

**Target**: 40-60%+ at scale

---

## Growth Metrics

### GMV Growth Decomposition

```
GMV Growth = New Buyer GMV + Existing Buyer Growth + Reactivation - Churn

Break down further:
- New Buyers × First Order Value
- Existing Buyers × Order Frequency Change × AOV Change
- Churned Buyer GMV Lost
```

### Cohort GMV Analysis

Track GMV by cohort over time:
- Month 0: First purchase
- Month 1-12: Subsequent activity
- Target: Flat or growing GMV curves

### Marketplace Maturity

| Stage | GMV | Liquidity | Focus |
|-------|-----|-----------|-------|
| Nascent | <$1M/mo | Struggling | Supply acquisition |
| Developing | $1-10M/mo | Improving | Balance both sides |
| Scaling | $10-100M/mo | Good | Efficiency, take rate |
| Mature | >$100M/mo | Strong | Expansion, adjacencies |

---

## Presenting Marketplace Metrics

### Investor Deck Essentials

1. **GMV** with growth rate
2. **Net Revenue** and take rate
3. **Liquidity metrics** (search-to-fill, utilization)
4. **Retention** (buyer and seller)
5. **Unit economics** (blended LTV:CAC)

### Avoid These Mistakes

1. Focusing only on GMV without net revenue
2. Ignoring supply-side economics
3. Not showing liquidity metrics
4. Hiding concentration risk
5. Mixing one-time and recurring GMV
