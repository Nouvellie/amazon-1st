# S3 BUCKET
## S3 management console
#### Create:

- Bucket name: \<bucketname\>
- Region: <US East (N. Virginia)> (or any other)
- [x] Block: *all* public access.
- Storage class: \<Standard\> (has none retrieval fees)

## Public objects

If we upload a file, we can not make it public, but if we go back to the main menu and click on *edit public access setting* and *confirm*. All objects can now be public if we want.

## Info

- **Buckets are a universal namespace**.
- Upload an object to S3 receive a **HTTP 200 Code**.
- Control access to buckets using either a **bucket ACL** or using **bucket policies**.