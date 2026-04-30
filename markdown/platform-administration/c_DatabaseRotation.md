---
title: Applying database rotation techniques
description: Manage table size growth, archive data, and boost query performance by configuring database rotation.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage data growth, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Applying database rotation techniques

Manage table size growth, archive data, and boost query performance by configuring database rotation.

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
</table>-   **[Activate database rotation](../task/t_ActivateDatabaseRotation.md)**  
Learn how to activate database rotation.
-   **[Table rotation](../../platform-performance/concept/c_TableRotation.md)**  
Optimize performance and manage data lifecycle by rotating tables, allowing older data to be systematically archived while maintaining system efficiency.
-   **[Table extension](../../managing-data/concept/table-extension.md)**  
Partition and preserve data sets for extended periods without overwriting.

**Parent Topic:**[Managing the growth of data on your instance](../../managing-data/concept/data-management-policies.md)

