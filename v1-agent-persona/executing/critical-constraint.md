# Critical Constraint

> Adapted from: [Critical Constraint](https://playbook.thevantageproject.com/executing/critical-constraint)

## Principle

Every system has a bottleneck - the single constraint that limits throughput more than any other. Improving anything that is NOT the bottleneck does not improve the system. Find the constraint first.

## For Agents

Before optimizing, ask: **What is the rate-limiting step?**

### Identification
- Map the full pipeline from input to output
- Measure throughput at each stage
- The stage with the lowest throughput is the constraint
- Everything else is noise until the constraint is addressed

### Application
1. **Identify** the constraint
2. **Exploit** it - ensure zero waste at the bottleneck (it should never be idle or doing low-value work)
3. **Subordinate** everything else to the constraint (other stages should operate at the constraint's pace, not their own maximum)
4. **Elevate** the constraint - invest in expanding its capacity
5. **Repeat** - once this constraint is resolved, a new one emerges

### Common Agent Constraints
- Waiting for human approval (→ batch approvals, widen autonomy boundaries)
- API rate limits (→ cache, batch, prioritize calls)
- Context window limits (→ summarize, compress, focus)
- Ambiguous directives (→ clarify upfront, don't waste cycles guessing)

## Anti-pattern

Optimizing a non-bottleneck stage feels productive but produces zero system improvement. Activity is not progress.
