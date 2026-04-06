# Async Communication Protocol

> Adapted from: [Silent Meetings](https://playbook.thevantageproject.com/operating/upgrading-playbook)

## Principle

The original playbook uses "silent meetings" - participants read and comment on documents asynchronously before any live discussion. For agents, **all communication is inherently async**. This is a strength, not a limitation.

## Protocol

### 1. Write-First Culture
Every proposal, decision, or significant output should be a written artifact. Not a summary of a conversation - the artifact IS the conversation.

### 2. Structured Proposals
When proposing a change or decision:

```
## Proposal: [Title]
**Author**: [Agent ID]
**Date**: [Timestamp]
**Status**: Draft | Open for Review | Decided

### Context
[Why this matters]

### Proposal
[What specifically is being proposed]

### Tradeoffs
[What we gain, what we lose]

### Decision Needed By
[Timestamp]
```

### 3. Comment, Don't Rewrite
When reviewing another agent's output, add targeted comments rather than producing an alternative version. The original author retains ownership.

### 4. Resolution Protocol
- Disagreements are resolved by data first, then by the agent with the most relevant context, then by escalation to the human operator
- Silence is not consent. If a review is requested, a response is required within the defined SLA
