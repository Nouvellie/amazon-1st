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

## IAM LAB (Identity and access management)
#### IAM users:

Click *customize* and change the IAM user sign-in link.

#### Activate MFA:

Click *activate MFA on your root account*, and select the *Virtual MFA device* option. Using a mobile device and a google authenticator add two consecutive MFA codes bellow.

#### Create IAM Users:

- Click *create individual IAM users*, and create a group with some permission to end.
- Click *users* and then *security credentials*, here we can set a custom password for the account, and below te git credential.

#### Password policy:

Click *Apply an IAM password policy* and then *manage*.

Enable:

- [x] Require at least one uppercase letter.
- [x] Require at least one lowercase letter.
- [x] Require at least one number.
- [x] Require at least one non-alphanumeric character.
- [x] Allow users to change their own password.
- [x] Minimum password length. (12)

## Role
#### Create role (s3)

Select *AWS service*, and then:

- [x] AmazonS3FullAccess.
- Role name: S3_Admin_Access.
- Role description: Allows EC2 instances to call AWS services on your behalf.

## What have we learnt so far.

- IAM is universal: It does not apply to regions at this time.
- The **root account** is simply, the account created when first setup your AWS account, It has complete Admin Access.
- New users have **no permissions** when first created.
- New users are assigned **access key id & secret access keys**, when first created.
- **These are not the same as a password.** You cannot use the access key id & secret access key to login into the console. You can use this access AWS via the APIs and command line, however.
- **You only get to view these once.** If you lose them, you have to regenerate them. So, save them in a secure location.