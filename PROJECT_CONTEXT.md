
# CloudGRC-Auditor — Project Context

## Project Overview
Open-source AWS Security & IT Audit automation tool.

## Project Status
Phase: 1 — Architecture and Environment Setup
Status: In progress

## Approved Decisions
- ADR-001: Modular Python CLI architecture approved.
- MVP v0.1.0: Scope approved.
- Development roadmap: 7 phases approved.

## Technology Stack
- AWS
- Python / Boto3
- Terraform
- Pytest
- GitHub Actions
- JSON / Markdown

## Local Environment
- OS: Pop!_OS
- Terraform: 1.16.6
- AWS CLI: 2.38.2
- AWS Region: us-east-1

## AWS Environment

### AWS Organizations
- AWS Organizations: Enabled
- Organization Features: All Features
- Management Account: jessicapicarelli
- Member Account: cloudgrc-lab (Active)
- Centralized Root Access: Enabled
- Root MFA: Enabled (Management Account)
- Member Account Root Credentials: Verified — no root password or access keys (TESTED)

### IAM Identity Center
- IAM Identity Center: Organization Instance
- Identity Center Region: us-east-1
- Identity Center User: jessica_picarelli
- Identity Center MFA: Configured and tested
- Identity Center MFA Policy: Always-on
- AWS Access Portal Login: Tested successfully with MFA

### AWS Account Access
- Administrative Permission Set: CloudGRCLabAdmin
- Permission Set Policy: AdministratorAccess
- Permission Set Session Duration: 1 hour
- Permission Set Assignment: cloudgrc-lab
- Assigned User: jessica_picarelli
- Member Account Console Access: Tested successfully via IAM Identity Center
- AWS CLI SSO Profile: cloudgrc-lab-admin
- SSO Session Name: cloudgrc-sso
- SSO Region: us-east-1
- Default Client Region: us-east-1
- CLI Output Format: json
- AWS CLI SSO Authentication: TESTED (STS GetCallerIdentity successful)

## Approved Security Principles
- Principle of least privilege
- Temporary AWS credentials
- Read-only security auditing
- No permanent credentials in source code
- No insecure public resources by default
- Evidence-based audit conclusions

## Architecture
Status: Approved (ADR-001)

Planned components:
- Terraform laboratory
- Python evidence collectors
- Security control evaluation engine
- GRC risk classification
- JSON and Markdown reports

## Completed
- Terraform installed
- AWS CLI v2 installed
- Legacy local AWS credentials cleared
- AWS Organizations verified
- IAM Identity Center instance verified
- IAM Identity Center MFA configured and tested
- AWS Member Account created
- Centralized Root Access enabled
- Administrative Permission Set created and assigned
- IAM Identity Center console access to Member Account tested successfully
- Member Account root password and access keys verified absent via AWS CLI
- AWS CLI SSO profile configured and authentication tested successfully
- Terraform laboratory directory initialized (`infra/`)
- Terraform AWS Provider version requirements configured
- Terraform initialization validated (`terraform init -backend=false`)
- Terraform configuration validated (`terraform fmt -check` and `terraform validate`)
- Terraform dependency lock file committed
- Terraform AWS Provider configured with IAM Identity Center SSO
- Terraform AWS Provider restricted to cloudgrc-lab using allowed_account_ids
- Terraform AWS Provider authentication validated using aws_caller_identity
- Terraform plan executed successfully without infrastructure changes

## Pending
- Review Terraform laboratory
- Implement and test infrastructure
- Define and validate Terraform state management strategy

## Technical Decisions
Record approved architectural decisions here.

## Known Issues
None confirmed.

## Next Step
Define and validate a secure Terraform state management strategy before provisioning AWS infrastructure.
