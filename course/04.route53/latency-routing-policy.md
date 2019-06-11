# LATENCY ROUTING POLICY
## Latency-based routing

Allows you to route your traffic based on the lowest network latency for your end user. (ie which region will give them the fastest response time)

To use latency-based routing, you create a latency resource record set for the Amazon EC2 (or ELC) resource in each region that hosts your website. When Amazon Route 53 receives a query for your site, it selects the latency resource record set for the region that gives the user the lowest latency. Route 53 then responds with the value associated with that resource record set.