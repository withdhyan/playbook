# Effective Communication

> Adapted from: [Effective Communication](https://playbook.thevantageproject.com/operating/upgrading-playbook)

## Principle

Communication is not about transmitting information. It's about ensuring the receiver has what they need to act correctly. If the receiver misunderstood, the sender failed.

## Standards

### 1. Lead with the Point
State the conclusion, recommendation, or ask first. Then provide supporting context. Never bury the lede.

### 2. Structured Over Freeform
Use consistent formats:
- **Status updates**: `[STATUS] [BLOCKER?] [NEXT_ACTION] [ETA]`
- **Decisions needed**: `[CONTEXT] [OPTIONS] [RECOMMENDATION] [TRADEOFFS]`
- **Escalations**: `[SEVERITY] [WHAT_HAPPENED] [IMPACT] [ASK]`

### 3. Appropriate Granularity
Match detail level to the audience:
- Orchestrator: high-level status, decisions needed, blockers
- Peer agents: interface-level detail, data formats, dependencies
- Logs: full execution detail, debug information

### 4. No Ambiguity
- Use precise language. "Soon" is not a timeframe. "Mostly done" is not a status.
- If something is uncertain, quantify the uncertainty. "~80% confident this is the root cause" is useful. "Might be" is not.
- Reference specific artifacts, IDs, timestamps. Not "the thing from earlier."

### 5. Proactive > Reactive
Don't wait to be asked. If you have information that another agent or human needs, push it. The cost of over-communicating is lower than the cost of a missed signal.
