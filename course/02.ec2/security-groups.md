# SECURITY GROUPS
## Tips

- All inbound traffic is blocked by default.
- All outbound traffic is allowed.
- Changes to security group take effect immediately.
- You can have any number of EC2 instances within a security group.
- You can have multiple security groups attached to EC2 instances.
- Security group are **STATEFUL**.
- If you create an inbound rule allowing traffic in, that traffic is automatically allowed back out again.
- You can not block specific IP address using security groups, instead use Network Access Control Lists.
- You can specify allow rules, but not deny rules.