# Watchdogs for AI Systems

Watchdogs are lightweight processes that continuously verify AI services are alive, responsive, and behaving within expected bounds.

They exist to catch failures that do not trigger hard crashes.

## What Watchdogs Monitor

- Process liveness (service still running)
- Inference responsiveness (requests complete within SLA)
- Heartbeat signals (periodic health confirmation)
- Resource usage (memory, GPU, disk saturation)
- Dependency availability (vector store, filesystem, network)

## Common Failure Modes Detected

- Hung inference processes
- Silent crashes with no logs
- Gradual memory leaks
- Deadlocks during model loading
- Services running but returning empty or invalid outputs

## Watchdog Design Principles

- Lightweight and isolated from the main service
- Independent failure detection (do not rely on app logs alone)
- Fast detection with conservative thresholds
- Fail closed — assume unhealthy unless proven healthy

## Typical Watchdog Actions

- Restart unhealthy services
- Escalate after repeated failures
- Capture logs and system state before restart
- Emit structured health events for auditing

## Why Watchdogs Matter in AI Systems

AI systems often fail *silently*.
A running process does not mean a working system.

Watchdogs provide the safety net that keeps AI services operational without constant human intervention.
