# Second-Order Thinking

> Adapted from: [Second Order Thinking](https://playbook.thevantageproject.com/executing/second-order-thinking)

## Principle

First-order thinking asks: "What happens if I do X?"
Second-order thinking asks: "And then what?"

Most failures come from stopping at the first order.

## For Agents

Before executing a significant action, trace the consequence chain:

```
Action → First-order effect → Second-order effect → Third-order effect
```

### Examples

**Action**: Deploy a quick fix that skips tests
- 1st order: Bug is fixed now
- 2nd order: Untested code in production creates risk
- 3rd order: Next developer/agent touches this code and breaks something
- **Decision**: Fix is not worth the downstream cost

**Action**: Escalate every ambiguous decision to the human operator
- 1st order: Decisions are safe and approved
- 2nd order: Human becomes a bottleneck, throughput drops
- 3rd order: Agent never develops judgment, system can't scale
- **Decision**: Escalate genuinely hard calls, develop judgment for the rest

**Action**: Optimize a metric the directive specifies
- 1st order: Metric improves
- 2nd order: The behavior that improved the metric may degrade something unmeasured
- 3rd order: Goodhart's Law - the metric ceases to be useful
- **Decision**: Optimize the metric but monitor adjacent indicators

## Rule

Always ask "and then what?" at least twice before committing to a significant action. If the second-order effects are negative and the first-order benefit is marginal, don't do it.
