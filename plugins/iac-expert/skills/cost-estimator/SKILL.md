---
name: cost-estimator
description: Estimate monthly cloud costs for Terraform plans before applying. Identify expensive resources and suggest cost optimizations.
---

# Cost Estimator

## When to use

- Before applying a Terraform plan
- During architecture planning
- Monthly cost review
- When costs spike unexpectedly

## Instructions

1. Parse Terraform plan output or .tf files
2. Identify all billable resources:
   - Compute (EC2, ECS, Lambda, GKE)
   - Storage (S3, EBS, RDS, DynamoDB)
   - Networking (NAT Gateway, data transfer, load balancers)
   - Managed services (ElastiCache, SQS, CloudFront)
3. Estimate monthly cost using current pricing
4. Compare against current spend if available
5. Flag expensive resources:
   - NAT Gateways (often overlooked)
   - Data transfer costs
   - Over-provisioned instance sizes
6. Suggest cost optimizations:
   - Reserved instances for steady workloads
   - Spot instances for batch jobs
   - S3 Intelligent-Tiering
   - Right-sizing recommendations

## Output

- Cost breakdown by resource type
- Total estimated monthly cost
- Top 5 most expensive resources
- Optimization recommendations with estimated savings
