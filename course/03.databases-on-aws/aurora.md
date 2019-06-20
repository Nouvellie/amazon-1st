# AURORA
## What is Aurora?

Amazon Aurora is a MySQL-compatible, relational database engine that combines the speed and availability of high-end commercial databases with the simplicity and cost-effectiveness of open source databases. Amazon Aurora provides up to five times better performance than MySQL at a price point one tenth that of a commercial database while delivering similar performance and availability.

## The basics of Aurora

**Things to know about Aurora**:

- Start with 10 GB, Scales in 10 GB increments to 64 TB. (storage autoscaling)
- Compute resources can scale up to 32vCPUs and 244 GB of Memory.
- 2 copies of your data is contained in each availability zone, with minimum of 3 availability zones. 6 copies of your data.

## Scaling Aurora

- Aurora is designed to transparently handle the loss of up to two copies of data without affecting database write availability and up to three copies without affecting read availability.
- Aurora storage is also self-healing. Data blocks and disks are continuously scanned for errors and repaired automatically.

## Two types of Aurora Replicas are available

- Aurora replicas. (currently 15)
- MySQL read replicas. (currently 5)

## Backups with Aurora

- Automated backups are always enabled on Amazon Aurora DB Instances. Backups do not impact database performance.
- You can also take snapshots with Aurora. This also does not impact on performance.
- You can share Aurora Snapshots with other AWS accounts.