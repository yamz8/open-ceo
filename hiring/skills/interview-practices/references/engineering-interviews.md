# Engineering Interview Guide

## Interview Structure for Engineers

### Recommended Process

| Round | Duration | Focus | Interviewer |
|-------|----------|-------|-------------|
| Phone Screen | 30-45 min | Background, technical communication | Recruiter + engineer |
| Technical 1 | 60 min | Coding, problem-solving | Senior engineer |
| Technical 2 | 60 min | System design (Senior+) | Staff+ engineer |
| Team Fit | 45 min | Collaboration, values | Cross-functional |
| Hiring Manager | 45 min | Experience deep-dive, working style | Engineering manager |

### Adjustments by Level

**Junior/Mid:** Skip system design, focus on coding and learning ability
**Senior:** Full process including system design
**Staff+:** Add architecture discussion, cross-team collaboration scenarios

## Coding Interviews

### What to Assess

| Competency | What to Look For |
|------------|------------------|
| Problem-solving | Breaks down problems, considers edge cases |
| Code quality | Clean, readable, well-structured code |
| Testing mindset | Thinks about test cases, validation |
| Communication | Explains thinking, asks clarifying questions |
| Technical knowledge | Appropriate data structures, algorithms |

### Best Practices

**DO:**
- Use problems similar to actual work
- Allow candidates to use their preferred language
- Provide clear problem statements
- Give hints if stuck (assess how they use hints)
- Evaluate process, not just final answer

**DON'T:**
- Use trick questions or gotchas
- Require obscure algorithm knowledge
- Focus solely on optimal solutions
- Let candidates struggle silently
- Test on whiteboard (use shared editor)

### Sample Assessment Rubric

**5 - Strongly Exceeds:**
- Solves optimally with minimal hints
- Identifies and handles all edge cases
- Code is production-quality
- Excellent communication throughout

**4 - Exceeds:**
- Solves correctly, possibly suboptimal
- Handles most edge cases
- Clean code with minor issues
- Good communication

**3 - Meets:**
- Solves with some hints
- Handles obvious edge cases
- Functional code, some style issues
- Adequate communication

**2 - Below:**
- Struggles without significant help
- Misses important edge cases
- Code has bugs or major issues
- Poor communication

**1 - Does Not Meet:**
- Cannot solve with help
- Fundamental misunderstanding
- Unworkable code
- Cannot explain thinking

## System Design Interviews

### What to Assess

| Competency | What to Look For |
|------------|------------------|
| Requirements gathering | Asks clarifying questions, defines scope |
| High-level design | Appropriate components, clear architecture |
| Deep-dive ability | Can drill into specific components |
| Trade-off awareness | Understands pros/cons of choices |
| Scale thinking | Considers growth, bottlenecks |

### Format (60 min)

1. **Problem statement** (5 min)
   - Present open-ended design problem
   - Example: "Design a URL shortener" or "Design a notification system"

2. **Requirements gathering** (10 min)
   - Candidate asks questions
   - Define scope, scale, constraints
   - Agree on what to focus on

3. **High-level design** (20 min)
   - Candidate draws architecture
   - Key components and interactions
   - Data flow

4. **Deep-dive** (20 min)
   - Pick 1-2 components to explore
   - Database schema, API design, specific algorithms
   - Discuss trade-offs

5. **Extensions** (5 min)
   - "What if we needed to add X?"
   - "How would this scale to 100x?"

### Sample Problems by Level

**Senior:**
- Design a rate limiter
- Design a notification service
- Design a chat application

**Staff:**
- Design a distributed cache
- Design a real-time analytics pipeline
- Design a search engine

**Principal:**
- Design a multi-region deployment strategy
- Design a platform migration
- Design a machine learning serving system

### Evaluation Criteria

**Strong:** Drives conversation, makes reasonable choices, articulates trade-offs, handles ambiguity well

**Weak:** Needs constant prompting, makes poor choices without justification, ignores scale/reliability

## Technical Deep-Dive (Experience Interview)

### Format

Rather than coding, discuss real projects from their experience:

1. "Walk me through the most technically challenging project you've worked on"
2. Probe for specifics:
   - What was the architecture?
   - What decisions did you make?
   - What would you do differently?
3. Assess depth of involvement:
   - Did they design it or implement someone else's design?
   - How did they handle challenges?

### Questions to Ask

- "What were the key technical decisions? Why did you make those choices?"
- "What alternatives did you consider?"
- "What was the hardest bug you encountered? How did you debug it?"
- "How did you ensure quality?"
- "What would you do differently with hindsight?"

### Red Flags

- Can't explain technical details (may not have done the work)
- Takes credit for team decisions without acknowledging others
- Can't articulate trade-offs
- No awareness of what could have been better

## Engineering Manager Interviews

### What to Assess

| Competency | What to Look For |
|------------|------------------|
| Team leadership | Building, growing, retaining engineers |
| Technical judgment | Makes sound technical decisions |
| Execution | Delivers projects on time, handles risk |
| Cross-functional | Works well with PM, design, etc. |
| Communication | Clear, appropriate for audience |

### Sample Questions

**Team Building:**
- "How do you approach hiring for your team?"
- "Tell me about someone you've helped grow significantly."
- "How do you handle underperformance?"

**Technical:**
- "How do you stay technical as a manager?"
- "How do you make build vs buy decisions?"
- "How do you handle technical debt?"

**Execution:**
- "How do you prioritize work for your team?"
- "Tell me about a project that was at risk. What did you do?"
- "How do you balance feature work with reliability/tech debt?"

**Leadership:**
- "How do you create psychological safety on your team?"
- "Tell me about a difficult people situation you navigated."
- "How do you give feedback?"

## Interview Calibration

### Signs You're Well-Calibrated

- Interviewers agree most of the time
- Scores correlate with job performance
- You hire people who succeed
- You pass on people who wouldn't succeed

### Common Calibration Issues

| Issue | Symptoms | Fix |
|-------|----------|-----|
| Too lenient | Most candidates pass, some fail on job | Raise bar, train on what "good" looks like |
| Too strict | Few candidates pass, miss good hires | Review false negatives, calibrate against successful hires |
| Inconsistent | Same candidate gets different scores | More structured questions, clearer rubrics |
| Biased | Demographic patterns in scores | Training, structured interviews, diverse panels |
