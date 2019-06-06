# AMI TYPES
## AMI's

You can select your AMI based on:

- Region. (see Regions and Availability Zones)
- Operating system.
- Architecture. (32-bit or 64-bit)
- Launch permissions.
- Storage for the Root Device. (Root Device Volumes)
	- Instance Store (**EPHEMERAL STORAGE**)
	- EBS Backed Volumes.

## EBS vs Instance Store Volumes

All AMIs are caterogized as either backed by Amazon EBS or backed by instance store.

**For EBS Volumes**: The root device for an instance launched from the AMI is an Amazon EBS volume create from an Amazon EBS snapshot.

**For Instance Store Volumes**: The root device for an instance launched from the AMI is an instance store volume created from a template stored in Amazon S3.

## Tips

- Instance store volumes are sometimes called Ephemeral storage.
- Instance store volumes can not be stopped. If the underlying host fails, you will lose your data.
- EBS backed instances can be stopped. You will not lose the data on this instance if it is stopped.
- You can reboot both, you will not lose your data.
- By default, both ROOT volumes will be deleted on termination. However, with EBS volumes, you can tell AWS to keep the root device volume.