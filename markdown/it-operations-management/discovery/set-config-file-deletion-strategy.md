---
title: Set the deletion strategy for tracked configuration files
description: You can specify what you want to do with tracked configuration file CI records when pattern discovery can no longer find them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/set-config-file-deletion-strategy.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 2
breadcrumb: [Configuration file tracking, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set the deletion strategy for tracked configuration files

You can specify what you want to do with tracked configuration file CI records when pattern discovery can no longer find them.

## Before you begin

A pattern that specifies [tracked configuration files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/track-configuration-files.md).

Role required: discovery\_admin, service\_mapping\_admin, or admin. Starting from Visibility Content version 6.30.0, pd\_admin and pd\_mid are also supported.

## About this task

You can set a deletion strategy for all discovered CIs, not just configuration file CIs. However the way you access the deletion strategy for standard CIs differs from configuration file CIs. See [Set a deletion strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/set-deletion-strategy.md) for instructions.

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
**Related topics**  


[CI deletion strategies for pattern discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/deletion-strategy.md)

[Set a deletion strategy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/set-deletion-strategy.md)

