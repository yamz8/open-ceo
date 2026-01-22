---
description: Generate due diligence checklist and organize DD preparation
argument-hint: [stage]
allowed-tools: Read, Write, Grep, Glob, Bash
---

Prepare for investor due diligence.

**Arguments:**
- Stage: $1 (options: pre-seed, seed, series-a, series-b, or leave blank to ask)

**Process:**

1. **Determine stage:**
   - If stage provided ($1), use that
   - Otherwise, check `.claude/fundraising.local.md` or ask

2. **Generate stage-appropriate checklist:**
   - Use the fundraising-knowledge skill's due diligence references
   - Customize based on company type (SaaS, marketplace, etc.)
   - Prioritize items by importance

3. **Assess current readiness:**
   - Ask user which documents they already have
   - Identify gaps and missing items
   - Flag urgent items that could delay closing

4. **Create action plan:**
   - Prioritized list of documents to prepare
   - Who should prepare each (founder, lawyer, accountant)
   - Estimated time to complete each
   - Dependencies between items

5. **Provide templates and guidance:**
   - Data room folder structure
   - File naming conventions
   - Common DD mistakes to avoid

**Output format:**

```markdown
# Due Diligence Preparation: [Stage]

## Checklist by Category

### Corporate (Priority: High)
- [ ] Certificate of Incorporation
- [ ] Cap table (Carta export or spreadsheet)
...

### Financial (Priority: High)
- [ ] Monthly P&L (last 24 months)
...

### Commercial (Priority: Medium)
...

## Readiness Assessment
| Category | Status | Gap |
|----------|--------|-----|
| Corporate | 80% | Missing board minutes |
...

## Action Plan

### This Week (Urgent)
1. [ ] [Task] - Owner: [Who] - Time: [Est]
2. [ ] [Task] - Owner: [Who] - Time: [Est]

### Next 2 Weeks
...

## Data Room Structure
```
📁 1. Corporate/
📁 2. Financial/
...
```

## Common Pitfalls to Avoid
1. [Pitfall]: [How to avoid]
2. ...
```

**Additional guidance:**
- Recommend data room tools (Dropbox, Google Drive, Ansarada)
- Suggest involving legal counsel for sensitive documents
- Flag items that typically delay closings
