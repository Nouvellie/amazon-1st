# DATABASE 101
## What is a relational database?

Relational databases are what most of us are all used to. They have been around since the 70's. Think of a traditional spreadsheet:

- Database.
- Tables.
- Row.
- Fields.

#### Relational databases on AWS:

- SQL Server.
- Oracle.
- MySQL Server.
- PostgreSQL.
- Aurora.
- MariaDB.

## Multi-AZ vs read replicas

RDS has two key features:

- **Multi-AZ**: For disaster recovery.
- **Read replicas**: For performance.

## Non relational databases are as follows

- **Collection**: Table.
- **Document**: Row.
- **Key Value Pairs**: Fields.

## What is Data Warehousing?

Used for business intelligence. Tools like Cognos, Jaspersoft, SQL Server Reporting Services, Oracle Hyperion, SAP NetWeaver.

Used to pull in very large and complex data sets. Usually used by management to do queries on data (such as current performance vs targets etc)

## OLTP vs OLAP

Online Transaction Processing (OLTP) differs from Online Analytics Processing (OLAP) in terms of the types of queries you will run.

#### OLTP Example:

Order number 9897898.
Pulls up a row of data such as Name, Date, Address to deliver to, delivery status, etc.

#### OLAP Example:

Net profit for EMEA and pacific for the digital radio product.
Pulls in large numbers of records.

Sum of radios sold in EMEA.
Sum of radios sold in pacific.
Unit cost of radio in each region.
Sales price of each radio.
Sales price. (unit cost)

Data Warehousing databases use different type of architecture both from a database perspective and insfrastructure layer.

Amazon's Data Warehouse solution is called Redshift.

## What is ElastiCache?

ElastiCache is a web service that makes it easy to deploy, operate, and scale an in-memory cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slower disk-based databases.

ElastiCache supports two open-source in-memory caching engines:

- Memcached.
- Redis.