# Designs and Implementation of InfluxData's IOx

* **System Architecture**: The architecture of Influx DB IOx (aka InfluxDB 3.0): a (cloud) scalable database that offers high performance for both data loading and querying, and focuses on time series use cases [published by InfluxData in June 2023](https://www.influxdata.com/blog/influxdb-3-0-system-architecture/) or in its [original pdf](InfluxDB_IOx_SystemArchitecture.pdf)

* **Sharding**: *Scaling throughput and performance in a sharding database system: Understand the two dimensions of scaling for database query and ingest workloads, and how sharding can make scaling elastic—or not* [published in InfoWorld in April 2022](https://www.infoworld.com/article/3656915/scaling-throughput-and-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/scaling-throughput-performance-sharding-database-system/) or its [original pdf](scaling_throughput_and_performance_in_a_sharidng_DB.pdf)
  
* **Partitioning**: *Partitioning effects in a sharding database system *[published in InfoWorld in August 2022](https://www.infoworld.com/article/3666513/partitioning-for-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/partitioning-performance-sharding-database-system/) or its [original pdf](partitioning_effects_in_a_sharding_database.pdf)
  
* **Deduplication**:
  * *Using deduplication for eventually consistent transactions* [published in InfoWorld in Jan 2023](https://www.infoworld.com/article/3683915/using-deduplication-for-eventually-consistent-transactions.html) or its [original pdf](deduplication.pdf)
  * [Specific implementation of Deduplication in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/dedup_and_sort.md)
  
* **Compaction**:
  * *Compactor: A hidden engine of database performance* [published in InfoWorld in Jan 2023](https://www.infoworld.com/article/3685496/compactor-a-hidden-engine-of-database-performance.html) or its [original pdf](compactor.pdf)
  * [Specific implementation of Compaction in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/compactor.md)
  
* **Data Retention**:
  * Coming soon: a general post on why implementation of data retention needs consideration on behaviors of different components in the system
  * [Specifc implementation of Data Retention in InfluxDB IOx](https://github.com/influxdata/influxdb_iox/blob/main/docs/retention_policy.md)
  
* **Projection & Predicate Pushdown**: [Querying Parquet with Millisecond Latency](https://www.influxdata.com/blog/querying-parquet-millisecond-latency/) - December 2022
  
* **Multi-Column Sorts**: Fast and Memory Efficient Multi-Column Sorts in Apache Arrow Rust: [Part 1](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-1/) and [Part 2](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-2/) - November 2022
  
* **Parallel Grouping**: [Aggregating Millions of Groups Fast in Apache Arrow DataFusion](https://www.influxdata.com/blog/aggregating-millions-groups-fast-apache-arrow-datafusion/) August 2023

* **Use cases of time series:**  [Metrics, Logs and Traces: More Similar Than They Appear?](https://www.influxdata.com/blog/metrics-logs-traces-more-similar-than-they-appear/) - May 2023

