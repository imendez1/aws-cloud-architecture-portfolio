
# Project 02 — Amazon EC2 Compute and Networking

**Status:** In Progress  
**Started:** November 17, 2026  
**AWS Region:** US East (Ohio) — us-east-2  
**Certification:** AWS Certified Solutions Architect — Associate (SAA-C03)

## Project Overview

This project documents hands-on experience deploying, connecting to, securing, monitoring, and managing Amazon EC2 instances.

The project is part of my AWS Cloud Architecture learning portfolio and supports my preparation for the AWS Solutions Architect Associate certification and WGU's B.S. Cloud and Network Engineering program.

## Environment

- AWS account: AWS Free Plan
- Region: us-east-2
- Operating systems: Amazon Linux and Windows Server
- Instance type: t3.micro
- Tools: AWS Management Console, AWS CLI, PowerShell, SSH, RDP, and Amazon CloudWatch

## Hands-On Activities Completed

### 1. EC2 Instance Deployment

- Launched Linux and Windows EC2 instances.
- Configured instance types, key pairs, and security groups.
- Reviewed instance states and public/private IP addresses.
- Practiced stopping and terminating instances.

### 2. Remote Instance Connectivity

- Connected to a Linux EC2 instance using SSH and AWS-supported connection methods.
- Connected to a Windows EC2 instance using Remote Desktop Protocol (RDP).
- Reviewed inbound security group rules for SSH (TCP 22) and RDP (TCP 3389).

### 3. EC2 User Data and Instance Metadata

- Launched EC2 instances with different metadata configurations.
- Retrieved instance metadata using curl.
- Compared IMDSv1 and IMDSv2 authentication.
- Practiced requesting IMDSv2 session tokens.
- Used EC2 user data to automate Apache HTTPD installation and configuration.
- Created and verified a webpage displaying the EC2 instance ID.

### 4. IAM Roles and EC2 Permissions

- Practiced using AWS credentials and IAM roles with EC2.
- Explored assigning permissions to an EC2 instance through an IAM role.
- Reviewed S3 read-only access and temporary credentials.
- Learned why IAM roles are preferable to storing long-term access keys on instances.

### 5. EC2 Monitoring

- Explored Amazon CloudWatch through the AWS Management Console.
- Reviewed EC2 system status checks.
- Studied instance status checks and their troubleshooting implications.
- Examined basic and detailed monitoring concepts.

### 6. Resource Management

- Stopped instances when they were temporarily unnecessary.
- Terminated EC2 instances after completing hands-on exercises.
- Reviewed the importance of monitoring AWS resource usage and costs.

## Additional Concepts Studied

The following topics were covered through course lectures:

- Cluster, partition, and spread placement groups
- Elastic Network Interfaces (ENI)
- Elastic Network Adapter (ENA)
- Elastic Fabric Adapter (EFA)
- Public and private IPv4 addresses
- Elastic IP addresses
- Enhanced networking and high-performance computing

These topics are documented as conceptual learning rather than completed deployment exercises.

## Security Best Practices

- Prefer IAM roles over long-term access keys for EC2 workloads.
- Use IMDSv2 to improve instance metadata security.
- Restrict SSH and RDP access to trusted source IP addresses.
- Apply least-privilege IAM permissions.
- Avoid storing secrets in EC2 user data.
- Terminate unused lab instances to reduce unnecessary costs.

## Key Lessons Learned

1. EC2 provides flexible compute capacity for Linux and Windows workloads.
2. Security groups control network access to instances.
3. User data enables automated instance initialization.
4. Instance metadata supports dynamic configuration.
5. IAM roles provide temporary credentials for AWS service access.
6. CloudWatch provides metrics for monitoring EC2 performance.
7. Placement groups and networking capabilities should be selected based on workload requirements.
8. Proper resource cleanup is an important part of AWS operations.

## Current Progress

**Neal Davis SAA-C03 Course — Section 3: Amazon EC2**

- Lessons completed: 24–36
- Section progress: 13 of 27 items (48.1%)
- Last updated: November 17, 2026

## Next Steps

- Complete the remaining Amazon EC2 lessons.
- Continue practicing EC2 networking, storage, and management.
- Expand this project with additional hands-on exercises.
- Update the project documentation as new skills are demonstrated.

## Security Notice

This repository is for educational and portfolio purposes.

No AWS access keys, private keys, passwords, account identifiers, or other sensitive credentials should be committed to this repository.
