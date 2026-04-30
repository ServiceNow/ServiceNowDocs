---
title: Preserving table hierarchy in Instance Data Replication
description: Decide if you want to replicate a parent-child table hierarchy and what strategy to use for replicating the data in Instance Data Replication \(IDR\).
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Preserving table hierarchy in Instance Data Replication

Decide if you want to replicate a parent-child table hierarchy and what strategy to use for replicating the data in Instance Data Replication \(IDR\).

Before you create a replication set, determine if the table that you want to replicate is part of a parent-child table hierarchy. If it is, decide if you want to preserve the hierarchy and whether to replicate the data from the parent perspective \(retaining only columns belonging to the parent table\) or from the child perspective \(retaining all columns that belong to the child tables\). Review the following available strategies.

-   **Strategy 1: Preserve the entire hierarchy and replicate child columns**

    You can preserve the entire hierarchy, including all of the child table columns, by creating an outbound entry for each child table, and specifying a sys\_class\_name filter for each child table.

    For example, to replicate the Task table and ensure that all of the columns from all of the child tables are included, specify the following:

    |Table|Filter|
    |-----|------|
    |Task|sys\_class\_name=task|
    |Incident|sys\_class\_name=incident|
    |Problem|sys\_class\_name=problem|
    |Change Request|sys\_class\_name=change|

    And so forth, for all of the child tables, including filters with each table for the sys\_class\_name.

    With this strategy, records are inserted into each child table on the consumer, including data from the columns that belong to each child table on the producer.

-   **Strategy 2: Preserve the hierarchy, but don't replicate child columns**

    To preserve the hierarchy but only replicate columns from the parent table, replicate the parent table and include the Class Name \[sys\_class\_name\] field in the **Included Fields** list. Including the Class Name field maintains the distinction between parent and child records on the consumer instance.

    For example, if you want to replicate the Task table and its children \(Incident, Problem, Change Request\), but only replicate the columns that belong to the Task table, specify the following:

    |Table|Included Fields|
    |-----|---------------|
    |Task|Class Name|

    In this strategy, the sys\_class\_name column on the consumer Task table receives entries for the parent table \(task\) and child tables \(incident, problem, and change\), and records are inserted into the respective child tables on the consumer. However, without the sys\_class\_name filter, the columns that are unique to each child table are not replicated.

-   **Strategy 3: Ignore the hierarchy, and only replicate parent table data**

    To ignore the hierarchy and only replicate parent records, replicate the parent table and exclude the Class Name \[sys\_class\_name\] field from the **Included Fields** list. Excluding the Class Name field removes the distinction between parent and child records on the consumer instance. All replicated records on the consumer will be parent table records.

    For example, if you want to replicate records from the Task table and simply consider all records as tasks for reporting or auditing purposes, specify the following:

    |Table|Included Fields|
    |-----|---------------|
    |Task|Any fields except for Class Name|

    In this strategy, when you replicate the Task table, all replicated records have a value of task in the sys\_class\_name column, and no columns belonging to the child tables are replicated.


**Parent Topic:**[Configuring Instance Data Replication](configuring-instance-data-replication.md)

