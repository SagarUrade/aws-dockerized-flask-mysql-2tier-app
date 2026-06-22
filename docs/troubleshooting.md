# Troubleshooting

## Container Not Starting

Check container logs:

```bash
docker logs <container-id>
```

---

## Target Group Unhealthy

Verify:

- Application is running
- Security group allows traffic
- Health check path is correct

---

## Cannot Pull Image from ECR

Verify:

- IAM role attached to EC2
- ECR permissions
- AWS CLI login completed

---

## CloudWatch Agent Not Sending Logs

Check:

```bash
sudo systemctl status amazon-cloudwatch-agent
```

Restart:

```bash
sudo systemctl restart amazon-cloudwatch-agent
```

---

## Systems Manager Session Fails

Verify:

- SSM Agent installed
- IAM role attached
- VPC endpoints configured
