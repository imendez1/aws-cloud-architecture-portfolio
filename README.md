
# AWS Cloud Architecture Portfolio

Hands-on AWS cloud architecture projects demonstrating networking, security, automation, high availability, and infrastructure design.

## About This Portfolio

This repository documents my hands-on learning and practical experience with Amazon Web Services (AWS).

The projects focus on cloud architecture, identity and access management, security, networking, compute services, monitoring, and infrastructure automation.

I am currently pursuing a Bachelor of Science in Cloud and Network Engineering at Western Governors University (WGU), following the AWS specialization.

**Certification Path:** AWS Certified Cloud Practitioner (Completed) → AWS Certified Solutions Architect – Associate (In Progress) → AWS Certified CloudOps Engineer – Associate (Planned)

## AWS Projects

### Project 01 — AWS IAM Security Fundamentals

**Status:** Completed — November 16, 2026

**AWS Services and Technologies:** AWS IAM, AWS Organizations, AWS STS, AWS CLI, AWS CloudShell, IAM Policy Simulator.

**Project Summary:**

Explored AWS Identity and Access Management (IAM), including authentication, authorization, IAM users, permissions policies, least-privilege security, MFA concepts, permissions boundaries, and Service Control Policies (SCPs).

**Hands-On Activities:**

- Created and managed an IAM test user.
- Assigned and subsequently removed administrative permissions.
- Investigated IAM authorization restrictions.
- Tested EC2 and S3 permissions using the IAM Policy Simulator.
- Created a sample least-privilege Amazon S3 JSON policy.
- Documented AWS Organizations restrictions encountered during the exercises.

[View Project 01 — AWS IAM Security Fundamentals](projects/01-iam-security/README.md)

---

### Project 02 — Amazon EC2 Compute and Networking

**Status:** In Progress — Started November 17, 2026

**AWS Region:** US East (Ohio) — us-east-2

**AWS Services and Technologies:** Amazon EC2, Amazon VPC, IAM Roles, AWS STS, Amazon CloudWatch, EC2 User Data, EC2 Instance Metadata, Security Groups.

**Project Summary:**

Deployed, configured, secured, monitored, and managed Amazon EC2 instances running Linux and Windows Server.

Explored EC2 networking, remote connectivity, automated instance initialization, instance metadata security, IAM roles, CloudWatch monitoring, and resource management.

**Hands-On Activities:**

- Launched Amazon Linux and Windows Server EC2 instances.
- Configured EC2 instance types, key pairs, and security groups.
- Connected to Linux instances using SSH and AWS-supported connection methods.
- Connected to Windows instances using Remote Desktop Protocol (RDP).
- Retrieved instance metadata using IMDSv1 and IMDSv2.
- Practiced IMDSv2 session token authentication.
- Automated Apache HTTPD installation using EC2 user data.
- Created and verified a webpage displaying EC2 instance metadata.
- Practiced assigning IAM roles and permissions to EC2 instances.
- Explored Amazon CloudWatch monitoring and EC2 status checks.
- Practiced stopping and terminating EC2 instances after lab completion.

**Additional Concepts Studied:**

- Cluster, partition, and spread placement groups.
- Elastic Network Interfaces (ENI).
- Elastic Network Adapter (ENA).
- Elastic Fabric Adapter (EFA).
- Public and private IPv4 addresses.
- Elastic IP addresses.
- Enhanced networking and high-performance computing.

**Current Progress:**

Neal Davis AWS SAA-C03 Course — Section 3: Amazon EC2

- Lessons completed: 24–36
- Progress: 13 of 27 items (48.1%)
- Last updated: November 17, 2026

[View Project 02 — Amazon EC2 Compute and Networking](projects/02-ec2-compute/README.md)

---

## Technologies and Tools

### AWS Services

- Amazon Elastic Compute Cloud (EC2)
- Amazon Virtual Private Cloud (VPC)
- AWS Identity and Access Management (IAM)
- AWS Organizations and Service Control Policies (SCPs)
- AWS Security Token Service (STS)
- Amazon CloudWatch
- AWS CloudShell

### Cloud Infrastructure and Security

- EC2 Instance Deployment and Management
- EC2 Security Groups
- IAM Roles and Permissions Policies
- EC2 User Data and Instance Metadata
- IMDSv1 and IMDSv2
- Public, Private, and Elastic IP Addressing
- Cloud Monitoring and Troubleshooting
- Least-Privilege Security

### Development and Administration Tools

- AWS Command Line Interface (CLI)
- Visual Studio Code
- Git and GitHub
- Windows PowerShell
- Linux Command Line
- SSH and Remote Desktop Protocol (RDP)
- JSON
- Bash Scripting

## Learning Objectives

- Design secure, scalable, and highly available AWS architectures.
- Apply cloud security and least-privilege principles.
- Deploy and manage AWS compute and networking resources.
- Develop practical experience with AWS services.
- Implement infrastructure automation and monitoring.
- Improve cloud infrastructure troubleshooting skills.
- Build hands-on AWS projects demonstrating real-world technical capabilities.
- Document cloud projects using Git and GitHub.

## Security Notice

All projects are developed in a learning environment.

No AWS credentials, passwords, access keys, private keys, account identifiers, or other sensitive information are intentionally published in this repository.

AWS resources are stopped or terminated when no longer required to reduce unnecessary costs.
