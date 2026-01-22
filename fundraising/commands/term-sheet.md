---
description: Analyze and compare term sheets, explain terms, identify red flags
argument-hint: [action]
allowed-tools: Read, Write, Grep, Glob
---

Analyze term sheets for fundraising decisions.

**Arguments:**
- Action: $1 (options: analyze, compare, explain, or leave blank)

**Actions:**

### If "analyze" or no argument:
Perform a comprehensive term sheet analysis:

1. **Request term sheet details:**
   - Ask user to paste or describe key terms
   - Or read from a file if path provided

2. **Analyze economics:**
   - Valuation (pre-money, post-money)
   - Investment amount and dilution
   - Option pool (size, pre vs post-money)
   - Liquidation preference (participating vs non-participating)
   - Anti-dilution provisions

3. **Analyze control:**
   - Board composition
   - Protective provisions
   - Voting rights

4. **Identify red flags:**
   - Participating preferred
   - Multiple liquidation preferences
   - Full ratchet anti-dilution
   - Excessive protective provisions
   - Unusual terms

5. **Provide recommendation:**
   - Overall assessment (founder-friendly, standard, aggressive)
   - Key negotiation points
   - Questions to ask the investor

### If "compare":
Compare multiple term sheets:

1. Request details for each term sheet (2-3 max)
2. Create side-by-side comparison table
3. Calculate effective dilution for each
4. Model exit scenarios ($25M, $50M, $100M, $250M)
5. Recommend which offer to accept and why
6. Suggest negotiation strategy

### If "explain":
Explain specific term sheet terms:

1. Ask which term(s) to explain
2. Provide clear definition
3. Show how it affects founders
4. Give market-standard benchmarks
5. Identify if founder-friendly or investor-friendly

**Output format:**

For analysis:
```markdown
# Term Sheet Analysis: [Company/Investor]

## Summary
[Overall assessment: Founder-friendly / Standard / Aggressive]

## Economics
| Term | Value | Assessment |
|------|-------|------------|
| Pre-money | $X | [Good/Concern] |
| ... | ... | ... |

## Red Flags
- [Flag 1]: [Explanation and risk]
- [Flag 2]: ...

## Negotiation Priorities
1. [Most important to negotiate]
2. [Second priority]
3. [Third priority]

## Recommendation
[Clear recommendation with reasoning]
```

For comparison:
```markdown
# Term Sheet Comparison

## Quick Summary
| Term | Offer A | Offer B | Winner |
|------|---------|---------|--------|
| ... | ... | ... | ... |

## Exit Scenario Analysis
[Table showing founder proceeds at different exit values]

## Recommendation
[Which offer to accept and why]
```
