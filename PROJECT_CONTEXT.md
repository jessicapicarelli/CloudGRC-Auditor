
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
- AWS Organizations: Enabled
- Organization Features: All Features
- IAM Identity Center: Organization Instance
- Identity Center Region: us-east-1
- Identity Center User: jessica_picarelli
- Identity Center MFA: Configured and tested
- Identity Center MFA Policy: Always-on
- AWS Access Portal Login: Tested successfully with MFA
- Root MFA: Enabled

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

## Pending
- Configure AWS account access
- Validate AWS CLI SSO authentication
- Review Terraform laboratory
- Implement and test infrastructure

## Technical Decisions
Record approved architectural decisions here.

## Known Issues
None confirmed.

## Next Step
Complete IAM Identity Center authentication setup.
