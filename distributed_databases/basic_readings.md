# Reading Materials for Building Distributed (Cloud) Databases

_Initial version: 2021/1/19_

_Latest updated: 2021/3/6_

More useful readings will be added time to time

--------------------------------------

These are classes, papers, journals or books written by DB researchers and builders that provide basic Database knowledge and references for you to understand how a database works and is built. If you have never read any of these, start from the top.


## Basic Distributed System Readings
* [System Design](https://www.amazon.com/System-Design-Interview-Insiders-Guide-ebook/dp/B08B3FWYBX) - 2020 - "System Design Interview - An Insider's Guide" by Alex Xu
A book that covers high-level designs of distributed systems, and, although it does not focus on DB, it introduces challenges all DB builders want to solve and relevant technologies used to do solve them. I highly recommend you to read at least the first half of this book in the order the chapters are laid out before reading the following materials.

## Classes

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
    * Data Type Presentation & Storage Models [class 8](https://www.youtube.com/watch?v=y6qFHu0YKMM&t=3692s), [slides](https://15721.courses.cs.cmu.edu/spring2020/slides/08-storage.pdf)
        * Type Presentation & Layout: Numbers (fixed & variable precision numbers), Varchar & Blob (fixed & variable length), time, null
        * Storage models: N-ary Storage Model (NSM) for row-store, Decomposition Storage Model (DSM) for column-store, and Hybrid Storage Model 
        * Hybrid workloads: [Casper](https://dl.acm.org/doi/pdf/10.14778/3358701.3358707?casa_token=zJVMHwuD6LQAAAAA:RdB_xUnAfrcFnnK4PTN1PFm0M3ZOJXQ0jUa3vhzy0t7DAWcF_Tntk9J_LGOKmfpRE47qBDDBohmqkA), [Peloton](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/arulraj-sigmod2016.pdf), [H2O](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/h2o.pdf), [HYRISE](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/p105-grund.pdf), [Column-Stores vs Row-stores](https://15721.courses.cs.cmu.edu/spring2020/papers/08-storage/p967-abadi.pdf)

    More to come: details of other classes

## References

* [Designing Data-Intensive Applications](https://www.amazon.com/Designing-Data-Intensive-Applications-Reliable-Maintainable/dp/1449373321) - 2017 by Martin Kleppmann
A thick book that describes a various sets of technologies used to design not only DBs but data-intensive applications. It is recommended to only read a little bit of this book everyday while reading the other materials, or use it as a reference to fill your missing knowledge. Without specific use cases for your designs, you will get lost easily in this book.
