# Posted
* Scaling throughput and performance in a sharding database system: Understand the two dimensions of scaling for database query and ingest workloads, and how sharding can make scaling elastic—or not [publised in InfoWorld](https://www.infoworld.com/article/3656915/scaling-throughput-and-performance-in-a-sharding-database-system.html) or its [original pdf verson](https://github.com/NGA-TRAN/Blogs/blob/main/scaling_throughput_and_performance_in_a_sharidng_DB.pdf)
* [Distributed Cloud Columnar Databases: Vertica Eon vs Snowflake](https://github.com/NGA-TRAN/Blogs/blob/main/vertica_snowflake.md)
* [Reading Materials for Building Distributed (Cloud) Databases](https://github.com/NGA-TRAN/Blogs/blob/main/readings.md)
# To be written

* Why are tools for system monitoring and log analysis top priority?
* The roles of three major components of a DB: Query Optimizer, Execution Engine, and Storage.
* Elastic throughput scaling vs elastic crunch scaling. Should we have a design that supports both?
* Transaction Isolation: Serial Execution vs Two-Phase Locking vs Serialization Snapshot Isolation
* Storage for availability, scaling, and performance. _Many possible subtopics_:
    * Segmentation vs Partitioning.
    * Segments vs Shards.
    * Fault Tolerance: buddy projections vs buddy subscription.
    * Hierarchical partitioning for hot and cold data.
* Why Query Optimizer and Execution go hand in hand? _Many possible subtopics_:
    * Global plan vs Local plan vs Execution plan.
    * Predicate push-down & SIPS.
    * Group-by push-down vs Group-by Pipeline.
    * Partition Prunning.
* Why does column-stored DB need a built-in & auto-run Database Designer?
* Materialized Views: What are specific use cases for the right designs?
    * Flattened Table vs Live Aggregate Projection
    



