---
title: ERP Semantic Mining snapshot prerequisite check
description: Before snapshot import and export in ERP Semantic Mining, a check is performed automatically to confirm that other related processes aren’t in progress.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, ERP Semantic Mining overview, Workflow Data Fabric]
---

# ERP Semantic Mining snapshot prerequisite check

Before snapshot import and export in ERP Semantic Mining, a check is performed automatically to confirm that other related processes aren’t in progress.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For process details, see [Create a snapshot to share and save data in ERP Semantic Mining](../task/create-a-snapshot-to-share-and-save-data.md).

<table id="table_bgl_xmh_2dc"><thead><tr><th>

Prerequisite check

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System not connected

</td><td>

If you chose to import another snapshot, or attach a system, the 'table flush trigger' flow immediately starts to delete data. Once data is deleted, the selected snapshot is imported, or the system is attached.

</td></tr><tr><td>

System Connected and attach new system

</td><td>

The 'table flush trigger' flow cancels Tasks that are currently executing. After tasks have been stopped, the 'table flush trigger' flow deletes data, and attaches the new system.

</td></tr><tr><td>

System Connected and import snapshot

</td><td>

The 'table flush trigger' flow starts by scheduling the creation of a snapshot. It waits for the snapshot to be created.

 Snapshot is created when all tasks for all Collector entries are completed. Different flows execute subflow 'Check set Snapshot to in progress'. This subflow checks whether a record in the snapshot table should be completed with data.

 The 'table flush trigger' flow resumes and deletes all data. Subsequently, snapshot is imported.

</td></tr><tr><td>

System Connected and export snapshot triggered

</td><td>

Snapshot is created when all tasks for all Collector entries are completed. Different flows execute subflow 'Check set Snapshot to in progress'. This subflow checks whether a record in the snapshot table should be completed with data.

 If you want\\ to delete all data, or attach a new system, 'table flush trigger' flow waits for the snapshot to be created.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Semantic Mining reference](erp-customization-mining-ref.md)

