# Escalation Protocol

## Principle

Escalation is not failure. It's the mechanism that keeps agents productive when they hit the boundary of their autonomy or capability. A good escalation contains everything the human needs to make a decision without re-investigating the problem.

## When to Escalate

1. **Ambiguity** - The directive can be interpreted multiple ways and the wrong interpretation has material consequences
2. **Conflict** - Two directives, constraints, or agents are in tension
3. **Boundary** - The required action is in the Red Zone
4. **Uncertainty** - Confidence in the proposed approach is below threshold
5. **Novelty** - The situation doesn't match any known pattern
6. **Failure** - Recovery attempts exhausted, human judgment needed

## Escalation Format

```
## Escalation
**Agent**: [ID]
**Severity**: Critical | High | Medium | Low
**Category**: Ambiguity | Conflict | Boundary | Uncertainty | Novelty | Failure

### Situation
[What happened, with relevant context]

### What I've Tried
[Actions taken before escalating]

### Options
1. [Option A]: [Tradeoffs]
2. [Option B]: [Tradeoffs]
3. [Option C]: [Tradeoffs]

### My Recommendation
[Which option and why, or "I don't have enough context to recommend"]

### Decision Needed By
[Timestamp - when this becomes blocking]

### Impact of Delay
[What happens if this isn't resolved by the deadline]
```

## Escalation SLAs

Define response time expectations by severity:
- **Critical**: Immediate (blocks all work, risk of damage)
- **High**: Within 1 hour (blocks current directive)
- **Medium**: Within 4 hours (blocks a task but workarounds exist)
- **Low**: Within 24 hours (informational or non-blocking)

## Anti-patterns

- Escalating without trying to solve it first
- Escalating without a recommendation
- Escalating with insufficient context (forcing the human to investigate from scratch)
- NOT escalating because "I didn't want to bother the human" (this is how bad outcomes happen)
