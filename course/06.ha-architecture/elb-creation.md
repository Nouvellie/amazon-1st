# ELB CREATION
## Load balancer type

Select *create load balancer*. (classic)

## Define load balancer

- **Load balancer name**: \<loadbalancername\>
- **Create LB inside**: \<vpcname\>
- [ ] Create an internal load balancer.
- [ ] Enable advanced VPC configuration.
- [ ] Listener configuration.
- **Load balancer protocol**: \<HTTP\>.

## Assign security groups

Select an existing or new security group.

## Configure health check

- **Ping protocol**: \<HTTP\>
- **Ping port**: \<80\>
- **Ping path**: \<projectpath-or-index.html\>

#### Advanced details:

- **Response timeout**: \<2\>
- **Interval**: \<5\>
- **Unhealthy threshold**: \<2\>
- **Healthy threshold**: \<3\>

## Select EC2 instances

Select all the instance to apply ELB.

- [x] Enable Cross-Zone load balancing.
- [x] Enable connection draining. \<300\>

#### Status of instance:

Check load balancer instances:
- [x] InService.
- [ ] OutOfService.

## Target group

Is basically where you load balancer is going to root request to the targets in that target group, and using the target that you specify and perform health checks.

So it is basically you could have a group of loot of easy two instances for your European customers, then you could have different ones for your American customers which have different language settings, etc. You can actually craete application load balancer that detect it and send it to the right groups.

#### Creation:

- **Target group name**: \<webgroupname\>
- **Target type**: \<Instance\>
- **Protocol**: <\HTTP\>
- **Port**: \<80\>
- **Vpc**: \<defaultone\>

- **Health check settings**:
	- Protocol: \<HTTP\>
	- Path: \<pathtoourweb\>
- **Advanced health check settings**:
	- Port: \<traffic-port\>
	- Healthy threshold: \<2\>
	- Unhealthy threshold: \<3\>
	- Timeout: \<5\>
	- Interval: \<6\>
	- Success codes: \<200\>
- Add instances to the registered target groups.

## Now create a load balancer with the target group

- Select *load balancer* and pick up the first option. (Application Load Balancer)
- Name: \<mynewloadbalancer\>
- Scheme: \<internet-facing\>

#### Listener:

On *listener* the rules can be edited.