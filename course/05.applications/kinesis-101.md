# KINESIS 101
## What is streaming data?

Streaming data is data that is generated continuously by thousand of data sources, which typically send in the data records simultaneously, and is small sizes. (order by Kilobytes)

- Purchases from online stores. (think amazon.com)
- Stock prices.
- Game data. (as the gamer plays)
- Social network data.
- Geospatial data. (think uber.com)
- iOT sensor data.

## What is Kinesis?

Amazon Kinesis is a platform on AWS to send your streaming data to.

Kinesis makes it easy to load and analyze streaming data, and also providing the ability for you to build your own custom applications for you business needs.

#### Types:

- Kinesis Streams: (shards)
	- 5 transactions per second for reads, up to a maximum total data read rate of 2 MB per second and up to 1,000 records per second for writes, up to a maximum total write rate of 1 MB per second. (including partition keys.)
	- The data capacity of your stream is a function of the number of shards that you specify for the stream. The total capacity of the stream is the sum of the capacities of its shards.


- Kinesis Firehose:
 Is a fully managed service for delivering real-time streaming data to destinations such as Amazon Simple Storage Service (Amazon S3), Amazon Redshift, Amazon Elasticsearch Service (Amazon ES), and Splunk. Kinesis Data Firehose is part of the Kinesis streaming data platform, along with Kinesis Data Streams, Kinesis Video Streams, and Amazon Kinesis Data Analytics. With Kinesis Data Firehose, you don't need to write applications or manage resources. You configure your data producers to send data to Kinesis Data Firehose, and it automatically delivers the data to the destination that you specified. You can also configure Kinesis Data Firehose to transform your data before delivering it.

- Kinesis Analytics.
Amazon Kinesis Data Analytics is the easiest way to analyze streaming data, gain actionable insights, and respond to your business and customer needs in real time. Amazon Kinesis Data Analytics reduces the complexity of building, managing, and integrating streaming applications with other AWS services. SQL users can easily query streaming data or build entire streaming applications using templates and an interactive SQL editor. Java developers can quickly build sophisticated streaming applications using open source Java libraries and AWS integrations to transform and analyze data in real-time. Amazon Kinesis Data Analytics takes care of everything required to run your real-time applications continuously and scales automatically to match the volume and throughput of your incoming data. With Amazon Kinesis Data Analytics, you only pay for the resources your streaming applications consume. There is no minimum fee or setup cost.