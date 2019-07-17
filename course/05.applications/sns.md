# SNS
## What is SNS?

Amazon Simple Notification Service (Amazon SNS) is a web service that makes it easy to set up, operate, and send notification from the cloud.

It provides developers with a highly scalable, flexible, and cost-effective capability to publish messages from an application and immediately deliver them to subscribers or other applications.

## Push notifications

Push notifications to Apple, Google, Fire OS, and Windows devices, as well as Android devices in China with Baidu Cloud Push.

## SQS Integration

Besides pushing cloud notifications directly to mobile devices, Amazon SNS can also deliver notifications by SMS text message or email to Amazon Simple Queue Service (SQS) queues, or to any HTTP endpoint.

## What is a Topic?

SNS allows you to group multiple recipients using topics. A topic is an "access point" for allowing recipients to dynamically subscribe for identical copies of the same notification.

One topic can support deliveries to multiple endpoint types, for example: you can group together iOS, Android and SMS recipients.
When you publish once to a topic, SNS delivers appropriately formatted copies of your message to each subscriber.

## SNS availability

To prevent messages from being lost, all messages published to Amazon SNS are stored redundantly across multiple availability zones.

## SNS benefits

- Instantaneous, push-based delivery. (no polling)
- Simple API's and easy integration with applications.
- Flexible message delivery over multiple transport protocols.
- Inexpensive, pay-as-you-go model with no upfront costs.
- Web-based AWS Management Console offers the simplicity of a point-and-click interface.

## SNS v SQS

- Both messaging services in AWS.
- SNS - Push.
- SQS - Polls. (pulls)