---
name: rollback-release
description: Rollback the current production deployment to the previous stable release.
---

# Rollback Release

Safely rollback production to the last known good version.

## Steps

1. Identify the last stable deployment tag
2. Confirm rollback target with deployment history
3. Execute rollback:
   - Kubernetes: `kubectl rollout undo deployment/app -n production`
   - Helm: `helm rollback app 0 -n production`
4. Monitor rollout until complete
5. Verify health checks pass
6. Alert team with rollback summary and reason
