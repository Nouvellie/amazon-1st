# S3 SECURITY AND ENCRYPTION
## Basic

By default, all newly create bucket are **PRIVATE**. You can setup access control to your buckets using:

- Bucket policies.
- Access control lists.

S3 Buckets can be configured to create access logs which log all requests made to the S3 bucket. This can be sent to another bucket and even another bucket in another account.

Encryption in transit is achieved by:

- **SSL/TLS**.

Encryption at rest (server side) is achieved by:

- **S3 managed keys. (SSE S3)**
- **AWS key management service, managed keys. (SSE KMS)**
- **Server side encryption with customer provided keys. (SSE C)**