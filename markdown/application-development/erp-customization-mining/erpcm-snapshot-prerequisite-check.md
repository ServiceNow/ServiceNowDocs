---
title: ERP Semantic Mining snapshot prerequisite check
description: Before snapshot import and export in ERP-CM, a check is performed automatically to confirm that other related processes aren’t in progress.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ERP Semantic Mining reference, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# ERP Semantic Mining snapshot prerequisite check

Before snapshot import and export in ERP-CM, a check is performed automatically to confirm that other related processes aren’t in progress.

For process details, see [Create a snapshot to share and save data in ERP Semantic Mining](../task/create-a-snapshot-to-share-and-save-data.md).

<table id="table_bgl_xmh_2dc"><thead><tr><th>

Prerequisite check

</th><th>

Description

</th></tr></thead><tbody><tr><td>

System not connected

</td><td>

If you chose to import another snapshot, or attach a system, the 'table flush trigger' flow will immediately start to delete data. Once data is deleted, the selected snapshot will be imported, or the system will be attached.

</td></tr><tr><td>

System Connected and attach new system

</td><td>

The 'table flush trigger' flow will cancel Tasks that are currently executing. After tasks have been stopped' 'table flush trigger' flow will delete data, and attach the new system.

</td></tr><tr><td>

System Connected and import snapshot

</td><td>

The 'table flush trigger' flow will start by scheduling the creation of a snapshot. It will wait for the snapshot to be created.

 Snapshot is created when all tasks for all Collector entries are completed. Different flows execute subflow 'Check set Snapshot to in progress'. This subflow checks whether a record in the snapshot table should be completed with data.

 The 'table flush trigger' flow resumes and deletes all data. Subsequently, snapshot is imported.

</td></tr><tr><td>

System Connected and export snapshot triggered

</td><td>

Snapshot is created when all tasks for all Collector entries are completed. Different flows execute subflow 'Check set Snapshot to in progress'. This subflow checks whether a record in the snapshot table should be completed with data.

 If user wants to delete all data, or attach a new system, 'table flush trigger' flow will wait for the snapshot to be created.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Semantic Mining reference](erp-customization-mining-ref.md)

