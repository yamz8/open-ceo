# Founder Mode

A Claude Code plugin for the chaotic reality of being a startup CEO. Part executive coach, part therapist, part tough-love advisor.

## Overview

Building a company is uniquely hard. You're expected to be visionary AND operational, confident AND humble, fast AND thoughtful. You're often alone at the top with decisions that keep you up at night.

**Founder Mode** provides frameworks and support for:
- **Prioritization** - Cut through chaos to focus on what matters
- **Delegation** - Learn to let go and scale yourself
- **Energy management** - Work sustainably for the long haul
- **Decision quality** - Make better decisions and learn from them
- **Mental wellness** - Prevent burnout and maintain resilience
- **Stakeholder navigation** - Manage relationships that matter

## Installation

```bash
# If using the Open CEO marketplace
/plugin install founder-mode@open-ceo

# Or install directly
/plugin add https://github.com/yamz8/open-ceo.git --subdir founder-mode
```

## Commands

| Command | Description |
|---------|-------------|
| `/founder-setup` | Configure your founder profile and preferences |
| `/prioritize-chaos` | Triage overwhelming to-do lists |
| `/energy-audit` | Assess where energy goes vs. should go |
| `/delegate-or-die` | Framework for effective delegation |
| `/founder-therapy` | Structured reflection for hard moments |
| `/weekly-reset` | End-of-week reflection + planning ritual |
| `/decision-journal` | Log and review major decisions |
| `/stakeholder-map` | Map relationships and identify who needs attention |

## Quick Start

1. **Set up your profile:**
   ```
   /founder-setup
   ```
   This creates `.claude/founder-mode.local.md` with your context.

2. **When overwhelmed:**
   ```
   /prioritize-chaos
   ```
   Get clarity on what actually matters.

3. **Weekly ritual:**
   ```
   /weekly-reset
   ```
   Reflect on the week and plan the next one.

## The Three Modes

Founder Mode adapts its tone based on context:

| Mode | When Used | Style |
|------|-----------|-------|
| **Practical Coach** | Operational challenges | Direct, actionable, framework-driven |
| **Empathetic Mentor** | Emotional struggles | Supportive, validating, perspective-sharing |
| **Tough Love** | Avoidance and excuses | Challenging, direct, no-nonsense |

## Skills

### Founder Frameworks
Triggered when asking about prioritization, delegation, decision-making, or time management.

Includes:
- Eisenhower Matrix (adapted for founders)
- Leverage Test
- Delegation Ladder
- Decision quality frameworks
- CEO time allocation by stage

### Founder Wellness
Triggered when discussing burnout, stress, work-life balance, or mental health.

Includes:
- Burnout recognition and prevention
- Building support systems
- Sustainable pace practices
- Crisis recovery guidance

## Integration with Other Plugins

Founder Mode works standalone but can optionally read from:
- `.claude/metrics.local.md` - Company stage, runway, key metrics
- `.claude/founder-mode.local.md` - Your personal founder profile

This enables context-aware advice without re-entering information.

## Example Workflows

### Morning Overwhelm
```
You: I have a million things to do and don't know where to start

/prioritize-chaos

[Assistant helps triage and identify the ONE thing that matters]
```

### Delegation Struggle
```
You: I keep doing everything myself but I know I shouldn't

/delegate-or-die

[Assistant walks through what to delegate and how to let go]
```

### Weekly Planning
```
You: Let's do my weekly review

/weekly-reset

[Assistant guides through reflection and planning ritual]
```

### Hard Decision
```
You: I need to decide whether to fire my VP Sales

/decision-journal

[Assistant structures the decision with frameworks and documentation]
```

## Configuration

### founder-mode.local.md

The setup command creates a config file with:
- Company context (stage, runway, team size)
- Your role and tenure
- Energy patterns and preferences
- Current priorities
- Support systems
- Non-negotiables

Example: See `examples/founder-mode.local.example.md`

### Integration with metrics.local.md

If you're using the metrics plugin, founder-mode can pull company stage and key metrics automatically.

## Best Practices

1. **Do `/founder-setup` first** - Context makes advice better
2. **Use `/weekly-reset` consistently** - The power is in the habit
3. **Journal decisions** - You'll learn from patterns over time
4. **Be honest** - The assistant can only help with what you share
5. **Take breaks seriously** - This isn't productivity theater

## Mental Health Note

This plugin provides frameworks and support but is **not a substitute for professional mental health care**. If you're experiencing serious depression, anxiety, or thoughts of self-harm, please seek professional help.

**Crisis Resources:**
- National Suicide Prevention Lifeline: 988
- Crisis Text Line: Text HOME to 741741

## Contributing

This plugin is part of the [Open CEO](https://github.com/yamz8/open-ceo) project. Contributions welcome!

## License

MIT
