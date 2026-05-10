---
title: Create an export target
description: Define where to export data to by creating an export target.
locale: en-US
release: australia
product: System Export Sets
classification: system-export-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export sets, Exports, Workflow Data Fabric]
---

# Create an export target

Define where to export data to by creating an export target.

## Before you begin

Role required: export\_set\_admin

## About this task

You must use a MID Server as the export destination. For more information on MID Server configuration, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

## Procedure

1.  Navigate to **All** &gt; **System Export Sets** &gt; **Export Targets** and create a new record \(see table for field descriptions\).

<table id="table_jn4_rvx_xs"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for the export target.

</td></tr><tr><td>

MID Server

</td><td>

Select the MID Server to export to. The MID Server must have a **Validated** value of **Yes** and a **Status** value of **Up**.**Note:** You must use a MID Server from the Geneva release or later. Earlier MID Server releases do not support export sets. Export sets are not supported on MID Servers in a cluster.

</td></tr><tr><td>

File Path

</td><td>

Specify a path relative to the MID Server directory to save the exported data to. The user account used to run the MID Server must have permission to write to this location.

</td></tr></tbody>
</table>
**Related topics**  


[https://msdn.microsoft.com/en-us/library/bb727008.aspx](https://msdn.microsoft.com/en-us/library/bb727008.aspx)

