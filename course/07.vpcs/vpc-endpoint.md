# VPC ENDPOINT
## What is a VPC Endpoint?

A VPC Endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Instances in your VPC do not require public IP addresses to communicate with resources in the service. Traffic between your VPC and the other service does not leave the Amazon Network.

Endpoints are virtual devices. They are horizontally scaled, redundant, and higly available VPC components that allow communication between instances in your VPC and services without imposing availability risks or bandwidth constraints on your network traffic.

## Types of VPC Endpoints

- Interface endpoints.
- Gateway endpoints.

## Tips

An interface endpoint is an elastic network interface with a private IP address that serves as an entry point for traffic destined to a supported service. The following services are supported:

- Amazon API Gateway.
- Amazon CloudWatch.
- Amazon CloudWatch Events.
- Amazon CloudWatch Logs.
- Amazon EC2 API.
- Amazon Kinesis Data Streams.
- Amazon SageMaker.
- Amazon SageMaker Runtime.
- Amazon SageMaker Notebook instance.
- Amazon SNS.
- Amazon SQS.
- AWS CloudFormation.
- AWS CodeBuild.
- AWS Config.
- AWS Key Management Service.
- AWS Secrets Manager.
- AWS Security Token Service.
- AWS Service Catalog.
- AWS System Manager.
- Elastic Load Balancing API.
- Endpoint services hosted by other AWS accounts.
- Supported AWS Marketplace partner services.

## Gateway endpoint

- Amazon S3.
- DynamoDB.