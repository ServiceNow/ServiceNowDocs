---
title: Set the deletion strategy for tracked configuration files
description: You can specify what you want to do with tracked configuration file CI records when pattern discovery can no longer find them.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Configuration file tracking, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set the deletion strategy for tracked configuration files

You can specify what you want to do with tracked configuration file CI records when pattern discovery can no longer find them.

## Before you begin

A pattern that specifies [tracked configuration files](track-configuration-files.md).

Role required: discovery\_admin, service\_mapping\_admin, or admin

## About this task

You can set a deletion strategy for all discovered CIs, not just configuration file CIs. However the way you access the deletion strategy for standard CIs differs from configuration file CIs. See [Set a deletion strategy](set-deletion-strategy.md) for instructions.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns** and open the desired pattern.

2.  Click the **Tracked Files** tab.

3.  Under **Related Links**, click **Edit deletion strategy for the configuration files of this pattern**.

    The Related CI Types list appears showing you filtered records in the Related CI Type \[sa\_ci\_to\_pattern\] table. The filter shows you only records with the CI type of Tracked Configuration files \[cmdb\_ci\_config\_file\_tracked\], which is the table where the system saves configuration file CIs.

4.  From the list view, double-click the value in the field in the **Deletion Strategy** column for the tracked configuration file.

5.  Select a new value:

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
**Related topics**  


[CI deletion strategies for pattern discovery](../concept/deletion-strategy.md)

[Set a deletion strategy](set-deletion-strategy.md)

