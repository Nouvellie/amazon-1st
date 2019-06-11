# CLOUDWATCH 101
## What is it?

Amazon CloudWatch is a monitoring service to monitor your AWS resources, as well as the application that you run on AWS.

## Monitors performance

- Compute:
	- Ec2 instances.
	- Autoscaling groups.
	- Elastic Load Balancers.
	- Route53 Health Checks.
- Storage and content delivery.
	- EBS volumes.
	- Storage gateways.
	- CloudFront.

## Host level metrics consist of

- CPU.
- Network.
- Disk.
- Status check.

## AWS CloudTrail

AWS CloudTrail increses visibility into your user and resource activity by recording AWS Management Console actions and API calls. You can identify which users and accounts called AWS, the source IP address from which the calls were made, and when the calls occurred.

## CloudWatch vs CloudTrail

- CloudWatch monitors performance.
- CloudTrail monitors API calls in the AWS platform.

## Tips

- CloudWatch is used for monitoring performance.
- CloudWatch can monitor most of AWS as well as your applications that run on AWS.
- CloudWatch with EC2 will monitor events every 5 minutes by default.
- You can have 1 minute intervals by turning on detailed monitoring.
- You can create CloudWatch alarms which trigger notifications.
- CloudWatch is all about performance. CloudTrail is all about auditing.