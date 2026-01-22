# Crisis Playbook

A Claude Code plugin for navigating the hardest moments in a startup's life. Layoffs, pivots, down rounds, PR crises, and existential threats - with frameworks, communication templates, and step-by-step guidance.

## Overview

Every startup faces crises. How you handle them determines whether the company survives and what kind of leader you become. This plugin provides battle-tested frameworks for:

- **Assessing crises** - Understand severity and appropriate response
- **Executing layoffs** - With dignity, legal compliance, and clear communication
- **Making pivot decisions** - Frameworks for when to pivot and how to execute
- **Navigating down rounds** - Protect what matters while getting funded
- **Responding to PR crises** - When to respond, how to respond, and when to stay silent
- **Restructuring and turnaround** - Cost cutting, bridge financing, and recovery

## Installation

```bash
# If using the Open CEO marketplace
/plugin install crisis-playbook@open-ceo

# Or install directly
/plugin add https://github.com/yamz8/open-ceo.git --subdir crisis-playbook
```

## Commands

| Command | Description |
|---------|-------------|
| `/crisis-assess` | Assess crisis severity and determine response |
| `/layoff-plan` | Plan and execute a reduction in force |
| `/pivot-decision` | Framework for deciding whether and how to pivot |
| `/down-round-prep` | Navigate raising at a lower valuation |
| `/pr-response` | Respond to PR crises and reputation threats |

## Quick Start

1. **When crisis hits, start with assessment:**
   ```
   /crisis-assess
   ```
   This will categorize the crisis and point you to the right next steps.

2. **For specific situations, go directly to the relevant command:**
   - Considering layoffs? → `/layoff-plan`
   - Product not working? → `/pivot-decision`
   - Can't raise at last valuation? → `/down-round-prep`
   - Bad press or social media crisis? → `/pr-response`

## Skills

### Crisis Communication
Triggered when asking about communicating bad news, stakeholder messaging, or crisis announcements.

Includes:
- Layoff announcement scripts
- Pivot communication templates
- Board and investor notification templates
- Customer communication templates

### Restructuring Guide
Triggered when asking about restructuring, turnaround, cost cutting, or winddown.

Includes:
- Cost reduction playbook
- Runway extension strategies
- Turnaround frameworks
- Winddown checklist

## Example Workflows

### Considering Layoffs
```
You: I think we need to do layoffs

/layoff-plan

[Assistant guides through decision validation, planning, execution, and communication]
```

### Facing a PR Crisis
```
You: There's negative press about us circulating on Twitter

/pr-response

[Assistant helps assess severity, decide whether to respond, and craft appropriate messaging]
```

### Need to Pivot
```
You: Our current product isn't getting traction. Should we pivot?

/pivot-decision

[Assistant walks through pivot vs persevere framework and, if pivoting, execution plan]
```

## Integration with Other Plugins

Crisis Playbook works standalone but can read from:
- `.claude/metrics.local.md` - For runway, burn rate, team size context
- `.claude/crisis-playbook.local.md` - Your crisis-specific configuration

This enables context-aware guidance without re-entering information.

## Important Notes

### This Is Not Legal Advice

This plugin provides frameworks and guidance, not legal advice. For serious matters:
- **Layoffs**: Consult employment counsel
- **Restructuring**: Consult corporate counsel
- **Down rounds**: Work with your lawyers and advisors
- **PR crises**: Consider professional PR support for major issues

### Confidentiality

Be thoughtful about what you share. While Claude doesn't retain conversations:
- Don't include specific employee names in layoff planning
- Be careful with material non-public information
- Treat sensitive situations appropriately

### Mental Health

Crises are hard on founders. If you're struggling:
- Use `/founder-therapy` from the founder-mode plugin
- Consider professional support (therapist, coach)
- Lean on your support network

## Philosophy

This plugin is built on core principles:

1. **Crises are defining moments** - How you handle them matters
2. **Speed matters, but so does doing it right** - Don't skip important steps
3. **Communication is as important as action** - How you tell people matters
4. **Protect people even in hard situations** - Treat everyone with dignity
5. **Most companies face crises** - You're not alone, and you can get through this

## Contributing

This plugin is part of the [Open CEO](https://github.com/yamz8/open-ceo) project. Contributions welcome!

## License

MIT
