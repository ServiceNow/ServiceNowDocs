---
title: Configure a severity map in the Security Exposure Management Workspace
description: Security Exposure Management Workspace severity mapping transforms third-party source severity fields to recognizable fields in Unified Security Exposure Management.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Implement, Unified Security Exposure Management, Security Operations]
---

# Configure a severity map in the Security Exposure Management Workspace

Security Exposure Management Workspace severity mapping transforms third-party source severity fields to recognizable fields in Unified Security Exposure Management.

## Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](../concept/sem-acls-for-admin-rules.md)

## About this task

Security Exposure Management Workspace ships with National Vulnerability Database \(NVD\) to normalized ServiceNow severity mapping. ServiceNow third-party integrations such as the Qualys Vulnerability Integration provide severity mappings on installation. These maps can be adjusted by changing the fields in existing maps.

Creating or editing a severity map is intended only for customized or non-standard third-party mappings in your environment.

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Under **Others**, select **Review** on the **Normalized Severity Mapping** tile.

4.  Select **New**.

5.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

The name of the source for the severity mapping.

</td></tr><tr><td>

Target value

</td><td>

The target severity value. Choices are: -   1- Critical
-   2 - High
-   3 - Medium
-   4 - Low
-   5 - None


</td></tr><tr><td>

Source value

</td><td>

The source severity value.

</td></tr></tbody>
</table>6.  Repeat Step 5 for each source severity level.

7.  Select **Save**.

8.  To edit the severity mapping for an integration, select the integration and update the values in the **Source Value** and **Target Value** fields.


