# Metrics Plugin

A comprehensive metrics toolkit for startup CEOs. Track, calculate, and benchmark SaaS and marketplace metrics. Part of the [Open CEO](https://github.com/yamz8/open-ceo) marketplace.

## Features

- **Metrics Setup**: Configure which metrics to track based on your business model and stage
- **Metrics Snapshot**: Generate current metrics reports for different audiences
- **Benchmarking**: Compare your metrics to stage and industry benchmarks
- **Calculations**: Calculate derived metrics (LTV, CAC Payback, Burn Multiple, etc.)
- **Shared Config**: Metrics integrate with other Open CEO plugins

## Installation

```bash
# Install via Claude Code marketplace
claude mcp add marketplace:metrics@open-ceo
```

Or add manually to your Claude Code configuration.

## Commands

| Command | Description |
|---------|-------------|
| `/metrics-setup [model] [stage]` | Configure metrics tracking |
| `/metrics-snapshot [format]` | Generate metrics report |
| `/metrics-benchmark [stage]` | Compare to benchmarks |
| `/metrics-calculate [metric]` | Calculate derived metrics |

### Examples

```bash
# Set up metrics for a Series A SaaS company
/metrics-setup saas series-a

# Generate a full metrics snapshot
/metrics-snapshot full

# Get investor-ready metrics summary
/metrics-snapshot investor

# Benchmark against Series A standards
/metrics-benchmark series-a

# Calculate LTV:CAC ratio
/metrics-calculate ltv
```

## Supported Business Models

### SaaS Metrics
- **Revenue**: MRR, ARR, New/Expansion/Churned MRR
- **Growth**: MoM/YoY growth, NRR, GRR
- **Unit Economics**: CAC, LTV, LTV:CAC, CAC Payback
- **Efficiency**: Burn Multiple, Magic Number, Rule of 40
- **Customers**: Logo count, churn rate, ARPU

### Marketplace Metrics
- **Volume**: GMV, Net Revenue, Take Rate, AOV
- **Liquidity**: Search-to-Fill, Time-to-Fill, Utilization
- **Supply/Demand**: Active buyers/sellers, B:S ratio
- **Retention**: Repeat rate, Seller retention
- **Economics**: Buyer/Seller LTV:CAC, Contribution margin

## Configuration

Create `.claude/metrics.local.md` with your metrics:

```yaml
---
company_name: "YourCo"
business_model: "saas"
stage: "series-a"

mrr: 185000
nrr: 112
gross_margin: 78
burn_multiple: 1.8
---
```

See `examples/metrics.local.example.md` for complete templates.

## Integration with Other Plugins

This plugin's config (`.claude/metrics.local.md`) is designed to be read by other Open CEO plugins:

```
              ┌─────────────┐
              │   Metrics   │ ← Single source of truth
              └──────┬──────┘
         ┌──────────┼──────────┐
         ▼          ▼          ▼
   Fundraising  Board Prep  Investor Updates
```

When you update metrics here, they flow automatically to:
- **Fundraising**: Pitch deck metrics sections
- **Board Prep**: Board deck KPI slides
- **Investor Updates**: Monthly metrics snapshots

## Benchmarks Included

Stage-appropriate benchmarks for:
- Pre-seed through Series C+
- SaaS by segment (SMB, Mid-Market, Enterprise)
- Marketplace by category
- Industry-specific targets

## Related Plugins

- **[Fundraising](../fundraising)**: Use metrics in pitch decks
- **[Board Prep](../board-prep)**: Board meeting metrics
- **[Investor Updates](../investor-updates)**: Monthly metrics reports

## License

MIT
