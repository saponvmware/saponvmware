---
title: 10 Myths about SAP HANA
excerpt: Prejudices about SAP HANA demystified
header:
  teaser: ""
category:
tags: [SAP, SAP HANA]
---

There are a lot of discussions about virtualizing SAP HANA. There are also prejudices in the field of SAP HANA and this blog wants to give you some clarifications.

* SAP HANA is a purely column-oriented database (Column Store)

No, in most cases SAP HANA stores the tables mainly column-based - in a Business Suite scenario over 95% of the tables - but SAP HANA also provides row-based tables for special use cases. The table type is specified in the ABAP Dictionary (Transaction Code SE11) for all SAP tables. The SAP Note [2222277](https://launchpad.support.sap.com/#/notes/2222277) is showing the advantages and disadvantages of row vs column stores.

* SAP HANA database stores all data in the memory

No, SAP HANA stores only a few columns of many tables in memory dependent on the regularity of access. With the function of table partitioning, it is even possible to keep only selected data in memory and “offload” the rest to persistent storage. There is no force to keep all the data in the memory.

* SAP HANA cloud loses data during a power outage

No, persistence disk storage for data and log will still be required. Without persistence the "durability" condition of the “ACID principle” would not exist. Every change needs to be logged in the “redo log files” to be persistent. Although SAP HANA 2.0 SPS 03 supports Non-volatile memory (NVM).

* SAP HANA combines OLTP and OLAP workload

SAP HANA can handle both application types, but not in one installation. Therefore, it’s still needed to deploy separated installations for OLTP and OLAP applications to run e.g. an ERP and a BW system. Both deployment types have different requirements and limitations especially in cases of Scale-up vs Scale-out.

* SAP HANA does not need ABAP Programmers any longer

With SAP HANA the topic is “moving the logic to the database level” or named as “code push down”. The most business logic continues to be driven out of ABAP, as the business processes are still mapped in ABAP as programming language. Therefore, ABAP programmers are still needed but maybe with additional qualifications.  

![Questions Marks]({{ site.url }}/images/questionmarks.jpg)  
*Disclaimer: Picture by pixabay.com*

* SAP HANA uses SQL queries like any other databases

No, because with SAP HANA there are changes due to the column-based store. An example of this is the output order - keyword “order by primary key”. These changes are incorporated in the SAP standard code, own developed code requires a change of the code. With SAP HANA, pool and cluster tables are deprecated because otherwise the optimization of the database side would not be possible.

* SAP HANA makes each program faster by factor x

No, this depends on the query and there is no reliable factor. Some queries run at the factor 1000, 100 or 10 times faster and some queries even slower than on AnyDB. It depends on the query - for example, never use “select \*” on a column store table - and how much parallelization is possible. There are many reports whose duration has been reduced from hours to a few minutes.

* SAP HANA tables can only store a certain number of entries

This is partly true, because a column store table can only store 2.147.483.648 entries regarding technical reasons. The reason is the attribute vector of a compressed column. Partitioning is a workaround for this limitation because each table partition can enter that number of entries.

* With SAP HANA there are no more update and delete operations

This statement is correct so far. When changing a data record the original data record will not be overwritten, but a new entry will be created in the delta store of the column table. The entry in the main store is shown as invalid and only removed at merges but is no longer visible through SQL statements. Overall, this is called “insert only-mode” and of course the SQL operation delete and update still exists.

* SAP HANA needs an authorization concept

SAP HANA offers the opportunity to use an own authorization concept, it depends on the system of use. If SAP applications are used the authorization check is performed by the application server like the ABAP Stack and therefore an own SAP HANA authentication concept is not relevant. But if users retrieve data directly from SAP HANA database the access must be regulated. If SAP HANA is only used as the database for SAP applications and the native function is not in use the authorization function effort is very limited.

*Disclaimer: Initial idea - in German - by addon.de*

*Tags: SAP, SAP HANA*
