---
name: github-actions-writer
description: Write complete GitHub Actions workflows for CI, CD, release automation, and scheduled tasks. Supports any language and cloud provider.
---

# GitHub Actions Writer

## When to use

- Setting up CI/CD for a new project
- Migrating from Jenkins/CircleCI to GitHub Actions
- Adding new pipeline stages (security scan, performance test)
- Automating release workflows

## Instructions

1. **Detect project type** from package.json, requirements.txt, go.mod, etc.
2. **Generate CI workflow** with:
   - Dependency caching
   - Lint and type check
   - Unit and integration tests
   - Coverage reporting
   - Security scanning
3. **Generate CD workflow** with:
   - Build and push Docker image
   - Deploy to staging on merge to develop
   - Deploy to production on release tag
   - Post-deploy health check
   - Slack/email notification
4. **Add reusable workflows** for shared steps
5. **Configure branch protection** rules recommendation

## Output

Complete `.github/workflows/` directory with:
- `ci.yml` - Test and lint on every PR
- `cd-staging.yml` - Deploy to staging on merge
- `cd-production.yml` - Deploy to production on release
- `security.yml` - Weekly security scans
