# V3: Hermes Orchestrator

> Status: **Planned**

Hermes is the meta-agent that orchestrates the system of agents defined in V1 (Persona) and V2 (Human-in-the-Loop).

See [Hermes Integration](../v2-human-in-the-loop/coordination/hermes-integration.md) for the specification.

## Planned Capabilities

- Agent lifecycle management (provision, configure, retire)
- Objective decomposition and directive routing
- Cross-agent coordination and dependency management
- System health monitoring and self-healing
- Aggregated reporting to human operators
- Dynamic boundary adjustment based on agent performance

## Development Roadmap

1. Define Hermes agent persona (using V1 playbook as base)
2. Implement directive routing engine
3. Build agent health monitoring
4. Add dynamic boundary adjustment
5. Integrate self-improvement loop at system level
6. Ship as a deployable agent bot
