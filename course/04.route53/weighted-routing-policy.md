# WEIGHTED ROUTING POLICY
## Tips

Allows you split your traffic based on different weights assigned.
For example: you can set 10% of your traffic to go to US-EAST-1 and 90% to go to EU-WEST-1.

- You can set health checks on individual record sets.
- If a record set fails a health check it will be removed from Route53 until it passes the health check.
- You can set SNS notifications to alert you if a health check is failed.