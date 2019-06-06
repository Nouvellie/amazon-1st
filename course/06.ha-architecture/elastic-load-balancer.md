# ELASTIC LOAD BALANCER
## What is it?

It is a physical or virtual device that's designed to help you balance network load across multiple web servers.

You can also use it for applications, it does not have to necessarily be internet facing load balancer but typically they are internet facing and primarily they are used to balance load across web servers.

## Types
#### Application load balancer:

Are best suited for load balancing of HTTP and HTTPS traffic. They operate at Layer 7 and are application-aware. They are intelligent, and you can create advanced request routing, sending specified requests to specific web servers.

#### Network load balancer:

Are best suited for load balancing of TCP traffic where extreme performance is required. Operating at the connection level (Layer 4), Network Load Balancer are capable of handling millions of requests per second, while maintaining ultra-low latencies. Use for extreme performance!

#### Classic load balancer:

Are the legacy Elastic Load Balancers. You can load balance HTTP/HTTPS applications and use Layer 7-specific features, such as X-Forwarded and sticky sessions. You can also use strict Layer 4 load balancing for applications that rely purely on the TCP protocol.

If your application stops responding, the ELB (Classic Load Balancer) responds with a 504 error. This means that the application is having issues. This could be either at the web server layer or at the database layer. Identify where the application is failing, and scale it up or out where possible.