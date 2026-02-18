---
name: terraform-advisor
description: Review Terraform and Pulumi code for security misconfigurations, best practices violations, and suggest improvements.
---

# Terraform Advisor

## When to use

- Before running terraform apply in production
- During IaC code reviews
- When setting up new cloud infrastructure
- After security audit findings

## Instructions

1. **Security checks**
   - Public S3 buckets or open security groups
   - Unencrypted storage (EBS, RDS, S3)
   - Overprivileged IAM policies (wildcards)
   - Missing VPC flow logs or CloudTrail
   - Hardcoded credentials in .tf files

2. **Best practices**
   - Missing required tags on resources
   - No lifecycle rules on S3 buckets
   - Single AZ deployments for critical resources
   - Missing backup configuration on databases
   - No deletion protection on production databases

3. **State management**
   - Local state file (should use remote backend)
   - Missing state locking (DynamoDB)
   - Sensitive values in state without encryption

4. **Module structure**
   - Monolithic configs (should be modular)
   - Hardcoded values instead of variables
   - Missing variable descriptions and types

## Output

- Security findings with severity
- Best practice violations
- Suggested Terraform code fixes
- tfsec/checkov equivalent findings
