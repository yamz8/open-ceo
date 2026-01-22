---
description: Generate a board meeting agenda
argument-hint: [meeting-duration-hours]
allowed-tools: Read, Write, AskUserQuestion
---

Generate a professional board meeting agenda for a VC-backed startup.

## Context Gathering

Check for company configuration at `.claude/board-prep.local.md` for board member information and meeting details.

If meeting duration not provided via argument ($1), default to 2 hours.

## Agenda Structure

Create an agenda following this standard structure, adjusting time allocations based on meeting duration:

### For 2-hour meeting:
| Section | Duration | Purpose |
|---------|----------|---------|
| Opening & Administrative | 5 min | Approvals, minutes |
| CEO Update | 20 min | Executive summary, highlights, challenges |
| Financial Review | 20 min | Metrics, P&L, runway |
| Business Update | 15 min | Progress on strategic priorities |
| Go-to-Market | 15 min | Sales, marketing, customer success |
| Product & Engineering | 10 min | Roadmap, releases |
| Strategic Discussion | 25 min | Deep-dive on 1-2 key topics |
| Team Update | 5 min | Headcount, key changes |
| Board Asks & Wrap-up | 5 min | Decisions, action items |

### For 90-minute meeting:
Condense to: Opening (5), CEO Update (15), Financial (15), GTM & Product (15), Strategic Discussion (20), Team & Asks (10), Buffer (10)

### For 3-hour meeting:
Expand strategic discussion to 45 min, add separate product demo section (15 min), add closed session (15 min)

## Agenda Content

For each section, include:
- Time slot and duration
- Section owner/presenter
- Key topics to cover
- Materials reference (slide numbers)

## Additional Components

Include in the agenda document:
- Meeting logistics (date, time, location/video link)
- Attendee list (board members, invited guests)
- Pre-read materials list with send date
- Post-meeting deliverables with owners and due dates
- Next meeting date placeholder

## Output

Write the agenda to a file (ask user for preferred location, default: `docs/board-agenda-[date].md`).

Reference the sample agenda template in the startup-board-prep skill examples for formatting guidance.
