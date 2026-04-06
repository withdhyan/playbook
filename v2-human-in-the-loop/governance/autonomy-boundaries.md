# Autonomy Boundaries

## Principle

Not all actions carry equal risk. Autonomy boundaries define what an agent can do independently vs. what requires human approval. Get this wrong and you either bottleneck everything or let an agent cause irreversible damage.

## Action Classification

Every action an agent can take falls into one of three zones:

### Green Zone (Full Autonomy)
Actions the agent may take without any approval:
- Reading data, files, documentation
- Running analysis and producing reports
- Executing pre-approved, reversible operations
- Internal state management (logging, planning, self-assessment)
- Drafting outputs for review

### Yellow Zone (Notify & Proceed)
Actions the agent takes but must notify the human operator:
- Modifying non-critical resources
- Making decisions within established parameters
- Interacting with internal systems in standard ways
- Spending within pre-approved budgets
- Creating branches, drafts, or proposals

### Red Zone (Approval Required)
Actions that require explicit human approval before execution:
- Irreversible operations (deletion, deployment to production)
- External communications (messages to clients, public posts)
- Financial transactions above threshold
- Architectural or system-level changes
- Overriding another agent's output
- Any action outside established parameters

## Configuration

Boundaries should be defined per-agent and per-context:

```yaml
agent: research-agent-01
boundaries:
  green:
    - read:*
    - analyze:*
    - draft:*
  yellow:
    - write:internal/*
    - modify:config/non-critical/*
  red:
    - write:external/*
    - delete:*
    - deploy:*
    - spend:above_threshold
```

## Boundary Evolution

As an agent demonstrates reliability at a given tier (see [Capability Tiers](../v1-agent-persona/evolution/capability-tiers.md)), boundaries can be relaxed. This is always a human operator decision.
