# 🟫 GP Admin — IAM Policy Template  
```markdown
# IAM Policy Template: GP Admin

## Description
Full administrative access for managing IAM, billing, compliance, and system governance.

## Trust Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::ACCOUNT-ID:root" },
      "Action": "sts:AssumeRole"
    }
  ]
}
## Permission Policy
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "iam:*",
        "organizations:*",
        "billing:*",
        "cloudtrail:*",
        "config:*"
      ],
      "Resource": "*"
    }
  ]
}

Tags
Departments, Environments, Purpose, ManagedBY
