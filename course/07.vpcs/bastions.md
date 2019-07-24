# BASTIONS
## What is a Bastion Host?

A bastion host is a special purpose computer on a network specifically designed and configured to withstand attacks. The computer generally hosts a single application, for example a proxy server, and all other service are removed or limited to reduce the threat to the computer. It is hardened in this manner primarily due to its location and purpose, which is either on the outside of a firewall or in a demilitarized zone (DMZ) and usually involves access from untrusted networks or computers.

## Tips

- A NAT Gateway or NAT instance is used to provide internet traffic to EC2 instances in a private subnets.
- A bastion is used to securely administer EC2 instances. (using SSH or RDP)
- Bastions are called jump boxes in Australia.
- You can not use a NAT Gateway as a Bastion Host.