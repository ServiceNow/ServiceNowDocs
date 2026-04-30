---
title: Table flattening
description: Table flattening stores a hierarchy of related tables as one table in a relational database.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing tables and indexes, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table flattening

Table flattening stores a hierarchy of related tables as one table in a relational database.

## Extension models

The system offers these extension models to store a table hierarchy on a relational database.

|Extension model|Flattens tables?|
|---------------|----------------|
|Table per class|No|
|Table per hierarchy|Yes|
|Table per partition|Yes|

## Table per class

The Table per class extension model stores each table of the hierarchy in its own physical table on the relational database. Each physical table uses the table prefix of the source table each stores a different class of records. An example of the Table per class extension model is the Asset \[alm\_asset\] table, and its child tables: Hardware \[alm\_hardware\], Consumable \[alm\_consumable\], Facility \[alm\_facility\], and Software License \[alm\_license\]. The parent table of the hierarchy, Asset, stores a copy of every record in its descendant tables.

To find records in the Table per class extension model, the system queries records from multiple tables and joins the results. For example, when searching for hardware in a related facility, the system must join results from the Hardware, Facility, and Asset tables.

Table joins cause a performance bottleneck on relational databases. The more classes a query includes, the worse the query performance. Therefore any query for records from the top of the table hierarchy has the worst performance because it requires joining all descendant tables.

The system uses the Table per class extension model by default when creating tables. Most system tables also use the Table per class extension model as there is no performance benefit from flattening them.

## Table per hierarchy

The Table per hierarchy extension model stores an entire table hierarchy in a single flat physical table on the relational database. The physical table is named after the parent table of the hierarchy, such as Task. The physical table contains all records of the table hierarchy and assigns a class name column value to each descendant table of the hierarchy. The system uses the name of the source table as the class name value. For example, Task records can have class names such as Change, Incident, or Problem.

To find records in a table hierarchy, the system queries the physical table and uses the class name column to constrain the results. Since such queries do not require joining results from multiple tables, the system provides better search performance.

The system uses the Table per hierarchy extension model for the Task table hierarchy on MySQL databases. Other tables use the Table per class extension model because there is no performance benefit to flattening them. To use Table per hierarchy on an Oracle database, contact Technical Support.

## Table per partition

The Table per partition extension model stores an entire table hierarchy in a single flat logical table on the relational database. Each logical table can have multiple physical storage tables called partitions supporting it. Each partition optimizes the database resources available to a physical table such as the column count, index count, and row size. The system adds a partition whenever the logical table needs additional relational database resources.

Each logical table is named after the parent table of the hierarchy, and each supporting physical partition consists of the logical name plus a partition name. For example, the Base Configuration Item \[cmdb\] table starts as a logical table with no partitions. Suppose your hardware configuration items consume enough database resources that the system creates a partition called **cmdb$par1** to store them. Later, computer configuration items could consume enough database resources to warrant the system creating a second partition called **cmdb$par2** to store these records.

Within each logical table, the system assigns a class name column value to each descendant table of the hierarchy. For example, within the Base Configuration Item logical table there are records with class names for Application, Computer, and IP Router. The system also assigns a two-digit class path value to each descendant table of the hierarchy. The class path is based on the table location in the hierarchy. For example, the parent class Hardware might have a class path such as **/!!/!D** and the child class Computer might have a class path such as **/!!/!D/!!**.

To find records in the Table per partition extension model, the system queries the logical table and its partitions and uses the class path column to constrain the results. Since these queries do not require joining results from multiple tables, the system provides better search performance. In addition, the class path reduces the total number of records to search, which further improves search performance.

The system uses the Table per partition extension model for the Base Configuration Item \[cmdb\] table hierarchy on MySQL databases. To use Table per partition on an Oracle database, contact Technical Support.

-   **[View a table hierarchy and the extension model](../task/t_TableHierarchyAndTheExtModel.md)**  
Determine the extension model used by a table.

**Parent Topic:**[Managing tables and indexes](../../table-administration/concept/using-table-administration.md)

