# DYNAMO DB
## What is Dynamo DB?

Amazon Dynamo DB is a fast and flexible NoSQL database service for all applications that need consistent, single-digit millisecond latency at any scale. It is a fully managed database and supports both document and key-value data models. Its flexible data model and reliable performance make it a great fit for mobile, web, gaming, ad-tech, IoT, and many other applications.

## The basics of Dynamo DB are as follows

- Store on SSD Storage.
- Spread across 3 geographically distinct data centres.
- Eventual consistent reads. (default)
- Strongly consistent reads.

#### Eventual consistent reads:

- Consistency across all copies of data is usually reached within a second. Repeating a read after a short time should return the updated data. (best read performance)

#### Strongly consistent reads:

- A strongly consistent read returns a result that reflects all writes that received a successful response prior to the read.