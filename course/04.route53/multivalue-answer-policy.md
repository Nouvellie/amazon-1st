# MULTIVALUE ANSWER POLICY
## Tips

Multivalue answer routing lets you configure Amazon Route 53 to return multiple values, such as IP addresses for your web servers, in response to DNS queries. You can specify multiple values for almost any record, but multivalue answer routing also lets you check the health of each resource, so Route 53 returns only values for healthy resources.

**This is similar to simple routing however it allows you to put health checks on each record set**.