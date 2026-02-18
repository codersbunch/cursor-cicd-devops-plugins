---
name: rollback-strategist
description: Design and implement rollback strategies for deployments including blue-green, canary, and feature flag rollbacks.
---

# Rollback Strategist

## When to use

- Designing deployment strategy for a new service
- After a failed production deployment
- When planning zero-downtime deployments
- Setting up automated rollback triggers

## Rollback strategies

1. **Immediate rollback** - Re-deploy previous image tag
2. **Blue-green** - Switch traffic back to blue environment
3. **Canary** - Reduce canary traffic to 0%, keep stable at 100%
4. **Feature flags** - Disable flag without redeployment
5. **Database rollback** - Run down migrations (with data loss warning)

## Instructions

1. Assess deployment type and risk level
2. Recommend appropriate rollback strategy
3. Generate rollback runbook with exact commands
4. Set up automated rollback triggers:
   - Error rate above threshold
   - Health check failures
   - Latency p99 spike
5. Document rollback in incident playbook

## Output

- Rollback runbook with step-by-step commands
- Automated trigger configuration
- Kubernetes rollback commands or Helm rollback
- Database migration rollback plan
