---
title: Create data filtration rules
description: Learn how to create data filtration rules to grant your users' access to records are tables.
locale: en-US
release: australia
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data filtration\(Legacy\), Access Management]
---

# Create data filtration rules

Learn how to create data filtration rules to grant your users' access to records are tables.

## Before you begin

Role required: security\_admin

**Note:** To create or modify data filtration rules you, must elevate to the privileged role. For details on this process, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md).

## Procedure

1.  Navigate to **All** &gt; **Data Filtration** &gt; **Data Filtration Records**.

2.  Click **New** in the **Data Filtration** list.

    A new data filtration form displays.

3.  In the form, fill in the fields as needed.

<table id="table_l4z_lc1_w4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table to which this data filtration rule applies.**Note:** Non-maint users cannot create data filtration on some tables, to work-around this remove the tableChoicesScript=DataFiltrationTableList attribute, but make sure that no filters will be created on any of the sys\_df\_xxx tables or any tables in the sys\_df\_table\_exclusion.

</td></tr><tr><td>

Active

</td><td>

Sets the data filtration rule as active.**Note:** Keep data filtration rules inactive until you are ready to test to avoid unintentionally locking users out of records.

</td></tr><tr><td>

Description

</td><td>

Description of the data filtration rule.

</td></tr><tr><td>

Cascading

</td><td>

Select to set the data filtration rule to apply to extended tables.

 For example, you select the Task\[task\] table, and enable cascading. In this case, the data filtration rule also applies to all tables extended from task, such as Incident\[incident\] and Change Request\[change\_request\]. For detail on table extension, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

 **Note:** This field is enabled by default.

</td></tr></tbody>
</table>4.  To narrow the scope of the rule fill in the **Conditions** fields as needed.

<table id="table_uhd_sh3_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subject Condition

</td><td>

All conditions must be met for access.

</td></tr><tr><td>

Security Attribute Condition

</td><td>

All conditions must be met for access. -   **Local**

The attribute is defined only in the scope of the data filtration rule.

-   **Existing**

The attribute is defined by reference to an already existing **Security Attribute**

</td></tr><tr><td>

Data condition

</td><td>

Defines the conditions for data to be subject to the rule.**Note:** An empty Data Condition will apply to all records in the selected table.

</td></tr></tbody>
</table>5.  Select **Save** from the form menu.

    After you have saved your data filtration rule, this rule automatically applies to all records on the selected table, unless specified otherwise by the data condition.


