# IAM
## What is IAM?

IAM allows you to manage users and their level of access to the AWS console.

## Features

- Centralised control of your AWS account.
- Shared access to your AWS account.
- Granular permissions.
- Identity federation. (including active directory, facebook, linkedin, etc)
- Multifactor authentication.
- Provide temporary access for users/devices and services where necessary.
- Allow you to set up your own password rotation policy.
- Integrates with many different AWS services.
- Supports PCI DSS compliance.

## Key terminology for IAM

- Users: End users such as people, employees of an organization, etc.
- Groups: A collection of users. Each user in the group will inherit the permission of the group.
- Policies: Polices are made up of documents, called policy documents. These documents are in a format called *JSON* ant they give permissions as to what user/group/role is able to do.
- Roles: You create roles and then assign them to AWS resources.

## IAM LAB
#### Activate MFA:

Click *activate MFA on your root account*, and select the *Virtual MFA device* option. Using a mobile device and a google authenticator add two consecutive MFA codes bellow.

#### Create IAM Users:

Click *create individual IAM users*, and create a group with some permission to end.

#### Password policy:

Click *Apply an IAM password policy* and then *manage*.

Enable:

- [x] Require at least one uppercase letter.
- [x] Require at least one lowercase letter.
- [x] Require at least one number.
- [x] Require at least one non-alphanumeric character.
- [x] Allow users to change their own password.
- [x] Minimum password length. (12)