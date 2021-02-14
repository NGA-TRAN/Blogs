# Reading Materials for Building Distributed (Cloud) Databases

_Initial version: 2021/1/19_

_Latest updated: 2021/2/14_

More useful readings will be added time to time

--------------------------------------

These are papers, journals or books written by DB researchers and builders that I find worth learning if you want to join the DB-builder community or even build your own DB. Some papers cover high-level architecture of a DB, some describe a major DB component in depth, some illustrate certain techniques to build or improve a specific sub-component. If you have never read any of these, start from the top and high-level ones. Each paper will include a short/nick name, year of publishing, full title and a brief summary.
<br>
<br>


### [System Design](https://www.amazon.com/System-Design-Interview-Insiders-Guide-ebook/dp/B08B3FWYBX) - 2020 - "System Design Interview - An Insider's Guide" by Alex Xu
A book that covers high-level designs of distributed systems, and, although it does not focus on DB, it introduces challenges all DB builders want to solve and relevant technologies used to do solve them. I highly recommend you to read at least the first half of this book in the order the chapters are laid out before reading the following materials.

### [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321) - 2017 by Martin Kleppmann
A thick book that describes a various sets of technologies used to design not only DBs but data-intensive applications. Even though this book is listed as one of the first readings, it is recommended to only read a little bit of it everyday while reading the below materials, or use it as a reference to fill your missing knowledge. Without specific use cases for your designs, you will get lost easily in this book.


### [CStore](https://web.archive.org/web/20100619191833/http://db.lcs.mit.edu/projects/cstore/vldb.pf) - 2005 - "C-Store: A Column-oriented DBMS"
A research paper that covers a full architecture of a *Distributed Share-nothing Columnar MPP* that fully support ACID.

### [Vertica](https://vldb.org/pvldb/vol5/p1790_andrewlamb_vldb2012.pdf) - 2012 - "The Vertica Analytic Database: C-Store 7 Years Later"
A full architecture of a high performance *On-premise Distributed Data Warehouse* implementing CStore research ideas.

### [Vertica Eon](https://www.vertica.com/wp-content/uploads/2018/05/Vertica_EON_SIGMOD_Paper.pdf) - 2018 - "Eon Mode: Bringing the Vertica Columnar Database to the Cloud"
Related talks: [Vertica Eon 2020](https://www.thecube.net/vertica-bigdata-2020/content/Videos/GGE42drgkAHfYoFbn)

An architecture of a *Distributed Cloud Data Warehouse* that enables the separation of compute and storage and fully supports ACID and fault tolerance. Vertica is famous for its high query performance and throughput.

### [Snowflake](http://pages.cs.wisc.edu/~remzi/Classes/739/Fall2018/Papers/p215-dageville-snowflake.pdf) - 2016 - "The Snowflake Elastic Data Warehouse" and
Related talks: [Snowflake CIDR 2021](https://www.youtube.com/watch?v=0K7h7WvC6D4), [Snowflake Architecture 2019](https://www.youtube.com/watch?v=dxrEHqMFUWI)

An architecture of a *DBaaS Distributed Cloud Data Warehouse* that enables the separation of compute and storage, and fully supports ACID and fault tolerance. Snowflake is famous for its DBaaS (DB as a Service) and ease of use.

### [Vertica Optimizer](https://www.researchgate.net/profile/Nga_Tran6/publication/269306314_The_Vertica_Query_Optimizer_The_case_for_specialized_query_optimizers/links/55aeb17208aed9b7dcdda55f.pdf) -2014 - "The Vertica Query Optimizer: The Case for Specialized Query Optimizers"
An in-depth architecture of Vertica *Query Optimizer* used for both On-Premise and Cloud (Eon) modes.

### [Snowflake Optimizer](https://www.youtube.com/watch?v=CPWn1SZUZqE&feature=youtu.be) - 2020 - Snowflake Query Optimizer Talk at CMU
An in-dept talk about the architecture of Snowflake Query Optimizer.

### [Vertica BDB](https://ieeexplore.ieee.org/document/6816725) - 2014 - "DBDesigner: A customizable physical design tool for Vertica Analytic Database"
An in-depth architecture of Vertica *Table's Physical Storage Design* applied to both On-Premise and Cloud (Eon) modes.

### [SIPS](https://15721.courses.cs.cmu.edu/spring2019/papers/15-execution/shrinivas-icde2013.pdf) - 2013 - "Materialization Strategies in the Vertica Analytic Database: Lessons Learned"
In-depth strategies of *data materialization for joins* of columnar DB.

### [Vertica Materialized View](https://github.com/NGA-TRAN/Notes/blob/main/Papers/FlattenedTable_LiveAggregateProjecttions.pdf) - ICDE 2019 - 2019 - "Vertica Flattened Tables and Live Aggregate Projections: A Column-based Alternative to Materialized Views for Analytics"
Designs of two different materialized views, *flattening and aggregation*, that are easy to use and, when combined, provide complete materialized views.