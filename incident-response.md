# Incident Response for AI Systems

AI incidents are operational events where inference, reliability, or observability degrades.

## Common Incidents
- Inference hangs or timeouts
- Missing or corrupted logs
- Model process crashes
- Degraded performance without alerts

## Response Flow
1. Detect via health checks or alerts
2. Capture system state and logs
3. Restart or recover affected services
4. Validate recovery
5. Document incident and prevention steps

## Goal
Restore service quickly while preserving enough context to prevent recurrence.
