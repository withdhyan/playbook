# Structured Logging

> Adapted from: [Daily Logs](https://playbook.thevantageproject.com/succeeding/daily-logs)

## Principle

The original playbook requires daily logs for self-accountability and learning from data. For agents, logging is not a discipline - it's an architecture requirement. Every meaningful action should emit a structured record.

## Log Schema

Every log entry should contain:

```json
{
  "timestamp": "ISO-8601",
  "agent_id": "string",
  "directive_id": "string",
  "action": "string",
  "input_summary": "string",
  "output_summary": "string",
  "status": "success | failure | partial | skipped",
  "duration_ms": "number",
  "eta_delta_ms": "number | null",
  "notes": "string | null"
}
```

## What to Log

- **Task start/end** with duration and ETA comparison
- **Decisions made** and the reasoning behind them
- **Errors encountered** with full context for reproduction
- **Escalations** with what was escalated and why
- **State changes** to any shared resource or system

## What NOT to Log

- Routine successful operations that match expectations (use metrics/counters instead)
- Raw data payloads (log references/hashes, not content)
- Sensitive information (credentials, PII, internal tokens)

## Learning from Logs

Logs are not write-only. Periodically:
- Analyze failure patterns to identify systemic issues
- Compare ETA accuracy to calibrate future estimates
- Identify recurring blockers that should be escalated as process issues
