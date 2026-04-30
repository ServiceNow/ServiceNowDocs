---
title: Add a custom column to the planning console
description: Define the columns that you want to make available in the project planning console, portfolio workbench, program workbench, and the release management Gantt chart.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Custom columns in the planning console, Using Planning console - Legacy, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add a custom column to the planning console

Define the columns that you want to make available in the project planning console, portfolio workbench, program workbench, and the release management Gantt chart.

## Before you begin

Role required: it\_pps\_admin

## Procedure

1.  Navigate to **All** &gt; **Project Administration** &gt; **Settings** &gt; **Planning Console**.

2.  Add a custom display column for planning console.

    1.  In the Planning Console list, select a console to which you want to add the custom column.

        For example, select `Project[pm_project]` to add a column to the project planning console.

    2.  To create a display column for the selected console, select **New** in the **Planning Console Display Column** related list.

    3.  On the Planning Console Display Column form, fill in the fields.

<table id="table_irt_mrm_rx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label for the column to be displayed in the planning console.

</td></tr><tr><td>

Type

</td><td>

Data type of the column.

</td></tr><tr><td>

JSON Column

</td><td>

The JSON column name used internally by the Gantt chart when data is sent. **Note:** Leave blank. This field is auto-populated when you add a column for the display column in step 3.

</td></tr><tr><td>

Order

</td><td>

Position at which the column appears in the planning console.

</td></tr><tr><td>

Include in Tooltip

</td><td>

Check box for the column to be shown in tooltip in timeline in the planning console.

</td></tr><tr><td>

Width

</td><td>

Default width of the column in planning console.

</td></tr><tr><td>

Fire BR on Save

</td><td>

Option if the business rules should be triggered when the column is modified in the planning console.**Note:** The field is not visible on the form by default. Configure the form to add this field.

</td></tr><tr><td>

Trigger recalculation

</td><td>

Option if the recalculation of date and duration should be triggered when the column is modified in the planning console.**Note:** The field is not visible on the form by default. Configure the form to add this field.

</td></tr></tbody>
</table>    4.  Select **Submit**.

    The column is added in the `Planning Console Display Column [pm_console_display_column]` table.

3.  Map the planning console display column created in step 2 to a column in a table defined in `Planning Console Table [pm_console_table]`.

    1.  In the **Planning Console Display Column** related list, open the display column record.

    2.  To create a record of actual column in the `Planning Console Column [pm_console_column]` table, select **New** in **Planning Console Columns** related list.

    3.  On the Planning Console Column form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Column

</td><td>

Display column created in the Planning Console Display Column `[pm_console_display_column]` table.

</td></tr><tr><td>

Console Table

</td><td>

Console table to be mapped to the display column.

</td></tr><tr><td>

Table

</td><td>

Actual table from where the data is pulled in the display column. The field is auto-populated when you select a Console Table.For example, select a table from `[pm_project]` or `[pm_project_task]` for a display column added in the Project planning console `Project [pm_project]`.

</td></tr><tr><td>

Column

</td><td>

Actual column in the **Table** from where data comes for the display column.

</td></tr><tr><td>

Editable

</td><td>

Check box to make the column editable in the planning console.

</td></tr></tbody>
</table>    4.  Select **Submit**.


## Result

The display column appears in the column filter list \(![Filter icon](../image/filter_icon.png)\) in the planning console.

**Parent Topic:**[Custom columns in the planning console](../concept/custom-columns-planning-console.md)

**Related topics**  


[Using Planning console - Legacy](../concept/c_TheProjectPlanningConsole.md)

