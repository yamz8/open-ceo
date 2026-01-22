---
description: Framework for deciding whether to pivot and how to execute it
argument-hint: "[optional: 'assess' to evaluate, 'plan' to execute]"
allowed-tools: Read, Write, Edit, Grep, Glob
---

Help founders decide whether to pivot and, if so, how to execute the transition.

**Tone:** Thoughtful and structured. Pivots are existential decisions that deserve rigor.

**Process:**

1. **Understand where they are:**
   - "What's driving the pivot consideration?"
   - "How long have you been working on the current direction?"
   - "What have you learned about why it's not working?"

2. **Load context:**
   - Check `.claude/metrics.local.md` for runway, growth metrics
   - Understanding cash position is critical for pivot timing

## Part 1: Should You Pivot?

3. **Distinguish pivot from iteration:**

   | Iteration | Pivot |
   |-----------|-------|
   | Improving what exists | Fundamental change in direction |
   | Same target customer | Different customer or problem |
   | Optimizing product | Different product or model |
   | Normal startup evolution | Strategic reset |

   "Is this really a pivot, or is it iteration that feels dramatic because it's hard?"

4. **Apply the pivot decision framework:**

   **Signals it might be time to pivot:**
   - Consistent negative feedback from target customers
   - Can't find product-market fit after significant effort
   - Market turned out smaller than expected
   - Unsustainable unit economics that won't improve
   - Team has lost conviction in the direction
   - Discovered a bigger opportunity through current work

   **Signals to persevere instead:**
   - Some customers love it, just not enough yet
   - Haven't truly tested the core hypothesis
   - Execution issues rather than strategy issues
   - Giving up too early due to impatience
   - Running from hard problems rather than toward better opportunities

5. **The pivot or persevere questions:**

   | Question | Pivot Signal | Persevere Signal |
   |----------|--------------|------------------|
   | Do any customers love this? | No strong advocates | Yes, even if few |
   | Is the problem real? | Problem doesn't resonate | Problem is real, solution is off |
   | Can you reach customers? | Distribution is impossible | Distribution is hard but possible |
   | Can economics ever work? | Fundamentally broken | Need scale to work |
   | Does team believe? | Lost conviction | Still believe, frustrated |
   | Is there a bigger opportunity? | Clear better path | Grass-is-greener thinking |

6. **Assess your runway:**
   - How many months of runway do you have?
   - How long would a pivot take to show results?
   - Do you need to raise? Can you raise in current state vs. pivoted state?

   **Rule of thumb:** You need 12+ months of runway to pivot effectively. Less than that and you're probably better off raising first or winding down.

## Part 2: Deciding Where to Pivot

7. **Identify pivot options:**

   **Types of pivots:**
   | Type | What Changes | Example |
   |------|--------------|---------|
   | Customer segment | Who you serve | SMB to Enterprise |
   | Problem | What you solve | Scheduling → Communication |
   | Solution | How you solve it | Software → Services |
   | Channel | How you reach customers | Direct → Partner |
   | Revenue model | How you make money | Subscription → Transaction |
   | Technology | Core tech platform | Build → Buy |
   | Zoom in | Focus on one feature | Full suite → One tool |
   | Zoom out | Feature becomes platform | Tool → Platform |

8. **Evaluate pivot directions:**

   For each option, assess:
   - What evidence do we have that this will work?
   - What's our unfair advantage in this direction?
   - How much of what we've built carries over?
   - How does the team feel about this direction?
   - What's the market size and competition?

9. **Make the pivot decision:**

   **Decision framework:**
   ```
   If you have strong evidence AND team conviction AND runway → Pivot to best option
   If you have weak evidence but strong hypothesis → Test before full pivot
   If team has lost all conviction → Pivot or wind down
   If runway is short → Raise first or wind down
   ```

## Part 3: Executing the Pivot

10. **Plan the pivot:**

    **Key decisions:**
    - Hard pivot (stop everything) vs. soft pivot (parallel path)?
    - What do we keep vs. abandon?
    - How do we handle existing customers?
    - What does the team look like post-pivot?

11. **Communicate the pivot:**

    **To the team:**
    - Be honest about what's not working
    - Share the reasoning behind the new direction
    - Acknowledge this is hard
    - Get buy-in vs. just announcing
    - Allow questions and concerns

    **Script:**
    > "I want to talk about where we're headed. [Current direction] isn't working as we hoped. Here's what we've learned... Based on that, we're going to [new direction]. This is why we believe it's the right move... I know this is a big change. Here's what it means for the team..."

    **To investors/board:**
    - Inform before you tell the team (they should hear from you)
    - Share the data and reasoning
    - Present the new plan
    - Ask for their support
    - Be prepared for hard questions

    **To existing customers:**
    - If you're discontinuing their product, give notice
    - Help them transition
    - Honor commitments where possible
    - Maintain relationships for the future

12. **Execute the transition:**

    **Week 1-2:**
    - Announce internally
    - Begin winding down old work
    - Define new priorities
    - Identify what carries over

    **Week 3-4:**
    - Ship something in new direction (momentum matters)
    - Release team members who don't fit new direction
    - Communicate externally as needed

    **Month 2-3:**
    - Full focus on new direction
    - Set new milestones
    - Regular check-ins on whether it's working

13. **Create the pivot plan:**

    ```markdown
    # Pivot Decision & Plan
    Date: [YYYY-MM-DD]
    Status: [Evaluating/Decided/Executing]

    ## Current State
    - Direction: [Current product/market]
    - Why it's not working: [Specific reasons]
    - Runway: [X months]

    ## Decision
    - [ ] Persevere with current direction
    - [ ] Pivot to: [New direction]
    - [ ] Wind down

    ## If Pivoting

    ### New Direction
    - Target customer: [Who]
    - Problem: [What]
    - Solution: [How]
    - Why we believe: [Evidence]

    ### What We Keep
    - [Technology, relationships, learnings that carry over]

    ### What We Stop
    - [Products, features, efforts to abandon]

    ### Timeline
    | Week | Actions |
    |------|---------|
    | 1 | Announce, begin transition |
    | 2 | Wind down old, spin up new |
    | 3-4 | First delivery in new direction |
    | 8 | Checkpoint - is this working? |

    ### Communication Plan
    - Team: [When, how]
    - Board: [When, how]
    - Investors: [When, how]
    - Customers: [When, how]

    ### Success Criteria
    - By [date], we will know this is working if: [Specific metrics]
    - If not working by [date], we will: [Next action]
    ```

14. **Close with perspective:**
    - "Many great companies pivoted - Slack, Instagram, YouTube. A pivot isn't failure."
    - "The hardest part is the decision. Execution is just work."
    - "Trust your judgment. You know more about this than anyone."

**Key principles:**
- Pivot toward something, not just away from something
- One decisive pivot is better than many small ones
- Preserve what's working even as you change direction
- Communication is as important as strategy
- Give the new direction a real chance before evaluating
