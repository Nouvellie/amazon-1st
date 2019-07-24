# NAT
## What is NAT instances?

You can use a network address translation (NAT) instance in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the Internet or other AWS services, but prevent the instances from receiving inbound traffic initiated by someone on the Internet.

NAT is not supported for IPv6 traffic—use an egress-only Internet gateway instead.

## NAT instance basics

The following figure illustrates the NAT instance basics. The main route table is associated with the private subnet and sends the traffic from the instances in the private subnet to the NAT instance in the public subnet. The NAT instance sends the traffic to the Internet gateway for the VPC. The traffic is attributed to the Elastic IP address of the NAT instance. The NAT instance specifies a high port number for the response; if a response comes back, the NAT instance sends it to an instance in the private subnet based on the port number for the response.

## Source/Destination Checks

Each EC2 instance performs source/destination checks by default. This means that the instance must be the source or destination of any traffic it sends or receives. However, a NAT instance must be able to send and receive traffic when the source or destination is not itself. Therefore, you must disable source/destination checks on the NAT instance.

## Testing your NAT instance configuration

After you have launched a NAT instance and completed the configuration steps above, you can perform a test to check if an instance in your private subnet can access the Internet through the NAT instance by using the NAT instance as a bastion server. To do this, update your NAT instance's security group rules to allow inbound and outbound ICMP traffic and allow outbound SSH traffic, launch an instance into your private subnet, configure SSH agent forwarding to access instances in your private subnet, connect to your instance, and then test the Internet connectivity.

## Tips
#### NAT instances:

- When creating a NAT instance, disable source/destination check on the instance.
- NAT instances must be in a public subnet.
- There must be a route out of the private subnet to the NAT instance, in order for this work.
- The amount of traffic that NAT instances can support depends on the instance size. If you are bottlenecking, increase the instance size.
- You can create high availability using Autoscaling Groups, multiple subnets in different AZs, and a script to automate failover.
- Behind a Security Group.

#### Nat gateways:

- Redundant inside the availability zone.
- Preferred by the enterprise.
- Starts at 5GBps and scales currently to 45Gbps.
- No need to patch.
- Not associated with security groups.
- Automatically assigned a public ip address.
- Remember to update your route tables.
- No need to disable source/destination checks.
- If you have resources in multiple availability zones and they share one Nat gateway, in the event that the NAT gateway's availability zone is down, resources in the other availability zone lose internet access. To create an availability zone-independent architecture, create a NAT gateway in each availability zone and configure your routing to ensure that resources use the NAT gateway in the same availability zone.