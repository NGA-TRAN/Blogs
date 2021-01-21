# Reading Materials for Building Distributed (Cloud) Databases

_Latest updated: **2021/1/19 - Initial version**_ 

More useful readings will be added time to time and the latest addition will be in bold. 

--------------------------------------

These are papers, journals or books written by DB researchers and builders that I find worth learning if you want to join the DB-builder community or even build your own DB. Some papers cover high-level architecture of a DB, some describe a major DB component in depth, some illustrate certain techniques to build or improve a specific sub-component. If you have never read any of these, start from the top and high-level ones. Each paper will include a short/nick name, year of publishing, full title and a brief summary.
<br>
<br>

### [CStore](https://web.archive.org/web/20100619191833/http://db.lcs.mit.edu/projects/cstore/vldb.pdf) - 2005 - "C-Store: A Column-oriented DBMS"
A research paper that covers a full architecture of a *Distributed Share-nothing Columnar MPP*.

### [Vertica](https://vldb.org/pvldb/vol5/p1790_andrewlamb_vldb2012.pdf) - 2012 - "The Vertica Analytic Database: C-Store 7 Years Later"
A full architecture of a high performance *On-premise Distributed Data Warehouse* implementing CStore research ideas.

### [Vertica Eon](https://www.vertica.com/wp-content/uploads/2018/05/Vertica_EON_SIGMOD_Paper.pdf) - 2018 - "Eon Mode: Bringing the Vertica Columnar Database to the Cloud"
An architecture of a *Distributed Cloud Data Warehouse* that enables the separation of compute and storage, and focuses on query performance and throughput.

### [Snowflake](http://pages.cs.wisc.edu/~remzi/Classes/739/Fall2018/Papers/p215-dageville-snowflake.pdf) - 2016 - "The Snowflake Elastic Data Warehouse"
An architecture of a *SaaS Distributed Cloud Data Warehouse* that enables the separation of compute and storage, and focuses on easy to use and maintenance.

### [Vertica Optimizer](https://www.researchgate.net/profile/Nga_Tran6/publication/269306314_The_Vertica_Query_Optimizer_The_case_for_specialized_query_optimizers/links/55aeb17208aed9b7dcdda55f.pdf) -2014 - "The Vertica Query Optimizer: The Case for Specialized Query Optimizers"
An in-depth architecture of Vertica *Query Optimizer* used for both On-Premise and Cloud (Eon) modes.

### [Vertica BDB]() - 2014 - "DBDesigner: A customizable physical design tool for Vertica Analytic Database"
An in-depth architecture of Vertica *Table's Physical Storage Design* applied to both On-Premise and Cloud (Eon) modes.

### [SIPS](https://15721.courses.cs.cmu.edu/spring2019/papers/15-execution/shrinivas-icde2013.pdf) - 2013 - "Materialization Strategies in the Vertica Analytic Database: Lessons Learned"
In-depth strategies of *data materialization for joins* of columnar DB.

### [Vertica Materialized View](https://github.com/NGA-TRAN/Notes/blob/main/Papers/FlattenedTable_LiveAggregateProjecttions.pdf) - ICDE 2019 - 2019 - "Vertica Flattened Tables and Live Aggregate Projections: A Column-based Alternative to Materialized Views for Analytics"
Detailed designs of two different materialized views, *flattening and aggregation*, focusing on easy-to-use but when combined providing complete materialized views.