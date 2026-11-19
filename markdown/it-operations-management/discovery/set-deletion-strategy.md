---
title: Set a deletion strategy
description: Set a deletion strategy when you want to take action on a configuration item \(CI\) that Discovery can no longer find through pattern discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/set-deletion-strategy.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-11-16"
reading_time_minutes: 2
breadcrumb: [CI deletion strategies for pattern discovery, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set a deletion strategy

Set a deletion strategy when you want to take action on a configuration item \(CI\) that Discovery can no longer find through pattern discovery.

## Before you begin

-   A pattern that discovers the CIs you want to set a deletion strategy for
-   Role required: cloud\_admin, service\_mapping\_admin, discovery\_admin, or admin. Starting from Visibility Content version 6.30.0, pd\_admin and pd\_mid are also supported.

## About this task

You can set a deletion strategy for all discovered CIs, including configuration file CIs. However, the way you access the deletion strategy for tracked configuration files differs from the procedure in this topic. See [Set the deletion strategy for tracked configuration files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/set-config-file-deletion-strategy.md) for instructions.

**Note:** You can set a deletion strategy for the main CI only when the pattern type is Application or Cloud Resource. You can't set one for the main CI in an Infrastructure pattern.

## Procedure

1.  Open the list of related CI types by entering `sa_ci_to_pattern.list` in the application filter.

2.  Filter the list to find the CI type that you want to set a deletion strategy for.

    For example, to set a deletion strategy for a cloud database, search the list for the **cmdb\_ci\_cloud\_database** CI type. You can set a deletion strategy for both AWS and Azure databases.

    \[Omitted image "deletion-strategy-main-ci-cloud-database.png"\] Alt text: Cloud database CIs

3.  From the list view, double click the value in the field in the **Deletion Strategy** column.

4.  Select a new value:

<table id="table_xl2_jwf_5z"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Keep

</td><td>

Preserves the CI record and makes no other changes to it. This option is the default setting.

</td></tr><tr><td>

Delete

</td><td>

Deletes the CI record from the CMDB, together with its relationships.

</td></tr><tr><td>

Mark as absent

</td><td>

Marks the **Status** \[install\_status\] field of the CI record as **Absent**, meaning that Discovery can't find the CI. This status doesn't instruct the system to delete the CI or or its relationships.**Note:** There are two exceptions. Discovery deletes CIs in the cmdb\_ci\_network\_adapter and cmdb\_ci\_ip\_address tables when it marks them as absent.

</td></tr><tr><td>

Delete relations

</td><td>

Deletes only the CI relationships between the related CI and the main CI.

</td></tr><tr><td>

Mark as retired

</td><td>

Marks the **Status** \[install\_status\] field of the CI record as **Retired**, meaning that Discovery no longer uses this CI. This status doesn't instruct the system to delete the CI or its relationship.

</td></tr></tbody>
</table>
**Parent Topic:**[CI deletion strategies for pattern discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/deletion-strategy.md)

