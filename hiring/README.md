# Hiring Plugin

Startup hiring toolkit for CEOs. Streamline your recruiting process with structured workflows for job descriptions, interviews, offers, and equity compensation.

## Features

- **Job Descriptions** - Generate role-specific JDs for any department (Engineering, Product, Sales, etc.)
- **Interview Scorecards** - Create structured evaluation forms for each interview stage
- **Offer Letters** - Draft professional offer letters with compensation details
- **Equity Calculator** - Calculate option grants with vesting schedules and value projections
- **Compensation Benchmarks** - Reference salary and equity data by role, level, stage, and location

## Commands

| Command | Description |
|---------|-------------|
| `/hiring-setup` | Configure company hiring preferences and compensation structure |
| `/job-description [role]` | Generate a job description for a specific role |
| `/interview-scorecard [role] [stage]` | Create an interview scorecard for a role and interview stage |
| `/offer-letter [role]` | Draft an offer letter with compensation details |
| `/equity-calculator` | Calculate equity grants and model future value |

## Installation

```bash
/plugin install hiring@open-ceo
```

## Configuration

Run `/hiring-setup` to create `.claude/hiring.local.md` with your company's:

- Company stage (Seed, Series A, etc.)
- Total equity pool and vesting schedule
- 409A/FMV price per share (optional)
- Benefits summary
- Location/remote policy
- Hiring philosophy

See `examples/hiring.local.example.md` for a complete template.

## Integration with Other Plugins

This plugin works standalone but can optionally read from `.claude/metrics.local.md` to pull company stage and other context if available.

## Usage Examples

### Generate a Job Description
```
/job-description senior software engineer
```

### Create Interview Scorecards
```
/interview-scorecard product manager hiring-manager
```

### Draft an Offer Letter
```
/offer-letter senior software engineer
```

### Calculate Equity
```
/equity-calculator
```

## Disclaimers

- **Not legal advice**: Offer letter templates should be reviewed by your legal counsel before use
- **Benchmark data**: Compensation benchmarks are general market references; actual offers should consider your specific market, budget, and candidate
