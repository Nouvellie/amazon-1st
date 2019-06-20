# REDSHIFT
## What is Redshift?

Amazon Redshift is a fast and powerful, fully managed, petabyte-scale data warehouse service in the cloud. Customers can start small for just 0.25 USD per hour with no commitments or upfront costs and scale to a petabyte or more for a 1000 USD per terabyte per year, less than a tenth of most other data warehousing solutions.

Data Warehousing databases use different type of architecture both from a database perspective and infrastructure layer.

## Redshift configuration

Redshift can be configured as follows:

- Single Node. (160 GB)
- Multi Node.
	- Leader Node. (manages client connections and receives queries)
	- Compute Node. (store data and perform queries and computations, up to 128 compute nodes)

## Advanced compression

Columnar data stores can be compressed much more than row-based data stores because similar data is stored sequentially on disk. Amazon Redshift employs multiple compression techniques and can often achieve significant compression relative to traditional relational data stores. In adition, Amazon Redshift does not require indexes or materialized views, and so uses less space than traditional relational database systems. When loading data into an empty table, Amazon Redshift automatically samples your data and selects the most appropiate compression scheme.

## Massively Parallel Processing (MPP)

Amazon Redshift automatically distributes data and query load across all nodes. Amazon Redshift makes it easy to add nodes to your data warehouse and enables you to maintain fast query performance as your data warehouse grows.

## Backups

- Enabled by default with a 1 day retention period.
- Maximum retention period is 35 days.
- Redshift always attempts to maintain at least three copies of your data. (the original and replica on the compute nodes and a backup in Amazon S3)
- Redshift can also asynchronously replicate your snapshots to S3 in another region for disaster recovery.

## Redshift is priced as follows

- Compute Node Hours. (total number of hours you run across all your compute nodes for the billing period. You are billed for 1 unit per node per hour, so a 3-node data warehouse cluster running persistently for an entire month would incur 2160 instance hours. You will not be charged for leader node hours, only compute nodes will incur charges)
- Backup.
- Data transfer. (only within a VPC, not outside it)

## Security considerations

- Encrypted in transit using SSL.
- Encrypted at rest using AES-256 encryption.
- By default Redshift takes care of key management.
	- Manage your own keys through HSM.
	- AWS Key Management Service.

## Redshift availability

- Currently only available in 1 AZ.
- Can restore snapshots to new AZs in the event of an outage.