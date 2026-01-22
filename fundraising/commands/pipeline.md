---
description: Track and manage investor pipeline (add, update, view status)
argument-hint: [action] [investor]
allowed-tools: Read, Write, Edit, Grep, Glob
---

Manage investor pipeline for fundraising.

**Arguments:**
- Action: $1 (options: add, update, view, summary, or leave blank for summary)
- Investor: $2 (investor name for add/update actions)

**Pipeline storage:**
Store pipeline in `.claude/fundraising.local.md` under a `## Pipeline` section.

**Pipeline stages:**
1. `researching` - Identifying fit, gathering info
2. `outreach` - Initial contact sent
3. `meeting-scheduled` - First meeting booked
4. `partner-meeting` - Met with partnership
5. `dd` - In due diligence
6. `term-sheet` - Received term sheet
7. `passed` - Investor passed
8. `closed` - Deal closed

**Actions:**

### If "add" or adding new investor:
1. Ask for investor details:
   - Investor/firm name
   - Contact person and email
   - Stage (default: researching)
   - Source (cold, warm intro, inbound)
   - Notes (optional)

2. Add to pipeline in `.claude/fundraising.local.md`

### If "update":
1. Find investor in pipeline
2. Ask what to update:
   - Stage progression
   - Add meeting notes
   - Update contact info
   - Mark as passed (with reason)

3. Update the entry with timestamp

### If "view":
1. Show all investors in current pipeline
2. Group by stage
3. Show days in current stage

### If "summary" or no argument:
1. Show pipeline overview:
   - Total investors by stage
   - Recent activity (last 7 days)
   - Stale conversations (no activity in 14+ days)
   - Next actions needed

**Output format:**

For summary:
```markdown
# Fundraising Pipeline Summary

## Overview
- Total active: X investors
- Term sheets: X
- In DD: X
- Meetings scheduled: X

## By Stage
| Stage | Count | Key Names |
|-------|-------|-----------|
| Term Sheet | 1 | Acme Ventures |
| DD | 2 | Beta Capital, Gamma... |
...

## Needs Attention
- [Investor]: No activity in 14 days - follow up?
- [Investor]: Meeting was 7 days ago - check status

## Recent Activity (Last 7 Days)
- [Date]: [Investor] moved to [stage]
- [Date]: Added [Investor]
...

## Next Actions
1. [ ] Follow up with [Investor] (last contact: X days)
2. [ ] Schedule meeting with [Investor]
3. [ ] Send DD docs to [Investor]
```

For view:
```markdown
# Full Pipeline

## Term Sheet (1)
### Acme Ventures
- Contact: Sarah Smith (sarah@acme.vc)
- Source: Warm intro from John
- Days in stage: 3
- Notes: $25M pre, clean terms

## Due Diligence (2)
### Beta Capital
...
```

**Pipeline entry format in .local.md:**
```yaml
pipeline:
  - name: "Acme Ventures"
    contact: "Sarah Smith"
    email: "sarah@acme.vc"
    stage: "term-sheet"
    source: "warm"
    added: "2024-01-15"
    last_updated: "2024-01-20"
    notes: "$25M pre, clean terms"
```
