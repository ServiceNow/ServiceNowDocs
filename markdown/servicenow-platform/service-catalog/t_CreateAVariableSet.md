---
title: Create a variable set and add it to an item
description: Create a set of variables and add them to multiple catalog items and order guides for reuse.Service Catalog enables you to add a variable set to one or more catalog items or order guides.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Service catalog variable sets, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a variable set and add it to an item

Create a set of variables and add them to multiple catalog items and order guides for reuse.

## Before you begin

Role required: catalog\_admin, admin, catalog\_editor, or catalog\_manager

## About this task

-   Variable sets within a catalog item cannot have the same internal name.
-   Within a catalog item, the name of a variable cannot be the same as the title or internal name of a variable set.
-   Any catalog client script or catalog UI policy script should refer to the internal name of a variable set instead of its name or title.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Variables** &gt; **Variable Sets**.

2.  Click **New**.

    The Variable Set Creation page is displayed.

3.  Select any of the following.

    |Option|Description|
    |------|-----------|
    |**Single-Row Variable Set**|Creates a variable set with variables that are grouped together. **Type** field is set to `Single Row`.|
    |**Multi-Row Variable Set**|Creates a variable set with multiple rows that captures variable data in a grid layout. **Type** field is set to `Multi Row`.|

4.  Enter details.

<table id="table_c2q_s1c_xq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title of a variable set. Appears if the **Display title** check box is selected.

</td></tr><tr><td>

Internal name

</td><td>

Variable set name for internal use. For example, to access the variable set for the front-end \(through the g\_form API\) and server side scripting.

</td></tr><tr><td>

Order

</td><td>

Order number for the variable set.

</td></tr><tr><td>

Type

</td><td>

Type of the variable set. Possible choices are:-   Single Row
-   Multi Row


</td></tr><tr><td>

Application

</td><td>

Applications that can use this variable set.

</td></tr><tr><td>

Display title

</td><td>

If selected, adds a title and an expandable header to the right of the variable set.**Note:** When a user requests the item, all check box variables are grouped under a default title of **Options**. To use a custom title, insert a variable of type **Label**, with an **Order** value that puts it directly above the check box variables.

</td></tr><tr><td>

Variable Set attributes

</td><td>

Attributes for configuring a multi-row variable set. Use the **max\_rows** attribute to set a limit to the number of rows that you can add to a multi-row variable set. For example, specify `max_rows=1` as the field value.

</td></tr><tr><td>

Layout

</td><td>

The layout display. Set to **1 Column Wide** or **2 Columns Wide, alternating sides** or **2 Columns Wide, one side, then the other**.

</td></tr><tr><td>

Description

</td><td>

Description of the variable set.

</td></tr></tbody>
</table>5.  Right-click and select **Save**.

6.  Create the variables to use in that set.

    1.  In the Variables related list, click **New**.

    2.  Follow the steps for [creating variables](t_CreateAVariableForACatalogItem.md).

        **Note:** For a multi-row variable set:

        -   The included variables are displayed as columns of a table.
        -   The column order is the order of variables defined in the variable set.
7.  To create an associated catalog data lookup rule, perform the following steps.

    1.  In the Catalog Data Lookup Definitions related list, click **New**.

    2.  On the Catalog Data Lookup Definitions form, fill the fields.

        For information on creating a data lookup rule, see [Create a catalog lookup definition](t_CreatACatDataLookupDefRec.md#).

8.  Click **Submit**.


**Parent Topic:**[Service catalog variable sets](../concept/c_ServiceCatalogVariableSets.md)

## Add a variable set to a catalog item or order guide

Service Catalog enables you to add a variable set to one or more catalog items or order guides.

### Before you begin

Role required: catalog\_admin, admin, catalog\_editor, or catalog\_manager

### Procedure

1.  Open a catalog item or an order guide.

    |Option|Navigation path|
    |------|---------------|
    |**Catalog item**|**Service Catalog** &gt; **Catalog Definition** &gt; **Maintain Items**|
    |**Order guide**|**Service Catalog** &gt; **Catalog Definition** &gt; **Order Guides**|

2.  In the **Variable Sets** related list, click **Edit**.

    You can configure the form to add the **Variable Sets** related list.

3.  Select and add a variable set.

    **Note:** If the **Cascade Variables** check box is selected for an order guide, multi-row variable set data should be cascaded to the included items.

4.  Click **Save**.

5.  Click **Try**.

    **Note:** For a multi-row variable set:

    -   The associated variables are displayed as columns of a table on a catalog item or record producer. Each row corresponds to a set of data for all variables in the variable set.
    -   The column order is the order of variables defined in the variable set.
6.  Edit a multi-row variable set.

    1.  To add a row, click **Add** within the variable set, specify the variable information in the **Add Row** window, and click **Add**.

        **Note:**

        -   A maximum of 50 rows can be added.
        -   Unless default values are provided for variables or On Load scripts are used to pre-populate data, you should add variable data for each row.
    2.  To edit a row, click the edit row icon ![Icon to edit a row](../image/EditRow.png) in the **Actions** column, specify the variable information in the Edit Row window, and click **Save**.

        **Note:** When you add or edit an existing row, all catalog UI policies and client scripts associated with the multi-row variable set should be honored.

    3.  To remove a row, click the remove row icon ![Icon to remove a row](../image/RemvRow.png)in the **Actions** column and click **Remove** in the confirmation window.

    4.  To remove all rows of the table, Click **Remove All** within the variable set and click **Remove** in the confirmation window.


