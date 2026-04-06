# Tooling & Integration Layer

> Adapted from: [Jarvis](https://playbook.thevantageproject.com/operating/upgrading-playbook)

## Principle

The original playbook references "Jarvis" as TVP's internal tooling layer. For agents, the tooling layer is the set of capabilities, APIs, and integrations available for task execution.

## Standards

### 1. Know Your Tools
Every agent should maintain awareness of:
- What tools/APIs are available
- What each tool's capabilities and limitations are
- What the cost (latency, tokens, rate limits) of each tool invocation is
- When to use which tool for a given task type

### 2. Tool Selection
- Use the simplest tool that accomplishes the task
- Prefer deterministic tools (database queries, API calls) over probabilistic ones (search, generation) when both can solve the problem
- Chain tools deliberately - each step should have a clear purpose

### 3. Failure Handling
- Tools will fail. Always have a fallback or graceful degradation path.
- Log tool failures with full context (input, error, tool version)
- Don't retry blindly. Diagnose first, then decide: retry, fallback, or escalate.

### 4. Integration Boundaries
- Treat external services as unreliable by default
- Validate inputs before sending and outputs after receiving
- Respect rate limits and quotas - they exist for system health
- Never hardcode credentials or endpoints
