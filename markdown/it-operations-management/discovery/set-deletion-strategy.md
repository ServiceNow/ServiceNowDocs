---
title: Set a deletion strategy
description: Set a deletion strategy when you want to take action on a related configuration item \(CI\) that Discovery can no longer find through pattern discovery. You can delete the main CI only when it is an Application or Cloud Resource pattern type.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [CI deletion strategies for pattern discovery, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set a deletion strategy

Set a deletion strategy when you want to take action on a related configuration item \(CI\) that Discovery can no longer find through pattern discovery. You can delete the main CI only when it is an Application or Cloud Resource pattern type.

## Before you begin

-   CIs: a main CI and related CIs that the discovery process found through pattern discovery
-   Role required: cloud\_admin, service\_mapping\_admin, discovery\_admin, or admin

## About this task

You can set a deletion strategy for all discovered CIs, including configuration file CIs. However, the way you access the deletion strategy for tracked configuration files differs from the procedure in this topic. See [Set the deletion strategy for tracked configuration files](set-config-file-deletion-strategy.md) for instructions.

## Procedure

1.  Open the list of related CI types by entering `sa_ci_to_pattern.list` in the application filter.

2.  Filter the list to find the CI type that is related to a main CI through pattern discovery.

    If you want to set a deletion strategy for a cloud database, search the list for **cmdb\_ci\_cloud\_database** CI type.

    Notice that the **cmdb\_ci\_cloud\_database** CI types have the **Is Main CI** value set to **true**. This indicates that you can set a deletion strategy for both AWS and Azure databases, even if they are the main CI that cloud discovery finds.

    ![Cloud database CIs](../image/deletion-strategy-main-ci-cloud-database.png)

3.  From the list view, double click the value in the field in the **Deletion Strategy** column.

4.  Select a new value:

<table id="table_xl2_jwf_5z"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Keep

</td><td>

Preserves the configuration file CI record and makes no other changes to the record. This option is the default setting.

</td></tr><tr><td>

Delete

</td><td>

Deletes the configuration file CI record from the CMDB, and the relationship to the main CI.

</td></tr><tr><td>

Mark as absent

</td><td>

Marks the **Status** \[install\_status\] field of the configuration file CI record as **Absent**, meaning that Discovery cannot find the tracked configuration file. This status does not instruct the system to delete the actual CI or the relationship.**Note:** There are two tables that do have their CIs deleted if marked as absent: cmdb\_ci\_network\_adapter and cmdb\_ci\_ip\_address.

</td></tr><tr><td>

Delete relations

</td><td>

Deletes only the CI relationships between the related CI and the main CI.

</td></tr><tr><td>

Mark as retired

</td><td>

Marks the **Status** \[install\_status\] field of the configuration file CI record as **Retired**, meaning that Discovery no longer uses this configuration file. This status does not instruct the system to delete the actual CI or the relationship.

</td></tr></tbody>
</table>
**Parent Topic:**[CI deletion strategies for pattern discovery](../concept/deletion-strategy.md)

