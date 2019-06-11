# ADVANCED LOAD BALANCER
## What are Sticky Sessions?

Classic Load Balancer routes each request independently to the registered EC2 instance with the smallest load.

Sticky sessions allow you to bind a user's session to a specific EC2 instance. This ensures that all requests from the user during the session are sent to the same instance.

You cab enable Sticky Sessions for application Load Balancer as well, but the traffic will be sent to at the Target Group Level.

## Cross Zone Load Balancing

- Without CZLB:
	- A (50%)
		- A1: 12.5%.
		- A2: 12.5%.
		- A3: 12.5%.
		- A4: 12.5%.
	- B (50)
		- B1: 50%.

- With CZLB:
	- A (50%)
		- A1: 20%.
		- A2: 20%.
		- A3: 20%.
		- A4: 20%.
	- B (50)
		- B1: 20%.

## What are path patterns?

You can create a listener with rules to forward requests based on the URL path. This is known as path-based routing. If you are running microservices, you can route traffic to multiple back-end services uing path-based routing. For example, you can route general requests to one target group and requests to render images to another target group.

## Advanced Load Balancer Theory

- Sticky Sessions enable your users to stick to the same EC2 instance. Can be useful if you are storing information locally to that instance.
- Cross Zone Load Balancing enables you to load balance across multiple availability zones.
- Path patters allow you to direct traffic to different EC2 instances based on the URL contained in the request.