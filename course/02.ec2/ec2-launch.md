# EC2 LAUNCH
## Create

Click on *services* and then **launch**.

- Configure instance:
	- Number of instances: 1. (by default)
	- [ ] Request Spot instances.
	- Network: default vpc.
	- Subnet: any.
	- Auto-assign public IP: Enable.
	- [ ] Placement group. (high performance computing)
	- Capacity reservation: Open.
	- IAM role: None.
	- Shutdown behavior: Stop.
	- [x] Enable termination protection.
	- [ ] Monitoring.
	- Tenancy: Shared.
	- [ ] Elastic interference.
	- [ ] T2/T3 unlimited.
- Add storage:
	- Volume Type: General purpose SSD. (gp2)
	- Size: 8 (GiB)
	- [x] Delete on termination.
- Tags:
	- [x] Instances.
	- [x] Volumes.

| Name  | WebServer |
| --- | --- |
| Department | Developer |
| EmployeeID | 123456 |

- Security group:
	- Select an **existing** security group.

- Review: 
	- Create a new key pair.
	- Key pair name: \<keypairname\>.
	- Download Key Pair and launch instances.

## Settings:

```sh
$ chmod 400 <keypairname.pem>
$ ssh ec2-user@<public-ip> -i <keypairname.pem>
yes
```

## Tips

- Termination protection is **turned off** by default, you must turn it on.
- On an EBS-Backed instance, the **default action is for the root EBS volume to be deleted** when the instance is terminated.
- EBS Root Volumes of your DEFAULT AMI's can not by encrypted. You can also use a third party tool (such as bit locker, etc.) to encrypt the root volume, or this can be done when creating AMI's (lab to follow) in the AWS console or using the API.
- Additional volumes can be encrypted.