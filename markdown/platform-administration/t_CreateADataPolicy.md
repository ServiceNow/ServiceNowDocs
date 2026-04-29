---
title: Create a data policy
description: You can create a new data policy to define data rules for a table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data policy, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a data policy

You can create a new data policy to define data rules for a table.

## About this task

Create data policies to enforce consistency. You can create data policies only for tables and database views that are in the same scope as the data policy and for other tables that have at least one field in the same scope as the data policy. For tables that are in a different scope from the data policy record, you can create data policy rules only for fields in the same scope as the data policy and you cannot make a field mandatory.

## Procedure

1.  Navigate to **Data Policies** by completing one of the following actions.

    -   Navigate to **System Policy** &gt; **Rules** &gt; **Data Policies**.
    -   From any form header, right-click the header bar and select **Configure** &gt; **Data Policies**.
    -   In List v2, open any column context menu and select **Configure** &gt; **Data Policies**.
    -   In List v3, open the list title menu and select **Configure** &gt; **Data Policies**.
2.  Click **New**.

3.  Select any options for the data policy.

4.  Create the condition that must exist for the platform to apply this policy.

    For example, your conditions might include **\[Problem state\] \[is\] \[Closed/Resolved\]**

5.  Right-click the header and select **Save**.

    The **Data Policy Rules** related list appears.

6.  Click **New** in the related list and create the record that identifies the field and the policy to apply.

    ![Data policy action](../image/DataPolicyAction2.png)

    It is possible to have multiple rules on a single field, but it is not recommended.

7.  Click **Submit**.

    ![Data policy data](../image/DataPolicyData2.png)

8.  Add more rules by repeating steps 6 and 7.


