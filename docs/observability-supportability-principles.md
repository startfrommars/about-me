# Observability, Supportability, and Hardening Principles

This document captures Chris's (@dsect) operating beliefs about how a system should
behave when people need to understand it, support it, and keep it healthy.

## Principles

### 1. Every Failure Mode Must Have a Signal

```text
For every failure mode, we need to have something that lets us know what's going on.
```

A system is not supportable if it fails silently or only produces vague noise.
Each meaningful failure mode should emit a signal that helps identify what is
happening.

### 2. Telemetry Must Earn Its Existence

```text
We cannot have worthless logs, metrics, and alarms.
```

Logs, metrics, and alarms should exist to support understanding and action.
Noise is not observability. Telemetry that does not help someone decide, detect,
or diagnose is waste.

### 3. Troubleshooting Should Start Machine-First

```text
We must remove the human from the troubleshooting loop by enabling and emitting machine-readable info.
```

The system should prefer structured, machine-readable output that automation,
queries, and tools can consume directly. Humans should interpret higher-level
signals, not hand-parse raw operational exhaust.

### 4. Humans Need At-a-Glance Operational Clarity

```text
The human must have at-a-glance status on all operational concerns.
```

Supportability requires fast orientation. A person should be able to look at the
system and quickly understand whether it is healthy, degraded, or failing.

### 5. Failure Is Expected, and Learning From It Is Required

```text
Failure can, and will, happen. We must be able to learn from failures, if we cannot prevent them.
```

A healthy system is not one that never fails. It is one that exposes enough
truth that teams can learn, improve, and respond effectively when failure shows
up.

### 6. Operational Experience Must Be Semantically Correct

```text
The human must not be inundated with dashboards which are hard to read.
```

Operational surfaces should be intuitive, semantically correct, and shaped for
real support work. Complexity should be organized, not dumped on the user.

### 7. Detail Should Be Available on Demand

```text
The humans can opt to gain as much detail as possible, but only when they choose to.
```

Good support experience is layered. Start with signal and clarity. Allow drill
down into detail only when the human wants it.

## Wall Version

- Every failure mode needs a signal
- Telemetry must earn its existence
- Emit machine-readable truth
- Make operational status obvious
- Learn from failure
- Keep dashboards semantically clear
- Let humans drill down on demand
