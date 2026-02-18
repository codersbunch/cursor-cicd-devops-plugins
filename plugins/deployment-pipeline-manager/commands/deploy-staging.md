---
name: deploy-staging
description: Build, test, and deploy the current branch to the staging environment with health check verification.
---

# Deploy to Staging

Build and deploy the current branch to staging.

## Steps

1. Run full test suite - abort if any fail
2. Build Docker image tagged with branch name and git SHA
3. Push image to container registry
4. Apply Kubernetes manifests or Helm upgrade to staging namespace
5. Wait for rollout to complete
6. Run health check against staging URL
7. Run smoke tests against staging
8. Post deployment summary with URL and version
