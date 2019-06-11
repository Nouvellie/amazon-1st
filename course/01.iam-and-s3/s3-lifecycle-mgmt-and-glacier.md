# S3 LIFECYCLE MANAGEMENT AND GLACIER
## Lifecycle

Click on *management* and then **Lifecycle**.

#### Name and scope:

- Enter a rule name: \<MyLifecycleRule\>

#### Transition:

- Storage class transition.
	- [x] Current version.
	- [x] Previous versions.
	- [x] Transition to Standard-IA after: <30> (days after creation)
	- [x] Transition to Amazon Glacier after: <60> (days after creation)

#### Expiration:

- Configure expiration.
	- [x] Current version.
	- [x] Previous versions.
	- [x] Expire current version of object. <425> (days after from becoming a previous version)
	- [x] Clean up incomplete multipart uploads. <7> (days after from start of upload)

## Tips

- Automates moving your objects between the different storage tiers.
- Can be used in conjunction with versioning.
- Can be applied to current versions and previous versions.