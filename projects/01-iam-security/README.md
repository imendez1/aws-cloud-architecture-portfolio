# Project 01 — AWS IAM Security Fundamentals

## Project Overview

This project documents hands-on experience with AWS Identity and Access Management (IAM), focusing on secure access management, authentication, authorization, IAM policy evaluation, and least-privilege security practices.

**Learning Resource:** Neal Davis — AWS Certified Solutions Architect Associate (SAA-C03)

**WGU Course:** D319 — AWS Cloud Architecture

**Project Status:** Completed — November 16, 2026

**Scope:** AWS IAM course section, including supported hands-on exercises and security analysis.

## Project Objectives

- Understand AWS IAM users, groups, roles, and policies.
- Differentiate authentication from authorization.
- Implement least-privilege access controls where supported.
- Understand multi-factor authentication (MFA).
- Explore IAM permissions boundaries and AWS Organizations SCPs.
- Evaluate IAM permissions using the IAM Policy Simulator.
- Configure and validate AWS CLI access.
- Document security best practices and architectural decisions.

## Development Environment

| Component | Technology |
|---|---|
| Cloud Platform | Amazon Web Services (AWS) |
| AWS Account | AWS Free Plan |
| AWS Region | US East (Ohio) — us-east-2 |
| Operating System | Windows |
| Development Environment | Visual Studio Code |
| Version Control | Git and GitHub |
| Command-Line Tools | AWS CLI v2, PowerShell, AWS CloudShell |

## Hands-On Labs

| Lab | Description | Status |
|---|---|---|
| 01 | AWS account setup and security review | Partially Completed |
| 02 | IAM user creation and permission management | Completed |
| 03 | IAM policies and least-privilege concepts | Completed — Conceptual |
| 04 | IAM roles and temporary credentials | Completed — Conceptual |
| 05 | AWS CLI authentication and verification | Completed |
| 06 | IAM Policy Simulator — EC2 and S3 | Completed |
| 07 | IAM MFA configuration | Restricted by Account |

## Implementation and Validation

### IAM User and Permission Management

- Created an IAM test user named `Isaac`.
- Attached the AWS-managed `AdministratorAccess` policy for training.
- Reviewed the user's permissions and security credentials.
- Removed `AdministratorAccess` after completing the exercise.
- Investigated IAM administration restrictions affecting group creation and console sign-in configuration.

### IAM Policy Simulator

Used the IAM Policy Simulator to evaluate permissions for the test IAM user.

| AWS Service | Actions Tested | Allowed | Denied |
|---|---:|---:|---:|
| Amazon EC2 | 834 | 0 | 834 |
| Amazon S3 — GetObject | 1 | 0 | 1 |

**Observed Result:** The simulator reported that the selected actions were denied by AWS Organizations.

These results demonstrate how organization-level permission guardrails can affect IAM authorization decisions.

### AWS CLI and CloudShell

- Configured AWS CLI tools for the learning environment.
- Used AWS CloudShell to execute AWS CLI commands.
- Verified the active AWS identity using AWS STS.
- Investigated an IAM `AccessDenied` error.
- Identified an explicit deny attributed to an AWS Organizations Service Control Policy.

### MFA and IAM Account Restrictions

The AWS Free Plan environment restricted certain IAM administration activities.

Observed limitations included:

- IAM group creation was unavailable.
- IAM console password configuration was not offered during test-user creation.
- MFA enrollment could not be completed for the test IAM user.
- An IAM API operation was denied by an AWS Organizations SCP.

These restrictions were documented rather than bypassed.

## Architecture and Security Considerations

The project reinforced the following security principles:

- **Least Privilege:** Grant only the permissions necessary to perform a task.
- **Temporary Credentials:** Prefer IAM roles and temporary credentials over embedded long-term access keys.
- **MFA:** Protect privileged identities using additional authentication factors.
- **Permissions Boundaries:** Limit the maximum permissions available through identity-based policies.
- **Service Control Policies:** Establish permission guardrails across AWS accounts.
- **Policy Evaluation:** Understand the differences between explicit allow, implicit deny, and explicit deny.
- **Identity Federation:** Prefer centralized workforce access management where appropriate.

## Lessons Learned

1. IAM users do not receive permissions automatically when created.
2. IAM policies use JSON statements to define allowed and denied actions.
3. Permissions boundaries restrict permissions but do not grant them.
4. AWS Organizations SCPs can restrict actions even when broad IAM permissions exist.
5. The IAM Policy Simulator provides a useful environment for evaluating authorization decisions.
6. Temporary credentials and IAM roles are preferable to embedding long-term access keys in applications.
7. AWS account restrictions can affect hands-on exercises, making documentation and troubleshooting important parts of cloud administration.
8. Administrative permissions should be removed when they are no longer required.

## Project Outcome

Completed Section 2 — AWS Identity and Access Management (IAM) of the SAA-C03 training course.

Gained hands-on experience with IAM user creation, permission assignment and removal, AWS CLI troubleshooting, IAM policy simulation, and analysis of AWS Organizations restrictions.

Some IAM configuration exercises could not be completed because of training-account limitations. These restrictions are documented as part of the learning experience.

## Security Notice

No AWS access keys, passwords, authentication tokens, or other sensitive credentials will be published in this repository.

All screenshots and command outputs will be reviewed before publication to avoid exposing sensitive account identifiers, credentials, or session information.