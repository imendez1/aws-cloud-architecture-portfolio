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

**Status:** Completed — November 18, 2026

**AWS Region:** US East (Ohio) — us-east-2

**AWS Services and Technologies:** Amazon EC2, Amazon VPC, IAM Roles, AWS STS, Amazon CloudWatch, EC2 User Data, EC2 Instance Metadata, Security Groups, Elastic Network Interfaces, Elastic IP Addresses, NAT Gateways.

**Project Summary:**

Deployed, configured, secured, monitored, and managed Amazon EC2 instances running Linux and Windows Server.

Implemented hands-on EC2 networking exercises involving Elastic Network Interfaces, public and private IP addressing, private subnets, bastion hosts, and NAT gateways.

Explored EC2 architecture, automated instance initialization, instance metadata security, IAM roles, CloudWatch monitoring, pricing models, and infrastructure lifecycle management.

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
- Created and attached Elastic Network Interfaces (ENIs).
- Explored public IPv4 address changes and Elastic IP addressing.
- Created a private subnet and associated route table.
- Launched a private EC2 instance without a public IP address.
- Configured a public EC2 instance as a bastion host.
- Practiced SSH connectivity to a private instance through a bastion host.
- Created a public NAT gateway with an Elastic IP address.
- Configured private subnet routing through the NAT gateway.
- Verified outbound internet connectivity from a private EC2 instance.
- Completed AWS resource cleanup after finishing the hands-on exercises.

**Additional Concepts Studied:**

- Cluster, partition, and spread placement groups.
- Elastic Network Adapter (ENA).
- Elastic Fabric Adapter (EFA).
- Enhanced networking and high-performance computing.
- EC2 instance lifecycle and storage options.
- Amazon Machine Images (AMIs).
- AWS Nitro System and Nitro Enclaves.
- On-Demand, Reserved, and Spot Instances.
- Savings Plans and Capacity Reservations.
- Dedicated Instances and Dedicated Hosts.
- EC2 architecture patterns and cost optimization.

[View Project 02 — Amazon EC2 Compute and Networking](projects/02-ec2-compute/README.md)

---

### Project 03 — AWS Elastic Load Balancing and Auto Scaling

**Status:** In Progress — Started November 19, 2026

**AWS Services and Technologies:** Amazon EC2, EC2 Auto Scaling, Application Load Balancer (ALB), Elastic Load Balancing (ELB), Amazon CloudWatch, EC2 Launch Templates, Target Groups, Security Groups, Amazon VPC, EC2 User Data.

**Project Summary:**

Implemented a highly available and scalable web application architecture using Amazon EC2 Auto Scaling and an Application Load Balancer.

Configured automatic EC2 instance replacement, distributed HTTP traffic across multiple Availability Zones, and implemented dynamic scaling policies based on application demand.

**Hands-On Activities:**

- Created an EC2 launch template with an Apache web server initialization script.
- Deployed an Auto Scaling Group with a desired capacity of two EC2 instances.
- Configured instance distribution across multiple Availability Zones.
- Tested automatic EC2 instance replacement.
- Created an Application Load Balancer and HTTP target group.
- Configured health checks and automatic target registration.
- Integrated the Application Load Balancer with the Auto Scaling Group.
- Verified HTTP traffic distribution across healthy EC2 instances.
- Increased the Auto Scaling Group maximum capacity to four instances.
- Configured a target tracking scaling policy using ALB request count per target.
- Generated application traffic to test dynamic scaling.
- Monitored CloudWatch alarms and Auto Scaling activity.
- Verified automatic scale-out and registration of additional EC2 instances.

**Additional Concepts Studied:**

- Vertical scaling versus horizontal scaling.
- Stateful versus stateless applications.
- High availability and fault tolerance.
- Synchronous and asynchronous replication.
- Application Load Balancer versus Network Load Balancer.
- Load balancer listeners and target groups.
- Target tracking, simple, step, and scheduled scaling.
- Instance warm-up periods and scaling cooldowns.
- Application durability versus availability.

**Course Progress:**

[View Project 03 — AWS Elastic Load Balancing and Auto Scaling](projects/03-elb-auto-scaling/README.md)

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
- Amazon EC2 NAT Gateways
- Amazon EC2 Elastic Network Interfaces (ENIs)
- Amazon EC2 Elastic IP Addresses
- Amazon EC2 Auto Scaling
- Elastic Load Balancing (ELB)
- Application Load Balancer (ALB)
- EC2 Launch Templates
- Elastic Load Balancing Target Groups

### Cloud Infrastructure and Security

- EC2 Instance Deployment and Management
- EC2 Security Groups
- IAM Roles and Permissions Policies
- EC2 User Data and Instance Metadata
- IMDSv1 and IMDSv2
- Public, Private, and Elastic IP Addressing
- VPC Subnets and Route Tables
- Bastion Host Configuration
- NAT Gateway Configuration
- SSH and RDP Connectivity
- Cloud Monitoring and Troubleshooting
- Least-Privilege Security
- EC2 Pricing and Cost Optimization
- AWS Resource Lifecycle Management
- EC2 Auto Scaling Group Configuration
- Multi-Availability Zone Deployments
- Application Load Balancer Configuration
- Target Groups and Health Checks
- Dynamic Scaling Policies
- CloudWatch Alarms and Metrics
- Load Testing and Scaling Validation
- Automatic EC2 Instance Replacement
- High Availability and Fault Tolerance

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

Temporary AWS resources are deleted after lab completion to reduce unnecessary costs.