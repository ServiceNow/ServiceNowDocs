---
title: Configure related record definitions
description: Related record definitions identify the types of records that the dynamic related records feature can display in the Related Records tab.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure dynamic related records, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure related record definitions

Related record definitions identify the types of records that the dynamic related records feature can display in the Related Records tab.

## Before you begin

Role required: admin

## About this task

The system administrator can create relate definitions and associate the desired definitions with a related record context. For example, the admin can associate SLA and escalation definitions with the Case related record context. Definitions can be associated with multiple contexts.

The Dynamic Related Records for Configurable Workspace plugin includes several related record definitions for case records. For more information, see [Related record definitions included with the plugin](../concept/dynamic-related-records-configure.md#section_khj_gwl_jpb).

## Procedure

1.  Navigate to **All** &gt; **Dynamic Related Record** &gt; **Related Record Definitions**.

2.  Click **New**.

3.  Enter a name for the definition in the **Display label** field.

    This label appears in the filter dropdown list in the Related Records tab. Agents click the filter icon and select the type of related record to view in the Related Records list.

4.  In the **Queries from** field, select the table that stores the related record data to be retrieved.

5.  Select a table in the **Primary reference table** field.

    The primary table used in the definition script. At runtime, the script expects to get passed a record of this type. If you entered a data type in the **Primary reference field** in the related record context, enter the table for that data type.

6.  If desired, select a table in the **Secondary reference table** field.

    The secondary table used in the definition script. At runtime, the script expects to get passed a record of this type. If you entered a data type in the **Secondary reference field** in the related record context, enter the table for that data type.

7.  Use the **Script** field to define which records are retrieved based on the context.

    At runtime, the script evaluates the current record's context, along with any selected conditions, and dynamically displays the related records.

8.  Click **Submit**.


