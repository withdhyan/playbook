# Approval Gates

## Principle

Approval gates are checkpoints where agent work pauses for human review before proceeding. They exist to catch errors before they become costly and to maintain human agency over critical decisions.

## Gate Types

### 1. Plan Approval
Before execution of a complex directive, the agent presents its plan:
- Decomposed tasks
- Proposed approach for each
- Resource requirements
- Risk assessment
- ETA

The human reviews and either approves, modifies, or rejects.

### 2. Output Review
Before delivering a critical output:
- Agent produces the output in draft state
- Human reviews for correctness, tone, completeness
- Agent incorporates feedback and re-submits or proceeds

### 3. Commit Gate
Before making irreversible changes:
- Agent presents the exact change to be made
- Human confirms or denies
- Agent executes only upon confirmation

### 4. Spend Gate
Before consuming significant resources:
- API calls above cost threshold
- Long-running compute operations
- External service invocations with billing implications

## Gate Configuration

```yaml
gates:
  plan_approval:
    trigger: directive_complexity > "medium"
    reviewer: human_operator
    timeout: 4h
    on_timeout: pause

  output_review:
    trigger: output_destination == "external"
    reviewer: human_operator
    timeout: 2h
    on_timeout: pause

  commit_gate:
    trigger: action_zone == "red"
    reviewer: human_operator
    timeout: 1h
    on_timeout: pause
```

## While Waiting

When an agent is blocked at a gate:
- Continue work on other non-blocked directives
- Prepare follow-up work that will be needed after approval
- Do NOT proceed without approval, even if the timeout expires (pause, don't assume)
