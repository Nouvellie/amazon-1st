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

- Mount your file system with a method listed following. If you need encryption of data in transit, use the EFS mount helper and the TLS mount option.

```sh
$ sudo mount -t efs fs-la3e80d2:/ efs # Using the EFS mount helper.
$ sudo mount -t efs -o tls fs-la3e80d2:/ efs # Using the EFS mount helper and the TLS mount option.
$ sudo mount -t nfs4 -o nfsvers=4.1,rsize=1048576,wsize=1048576,hard,timeo=600,retrans=2,noresvport fs-la3e80d2.efs.eu-west-1.amazonaws.com:/ efs # Using the NFS client.
```

## Tips

- Supports the network file system version 4 (NFSv4) protocol.
- You only pay for the storage you use. (no pre-provisioning required)
- Can scale up to the petabytes.
- Can support thousands of concurrent NFS connections.
- Data is stored across multiple AZ's within a region.
- Read after write consistency.