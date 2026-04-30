---
title: Configure related record contexts
description: This type of configuration record defines the context in which related records appear in the Related Records tab.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure dynamic related records, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure related record contexts

This type of configuration record defines the context in which related records appear in the Related Records tab.

## Before you begin

Role required: admin

## About this task

In a related record context, the system administrator configures the following information:

-   The table that stores the record type for the context. You can create a context for a source record, such as a case, or for a playbook activity.
-   Conditions to apply to the selected table. These conditions determine if the related record definitions associated with this context are executed at runtime.
    -   If the conditions evaluate to true, the system executes the related record definitions.
    -   If the conditions evaluate to false, the system ignores these definitions.

        **Note:** If a context has no conditions, this evaluates to true.

-   The related record definitions to execute. Associate a definition for each type of related record to display for this context.

## Procedure

1.  Navigate to **All** &gt; **Dynamic Related Record** &gt; **Related Record Contexts**.

2.  Click **New**.

3.  Enter a **Name** for the context record.

4.  Select the table that stores the record type for the context in the **Applies to table** field.

5.  In the **Primary reference field**, select the field from the **Applies to table** that is passed to the Context Related Record Definition for evaluation.

    The following data types are supported:

    -   Sys ID
    -   Doc ID
    -   Reference
6.  If desired, select another reference field from the **Applies to table** in the **Secondary reference field**.

7.  Enable the **Inherited** field if you want the context record to also consider tables that extend from the **Applies to table**.

8.  Use the condition builder to select conditions that are applied to the records in the **Applies to table**.

    For example, if you are creating a context for a playbook activity, you can use the condition builder to identify the playbook and then the specific activity within that playbook.

9.  Click **Submit**.

    The context is added to the Related Record Contexts list.


