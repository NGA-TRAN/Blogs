# Designs of Opensource and Commercial Distributed (Cloud) Databases

More useful readings will be added time to time

--------------------------------------

These are papers, journals and talks by DB researchers and builders that I find worth learning if you want to join the DB-builder community or even build your own DB. Some papers cover high-level architecture of a DB, some describe a major DB component in depth, some illustrate certain techniques to build or improve a specific sub-component. If you have never read any of these, you may want to start with the [Basic Readings](basic_readings.md) instead. Each paper will include a short/nick name, year of publishing, full title and a brief summary.

## Designs and Implementation of InfluxData's IOx

* **Sharding**: Scaling throughput and performance in a sharding database system: Understand the two dimensions of scaling for database query and ingest workloads, and how sharding can make scaling elastic—or not [publised in InfoWorld in April 2022](https://www.infoworld.com/article/3656915/scaling-throughput-and-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/scaling-throughput-performance-sharding-database-system/) or its [original pdf verson](scaling_throughput_and_performance_in_a_sharidng_DB.pdf)
* **Partitioning**: Partitioning effects in a sharding database system [publised in InfoWorld in August 2022](https://www.infoworld.com/article/3666513/partitioning-for-performance-in-a-sharding-database-system.html) or [republished by InfluxData in November 2022](https://www.influxdata.com/blog/partitioning-performance-sharding-database-system/)  its [original pdf](partitioning_effects_in_a_sharding_database.pdf)
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

--------------------------------------

## Designs of other Commercial Databases

### Comparisons of Internal Implementations and Offerings between Databases
* **Snowflake vs Vertica**: [Distributed Cloud Columnar Databases: Vertica Eon vs Snowflake](vertica_snowflake.md) - February 2021

### High-Level Designs
* [CStore](https://web.archive.org/web/20100619191833/http://db.lcs.mit.edu/projects/cstore/vldb.pf) - 2005 - "C-Store: A Column-oriented DBMS": A research paper that covers a full architecture of a *Distributed Share-nothing Columnar MPP* that fully support ACID.

* [Vertica](https://vldb.org/pvldb/vol5/p1790_andrewlamb_vldb2012.pdf) - 2012 - "The Vertica Analytic Database: C-Store 7 Years Later": A full architecture of a high performance *On-premise Distributed Data Warehouse* implementing CStore research ideas.

* [Vertica Eon](https://www.vertica.com/wp-content/uploads/2018/05/Vertica_EON_SIGMOD_Paper.pdf) - 2018 - "Eon Mode: Bringing the Vertica Columnar Database to the Cloud" & its related talks: [Vertica Eon 2020](https://www.thecube.net/vertica-bigdata-2020/content/Videos/GGE42drgkAHfYoFbn): An architecture of a *Distributed Cloud Data Warehouse* that enables the separation of compute and storage and fully supports ACID and fault tolerance. Vertica is famous for its high query performance and throughput.

* [Snowflake](http://pages.cs.wisc.edu/~remzi/Classes/739/Fall2018/Papers/p215-dageville-snowflake.pdf) - 2016 - "The Snowflake Elastic Data Warehouse" and its related talks: [Snowflake CIDR 2021](https://www.youtube.com/watch?v=0K7h7WvC6D4), [Snowflake Architecture 2019](https://www.youtube.com/watch?v=dxrEHqMFUWI): An architecture of a *DBaaS Distributed Cloud Data Warehouse* that enables the separation of compute and storage, and fully supports ACID and fault tolerance. Snowflake is famous for its DBaaS (DB as a Service) and ease of use.

### Designs of Specific Components

* [Vertica Optimizer](https://www.researchgate.net/profile/Nga_Tran6/publication/269306314_The_Vertica_Query_Optimizer_The_case_for_specialized_query_optimizers/links/55aeb17208aed9b7dcdda55f.pdf) -2014 - "The Vertica Query Optimizer: The Case for Specialized Query Optimizers"
An in-depth architecture of Vertica *Query Optimizer* used for both On-Premise and Cloud (Eon) modes.
* [Snowflake Optimizer](https://www.youtube.com/watch?v=CPWn1SZUZqE&feature=youtu.be) - 2020 - Snowflake Query Optimizer Talk at CMU
An in-dept talk about the architecture of Snowflake Query Optimizer.

* [Vertica BDB](https://ieeexplore.ieee.org/document/6816725) - 2014 - "DBDesigner: A customizable physical design tool for Vertica Analytic Database"
An in-depth architecture of Vertica *Table's Physical Storage Design* applied to both On-Premise and Cloud (Eon) modes.

* [SIPS](https://15721.courses.cs.cmu.edu/spring2019/papers/15-execution/shrinivas-icde2013.pdf) - 2013 - "Materialization Strategies in the Vertica Analytic Database: Lessons Learned"
In-depth strategies of *data materialization for joins* of columnar DB.

* [Vertica Materialized View](https://github.com/NGA-TRAN/Notes/blob/main/Papers/FlattenedTable_LiveAggregateProjecttions.pdf) - ICDE 2019 - 2019 - "Vertica Flattened Tables and Live Aggregate Projections: A Column-based Alternative to Materialized Views for Analytics"
Designs of two different materialized views, *flattening and aggregation*, that are easy to use and, when combined, provide complete materialized views.
