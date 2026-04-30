---
title: Create a Timeline Visualization
description: Set up timeline visualizations for the organization's leaders by creating a timeline that provides visual representations of the organization's operational and strategic activities.
locale: en-US
release: yokohama
product: Timeline Visualizations
classification: timeline-visualizations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Timeline Visualizations, Personalize your experience, Configure user experiences]
---

# Create a Timeline Visualization

Set up timeline visualizations for the organization's leaders by creating a timeline that provides visual representations of the organization's operational and strategic activities.

## Before you begin

Role required: timeline\_admin

## About this task

Additionally, create timeline visualization views to define what data appears in the summary window when a user clicks a panel on the timeline.

**Note:** Activating timeline visualizations doesn't activate predefined CIO roadmap. You require PPM \(com.snc.financial\_planning\_pmo\) plugin to use CIO roadmap.

## Procedure

-   Navigate to **Timeline Visualization** &gt; **Create New** and create a new record.

    ![Timeline visualization configuration form](../image/TimelineVisualizationConfigurationForm.png "Timeline visualization configuration form")

<table id="table_hbg_cwd_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the visualization.

</td></tr><tr><td>

Panel table

</td><td>

Table that provides the records displayed as lanes and panels in the timeline.

 **Note:** The list shows only tables and database views that are in the same scope as the visualization.

</td></tr><tr><td>

Relationship field

</td><td>

Field on the table that contains values displayed as lane titles. Typically this field is a reference field or a field that contains a limited range of values.

 **Note:** The CIO Roadmap timeline visualization is a ServiceNow customized visualization for the Project application that does not use the Relationship field.

</td></tr><tr><td>

Show slider

</td><td>

Check box that enables \(selected\) or disables \(cleared\) displaying the timeline slider that users move to change the dates shown.

</td></tr><tr><td>

Panel name

</td><td>

Field from the Panel table that contains the values displayed in the panel body.

</td></tr><tr><td>

Panel date

</td><td>

Field from the Panel table that contains the date values displayed in the panel head in 3D view and in the panel body in 2D view. These dates also determine placement of panels on a lane. Only date and date-time fields are available on the choice list.

</td></tr><tr><td>

Default

</td><td>

Check box that sets \(selected\) or removes \(cleared\) the default status of a visualization when you have more than one defined for a specific table. Applications that include a visualization use the default visualization.

</td></tr><tr><td>

Max items per lane

</td><td>

Maximum number of items that are displayed in a lane in 3D view. The default value is 500.**Note:** The field is not visible on the form by default. Configure the form to add this field.

</td></tr><tr><td>

Max items per lane 2d

</td><td>

Maximum number of items that are displayed in a lane in 2D view. The default value is 99.**Note:** The field is not visible on the form by default. Configure the form to add this field.

</td></tr></tbody>
</table><table id="table_tsv_txd_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Lane condition

</td><td>

Condition builder used to create filters and apply sorting to values that are used as lanes in 3D view visualizations. For example, if you set **\[Name\] \[is not\] \[IT\]** as a lane condition for the CIO Roadmap, then IT no longer appears as a lane in the roadmap, nor does it appear as a lane option in the Settings pane. Removing the filter restores the IT lane to the visualization and to lane options in the Settings pane.

 To order the results, specify sorting based on relevant field names. For example, to order the portfolio names so that they appear in reverse alphabetical order on the CIO Roadmap, set the sort fields to **\[Name\] \[z to a\]**.

</td></tr><tr><td>

Panel condition

</td><td>

Condition builder used to create filters and apply sorting to values that are used as panels in 2D and 3D view visualizations. For example, if you set **\[State\] \[is one of\] \[Pending, Open, Work in Progress\]** as the panel condition for the CIO Roadmap, only projects that are in one of those states appear on the roadmap.

</td></tr></tbody>
</table><table id="table_ajs_b12_jq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Panel color key

</td><td>

Field from the Panel table that contains values used for color coding the information displayed. The field selected here determines the values that are available in the **Label** fields on the form.

 The CIO Roadmap uses **State**, which is a field in the Project table. Panels on the CIO Roadmap are color coded according to the project state, which can be Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Skipped.

**Note:** You require PPM \(com.snc.financial\_planning\_pmo\) plugin to use CIO roadmap.

 Examples of other fields that are suitable for this selection include **Priority**, **Risk**, and **Approval**.

</td></tr><tr><td>

Label 1

 Label 2

 Label 3

 Label 4

</td><td>

Values to be color coded. The values available are determined by the **Panel color key** field. For example, the CIO Roadmap is based on the Project table and has the **Panel color key** set to the **State** field, which contains the values Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, and Closed Skipped.

 You can set set specific colors for up to four values from the selected field. Other values are shown in the **Default color**.

</td></tr><tr><td>

Default color

</td><td>

Color applied to values that are not selected for labels. For example, the CIO Roadmap color codes and creates labels for the values Pending, Open, Work in Progress, and Closed Complete. The additional values, Closed Incomplete and Closed Skipped, use the default color.

</td></tr><tr><td>

Color 1

 Color 2

 Color 3

 Color 4

</td><td>

Colors that correspond to each of the **Label** field values. For example, if **Label 1** is the Pending state, and **Color 1** is red, then panels for projects in the pending state are red.

</td></tr></tbody>
</table>
**Parent Topic:**[Timeline Visualizations](../concept/c_TimelineVisualizations.md)

