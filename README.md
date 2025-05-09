# AWS Resource List Script

## Author
Mause / DevOps Team

## Version
v0.0.2

## Description
This script lists resources for various AWS services in a specified AWS region. The script uses AWS CLI commands to query specific services and display their resources.

## Supported AWS Services
The script currently supports the following AWS services:

1. EC2
2. S3
3. RDS
4. DynamoDB
5. Lambda
6. CloudFront
7. EBS
8. ELB
9. CloudWatch
10. SNS
11. SQS
12. Route53
13. VPC
14. CloudFormation
15. IAM

## Prerequisites
- **AWS CLI** must be installed on your system.
- **AWS CLI must be configured** with the necessary IAM permissions to access the desired AWS resources.

## Usage

Run the script with the following syntax:

```bash
./aws_resource_list.sh <region> <service_name>


-🔄 Script Flow
✅ Argument Check
Ensures two arguments (region and service_name) are provided.

✅ AWS CLI Check
Verifies that the AWS CLI is installed and configured.

✅ Service Execution
Executes the appropriate AWS CLI command to list resources based on the service name.

📌 Supported Services and Commands
🖥️ EC2 — List EC2 instances

aws ec2 describe-instances --region <region>
🪣 S3 — List all S3 buckets

aws s3api list-buckets --region <region>
🗄️ RDS — List RDS DB instances

aws rds describe-db-instances --region <region>
🧮 DynamoDB — List DynamoDB tables

aws dynamodb list-tables --region <region>
🌀 Lambda — List Lambda functions

aws lambda list-functions --region <region>
🌍 CloudFront — List distributions

aws cloudfront list-distributions --region <region>
💾 EBS — List EBS volumes

aws ec2 describe-volumes --region <region>
🔁 ELB — List load balancers

aws elb describe-load-balancers --region <region>
📊 CloudWatch — List alarms

aws cloudwatch describe-alarms --region <region>
📣 SNS — List topics

aws sns list-topics --region <region>
📬 SQS — List queues


aws sqs list-queues --region <region>
🧭 Route 53 — List hosted zones

aws route53 list-hosted-zones
🕸️ VPC — List VPCs

aws ec2 describe-vpcs --region <region>
🧱 CloudFormation — List stacks

aws cloudformation list-stacks --region <region>
🧑‍💼 IAM — List users

aws iam list-users

##⚠️ Error Handling
If incorrect arguments are provided, a usage message is displayed.

If AWS CLI is not installed or configured, the script exits with an error.

If an unsupported service is provided, the script displays a list of supported services.

💡 Tip: Make sure your AWS credentials are correctly configured using aws configure.

📄 License
MIT License

```   You can now copy this and paste it directly into your `README.md`. GitHub will render it beautifully with emojis,     formatting, and syntax highlighting.

Would you like a downloadable `.md` file or help pushing this to your repo?

```

