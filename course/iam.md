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