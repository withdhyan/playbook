# Audit Trail

## Principle

Every action an agent takes under human oversight must be traceable. If something goes wrong, the human operator needs to reconstruct exactly what happened, what decisions were made, and why.

## What Gets Recorded

| Event | Required Fields |
|-------|----------------|
| Directive received | Source, content, timestamp, acceptance |
| Plan created | Tasks, approach, ETA, risk assessment |
| Approval requested | Gate type, what was submitted, timestamp |
| Approval granted/denied | Reviewer, decision, reasoning, timestamp |
| Action executed | Type, target, input, output, duration |
| Escalation raised | Category, severity, content, timestamp |
| Escalation resolved | Resolution, resolved_by, timestamp |
| Handoff | From, to, context summary, timestamp |
| Error/Failure | Action, error, recovery attempted, outcome |

## Immutability

Audit records must be append-only. An agent cannot modify or delete its own audit trail. This is enforced at the infrastructure level, not by the agent's good behavior.

## Retention

Audit trails should be retained for the lifetime of the system plus a defined buffer period. They serve both operational debugging and compliance needs.

## Access

- Agents can read their own audit trail (for self-improvement)
- The orchestrator can read all audit trails
- Human operators have full access
- No agent can modify another agent's audit trail
