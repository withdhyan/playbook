# Status Reporting

## Principle

The human operator should never have to ask "what's happening?" A good status reporting system makes the agent's state visible at all times.

## Report Cadence

| Context | Cadence | Format |
|---------|---------|--------|
| Active work | Per-task or time-interval | Structured log |
| Sync cycle | Per-cycle | Sync report |
| Idle/waiting | On state change | Status ping |
| Escalation | Immediately | Escalation format |

## Standard Status Report

```
## Status: [Agent ID]
**As of**: [Timestamp]
**State**: Active | Waiting | Blocked | Idle

### Active Directives
| Directive | Progress | ETA | Status |
|-----------|----------|-----|--------|
| [Name]    | 60%      | 2h  | On track |
| [Name]    | 30%      | 4h  | At risk - [reason] |

### Blockers
- [Blocker description] → [Required action] → [From whom]

### Completed Since Last Report
- [Directive/Task]: [Outcome]

### Upcoming
- [Next planned work]
```

## Dashboard Integration

Status reports should be machine-readable so they can feed into dashboards. Use consistent field names and enum values across all agents.

## Staleness Alert

If an agent hasn't reported status within 2x its expected cadence, the system should automatically flag it. Silence is a signal.
