# Designs of Specific Database Components

* [Vertica Optimizer](https://www.researchgate.net/profile/Nga_Tran6/publication/269306314_The_Vertica_Query_Optimizer_The_case_for_specialized_query_optimizers/links/55aeb17208aed9b7dcdda55f.pdf) - 2014 - "The Vertica Query Optimizer: The Case for Specialized Query Optimizers"
An in-depth architecture of Vertica *Query Optimizer* used for both On-Premise and Cloud (Eon) modes.

* [Snowflake Optimizer](https://www.youtube.com/watch?v=CPWn1SZUZqE&feature=youtu.be) - 2020 - Snowflake Query Optimizer Talk at CMU
An in-dept talk about the architecture of Snowflake Query Optimizer.

* [Vertica BDB](https://ieeexplore.ieee.org/document/6816725) - 2014 - "DBDesigner: A customizable physical design tool for Vertica Analytic Database"
An in-depth architecture of Vertica *Table's Physical Storage Design* applied to both On-Premise and Cloud (Eon) modes.

* [SIPS](https://15721.courses.cs.cmu.edu/spring2019/papers/15-execution/shrinivas-icde2013.pdf) - 2013 - "Materialization Strategies in the Vertica Analytic Database: Lessons Learned"
In-depth strategies of *data materialization for joins* of columnar DB.

* [Vertica Materialized View](https://github.com/NGA-TRAN/Notes/blob/main/Papers/FlattenedTable_LiveAggregateProjecttions.pdf) - ICDE 2019 - 2019 - "Vertica Flattened Tables and Live Aggregate Projections: A Column-based Alternative to Materialized Views for Analytics"
Designs of two different materialized views, *flattening and aggregation*, that are easy to use and, when combined, provide complete materialized views.

* [Sharding](https://www.infoworld.com/article/3656915/scaling-throughput-and-performance-in-a-sharding-database-system.html) - 2022 - "Scaling throughput and performance in a sharding database system"
Understanding the two dimensions of scaling for database query and ingest workloads, and how sharding can make scaling elastic—or not.
  
* [Partitioning](https://www.infoworld.com/article/3666513/partitioning-for-performance-in-a-sharding-database-system.html) - 2022 - "Partitioning for performance in a sharding database system"
Understanding partitioning effects and techniques for your choice of partitioning your data.
      
* [Projection & Predicate Pushdown](https://www.influxdata.com/blog/querying-parquet-millisecond-latency/) - 2022 - "Querying Parquet with Millisecond Latency"
Learning pusdown techniques for better query perfornance.
  
* Multi-Column Sorts: [Part 1](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-1/) and [Part 2](https://arrow.apache.org/blog/2022/11/07/multi-column-sorts-in-arrow-rust-part-2/) - 2022 - "Fast and Memory Efficient Multi-Column Sorts in Apache Arrow Rust"
Learning low-level techniques for building fast multi-column sorts

* **Deduplication**: Coming soon
  
* **Compaction**: Coming soon
