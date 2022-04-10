# Reading Materials for Building Distributed (Cloud) Databases

_Initial version: 2021/1/19_

_Latest updated: 2021/3/6_

More useful readings will be added time to time

--------------------------------------

These are classes, papers, journals or books written by DB researchers and builders that I find worth learning if you want to join the DB-builder community or even build your own DB. Some papers cover high-level architecture of a DB, some describe a major DB component in depth, some illustrate certain techniques to build or improve a specific sub-component. If you have never read any of these, start from the top and high-level ones. Each paper will include a short/nick name, year of publishing, full title and a brief summary.
<br>
<br>

## Basic Readings & Classes 

### Readings
* [System Design](https://www.amazon.com/System-Design-Interview-Insiders-Guide-ebook/dp/B08B3FWYBX) - 2020 - "System Design Interview - An Insider's Guide" by Alex Xu
A book that covers high-level designs of distributed systems, and, although it does not focus on DB, it introduces challenges all DB builders want to solve and relevant technologies used to do solve them. I highly recommend you to read at least the first half of this book in the order the chapters are laid out before reading the following materials.

### Classes

* [CMU's Intro to Database System](https://www.youtube.com/playlist?list=PLSE8ODhjZXjbohkNBWQs_otTrBTrjyohi) - 2019 by Prof. Andy Pavlo

* [CMU's Advanced Database Systems](https://15721.courses.cs.cmu.edu/spring2020/schedule.html) that links to all slides & [videos](https://www.youtube.com/playlist?list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O) - 2020 by Prof. Andy Pavlo
    * In-memory DBs & Comparisons of different transaction management schemes: [class 2](https://www.youtube.com/watch?v=a70jRWLjQFk&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=2)
    * MVCC (Multi-Version Concurrency Control)
        * [CMU's MVCC design](https://15721.courses.cs.cmu.edu/spring2019/papers/03-mvcc1/wu-vldb2017.pdf) on their Peloton DB: [class 3](https://www.youtube.com/watch?v=1Od_SuOQshM&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=3)
         * MVVC designs of [MS Hekaton](http://pages.cs.wisc.edu/~yxy/cs839-s20/papers/Hekaton-Sigmod2013-final.pdf), 
[TUM HyPer](http://www.cs.albany.edu/~jhh/courses/readings/kemper.icde11.memory.pdf), [SAP HANA](https://www.cs.cmu.edu/~pavlo/courses/fall2013/static/papers/p731-sikka.pdf), [CMU Cicada](https://15721.courses.cs.cmu.edu/spring2019/papers/04-mvcc2/lim-sigmod2017.pdf): [class 4](https://www.youtube.com/watch?v=DjWo8ixF9QY&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=4)
         * Garbage Collector methods: [MS Hekaton](http://pages.cs.wisc.edu/~yxy/cs839-s20/papers/Hekaton-Sigmod2013-final.pdf), [TUM HyPer](https://db.in.tum.de/~boettcher/p128-boettcher.pdf), [SAP HANA](https://www.researchgate.net/profile/Seongyun-Ko/publication/304021444_Hybrid_Garbage_Collection_for_Multi-Version_Concurrency_Control_in_SAP_HANA/links/5d5b7fd592851c37636bd897/Hybrid-Garbage-Collection-for-Multi-Version-Concurrency-Control-in-SAP-HANA.pdf), [CMU Cicada](https://15721.courses.cs.cmu.edu/spring2019/papers/04-mvcc2/lim-sigmod2017.pdf): [class 5](https://www.youtube.com/watch?v=8cwokv2y-c4&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=5)
    * OLTP Indexes
        * In-Memory T-Tree, Latch-Free Bw-Tree, B+Tree Optimistic Latching: [class 6](https://www.youtube.com/watch?v=asyvZHhpMOY&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=6)
        * Latches, B+Trees, Judy Array, ART, MassTree: [class 7](https://www.youtube.com/watch?v=N6rhECUjdaI&list=PLSE8ODhjZXjasmrEd2_Yi1deeE360zv5O&index=7)
    * Data Type Presentation & Storage Models [class 8](https://www.youtube.com/watch?v=y6qFHu0YKMM&t=3692s), [slides](https://15721.courses.cs.cmu.edu/spring2017/slides/10-storage.pdf)
        * Type Presentation & Layout: Numbers (fixed & variable precision numbers), Varchar & Blob (fixed & variable length), time, null
        * Storage models: N-ary Storage Model (NSM) for row-store, Decomposition Storage Model (DSM) for column-store, and Hybrid Storage Model 
        * Hybrid workloads: [Casper](https://dl.acm.org/doi/pdf/10.14778/3358701.3358707?casa_token=zJVMHwuD6LQAAAAA:RdB_xUnAfrcFnnK4PTN1PFm0M3ZOJXQ0jUa3vhzy0t7DAWcF_Tntk9J_LGOKmfpRE47qBDDBohmqkA), [Peloton](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/arulraj-sigmod2016.pdf), [H2O](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/h2o.pdf), [HYRISE](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/p105-grund.pdf), [Column-Stores vs Row-stores](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/p967-abadi.pdf)

## Designs of Commercial Databases

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

## References

* [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321) - 2017 by Martin Kleppmann
A thick book that describes a various sets of technologies used to design not only DBs but data-intensive applications. It is recommended to only read a little bit of this book everyday while reading the other materials, or use it as a reference to fill your missing knowledge. Without specific use cases for your designs, you will get lost easily in this book.
