# Health Checks for AI Services

Health checks are used to verify that AI services are alive, responsive, and producing valid outputs.

## What to Check
- Process liveness (service running)
- Inference responsiveness (request → response within threshold)
- Memory / resource saturation
- Model load state
- Dependency availability (vector store, disk, network)

## Failure Signals
- Hung inference requests
- Silent failures with no errors
- Gradual latency degradation
- Memory growth over time

## Response Strategy
- Restart unhealthy services
- Escalate after repeated failures
- Log state before restart for post-incident analysis
