# System Maturity Model

> Adapted from: [Organisational Maturity Path](https://playbook.thevantageproject.com/evolving/organisational-maturity-path), [Team Maturity Path](https://playbook.thevantageproject.com/evolving/organisational-maturity-path)

## Principle

The original playbook tracks organizational and team maturity. For agent systems, maturity is measured by how much the system can accomplish with decreasing human intervention.

## Maturity Levels

### Level 0: Manual
- Humans define every task
- Agents execute single steps
- All decisions require human approval
- No inter-agent coordination

### Level 1: Assisted
- Agents can decompose objectives into tasks
- Basic inter-agent communication exists
- Humans approve plans but not individual steps
- Structured logging and sync cycles operational

### Level 2: Supervised
- Agents operate semi-autonomously within defined boundaries
- Human-in-the-loop for escalations and approvals only
- Multi-agent coordination via shared protocols
- Self-improvement proposals generated and implemented (with approval)

### Level 3: Autonomous
- Agents handle most operations without human intervention
- Human oversight is strategic, not operational
- Hermes orchestrator manages agent coordination
- System self-heals from common failure modes

### Level 4: Self-Evolving
- System identifies and implements its own improvements
- New agents are provisioned and configured automatically
- Human role is governance and strategic direction only
- Playbook is a living document maintained by the system itself

## Assessment

Maturity is assessed per-capability, not globally. A system might be Level 3 for code deployment but Level 1 for customer communication. Map each domain independently and invest where the gap between current and needed maturity is largest.
