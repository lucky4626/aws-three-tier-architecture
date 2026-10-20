# AWS Three-Tier Web Application Architecture

## Project Overview

This project focuses on designing a secure, scalable, and highly available three-tier web application architecture using Amazon Web Services (AWS). The architecture separates the presentation, application, and database layers to support better security, maintainability, and scalability.

## Architecture Components

### 1. Networking and Infrastructure
- **Amazon VPC:** Provides an isolated virtual network for AWS resources.
- **Public and Private Subnets:** Separate internet-facing resources from application and database components.
- **Internet Gateway:** Provides internet connectivity through configured routes.
- **NAT Gateway:** Enables outbound internet access for resources in private subnets when configured.
- **Amazon Route 53:** Provides DNS resolution for the application domain.

### 2. Application Layer
- **Application Load Balancer (ALB):** Distributes incoming application traffic across healthy targets.
- **Amazon EC2:** Hosts application servers in private subnets.
- **EC2 Auto Scaling:** Adjusts the number of application instances based on configured scaling policies.

### 3. Database Layer
- **Amazon RDS for MySQL:** Provides managed relational database storage for application data.
- **Private Subnets:** Help isolate the database from direct public internet access.

### 4. Security, Monitoring, and Auditing
- **AWS IAM:** Manages identities, roles, and permissions.
- **Security Groups:** Control inbound and outbound traffic to AWS resources.
- **Network ACLs:** Apply traffic rules at the subnet level.
- **Amazon CloudWatch:** Supports monitoring through metrics, logs, and alarms.
- **VPC Flow Logs:** Capture information about IP traffic in the VPC.
- **AWS CloudTrail:** Records AWS API activity for auditing and troubleshooting.

## Architecture Workflow

1. A user accesses the application through a web browser.
2. Amazon Route 53 resolves the application domain name.
3. The Application Load Balancer receives incoming requests and distributes them to healthy application targets.
4. Amazon EC2 instances process application requests.
5. The application communicates with Amazon RDS for database operations.
6. CloudWatch, VPC Flow Logs, and CloudTrail support monitoring, network visibility, and auditing.

## Key Learning Outcomes

- AWS networking and VPC architecture
- Public and private subnet design
- Load balancing and Auto Scaling concepts
- Database isolation and network security
- Identity and access management
- Cloud monitoring, logging, and auditing

## Technologies Used

Amazon Web Services (AWS), Amazon VPC, Amazon EC2, Application Load Balancer, EC2 Auto Scaling, Amazon RDS for MySQL, Route 53, IAM, Security Groups, Network ACLs, CloudWatch, VPC Flow Logs, CloudTrail, and diagrams.net.

## Project Status

This repository documents the architecture design and its key AWS components. Deployment and testing are not claimed unless completed separately.
