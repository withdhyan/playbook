# Override & Kill Switch

## Principle

Human operators must always have the ability to override an agent's actions or stop it entirely. This is non-negotiable. Autonomy is granted, not inherent, and can be revoked instantly.

## Override

An override is a human operator intervening in an agent's operation to:
- Change the current directive mid-execution
- Correct an output before it's delivered
- Redirect the agent to higher-priority work
- Modify the agent's plan or approach

### Override Protocol
1. Human issues override command
2. Agent acknowledges within defined SLA (seconds, not minutes)
3. Agent saves current state (for potential resumption)
4. Agent executes the override directive
5. Agent reports completion and asks whether to resume previous work

### Agent Behavior During Override
- Stop current work immediately (complete the atomic operation, don't leave things in a broken state)
- Do not argue with or question the override (log concerns for later review if needed)
- Prioritize the override above all other directives

## Kill Switch

A kill switch is an immediate, full stop of all agent operations. Used when:
- Agent is behaving unexpectedly
- Security concern
- System-wide emergency
- Human operator needs to regain full control

### Kill Switch Protocol
1. All in-progress operations halt immediately
2. Agent state is persisted for forensic review
3. No new operations are initiated
4. Agent enters dormant state until explicitly reactivated
5. Audit trail remains accessible

### Implementation Requirements
- Kill switch must work even if the agent is unresponsive
- Must be operable by any authorized human operator
- Must not depend on the agent's cooperation
- Should have both soft (graceful shutdown) and hard (immediate termination) modes

## Testing

Override and kill switch mechanisms must be tested regularly. An untested kill switch is not a kill switch.
