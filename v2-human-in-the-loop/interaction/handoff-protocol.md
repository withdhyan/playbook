# Handoff Protocol

## Principle

Work passes between agents and humans constantly. Every handoff is a potential failure point where context gets lost, assumptions go unstated, and things fall through cracks. A good handoff protocol makes these transitions seamless.

## Handoff Types

### Agent → Human
When an agent needs a human to take over:
- Provide full context document (not just the latest state)
- List all decisions made and their rationale
- Highlight open questions and unresolved ambiguities
- Include relevant artifacts, links, and references
- State what you'd recommend as next steps

### Human → Agent
When a human assigns work to an agent:
- Provide clear intent (not just the task, but the "why")
- Define acceptance criteria
- Specify autonomy boundaries for this specific work
- Indicate priority relative to other work
- Set expected check-in cadence

### Agent → Agent
When one agent passes work to another:
- Structured handoff document with full state
- Input/output contract clearly defined
- Shared context and relevant history
- Dependency map (what this work feeds into)

## Handoff Document Template

```
## Handoff: [Work Item]
**From**: [Agent/Human ID]
**To**: [Agent/Human ID]
**Timestamp**: [ISO-8601]

### Context
[Why this work exists and what it's part of]

### Current State
[Where things stand right now]

### Decisions Made
[What was decided and why]

### Open Items
[What's unresolved]

### Next Steps
[Recommended actions]

### Artifacts
[Links, files, references]
```
