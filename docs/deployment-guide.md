# Deployment Guide

## Prerequisites
- AWS Account
- Docker installed
- AWS CLI configured
- IAM permissions
- Amazon ECR repository

## Step 1: Clone Repository

```bash
git clone <repository-url>
cd aws-dockerized-flask-mysql-2tier-app
```

## Step 2: Build Docker Image

```bash
docker build -t flask-app ./app
```

## Step 3: Push Image to Amazon ECR

Authenticate Docker:

```bash
aws ecr get-login-password --region <region> | docker login --username AWS --password-stdin <ecr-url>
```

Tag and push:

```bash
docker tag flask-app:latest <ecr-url>:latest
docker push <ecr-url>:latest
```

## Step 4: Launch EC2 Instances

- Configure IAM Role
- Configure Security Groups
- Install Docker
- Pull image from ECR

## Step 5: Configure ALB

- Create Target Group
- Register EC2 instances
- Configure Listener Rules

## Step 6: Verify Deployment

Access the ALB DNS endpoint.
