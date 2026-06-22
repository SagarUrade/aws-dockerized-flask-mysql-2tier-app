# Application Load Balancer (ALB)

## Overview
The Application Load Balancer distributes incoming HTTP traffic across multiple EC2 instances running in private subnets.

## Features
- Internet-facing ALB in public subnet
- Target group configured for EC2 instances
- Health checks enabled for application availability
- Cross-AZ load balancing

## Flow
User → ALB → EC2 Instances → Flask Application
