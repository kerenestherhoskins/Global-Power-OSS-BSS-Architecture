# 🟩 GP Support — IAM Policy Template  
```markdown
# IAM Policy Template: GP Support

## Description
Support access for ticketing, monitoring dashboards, and customer issue resolution.

## Trust Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::ACCOUNT-ID:role/GP-Support" },
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
        "cloudwatch:GetMetricData",
        "cloudwatch:DescribeAlarms",
        "dynamodb:GetItem",
        "dynamodb:Query"
      ],
      "Resource": "*"
    }
  ]
}
