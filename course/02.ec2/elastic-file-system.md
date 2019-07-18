# ELASTIC FILE SYSTEM
## What is EFS?

Amazon Elastic File System (Amazon EFS) is a file storage service for amazon elastic compute cloud (Amazon EC2) instances.
Amazon EFS is a easy to use and provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon EFS, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your applications have the storage they need, when they need it.

## Mount instructions

- Open SSH client and connect to your EC2 instance.
- Create a new directory on your EC2 instance, such as "efs".
```sh
$ sudo mkdir efs
```