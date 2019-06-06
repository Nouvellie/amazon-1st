# VOLUMES AND SNAPSHOTS
## Tips

- Volumes exist on EBS. Think of EBS as a virtual hard disk.
- Snapshots exist on S3. Think of snapshots as a photograph of the disk.
- Snapshots are point in time copies of Volumes.
- Snapshots are incremental. (this meas that only the blocks that have changed since your last snapshots are moved to S3)
- If this is your first snapshots, it may take some time to create.
- To create a snapshot for Amazon EBS volumes that serve as roo devices, you should stop the instance before taking the snapshot.
- However you can take a snap while the instance is running.
- You can create AMI's from both Volumes and Snapshots.
- You can change EBS volume size on the fly (only increase), including changing the size and storage type.
- Volumes will ALWAYS be in the same availability zone as the EC2 instance.
- To move an EC2 volume from one AZ to another, take a snapshot of it, create an AMI from the snapshot and then use the AMI to launch the EC2 instance in a new AZ.
- To move an EC2 volume from one region to another, take a snapshot of it, create an AMI from the snapshot and then copy the AMI from one region to the other. Then use the copied AMI to launch the new EC2 instance in the new region.

## Extra

- [Ami and snapshots.](https://github.com/Nouvellie/amazon/blob/amazon/contents/ami-snapshots.md)
- [Attach volume.](https://github.com/Nouvellie/amazon/blob/amazon/contents/attach-volume.md)