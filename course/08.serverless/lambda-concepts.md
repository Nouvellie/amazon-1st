# LAMBDA CONCEPTS
## What is Lambda ?

Is a compute service where you can upload your code and create a lambda function. AWS Lambda takes care of provisioning and managing the servers that you use to run the code. You do not have to worry about operating systems, patching, scaling, etc.

Lambda is the ultimate abstraction layer.

- Data Centres.
- Hardware.
- Assembly code/protocols.
- High level languages.
- Operating systems.
- Application layer/AWS APIs.
- AWS Lambda.

## Basics

You can use Lambda in the following ways;

- As an event-driven compute service where AWS Lambda runs your code in response to events. These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table.
- As a compute service to run your code in response to HTTP requests using Amazon API Gateway or API calls made using AWS SDKs.

## What languages does Lambda support?

- Node.js.
- Java.
- Python.
- C#.

## PHow is Lambda priced?
#### Number of requests:

First 1 million requests are free. USD 0.20 per 1 million requests thereafter.

#### Duration:

Duration is calculated from the time your code begins executing until it returns or otherwise terminates, rounded up to the nearest 100ms. The price depends on the amount of memory you allocte to your function. You are charged USD 0.00001667 for every GB-second used.

## Why is Lambda cool?

- No servers. (important!)
- Continuous scaling.
- Super cheap!

## Tips

- Lambda scales out (not up) automatically.
- Lambda functions are independent. (1 event = 1 funtion)
- Lambda is serverless.
- Know what services are serverless.
- Lambda functions can trigger other Lambda functions. (1 event can = x functions, if functions trigger other functions)
- Architectures can get extremely complicated, AWS X-ray allows you to debug what is happening.
- Lambda can do things globally, you can use it to back up S3 buckets to other S3 buckets, etc.
- Know your triggers.