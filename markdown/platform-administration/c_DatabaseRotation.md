---
title: Database rotation
description: Database rotation involves managing table size growth and archiving old data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Database rotation

Database rotation involves managing table size growth and archiving old data.

Instance data grows quickly, and as these tables grow in size they require management. Database rotation preserves instance performance and averts risk associated with querying growing data sets utilizing three techniques. These techniques are based on the concept of managing large quantities of data by separating whole sets into individual tables. After this task is performed, each technique handles data in a different manner:

-   Table Rotation works by rotating among a small set of tables, and deleting and reusing the old tables for new data.
-   Table Extension works by periodically starting a new table and allowing old tables to be easily archived and removed from the system.
-   Table Sharding works by enabling records to be grouped in a single table by document ID.

<table id="table_n4k_qbq_z4"><thead><tr><th>

Functionality

</th><th>

Tables applied to

</th></tr></thead><tbody><tr><td>

Table Rotation

</td><td>

`syslog` `sys_querystat`

 `ecc_queue`

 `ecc_event`

 `cmdb_metric`

 `sysevent`

</td></tr><tr><td>

Table Extension

</td><td>

`sys_email`

</td></tr></tbody>
</table>## Table rotation and extension

The Table Rotations module allows you to define a new table rotation, a new table extension, a new table shard, or modify an existing one. You can access a list of table rotations on your instance by navigating to **All** &gt; **System Definition** &gt; **Table Rotations** &gt; **.**

![Table rotation groups](../image/DatabaseRotation.png "Table rotation groups")

-   **Name**: auto-generated from table name
-   **Duration**: overall time parameter for function
-   **Initialized**: sets function as active \(true\) or inactive \(false\)
-   **Rotations**: number of tables to be created within Duration
-   **Type**: indicates Extension \(archiving\), Rotation \(deletion\), or Shard \(doc ID\) functionality

When you define a new rotation, a schedule is created and new data is subsequently written to one of the tables in the rotation group. You will notice the that the group includes the original table plus a number of additional tables. Be aware that deleting a rotation will delete the additional tables and all the data, therefore the rotation should not be deleted if the data is needed.

-   **[Activate database rotation](../task/t_ActivateDatabaseRotation.md)**  
Learn how to activate database rotation.
-   **[Table rotation](../../platform-performance/concept/c_TableRotation.md)**  
Optimize performance and manage data lifecycle by rotating tables, allowing older data to be systematically archived while maintaining system efficiency.
-   **[Table extension](../../managing-data/concept/table-extension.md)**  
Partition and preserve data sets for extended periods without overwriting.

**Parent Topic:**[Data Management](../../managing-data/concept/c_DataManagement.md)

