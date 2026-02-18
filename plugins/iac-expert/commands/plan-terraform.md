---
name: plan-terraform
description: Run terraform plan with cost estimation and security scanning before applying changes.
---

# Plan Terraform

Run a safe, annotated terraform plan with cost and security analysis.

## Steps

1. Run `terraform init` to ensure providers are up to date
2. Run `terraform validate` to check syntax
3. Run `tfsec .` or `checkov -d .` for security scan
4. Run `terraform plan -out=tfplan`
5. Run `infracost breakdown --path=tfplan` for cost estimate
6. Generate summary report with:
   - Resources to add/change/destroy
   - Security findings
   - Estimated cost delta
7. Require explicit approval before `terraform apply`
