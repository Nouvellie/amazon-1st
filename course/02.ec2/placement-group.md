# PLACEMENT GROUP
## Clustered placement group

A cluster placement group is a grouping of instances within a single Availability Zone. Placement groups are recommended for applications that need low network latency, high network throughput, or both.

Only certain instances can be launched in to a Clustered Placement Group.

## Spread placement group

A spread placement group is a group of instances that are each placed on distinct underlying hardware.

Spread placement groups are recommended for applications that have a small number of critical instances that should be kept separate from each other.

## Tips

- A clustered placement group can not span multiple Availability Zones.
- A spread placement group can.
- The name you specify for a placement group must be unique within your AWS account.
- Only certain types of instances can be launched in a placement group. (compute optimized, gpu, memory optimized, storage optimized)
- AWS recommended homogenous instances within placement groups.
- You can not merge placement groups.
- You can not move an existing instance into a placement group. You can create an AMI from your existing instance, and the launch a new instance from the AMI into a placement group.