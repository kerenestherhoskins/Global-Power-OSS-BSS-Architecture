# 🟦 GP Operations — IAM Policy Template  
```markdown
# IAM Policy Template: GP Operations

## Description
Operational access for provisioning, activation, monitoring, and network inventory.

## Trust Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::ACCOUNT-ID:role/GP-Operations" },
      "Action": "sts:AssumeRole"
    }
  ]
}

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "lambda:InvokeFunction",
        "s3:GetObject",
        "s3:PutObject",
        "rds:DescribeDBInstances",
        "cloudwatch:GetMetricData",
        "cloudwatch:DescribeAlarms"
      ],
      "Resource": "*"
    }
  ]
}
