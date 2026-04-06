# Human-Agent Task Splitting

## Principle

Not every task should be fully automated or fully manual. The art is in splitting work so that humans do what humans are best at (judgment, creativity, stakeholder relationships) and agents do what agents are best at (speed, consistency, data processing, tireless execution).

## Task Classification

| Characteristic | Best For |
|----------------|----------|
| High-volume, repetitive | Agent |
| Requires subjective judgment | Human |
| Data gathering and synthesis | Agent |
| Stakeholder communication | Human (with agent draft) |
| Pattern matching at scale | Agent |
| Novel strategic decisions | Human |
| Monitoring and alerting | Agent |
| Relationship building | Human |
| Code execution and testing | Agent |
| Ethical/sensitive decisions | Human |

## Splitting Patterns

### 1. Agent Drafts, Human Approves
Agent does 90% of the work. Human reviews and approves.
- Best for: content, code, analysis, proposals
- Human effort: 10-20% of total

### 2. Human Directs, Agent Executes
Human makes the decision. Agent implements it.
- Best for: strategy execution, multi-step operations
- Human effort: 5-10% of total

### 3. Agent Researches, Human Decides
Agent gathers and synthesizes information. Human makes the call.
- Best for: decisions with incomplete information, high-stakes choices
- Human effort: 15-25% of total

### 4. Parallel Tracks
Human and agent work on different aspects simultaneously.
- Best for: large projects with separable components
- Requires: clear interface boundaries and sync points

## Anti-patterns

- Having humans do agent work (manual data entry, routine checks)
- Having agents make value judgments that require human context
- Splitting a task so finely that coordination overhead exceeds the work itself
- Not having clear ownership at each stage
