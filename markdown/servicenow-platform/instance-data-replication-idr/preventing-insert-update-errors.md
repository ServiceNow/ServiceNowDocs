---
title: Avoiding insert and update errors in Instance Data Replication
description: You can avoid insert and update failures in Instance Data Replication \(IDR\) by specifying a class name filter in the producer replication set.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Avoiding insert and update errors in Instance Data Replication

You can avoid insert and update failures in Instance Data Replication \(IDR\) by specifying a class name filter in the producer replication set.

**Important:** This topic only applies to producer replication sets created prior to the Utah release.

When you replicate a parent table and one or more child tables, you must add a sys\_class\_name filter to the parent table in the outbound entry of your producer replication set. If the sys\_class\_name filter is missing, insert and update failures appear in **Instance Data Replication** &gt; **Replication Payload Error** in the following scenarios:

-   A failed insert occurs when a record in the child table is replicated because the system attempts two inserts with the same sys\_id to the parent table. Adding the sys\_class\_name filter to the parent prevents the unique key violation during the INSERT into the parent table.
-   A new record is added to a replicated child table on the producer instance. Instance Data Replication \(IDR\) initially creates the record in the parent table on the consumer, but not the child table. If the child record is changed on the producer instance, during replication a failed update occurs on the child table in the consumer instance because the record only exists in the parent table.

If the table is a parent, decide if you want to replicate any of its child tables.

-   If you want to replicate one or more child tables, you must identify the sys\_class\_name value for the parent table, and then add a corresponding sys\_class\_name filter to the parent table.

    For example, **Task Type** is the label for sys\_class\_name on the Task \[task\] table. To start replicating the incidents in addition to tasks, you must add **\[Task Type\] \[is\] \[Task\]** to the outbound entry for the Task \[task\] table.

-   If you only want to replicate the parent table, the filter is optional.
-   If the parent table is already being replicated, you must edit the parent and add the sys\_class\_name filter.

If the table is a child, decide if you want to replicate its parent.

-   If you want to replicate the parent table as well, you must identify the sys\_class\_name value for the parent table, and then add a corresponding sys\_class\_name filter to the parent table.

    For example, **Task Type** is the label for sys\_class\_name on the Task \[task\] table. To start replicating tasks in addition to incidents, you must add **\[Task Type\] \[is\] \[Task\]** to the outbound entry for the Task \[task\] table.

-   If you only want to replicate the child table, the filter is optional.
-   If one or more child tables are already being replicated, you must add the sys\_class\_name filter to the parent.

**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication](../task/approve-consumer.md)

[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md)

[Cloning options with Instance Data Replication](cloning-with-instance-data-replicaton.md)

[Monitoring replication status in Instance Data Replication](instance-data-replication-dashboard.md)

[Monitoring queues in Instance Data Replication](idr-queue-dashboard.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

