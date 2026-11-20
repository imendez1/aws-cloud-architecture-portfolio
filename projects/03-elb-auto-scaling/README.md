# Project 03 — AWS Elastic Load Balancing and Auto Scaling

**Status:** In Progress
**Started:** November 19, 2026
**AWS Certification:** Solutions Architect – Associate (SAA-C03)
**Course:** Neal Davis — AWS Certified Solutions Architect Associate

## Project Overview

This project demonstrates how to deploy a scalable, highly available web application using Amazon EC2 Auto Scaling and Elastic Load Balancing.

The hands-on exercises focus on distributing application traffic across multiple EC2 instances, automatically replacing terminated instances, and dynamically adjusting compute capacity in response to application demand.

## AWS Services and Technologies

- Amazon EC2
- Amazon EC2 Auto Scaling
- Application Load Balancer (ALB)
- Elastic Load Balancing (ELB)
- Amazon CloudWatch
- EC2 Launch Templates
- EC2 Security Groups
- Amazon VPC and Availability Zones
- EC2 User Data
- Apache HTTP Server

## Architecture

The architecture consists of an internet-facing Application Load Balancer distributing HTTP traffic to EC2 web servers managed by an Auto Scaling Group across multiple Availability Zones.

**Traffic Flow:**

Internet Users → Application Load Balancer → Target Group → EC2 Instances (Auto Scaling Group)

The Auto Scaling Group maintains the configured desired capacity and launches replacement instances when necessary.

## Hands-On Lab 1 — Create an Auto Scaling Group

**Status:** Completed

### Implementation

1. Prepared a user data script (`user_data_web_server.sh`) to install Apache and configure a web page displaying the instance's Availability Zone.
2. Created an EC2 launch template specifying an Amazon Machine Image, instance type, security group, and user data.
3. Created an Auto Scaling Group named `ASG1`.
4. Configured a desired capacity of two EC2 instances.
5. Selected multiple Availability Zones for high availability.
6. Verified that EC2 instances launched successfully.
7. Terminated an instance to test automatic replacement.

### Validation

The Auto Scaling Group successfully launched a replacement EC2 instance to restore the configured desired capacity.

## Hands-On Lab 2 — Create an Application Load Balancer

**Status:** Completed

### Implementation

1. Created an HTTP target group using port 80.
2. Configured health checks to monitor registered EC2 instances.
3. Associated the target group with the existing Auto Scaling Group.
4. Created an internet-facing Application Load Balancer.
5. Configured subnets, security groups, and an HTTP listener.
6. Verified automatic target registration.
7. Tested HTTP traffic distribution across EC2 instances in different Availability Zones.

### Validation

The Application Load Balancer successfully distributed requests between healthy EC2 instances.

New instances launched by the Auto Scaling Group were automatically registered with the target group.

## Hands-On Lab 3 — Create a Scaling Policy

**Status:** Completed

### Implementation

1. Updated the Auto Scaling Group's maximum capacity to four EC2 instances.
2. Created a target tracking scaling policy.
3. Selected the Application Load Balancer request count per target metric.
4. Configured a target value of 50 requests per target.
5. Generated application traffic to test the scaling policy.
6. Monitored CloudWatch alarms and Auto Scaling activity.
7. Observed additional EC2 instances launch in response to increased demand.
8. Verified that newly launched instances registered as healthy targets.

### Validation

The scaling policy successfully increased EC2 capacity in response to application traffic.

The Application Load Balancer distributed traffic across the expanded group of healthy instances.

## Key Technical Concepts

### High Availability

Deploying EC2 instances across multiple Availability Zones reduces dependence on a single Availability Zone.

### Elasticity

Auto Scaling dynamically adjusts compute capacity to meet changing application demand.

### Health Checks

Load balancer health checks help prevent traffic from being routed to unhealthy targets.

### Dynamic Scaling

Target tracking scaling policies adjust capacity automatically to maintain a specified performance metric.

### Fault Recovery

Auto Scaling Groups replace failed or terminated instances to maintain desired capacity.

## Skills Demonstrated

- EC2 Auto Scaling Group deployment
- Launch template configuration
- EC2 user data automation
- Multi-Availability Zone architecture
- Application Load Balancer configuration
- Target group and health check management
- CloudWatch monitoring
- Target tracking scaling policies
- Application load testing
- Automatic instance replacement
- AWS infrastructure validation

## Project Progress

**Section 4 — Elastic Load Balancing and Auto Scaling**

- Course items completed: 10 of 19 (52.6%)
- Hands-on labs completed: 3
- Remaining course items: 9

## Next Steps

Continue Section 4 by studying cross-zone load balancing, session stickiness, secure listeners, and Network Load Balancer deployments.

Additional hands-on exercises and technical findings will be incorporated as the course progresses.

## Resource Management

AWS infrastructure resources should be removed when no longer required to minimize unnecessary charges. Resource cleanup will be verified as part of the project completion process.

---

**Project Status:** In Progress
**Last Updated:** November 19, 2026