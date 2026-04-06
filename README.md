# The Vantage Project - Agent Playbook

An agent-native adaptation of [The Vantage Project PlayBook](https://playbook.thevantageproject.com), stripped of human-level scaffolding (compensation, time-off, hiring) and restructured for autonomous agent operations.

## Versions

| Version | Purpose | Status |
|---------|---------|--------|
| [Agent Persona](./v1-agent-persona/) | Instruct agent identity, principles, and behavioral standards | Active |
| [Human-in-the-Loop](./v2-human-in-the-loop/) | Operations framework for agents working under human oversight | Active |
| Hermes Orchestrator | Meta-agent that orchestrates the system of agents | Planned |

## Architecture

```
┌─────────────────────────────────────────┐
│            Hermes (Orchestrator)         │
│         system-level coordination        │
├──────────────┬──────────────────────────┤
│  Agent Persona  │  Human-in-the-Loop Ops │
│  (v1: identity) │  (v2: oversight model)  │
└──────────────┴──────────────────────────┘
```

## What was removed from the original PlayBook

The original TVP PlayBook is designed for humans. This version strips:

- **Compensation & Pay** - Agents don't get paid
- **Applying / Joining** - Agents are instantiated, not hired
- **Work Schedule / Time Off** - Agents operate continuously
- **Short-Term Hires / Guest Co-passengers** - Not applicable
- **6-Month Audit** - Replaced with continuous self-evaluation loops

## What was adapted

| Original (Human) | Agent Version |
|-------------------|---------------|
| A-Player Attributes | Agent Excellence Standards |
| Daily Logs | Structured Logging Protocol |
| Weekend Syncups | Sync Cycles |
| DKRs & Goal Setting | Objectives & Directives |
| Feedback Loops | Feedback Loops (preserved) |
| ETA Culture | ETA Culture (preserved) |
| Silent Meetings | Async Communication Protocol |
| Effective Communication | Effective Communication (preserved) |
| Jarvis (internal tool) | Tooling & Integration Layer |
| Upgrading Playbook | Self-Improvement Protocol |
| Long-term Games | Long-term Alignment |
| Problem Solver/See-er Paths | Agent Capability Tiers |
| Org/Team Maturity | System Maturity Model |

## GitBook

This playbook is structured for [GitBook](https://www.gitbook.com/) hosting. Each version contains its own `SUMMARY.md` for navigation.

## License

Internal use - The Vantage Project.
