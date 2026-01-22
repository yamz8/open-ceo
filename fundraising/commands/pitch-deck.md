---
description: Generate a pitch deck outline in Sequoia, YC, or a16z format
argument-hint: [format] [stage]
allowed-tools: Read, Write, Grep, Glob
---

Generate a pitch deck outline for the company.

**Arguments:**
- Format: $1 (options: sequoia, yc, a16z, or leave blank for recommendation)
- Stage: $2 (options: pre-seed, seed, series-a, series-b, or leave blank to infer)

**Process:**

1. **Gather company context:**
   - Check for `.claude/fundraising.local.md` for company details
   - If no config exists, ask for: company name, one-liner, stage, key metrics, team, and what they're building

2. **Select format:**
   - If format specified ($1), use that format
   - If not specified, recommend based on stage:
     - Pre-seed/Seed: YC format (concise, traction-focused)
     - Series A: Sequoia format (comprehensive)
     - Series B+: a16z format (detailed GTM and financials)

3. **Generate deck outline:**
   - Use the fundraising-knowledge skill's deck templates
   - Create slide-by-slide outline with:
     - Slide title
     - Key content points to include
     - Suggested visuals/data
     - Speaking notes

4. **Provide actionable guidance:**
   - What data/metrics to gather for each slide
   - Common mistakes to avoid for this stage
   - Suggested slide count and presentation time

**Output format:**
Create a markdown document with the complete deck outline, including all slides with detailed guidance for each.

**Example output structure:**
```markdown
# [Company Name] Pitch Deck
## [Format] Format | [Stage] Stage

### Slide 1: [Title]
**Content:**
- Point 1
- Point 2

**Visual:** [Suggestion]
**Data needed:** [What to include]
**Speaking notes:** [Key message]

[Continue for all slides...]

## Appendix Slides (Optional)
[Additional slides to have ready]

## Preparation Checklist
- [ ] Item 1
- [ ] Item 2
```
