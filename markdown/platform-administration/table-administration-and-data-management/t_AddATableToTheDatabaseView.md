---
title: Add a table to the database view
description: Specify the table to join to the database view.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Joining tables, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a table to the database view

Specify the table to join to the database view.

## Before you begin

Role required: admin.

## About this task

The **Table** field in the View Table form specifies the table to join to the database view. The **Variable prefix** is used by the **Where clause** to define the conditions for the join. These conditions can refer to any field, but typically define the join by matching a field in the table to a field in another table in the database view.

**Note:** The Variable prefix field is mandatory.

When you write the **Where clause**, add the field name to the **Variable prefix** of its table with an underscore. In the following example, **mi\_id** refers to the **id** field in the Metric Instance \[metric\_instance\] table \(mi\) and **inc\_sys\_id** refers to the **sys\_id** field in the Incident \[incident\] table \(inc\).

![Database View Table form](../image/Dbviews4.png "Database View Table form")

**Note:**

-   Database views cannot be created on tables that participate in [table rotation](../../../administer/platform-performance/concept/c_TableRotation.md).
-   Use only lowercase characters in the **Variable prefix**. Using uppercase characters may prevent you from viewing the database view in a list.

To see an example of using left joins to create a view, see [Example left join in creating a database view](example-left-join-db-view.md).

The **Where clause** supports these JavaScript conditional operators:

-   =
-   !=
-   &lt;
-   &lt;=
-   &gt;
-   &gt;=
-   &amp;&amp;
-   \|\|

There is no support for LIKE or CONTAINS conditions in the **Where clause** clause of a database view. Link tables based on the sys\_id using the = operator to work with the full dataset when filtering lists, running glide queries, or running reports.

## Procedure

1.  From the Database View form, select **New** on the View Tables related list.

2.  [Configure the form](../../../administer/form-administration/concept/configure-form-layout.md#) and add the **Left join** field \(a check box\) to the form.

3.  Select **Save**.

4.  Complete the form and select the **Left join** check box.

    -   Selecting **Left join** causes the left-hand table in the database view to display all records, even if the join condition does not find a matching record on the right-hand table. Select this check box to view tables that specify a **Where clause**. Selecting **Left join** for view tables without a **Where clause** does not affect the query.
    -   Joined tables are ordered left to right from lowest to highest **Order** values.
5.  Select **Submit**.

6.  Personalize the **View Tables** related list to show the **Left join** column.

    The **Left join** field is **true**.

7.  Select a record to view a table.

8.  To add an OR to your Where clause, use \|\|.

    For example, to query all incidents related to RFCs OR all incidents that are the parent of a change request, use the syntax: `inc_rfc = chg_sys_id || chg_parent = inc_sys_id`.


