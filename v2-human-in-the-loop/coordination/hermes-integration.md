# Hermes Integration

> Status: **Planned** - This section defines the integration point for the Hermes orchestrator agent.

## What is Hermes

Hermes is the planned meta-agent that orchestrates the entire system of agents. Named after the messenger god and mediator between realms, Hermes sits above individual agents and manages:

- **Agent provisioning**: Spinning up the right agents for the right work
- **Directive routing**: Breaking high-level objectives into agent-level directives
- **Coordination**: Managing dependencies and communication between agents
- **Load balancing**: Distributing work across available agents
- **Health monitoring**: Detecting agent failures and initiating recovery
- **Escalation routing**: Deciding what goes to which human operator

## Architecture

```
         Human Operators
              │
              ▼
     ┌──────────────┐
     │    Hermes     │  ← Orchestrator (V3)
     │  Orchestrator │
     └──┬───┬───┬───┘
        │   │   │
        ▼   ▼   ▼
      ┌───┐┌───┐┌───┐
      │ A1 ││ A2 ││ A3 │  ← Individual Agents
      └───┘└───┘└───┘     (V1 Persona + V2 HITL)
```

## Integration Points

### From Hermes → Agents
- Directive assignment (with priority, deadline, context)
- Boundary configuration (what this agent is allowed to do)
- Override and kill switch commands
- Feedback and evaluation signals

### From Agents → Hermes
- Status reports and sync cycle outputs
- Escalation requests
- Completion notifications
- Self-improvement proposals
- Resource requests

### From Hermes → Humans
- Aggregated system status
- Escalations that require human judgment
- Proposals for system-level changes
- Performance reports

### From Humans → Hermes
- High-level objectives and strategy
- Approval decisions
- Boundary adjustments
- System configuration changes

## When Hermes Ships

Hermes will be developed as V3 of this playbook. Until then:
- Individual agents operate under direct human supervision (V2 model)
- Coordination between agents is manual or via simple protocols
- The patterns defined in V1 and V2 are designed to be Hermes-compatible

## Preparing for Hermes

To make current agents Hermes-ready:
1. Follow all structured formats defined in V1 and V2
2. Use consistent agent IDs and directive tracking
3. Emit machine-readable status reports
4. Implement the override and kill switch protocols
5. Keep audit trails clean and complete
