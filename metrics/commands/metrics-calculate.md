---
description: Calculate derived metrics from raw inputs
argument-hint: [metric]
allowed-tools: Read, Write, Grep, Glob
---

Calculate derived metrics from raw inputs.

**Arguments:**
- Metric: $1 (options: ltv, cac-payback, burn-multiple, magic-number, rule-of-40, nrr, all, or leave blank for interactive)

**Process:**

1. **If specific metric requested, calculate that metric:**

   **LTV (Customer Lifetime Value)**:
   ```
   Inputs needed: ARPU, Gross Margin, Monthly Churn Rate
   Formula: LTV = ARPU × Gross Margin / Monthly Churn Rate
   ```

   **CAC Payback**:
   ```
   Inputs needed: CAC, ARPU, Gross Margin
   Formula: CAC Payback (months) = CAC / (ARPU × Gross Margin)
   ```

   **LTV:CAC Ratio**:
   ```
   Inputs needed: LTV, CAC (or inputs to calculate both)
   Formula: LTV:CAC = LTV / CAC
   ```

   **Burn Multiple**:
   ```
   Inputs needed: Net Burn (monthly), Net New ARR (monthly)
   Formula: Burn Multiple = (Net Burn × 12) / (Net New ARR × 12)
             Or simply: Monthly Net Burn / Monthly Net New ARR
   ```

   **Magic Number**:
   ```
   Inputs needed: Current Quarter ARR, Prior Quarter ARR, Prior Quarter S&M Spend
   Formula: Magic Number = (Current Q ARR - Prior Q ARR) / Prior Q S&M Spend
   ```

   **Rule of 40**:
   ```
   Inputs needed: YoY Revenue Growth Rate, Profit Margin (or EBITDA margin)
   Formula: Rule of 40 = Growth Rate (%) + Profit Margin (%)
   ```

   **NRR (Net Revenue Retention)**:
   ```
   Inputs needed: Starting MRR, Expansion MRR, Contraction MRR, Churned MRR
   Formula: NRR = (Starting MRR + Expansion - Contraction - Churn) / Starting MRR × 100
   ```

   **GRR (Gross Revenue Retention)**:
   ```
   Inputs needed: Starting MRR, Contraction MRR, Churned MRR
   Formula: GRR = (Starting MRR - Contraction - Churn) / Starting MRR × 100
   ```

2. **If "all" or no argument, offer menu:**
   - List available calculations
   - Let user select which to calculate
   - Gather inputs for each
   - Calculate and display results

3. **Gather inputs:**
   - Check `.claude/metrics.local.md` for existing values
   - Ask user for any missing inputs
   - Validate inputs (positive numbers, percentages as decimals or %)

4. **Calculate and explain:**
   - Show the formula
   - Show the calculation with actual numbers
   - Display the result
   - Provide interpretation (good/bad/neutral for this stage)
   - Compare to benchmark if available

**Output format:**

```markdown
# Metric Calculation: [Metric Name]

## Inputs
| Input | Value | Source |
|-------|-------|--------|
| ARPU | $X | User provided |
| Gross Margin | X% | User provided |
| Monthly Churn | X% | User provided |

## Calculation
```
LTV = ARPU × Gross Margin / Monthly Churn
LTV = $500 × 0.80 / 0.02
LTV = $20,000
```

## Result
**LTV = $20,000**

## Interpretation
- Benchmark for [stage]: $15,000 - $25,000
- Your LTV is in the healthy range ✅
- This means each customer is worth $20,000 over their lifetime

## Related Metrics
With this LTV and a CAC of $X, your LTV:CAC would be X:1
```

**Batch mode:**
If calculating multiple metrics, show a summary table at the end with all results.
