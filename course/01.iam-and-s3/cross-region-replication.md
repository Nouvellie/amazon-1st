# CROSS REGION REPLICATION
## Replication

Click on *management* and then **Replication**.

#### Replication rule:

- Set source.
	- [x] Entire bucket. <\bucketname\>

- Destination.
	- [x] Create a new bucket.
		- Bucket name: \<bucketname\>
		- Bucket region: \<bucketregion\> (<US East (N. Virginia)>)
	- Destination bucket: \<destinationbucketname\>

- Configuration rule.
	- IAM role: \<newrole\>
	- Rule name: \<rolename\>
	- [x] Status.

#### Tips:

- Any new update, addition or deletion of objects will also apply to the new replication.
- Versioning must be enabled on both the source and destination buckets.
- Regions must be unique.
- Files in an existing bucket are not replicated automatically.
- All subsequent updated files will be replicated automatically.
- Delete markers are not replicated.
- Deleting individual versions or delete markers will not be replicated.