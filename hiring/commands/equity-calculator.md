---
description: Calculate equity grants with vesting schedules, current value, and future projections
argument-hint: [role] [level]
allowed-tools: Read, Grep, Glob
---

Calculate equity compensation for a role or specific grant.

**Arguments:**
- Role: $1 (optional, for benchmark comparison)
- Level: $2 (optional: junior, mid, senior, staff, manager, director, vp, c-level)

**Process:**

1. **Load company context:**
   - Check `.claude/hiring.local.md` for equity structure and 409A data
   - Key fields needed:
     - `total_shares_outstanding` (for % calculations)
     - `fmv_per_share` (for current value)
     - `preferred_price_per_share` (for context)
     - `standard_vesting_years` and `cliff_months`
     - `remaining_equity_pool_percent` (to check if grant is feasible)

2. **Determine calculation mode:**

   **Mode A: Grant sizing (role/level provided)**
   - Look up benchmark equity ranges for role and level at company stage
   - Suggest grant size as % of company
   - Convert to shares if `total_shares_outstanding` available

   **Mode B: Grant analysis (specific numbers provided)**
   - Ask for: number of options OR percentage
   - Calculate the other value if shares outstanding known

3. **Generate equity analysis:**

   **Grant Summary:**
   | Field | Value |
   |-------|-------|
   | Number of Options | [X,XXX] |
   | % of Company (fully diluted) | [X.XX%] |
   | Strike Price (409A FMV) | $[X.XX] |
   | Vesting Schedule | [4 years, 1-year cliff] |

   **Current Value Analysis:**
   (If 409A data available)
   - Current FMV value: Options × FMV = $[X,XXX]
   - "Paper gain" at preferred price: Options × (Preferred - FMV) = $[X,XXX]
   - Note: Options have no guaranteed value and cannot be sold until a liquidity event

   **Future Value Projections:**
   Model at various exit multiples (assuming preferred price as baseline):

   | Exit Multiple | Company Valuation | Share Price | Grant Value | After Tax* |
   |---------------|-------------------|-------------|-------------|------------|
   | 2x | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |
   | 5x | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |
   | 10x | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |

   *Assumes long-term capital gains (20%) + state tax estimate. Actual taxes depend on many factors.

   **Dilution Modeling (optional):**
   If user provides expected future fundraising:
   - Show how grant % changes with dilution
   - Typical dilution: 15-25% per round

   **Benchmark Comparison:**
   (If role/level provided)
   - Show typical equity ranges for this role/level at company stage
   - Compare proposed grant to 25th, 50th, 75th percentile

   | Percentile | Equity (%) | This Grant |
   |------------|-----------|------------|
   | 25th | [X.XX%] | |
   | 50th (median) | [X.XX%] | [X.XX%] ← |
   | 75th | [X.XX%] | |

   **Vesting Schedule Breakdown:**
   | Period | Shares Vested | Cumulative | % of Grant |
   |--------|---------------|------------|------------|
   | Year 1 (cliff) | [X,XXX] | [X,XXX] | 25% |
   | Year 2 | [X,XXX] | [X,XXX] | 50% |
   | Year 3 | [X,XXX] | [X,XXX] | 75% |
   | Year 4 | [X,XXX] | [X,XXX] | 100% |

4. **Provide context and caveats:**
   - Options are not shares - must be exercised (purchased) to own
   - Strike price is typically the 409A FMV at grant date
   - Explain ISO vs NSO basics if relevant
   - Note that projections are illustrative, not guaranteed
   - Recommend candidate consult financial advisor

**Output format:**

```markdown
# Equity Calculator

## Grant Summary

| Field | Value |
|-------|-------|
| Number of Options | [X,XXX] |
| % of Company | [X.XX%] |
| Strike Price | $[X.XX] |
| Vesting | [4] years, [1]-year cliff |

## Current Value

| Metric | Value |
|--------|-------|
| FMV Value | $[X,XXX] |
| Spread at Preferred | $[X,XXX] |

## Future Value Scenarios

| Scenario | Company Value | Share Price | Gross Value | After Tax* |
|----------|---------------|-------------|-------------|------------|
| 2x exit | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |
| 5x exit | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |
| 10x exit | $[X]M | $[X.XX] | $[X,XXX] | $[X,XXX] |

*Estimated. Assumes LTCG + 5% state tax. Actual taxes vary.

## Vesting Schedule

| Period | Vests | Cumulative |
|--------|-------|------------|
| Month 12 (cliff) | [X,XXX] | [X,XXX] (25%) |
| Month 24 | [X,XXX] | [X,XXX] (50%) |
| Month 36 | [X,XXX] | [X,XXX] (75%) |
| Month 48 | [X,XXX] | [X,XXX] (100%) |

## Benchmark Comparison

[Role] at [Stage] companies:

| Percentile | Typical Equity |
|------------|----------------|
| 25th | [X.XX%] |
| 50th | [X.XX%] |
| 75th | [X.XX%] |

**This grant ([X.XX%])** is at the [Xth] percentile.

---

## Important Notes

- **Options ≠ shares**: You have the right to purchase shares at the strike price
- **Exercise cost**: To own shares, you'll pay [shares] × $[strike] = $[X,XXX]
- **Taxes**: Exercise and sale may trigger taxable events (consult a tax advisor)
- **Projections are illustrative**: Actual outcomes depend on company performance and exit terms
```

**If 409A data not available:**
Explain that without 409A/FMV data, calculations will be shown as percentages only, and dollar values can't be computed. Encourage running `/hiring-setup` to add this data.
