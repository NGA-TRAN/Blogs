# Designs and Implementation of InfluxData's IOx

* **Sharding**: Scaling throughput and performance in a sharding database system: Understand the two dimensions of scaling for database query and ingest workloads, and how sharding can make scaling elastic—or not [publised in InfoWorld in April 2022](https://www.infoworld.com/article/3656915/scaling-throughput-and-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/scaling-throughput-performance-sharding-database-system/) or its [original pdf verson](scaling_throughput_and_performance_in_a_sharidng_DB.pdf)
  
* **Partitioning**: Partitioning effects in a sharding database system [publised in InfoWorld in August 2022](https://www.infoworld.com/article/3666513/partitioning-for-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/partitioning-performance-sharding-database-system/) or its [original pdf](partitioning_effects_in_a_sharding_database.pdf)
  
* **Deduplication**:
  * Coming soon: a general post to describe the job of deduplciation and its effective alternative to transaction
  * [Specific implementation of Deduplication in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/dedup_and_sort.md)
  
* **Compaction**:
  * Coming soon: a general post to describe the job of compaction and why it helps with better performance in data ingesting and querying
  * [Specific implementation of Compaction in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/compactor.md)
  
* **Data Retention**:
  * Coming soon: a general post on why implementation of data retention needs consideration on behaviors of different components in the system
  * [Specifc implementation of Data Retention in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/retention_policy.md)
  
* **Projection & Predicate Pushdown**: [Querying Parquet with Millisecond Latency](https://www.influxdata.com/blog/querying-parquet-millisecond-latency/) - December 2022
  
* **Multi-Column Sorts**: Fast and Memory Efficient Multi-Column Sorts in Apache Arrow Rust: [Part 1](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-1/) and [Part 2](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-2/) - November 2022