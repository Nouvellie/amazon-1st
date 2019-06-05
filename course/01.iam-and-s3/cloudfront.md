# CLOUDFRONT
## What is Content delivery network (CDN)

Is a system of distributed servers (network) that deliver webpages and other web content to a user based on the geographic locations of the user, the origin of the webpage, and a content delivery server.

## Key terminology (CDN)

- **Edge location** - This is the location where content will be cached. This is separate to an AWS region/az.
- **Origin** - This is the origin of all the files that the CDN will distribute. This can be an S3 Bucket, an EC2 Instance. an Elastic Load Balancer, or Route53.
- **Distribution** - This is the name given the CDN which consists of a collection of Edge Locations.

## What is CloudFront?

It can be used to deliver your entire website, including dynamic, static, streaming, and interactive content using a global network of edge locations. Requests for your content are automatically routed to the nearest edge location, so content is delivered with the best possible performance.

## Key terminology (CF)

- **Web distribution** - Typically used for websites.
- **RTMP** - Used for media streaming.

## Tips

- Edge location are not just READ only. (you can write to them too, ie put an object on to them)
- Objects are cached for the life of the **TTL**. **(time to live)**
- You can clear cached objects, but you will be charged.

## Creation
##### CloudFront getting started

Click on *CloudFront*, then *create distribution*.

- Select a delivery method for your content.
	- [x] Web.
	- [ ] RTMP.

#### Origin settings

- Origin domain name: \<cloudname\>
- Origin path: \<filedefaultpath\> (optional)
- Origin ID: \<S3-cloudname\>
- Restrict bucket access:
	- [ ] Yes.
	- [x] No.

The rest of the options by default.

## CloudFront domain

Copy the domain name, and open the URL with the S3 bucket filename as extension.