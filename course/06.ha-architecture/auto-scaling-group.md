# AUTO SCALING GROUP
## Create launch configuration

- **Name**: \<nameoflc\>
- [ ] Request spot instances.
- **IAM role**: <anyrole>
- [ ] Enable CloudWatch detailed monitoring.

#### Advanced details:

- **Kernel ID**: default.
- **RAM disk ID**: default.
- **User data**: \<scrip\> (any script)
- **IP address type**: Only assign a public IP address to instances launched in the default VPC and subnet. (default)

## Create auto scaling group

- **Group name**: \<asgname\>
- **Launch configuration**: \<nameoflc\>
- **Group size**: Star with \<3\> instances.
- **Subnet**: all.
- [ ] Keep this group at its initial size.
- [x] Use scaling policies to adjust the capacity of this group.

#### Conf:

- **Name**: \<scalegroupsize\>
- **Metric type**: \<Average CPU Utilization\>
- **Targer value**: \<80\>
- [ ] Disable scale-in.

## Tips

If we remove (termination) an instance of EC2, a new one is automatically created in the same availability zone to satisfy the established minimum requirement.