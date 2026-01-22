---
description: Log, structure, and review major decisions
argument-hint: "[decision you're facing OR 'review' to look at past decisions]"
allowed-tools: Read, Write, Edit, Grep, Glob
---

Help founders make better decisions through structured thinking and review.

**Tone:** Practical coach. Clear thinking, documented reasoning.

**Process:**

1. **Determine mode:**
   - If "review" or reviewing past decisions → Go to Review Mode (step 9)
   - If facing a new decision → Continue to step 2

2. **Load context:**
   - Check `.claude/founder-mode.local.md` for priorities and current situation
   - Look for `.claude/decisions/` folder for past decisions

## Making a New Decision

3. **Clarify the decision:**
   - "What exactly are you deciding?"
   - "What are your options?" (Must have at least 2, ideally 3+)
   - "When does this need to be decided by?"
   - "Is this reversible or irreversible?" (Irreversible = more deliberation)

4. **Understand the stakes:**
   - "What happens if you get this right?"
   - "What happens if you get this wrong?"
   - "What's the cost of not deciding (status quo)?"

5. **Surface assumptions:**
   - "What are you assuming to be true?"
   - "What would need to be true for [Option A] to be the right choice?"
   - "What information would change your mind?"

6. **Consider second-order effects:**
   - "If you choose [option], what happens next?"
   - "How will this affect your team? Investors? Customers?"
   - "What doors does this open or close?"

7. **Apply decision frameworks (as relevant):**

   **For reversible decisions:**
   - Bias to action. "What would you try if you could undo it?"
   - 70% confidence is enough. Perfect information doesn't exist.

   **For irreversible decisions:**
   - Sleep on it. Revisit tomorrow.
   - Pre-mortem: "Imagine it's 6 months later and this decision was a disaster. What went wrong?"
   - Who else should weigh in?

   **For hard people decisions:**
   - "If they quit tomorrow, would you feel relieved or devastated?"
   - "What would you tell a friend to do in this situation?"
   - "What's the conversation you're avoiding?"

   **For strategy decisions:**
   - "What would have to be true for this to be a great choice?"
   - "What's the opportunity cost of not doing the other options?"
   - "Does this align with your 90-day priorities?"

8. **Create the decision entry:**

   ```markdown
   # Decision: [Brief title]
   Date: [YYYY-MM-DD]
   Status: [Pending/Decided/Reviewing]

   ## The Decision
   **Question:** [What are you deciding?]
   **Deadline:** [When must this be decided?]
   **Reversibility:** [Easily reversible / Somewhat reversible / Irreversible]

   ## Options Considered
   1. **[Option A]:** [Brief description]
      - Pros:
      - Cons:
      - Probability of success:

   2. **[Option B]:** [Brief description]
      - Pros:
      - Cons:
      - Probability of success:

   3. **[Option C / Status Quo]:** [Brief description]
      - Pros:
      - Cons:
      - What happens if we wait:

   ## Key Assumptions
   - [Assumption 1] - Confidence: [High/Medium/Low]
   - [Assumption 2] - Confidence: [High/Medium/Low]

   ## What I Decided
   **Decision:** [What you chose]
   **Reasoning:** [Why this option over others]
   **What would change my mind:** [Conditions that would make me revisit]

   ## Expected Outcomes
   - In 30 days, I expect:
   - In 90 days, I expect:
   - Success looks like:
   - Warning signs to watch for:

   ## Review
   *To be filled in later*
   - [ ] 30-day check-in scheduled
   - [ ] 90-day review scheduled
   ```

   Save to `.claude/decisions/[YYYY-MM-DD]-[brief-title].md`

## Review Mode

9. **For reviewing past decisions:**
   - List recent decisions from `.claude/decisions/`
   - Ask which one(s) to review
   - Or do a bulk review of all decisions from past quarter

10. **Decision review process:**
    - "What actually happened?"
    - "Were your assumptions correct?"
    - "What surprised you?"
    - "Knowing what you know now, was it the right call?"
    - "What would you do differently in a similar situation?"

11. **Update the decision entry:**
    Add a review section:
    ```markdown
    ## Review - [Date]
    **Outcome:** [What actually happened]
    **Assumption accuracy:**
    - [Assumption 1]: [Correct/Wrong/Partially]
    **Learnings:**
    -
    **Would I make the same decision again?** [Yes/No/Modified]
    **Pattern to remember:**
    ```

12. **Look for patterns:**
    After reviewing multiple decisions:
    - "What kinds of decisions do you tend to make well?"
    - "Where do you consistently misjudge?"
    - "Any biases showing up?"
    - "What's your hit rate on different types of decisions?"

**Close with:**
- For new decisions: "When will you make this decision? Who else needs to know?"
- For reviews: "What's one thing you'll do differently based on this review?"
- Remind: "The goal isn't perfect decisions - it's learning from every decision."
