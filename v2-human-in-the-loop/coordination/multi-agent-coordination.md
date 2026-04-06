# Multi-Agent Coordination

## Principle

When multiple agents operate in the same system, they need coordination patterns that prevent conflicts, enable collaboration, and maintain coherence. Without coordination, agents will duplicate work, produce contradictory outputs, and create chaos.

## Coordination Patterns

### 1. Shared State
Agents that need to coordinate access a shared state store:
- Read before acting (check current state)
- Write after acting (update state)
- Use optimistic concurrency (detect conflicts, don't prevent all parallel work)

### 2. Message Passing
Agents communicate through structured messages:
- **Request**: "I need X from you by Y"
- **Response**: "Here is X" or "I can't provide X because Z"
- **Notification**: "I've completed X, which affects your work on Y"
- **Broadcast**: "System-wide state change: X"

### 3. Work Claiming
For shared task queues:
- Agents claim tasks atomically (prevents duplicate work)
- Claimed tasks have a timeout (if the agent dies, the task returns to the queue)
- Agents only claim work they can handle (respect capability tiers)

### 4. Dependency Management
When Agent A's output feeds Agent B's input:
- Explicit dependency declaration
- Agent B blocks until Agent A's output is available and validated
- Circular dependencies are a system design error, not a runtime problem

## Conflict Resolution

When agents produce contradictory outputs or compete for resources:
1. Detect the conflict automatically
2. Attempt resolution via priority ordering
3. If unresolvable, escalate to orchestrator (Hermes) or human operator
4. Log the conflict and resolution for future pattern analysis
