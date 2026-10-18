# 🟪 GP Compliance — IAM Policy Template  
```markdown
# IAM Policy Template: GP Compliance

## Description
Compliance access for audits, regulatory reporting, and IAM policy review.

## Trust Policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": { "AWS": "arn:aws:iam::ACCOUNT-ID:role/GP-Compliance" },
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
        "cloudtrail:LookupEvents",
        "config:GetComplianceDetailsByResource",
        "iam:ListPolicies",
        "iam:GetPolicy",
        "iam:GetPolicyVersion"
      ],
      "Resource": "*"
    }
  ]
}
