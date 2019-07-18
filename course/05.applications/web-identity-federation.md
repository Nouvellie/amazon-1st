# WEB IDENTITY FEDERATION
## What is web identity federation?

Web identity federation lets you give your users access to AWS resources after they have successfully authenticated with a web-based identity provider like Amazon, Facebook, or Google. Following successful authentication, the user receives an authentication code from the Web ID provider, which they can trade for temporary AWS security credentials.

## Amazon cognito

Amazon Cognito provides Web Identity Federation with the following features:

- Sign-up and sign-in to your apps.
- Access for guest users.
- Acts as an identity broker between your application and Web ID providers, so you do not need to write any additional code.
- Synchronizes user data for multiple devices.
- Recommended for all mobile applications AWS services.

## Use cases

Cognito brokers between the app and Facebook or Google to provide temporary credentials which map to an IAM role allowing access to the required resources.

No need for the application to embed or store AWS credentials locally on the device and it gives users a seamless experience across all mobile devices.

## User pools

User pools are user directories used to manage sign-up and sign-in functionality for mobile and web applications.

User can sign-in directly to the user pool, or using Facebook, Amazon, or Google. Cognito acts as an identity broker between the identity provider and AWS. Successful authentication generates a JSON Web token. (JWTs)

## Identity pools

Identity pools enable provide temporary AWS credentials to access AWS services like S3 or DynamoDB.

## Cognito synchronisation

Cognito tracks the association between user identity and the various different devices they sign-in from. In order to provide a seamless user experience for your application, Cognito uses push synchronization to push updates and synchronize user data across multiple devices. Cognito uses SNS is to send a notification to all the devices associated with a given user identity whenever data stored in the cloud changes.

## Tips

- Federation allows users to authenticate with a web identity provider. (Google, Facebook, Amazon)
- The user authenticates first with the Web ID provider and receives an authentication token, which is exchanged for temporary AWS credentials allowing them to assume an IAM role.
- Cognito is an identity broker which handles interaction between your applications and the Web ID provider. (you do not need to write your own code to do this)
- User pool is user based. It handles things like user registration, authentication, and account recovery.
- Identity pools authorise access to your AWS resources.