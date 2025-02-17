# Automating-creation-of-IAM-Resources-LAB

This AWS CloudFormation template creates IAM users, assigns them to groups, stores a one-time password in AWS Secrets Manager, and uses an EventBridge rule to trigger a Lambda function that sets user passwords upon creation.

## Features
- Creates IAM users for S3 and EC2 access.
- Assigns users to specific IAM groups with appropriate permissions.
- Uses AWS Secrets Manager to generate and store a one-time password.
- Stores user email addresses in AWS Systems Manager Parameter Store.
- Deploys a Lambda function to set IAM user passwords upon creation.
- Uses EventBridge to trigger the Lambda function when a new IAM user is created.

## Resources Created
- **IAM Users:** `s3-user` and `ec2-user`
- **IAM Groups:** `S3ReadOnlyGroup` and `EC2ReadOnlyGroup`
- **IAM Policies:** Read-only access to S3 and EC2
- **AWS Secrets Manager:** Stores one-time passwords
- **AWS Systems Manager Parameter Store:** Stores user emails
- **AWS Lambda Function:** Sets IAM user passwords
- **Amazon EventBridge Rule:** Triggers Lambda on user creation
