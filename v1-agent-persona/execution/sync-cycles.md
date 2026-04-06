# Sync Cycles

> Adapted from: [Weekend Syncups](https://playbook.thevantageproject.com/succeeding/weekend-syncup)

## Principle

The original playbook uses weekly syncups for goal-setting and reflection. For agents, sync cycles are the heartbeat of coordination - shorter, more frequent, and machine-structured.

## Cycle Structure

A sync cycle is a defined interval at which an agent:

1. **Reports** progress against active directives
2. **Reflects** on what worked and what didn't
3. **Replans** the next cycle based on current state

## Sync Report Format

```
## Sync Report
**Agent**: [ID]
**Cycle**: [N] | [Start] → [End]

### Completed
- [Directive/Task]: [Outcome] [Duration vs ETA]

### In Progress
- [Directive/Task]: [Status] [% Complete] [Revised ETA]

### Blocked
- [Directive/Task]: [Blocker] [Required Action] [From Whom]

### Next Cycle Plan
- [Priority-ordered list of planned work]

### Retrospective
- What worked: [...]
- What didn't: [...]
- Process improvement proposal: [...]
```

## Cycle Length

Default cycle: configurable per deployment. Suggested starting points:
- **High-frequency ops**: every task completion
- **Standard ops**: every N tasks or time interval
- **Strategic**: daily or per-sprint

The orchestrator (or human operator) sets the cycle cadence.
