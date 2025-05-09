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


- **Script Flow
        Argument Check: The script checks if two arguments (region and service_name) are passed.

        AWS CLI Check: The script checks if AWS CLI is installed and configured.

     Service Execution: Based on the provided service_name, the script executes the corresponding AWS CLI command to list the resources for the selected service.

   Supported Services and Commands
EC2: Lists EC2 instances in the given region.


aws ec2 describe-instances --region <region>
S3: Lists all S3 buckets in the given region.


aws s3api list-buckets --region <region>
RDS: Lists RDS DB instances in the given region.

aws rds describe-db-instances --region <region>
DynamoDB: Lists DynamoDB tables in the given region.


aws dynamodb list-tables --region <region>
Lambda: Lists Lambda functions in the given region.


aws lambda list-functions --region <region>
CloudFront: Lists CloudFront distributions in the given region.


aws cloudfront list-distributions --region <region>
EBS: Lists EBS volumes in the given region.

aws ec2 describe-volumes --region <region>
ELB: Lists ELB load balancers in the given region.


aws elb describe-load-balancers --region <region>
CloudWatch: Lists CloudWatch alarms in the given region.


aws cloudwatch describe-alarms --region <region>
SNS: Lists SNS topics in the given region.


aws sns list-topics --region <region>
SQS: Lists SQS queues in the given region.


aws sqs list-queues --region <region>
Route53: Lists Route 53 hosted zones.


aws route53 list-hosted-zones
VPC: Lists VPCs in the given region.


aws ec2 describe-vpcs --region <region>
CloudFormation: Lists CloudFormation stacks in the given region.


aws cloudformation list-stacks --region <region>
IAM: Lists IAM users.

aws iam list-users
Error Handling
If the script is not provided with the correct number of arguments, it will show a usage message.

If the AWS CLI is not installed or configured, the script will exit with a relevant error message.

If an invalid service name is passed, the script will display a message with the supported services.

## License
## MIT License


This markdown format provides clear structure and readability for documenting the script and its usage.