# 🟧 GP Billing — IAM Policy Template  
```markdown
# IAM Policy Template: GP Billing

## Description
Billing access for invoicing, payment processing, and revenue assurance.

## Trust Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::ACCOUNT-ID:role/GP-Billing" },
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
        "s3:GetObject",
        "s3:PutObject",
        "dynamodb:Query",
        "dynamodb:UpdateItem",
        "ce:GetCostAndUsage"
      ],
      "Resource": "*"
    }
  ]
}
