# Project 03 — AWS Elastic Load Balancing and Auto Scaling

**Status:** Completed — November 20, 2026
**Started:** November 19, 2026
**AWS Certification:** AWS Certified Solutions Architect – Associate (SAA-C03)
**Course:** Neal Davis — AWS Certified Solutions Architect Associate

## Project Overview

This project demonstrates the deployment and management of scalable, highly available application infrastructure using Amazon EC2 Auto Scaling and Elastic Load Balancing.

The hands-on exercises focused on deploying EC2 Auto Scaling Groups, configuring Application and Network Load Balancers, implementing dynamic scaling policies, and validating application connectivity across AWS networking environments.

The project demonstrates how AWS services work together to distribute application traffic, maintain compute capacity, automatically replace failed instances, and respond to changing application demand.

## AWS Services and Technologies

- Amazon Elastic Compute Cloud (EC2)
- Amazon EC2 Auto Scaling
- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Elastic Load Balancing (ELB)
- Amazon CloudWatch
- EC2 Launch Templates
- Amazon Virtual Private Cloud (VPC)
- EC2 Security Groups
- Elastic IP Addresses
- EC2 User Data
- Apache HTTP Server
- Target Groups and Health Checks
- Network Access Control Lists (NACLs)
- AWS Availability Zones

## Architecture Overview

The primary architecture uses an internet-facing Application Load Balancer to distribute incoming HTTP requests across EC2 instances managed by an Auto Scaling Group.

**Application Traffic Flow:**

Internet Users → Application Load Balancer → Target Group → EC2 Instances (Auto Scaling Group)

The Auto Scaling Group maintains the configured desired capacity and automatically launches replacement instances when necessary.

Dynamic scaling policies adjust compute capacity based on application traffic and CloudWatch monitoring.

A separate hands-on exercise demonstrates Network Load Balancer deployment using TCP traffic, static public IP addresses, and application connectivity testing.

## Hands-On Lab 1 — Create an Auto Scaling Group

**Status:** Completed — November 19, 2026

### Objective

Deploy an Amazon EC2 Auto Scaling Group that maintains application availability by automatically managing and replacing EC2 instances.

### Implementation

1. Prepared a user data script named `user_data_web_server.sh` to install Apache HTTP Server and configure a custom webpage displaying the instance's Availability Zone.
2. Created an EC2 launch template defining the Amazon Machine Image (AMI), EC2 instance type, security group, and user data.
3. Configured a `t2.micro` EC2 instance type for the exercise.
4. Created an Auto Scaling Group named `ASG1`.
5. Configured a desired capacity of two EC2 instances.
6. Selected multiple Availability Zones for improved availability.
7. Verified that the Auto Scaling Group successfully launched the configured EC2 instances.
8. Manually terminated an EC2 instance to test automatic replacement.

### Validation

The Auto Scaling Group automatically launched a replacement EC2 instance after one of the original instances was terminated.

The replacement restored the configured desired capacity of two instances.

### Technical Skills Demonstrated

- EC2 launch template configuration
- EC2 user data automation
- Auto Scaling Group deployment
- Desired capacity management
- Multi-Availability Zone deployment
- Automatic EC2 instance replacement

## Hands-On Lab 2 — Create an Application Load Balancer

**Status:** Completed — November 19, 2026

### Objective

Deploy an Application Load Balancer to distribute HTTP traffic across multiple EC2 instances managed by an Auto Scaling Group.

### Implementation

1. Created an HTTP target group using port 80.
2. Configured health checks to monitor the availability of registered EC2 instances.
3. Associated the target group with the existing Auto Scaling Group.
4. Created an internet-facing Application Load Balancer.
5. Selected the appropriate VPC and subnets across multiple Availability Zones.
6. Configured security groups to allow application traffic.
7. Created an HTTP listener to forward incoming requests to the target group.
8. Verified automatic target registration for EC2 instances launched by the Auto Scaling Group.
9. Tested application traffic distribution across EC2 instances in different Availability Zones.

### Validation

The Application Load Balancer successfully distributed incoming HTTP requests between healthy EC2 instances.

The target group registered the EC2 instances managed by the Auto Scaling Group.

The exercise demonstrated how load balancing and Auto Scaling work together to support highly available applications.

### Technical Skills Demonstrated

- Application Load Balancer deployment
- HTTP listener configuration
- Target group configuration
- Health check management
- Auto Scaling integration
- Multi-Availability Zone traffic distribution
- Application connectivity testing

## Hands-On Lab 3 — Create a Scaling Policy

**Status:** Completed — November 19, 2026

### Objective

Implement dynamic EC2 Auto Scaling based on application traffic to automatically increase compute capacity when demand rises.

### Implementation

1. Accessed the existing EC2 Auto Scaling Group.
2. Increased the maximum group capacity from two to four EC2 instances.
3. Created a dynamic target tracking scaling policy.
4. Selected the Application Load Balancer request count per target metric.
5. Configured a target value of 50 requests per target.
6. Generated application traffic to simulate increased demand.
7. Monitored CloudWatch alarms and Auto Scaling activity.
8. Observed the Auto Scaling Group launch additional EC2 instances.
9. Verified that newly launched instances automatically registered with the load balancer target group.
10. Confirmed that the Application Load Balancer distributed traffic across the expanded group of healthy instances.

### Validation

The increased application traffic triggered the scaling policy, causing the Auto Scaling Group to launch additional EC2 instances.

New instances successfully registered as healthy targets.

The exercise demonstrated automatic capacity adjustment in response to changing application demand.

### Technical Skills Demonstrated

- Target tracking scaling policy configuration
- Application Load Balancer request count metrics
- CloudWatch monitoring
- Auto Scaling capacity management
- Application load testing
- Automatic scale-out validation
- Dynamic infrastructure scaling

## Hands-On Lab 4 — Create a Network Load Balancer

**Status:** Completed — November 20, 2026

### Objective

Deploy an internet-facing Network Load Balancer to support TCP application traffic using static public IP addresses.

### Implementation

1. Created an internet-facing Network Load Balancer.
2. Configured Elastic IP addresses to provide static public IP connectivity.
3. Created a TCP listener using custom port `8181`.
4. Configured a target group for the application instances.
5. Created an EC2 launch template defining the application instance configuration.
6. Configured an Auto Scaling Group to manage the application instances.
7. Reviewed network ACL settings to restrict traffic based on approved source IP addresses.
8. Tested application connectivity from a separate VPC.
9. Used the `curl` command to verify connectivity to the application through the Network Load Balancer.
10. Removed temporary AWS resources after completing the exercise.

### Validation

Successfully completed the Network Load Balancer deployment and connectivity testing.

The exercise demonstrated how an NLB supports TCP-based applications and static public IP addressing.

Application connectivity was validated using `curl` from a separate VPC.

### Technical Skills Demonstrated

- Network Load Balancer deployment
- TCP listener configuration
- Custom application ports
- Elastic IP configuration
- Target group management
- Auto Scaling Group integration
- Network ACL configuration concepts
- Cross-VPC connectivity testing
- Linux command-line troubleshooting
- AWS resource cleanup

## Key Technical Concepts

### High Availability

Deploying EC2 instances across multiple Availability Zones reduces dependence on a single Availability Zone and improves application availability.

### Elasticity

EC2 Auto Scaling adjusts compute capacity in response to changing application demand.

### Health Checks

Elastic Load Balancing health checks help ensure that incoming traffic is directed to healthy application targets.

### Dynamic Scaling

Target tracking policies automatically adjust EC2 capacity to maintain a specified performance metric.

### Automatic Instance Replacement

Auto Scaling Groups automatically replace terminated or unhealthy EC2 instances to maintain configured capacity.

### Application Load Balancing

Application Load Balancers operate at Layer 7 and support HTTP/HTTPS applications, including advanced routing capabilities.

### Network Load Balancing

Network Load Balancers operate at Layer 4 and support TCP/UDP workloads, low-latency connectivity, and static public IP addressing.

### Multi-Availability Zone Architecture

Distributing application instances across multiple Availability Zones improves resilience and reduces the impact of individual Availability Zone failures.

## Skills Demonstrated

- Amazon EC2 deployment and management
- EC2 Auto Scaling Group configuration
- EC2 launch template configuration
- EC2 user data automation
- Apache web server deployment
- Application Load Balancer configuration
- Network Load Balancer deployment
- Target group configuration
- Health check management
- Multi-Availability Zone deployments
- Dynamic scaling policy configuration
- CloudWatch metrics and alarms
- Elastic IP address configuration
- TCP and HTTP connectivity testing
- Network ACL configuration concepts
- Application load testing
- Automatic EC2 instance replacement
- AWS infrastructure validation
- AWS resource lifecycle management

## Course Completion

**Neal Davis AWS SAA-C03 Course — Section 4: Elastic Load Balancing and Auto Scaling**

- Hands-on exercises successfully completed: 4
- Section completed: November 20, 2026

## Resource Management

Temporary AWS resources were deleted following the hands-on exercises to minimize unnecessary charges.

Resource cleanup was confirmed after completing the final Network Load Balancer exercise.

## Project Outcome

Successfully deployed and tested scalable AWS application infrastructure using Amazon EC2 Auto Scaling, Application Load Balancers, Network Load Balancers, and dynamic scaling policies.

The completed hands-on exercises demonstrated automatic instance replacement, traffic distribution, scaling in response to application demand, and TCP connectivity through a Network Load Balancer.

This project reinforces practical AWS architecture, networking, availability, and automation skills relevant to cloud engineering and the AWS Certified Solutions Architect – Associate certification.