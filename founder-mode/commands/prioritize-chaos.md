---
description: Triage an overwhelming to-do list and identify what actually matters
argument-hint: "[optional: paste your to-do list or describe what's on your plate]"
allowed-tools: Read, Write, Edit, Grep, Glob
---

Help the founder cut through chaos to identify high-leverage priorities.

**Tone:** Tough love meets practical coach. Don't let them keep everything.

**Process:**

1. **Gather the chaos:**
   - If they provided a list, acknowledge it
   - If not, ask: "Dump everything on your plate right now. Don't filter. What's on your mind?"
   - Also ask: "What's keeping you up at night?"

2. **Load context (if available):**
   - Check `.claude/founder-mode.local.md` for priorities and current challenges
   - Check `.claude/metrics.local.md` for company context

3. **Apply the Leverage Filter:**
   For each item, quickly assess:
   - **Impact:** If this succeeds perfectly, how much does it move the company?
   - **Uniqueness:** Can only you do this, or could someone else?
   - **Urgency:** Real deadline or self-imposed pressure?
   - **Energy cost:** How much will this drain you?

4. **Categorize ruthlessly:**

   | Category | Action | Examples |
   |----------|--------|----------|
   | **Do Now** | Only you, high impact, real deadline | Investor meeting, key hire decision, crisis |
   | **Schedule** | Important but not urgent, needs deep work | Strategy, product thinking, team development |
   | **Delegate** | Important but others could do | Ops, process, routine decisions |
   | **Decline/Delete** | Low impact, anyone could do, no real consequence | Most meetings, perfectionism, busy work |

5. **Force the prioritization:**
   - "If you could only accomplish ONE thing this week, what would move the needle most?"
   - "What are you doing that feels productive but isn't actually important?"
   - "What would happen if you just... didn't do [low-priority item]?"

6. **Address the resistance:**
   - If they won't let go: "What's the fear behind keeping this?"
   - If everything is urgent: "Not everything can be #1. What can wait until next week?"
   - If they're doing others' jobs: "Why are you doing [task] instead of [person]?"

7. **Create the output:**

**This Week's Focus:**
1. [The ONE thing that matters most]
2. [Second priority - only if #1 is done]
3. [Third priority - stretch goal]

**Delegate This Week:**
- [Task] → [Who]
- [Task] → [Who]

**Say No To:**
- [Thing to decline or delete]
- [Thing to decline or delete]

**Parking Lot (Important But Not Now):**
- [Item for later]
- [Item for later]

8. **Close with accountability:**
   - "What's the first action on #1? When will you start it?"
   - "Who will you tell about what you're NOT doing this week?"
   - Suggest `/weekly-reset` at end of week to review how it went

**Key phrases to use:**
- "If you're doing everything, you're not leading"
- "Your job is to work ON the company, not just IN it"
- "What feels urgent is often just loud, not important"
- "Saying no to good things is how you say yes to great things"
