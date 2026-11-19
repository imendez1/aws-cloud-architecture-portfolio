
# Project 02 — Amazon EC2 Compute and Networking

**Status:** Completed
**Started:** November 17, 2026
**Completed:** November 18, 2026
**AWS Region:** US East (Ohio) — us-east-2  
**Certification:** AWS Certified Solutions Architect — Associate (SAA-C03)

## Project Overview

This project documents hands-on experience deploying, connecting to, securing, monitoring, and managing Amazon EC2 instances and associated networking resources.

The project is part of my AWS Cloud Architecture learning portfolio and supports my preparation for the AWS Certified Solutions Architect — Associate certification and WGU's B.S. Cloud and Network Engineering program.

## Environment

- AWS account: AWS Free Plan
- Region: US East (Ohio) — us-east-2
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

### 6. Elastic Network Interfaces and IP Addressing

- Examined primary and secondary Elastic Network Interfaces (ENIs).
- Practiced creating and attaching network interfaces to EC2 instances.
- Observed how automatically assigned public IPv4 addresses can change after stopping and starting an instance.
- Explored Elastic IP addresses for persistent public IPv4 connectivity.
- Reviewed network interface placement requirements within an Availability Zone.

### 7. Private Subnets and Bastion Hosts

- Created a private subnet and associated route table.
- Launched a private EC2 instance without a public IP address.
- Configured a public EC2 instance as a bastion host.
- Practiced private-instance connectivity through a bastion host.
- Reviewed security group configurations for controlled SSH access.
- Studied how VPC routing enables communication between public and private subnets.

### 8. NAT Gateway Configuration

- Created a public NAT gateway in a public subnet.
- Associated an Elastic IP address with the NAT gateway.
- Updated the private subnet route table to direct outbound traffic through the NAT gateway.
- Tested outbound internet connectivity from the private EC2 instance.
- Reviewed how NAT gateways enable private instances to initiate internet connections without exposing them to unsolicited inbound internet traffic.

### 9. Resource Management and Cleanup

- Practiced stopping and terminating EC2 instances.
- Reviewed the billing implications of running and stopped instances.
- Studied the importance of releasing unused Elastic IP addresses.
- Reviewed NAT gateway hourly and data processing charges.
- Completed post-lab cleanup by terminating unused EC2 instances, deleting the NAT gateway and associated networking resources, and releasing unused Elastic IP addresses.
- Removed temporary resources after completing the hands-on exercises to avoid unnecessary ongoing charges.

## Additional Concepts Studied

The following topics were covered through course lectures and architecture examples.

### EC2 Networking and Performance

- Cluster, partition, and spread placement groups
- Elastic Network Adapter (ENA)
- Elastic Fabric Adapter (EFA)
- Enhanced networking
- High-performance computing (HPC)
- Multi-AZ networking architecture

### EC2 Lifecycle and Infrastructure

- EC2 instance lifecycle states
- Rebooting, stopping, hibernating, and terminating
- EBS-backed versus instance store storage
- Amazon Machine Images (AMIs)
- AWS Nitro System
- Nitro Hypervisor and Nitro Cards
- Nitro Enclaves and secure data processing

### EC2 Pricing and Cost Optimization

- On-Demand Instances
- Reserved Instances
- Standard and Convertible Reserved Instances
- Spot Instances
- Compute and EC2 Instance Savings Plans
- Dedicated Instances
- Dedicated Hosts
- On-Demand Capacity Reservations

### Architecture Patterns

- User data for automated instance configuration
- Cluster placement groups and EFA for HPC
- Reserved Instances for baseline capacity
- Spot Instances for fault-tolerant workloads
- Elastic IP addresses for static public IPv4 requirements
- NAT gateways for private subnet outbound connectivity
- Bastion hosts for administrative access
- Spread placement groups for hardware fault isolation
- Nitro-based instances for improved performance and security

## Security Best Practices

- Prefer IAM roles over long-term access keys for EC2 workloads.
- Use IMDSv2 to improve instance metadata security.
- Restrict SSH and RDP access to trusted source IP addresses.
- Apply least-privilege IAM permissions.
- Avoid storing secrets in EC2 user data.
- Keep private SSH keys outside EC2 bastion hosts.
- Use private subnets for instances that do not require direct internet access.
- Configure security groups to restrict access between public and private instances.
- Consider AWS Systems Manager Session Manager as an alternative to bastion hosts.
- Terminate unused lab instances and remove unnecessary networking resources.

## Key Lessons Learned

1. EC2 provides flexible compute capacity for Linux and Windows workloads.
2. Security groups control network access to EC2 instances.
3. User data enables automated instance initialization.
4. Instance metadata supports dynamic configuration and application bootstrapping.
5. IAM roles provide temporary credentials for AWS service access.
6. CloudWatch provides monitoring and EC2 status checks.
7. ENIs provide flexible network connectivity within an Availability Zone.
8. Elastic IP addresses support persistent public IPv4 addressing.
9. Private subnets help isolate resources from direct internet access.
10. Bastion hosts enable controlled administrative access to private instances.
11. NAT gateways provide outbound connectivity for private subnet resources.
12. Placement groups and enhanced networking support workload-specific performance requirements.
13. EC2 purchasing options should be selected according to workload duration, predictability, and interruption tolerance.
14. AWS Nitro improves EC2 performance and security.
15. Proper resource cleanup and cost monitoring are essential AWS operational practices.

## Course Completion

**Neal Davis SAA-C03 Course — Section 3: Amazon EC2**

- Lessons covered: 24–49
- Section items completed: 27 of 27
- Section completion: 100%
- Completed: November 18, 2026

## Project Outcome

Completed the Amazon EC2 section of the SAA-C03 course, combining conceptual architecture knowledge with hands-on exercises involving EC2 instances, IAM roles, monitoring, network interfaces, private subnets, bastion hosts, and NAT gateways.

The project demonstrates foundational skills in AWS compute deployment, network connectivity, access control, cost optimization, and cloud infrastructure management.

All temporary AWS resources used for the EC2 hands-on labs were cleaned up after the exercises.

## Future Improvements

- Add sanitized architecture diagrams for EC2 networking.
- Expand infrastructure deployment using Infrastructure as Code (IaC).
- Explore AWS Systems Manager Session Manager.
- Practice multi-AZ high availability and Auto Scaling architectures.
- Continue building AWS projects as additional course sections are completed.

## Security Notice

This repository is for educational and portfolio purposes.

No AWS access keys, private keys, passwords, account identifiers, or other sensitive credentials should be committed to this repository.
