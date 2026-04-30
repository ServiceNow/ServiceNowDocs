---
title: Create or modify to-dos
description: Create or modify a to-dos in the Employee Center.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Employee tasks page, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Create or modify to-dos

Create or modify a to-dos in the Employee Center.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

You can use a condition builder to specify the conditions that a task must meet for it to appear on the user to-dos page. You can also define the appearance of the to-dos configuration header. You can associate both task and non-task tables in to-do configuration.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configuration**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_ipr_bbk_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the to-dos configuration filter.

</td></tr><tr><td>

Table

</td><td>

Name of the table that the to-dos configuration is associated with.**Note:**

-   You can associate one filter per table.
-   The table must be an extension of the Task \[task\] table.


</td></tr><tr><td>

Tab

</td><td>

The tab where you want the to-dos to appear.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that a task must meet to appear on the to-dos page in the Employee Center.The conditions available to use are dependent on the table you select. **Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Check box to activate the to-dos configuration for use.

</td></tr><tr><td>

Applies to

</td><td>

Indicates the service portal the to-dos configuration applies to.

</td></tr></tbody>
</table>4.  Select **Save**.

    The **Title row** and **Detail row** tabs appear.

5.  In the **Title row** tab, configure the title row of the to-dos configuration header.

<table id="table_nht_lxy_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title type

</td><td>

Indicates what the title type applies to. The choices are:-   Fields: Uses a field from the table you selected for the title.
-   Custom: Provide custom text to appear as the to-dos configuration title.


</td></tr><tr><td>

Title field

</td><td>

Appears when you select **Fields** from the **Title type** list. Map a field from the table you selected to appear as the to-dos configuration title.

</td></tr><tr><td>

Custom title

</td><td>

Appears when you select **Custom** from the **Title type** list.Enter text you want to appear for the title.

</td></tr></tbody>
</table>6.  In the **Detail row** tab, configure the details row of the to-dos configuration header.

<table id="table_w3l_4xy_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Detail type

</td><td>

Indicates the type of detail you want to appear in the to-dos.-   Custom: Indicates custom text appears as the to-dos configuration details.
-   Parent fields: Select a parent table, and then map one or more fields from that table to appear as the to-dos configuration details. The fields will be separated by a hyphen.

**Note:** To display a link to the parent ticket page, make sure that the **Link to parent** check box is selected.

-   Fields: Map one or more fields from the associated table to appear as the to-dos configuration details. The fields will be separated by a hyphen.

**Note:** To display a link to the corresponding ticket page, make sure that the **Link to task** check box is selected.

</td></tr><tr><td>

Custom detail

</td><td>

Enter custom text you want to appear in the to-dos list. Only appears when you select **Custom** from the **Detail type** list.

</td></tr><tr><td>

Parent table

</td><td>

The table you want to use to select fields from in the detail row of your to-dos.Only appears when you select **Parent fields** from the **Detail type** list.

</td></tr><tr><td>

Parent fields

</td><td>

The fields you want to appear in the detail row of your to-dos. The fields you choose are based on the table you selected.Only appears when you select **Parent fields** from the **Detail type** list.

</td></tr><tr><td>

Link to parent

</td><td>

Indicates you want a link that opens the parent task to appear on the ticket page.Only appears when you select **Parent fields** from the **Detail type** list.

</td></tr><tr><td>

Detail fields

</td><td>

Indicates the fields you want to appear as the to-dos configuration details. If you select multiple fields, they are separated by a hyphen.Only appears when you select **Fields** from the **Detail type** list.

</td></tr><tr><td>

Link to task

</td><td>

Indicates you want a link to appear that prompts the user to select to open a task on the ticket page.**Note:** Link to task works only when the table extends the task table.

Only appears when you select **Fields** from the **Detail type** list.

</td></tr></tbody>
</table>7.  In the **To-dos Widget Mappings** list, you can map the filter to one or more custom to-dos widgets.

    **Note:** If no widget mapping is provided, a default to-dos widget is used.

    1.  Click **New** or open a record.

    2.  Fill in the fields on the form.

<table id="table_ork_bxq_sfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To-dos Configuration

</td><td>

This field is automatically set to the to-dos configuration that the widget mapping is associated with.

</td></tr><tr><td>

Table

</td><td>

This field is automatically set to the table that the to-dos configuration is associated with.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that a to-do must meet for it to display with the widget.**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Check box to activate the widget mapping for use.

</td></tr><tr><td>

Widget

</td><td>

Name of the widget that the to-dos configuration is associated with.**Note:** To learn more about widgets and how to configure them, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td></tr></tbody>
</table>    3.  Click **Submit** or **Update**.

8.  In the **To-dos Configuration Detail** list, you can map the source table fields based on the defined conditions.

    1.  Click **New** or open an existing record.

    2.  On the form, fill or modify the fields.

<table id="table_wgf_k2n_wqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

To-dos Configuration

</td><td>

Select the to-dos configuration that you want to associate with the widget.

</td></tr><tr><td>

Table

</td><td>

This field is automatically set to the table that the to-dos configuration is associated with.

</td></tr><tr><td>

To-do Target

</td><td>

Select the target table that you want to map the configuration to.

</td></tr><tr><td>

Conditions

</td><td>

Enter the Conditions that a to-do must meet for the configuration mapping.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Check box to activate the widget mapping for use.

</td></tr><tr><td>

Order

</td><td>

Enter the order number in which you want the To-do to appear in the widget.

</td></tr></tbody>
</table>    3.  Under **Field Mappings**, map the fields of the selected **To-dos configuration** table with the **To-do target** table.

        ![field mapping details](../images/to-do-config-field-mapping.png "To-do configuration detail field mappings")

    4.  Click **Submit** or **Update**.

9.  Click **Submit** or **Update**.


**Related topics**  


[Enable task configuration for approvals](approval-hub-to-dos-page-filters.md)

