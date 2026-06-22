# Security Best Practices

## Network Isolation

- Application instances run in private subnets.
- No public IP assigned to EC2 instances.

## Secure Administration

- AWS Systems Manager Session Manager used instead of SSH.
- No inbound port 22 exposed.

## IAM Least Privilege

- EC2 instances use IAM Roles.
- No hardcoded AWS credentials.

## VPC Endpoints

Private access enabled for:

- Amazon ECR
- CloudWatch
- Systems Manager

## Monitoring

- CloudWatch metrics and logs enabled.
- Centralized observability.

## Security Groups

- Only ALB can access application instances.
- Public traffic terminates at ALB.

## Image Security

- Docker images stored in Amazon ECR.
- Version-controlled deployments.
