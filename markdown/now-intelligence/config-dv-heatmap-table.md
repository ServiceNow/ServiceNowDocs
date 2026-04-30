---
title: Table data options for heatmap visualizations
description: When you select a table data source for a heatmap visualization, the following Data configuration options are available.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Create a heatmap visualization, Data visualizations in Platform Analytics, Platform Analytics]
---

# Table data options for heatmap visualizations

When you select a table data source for a heatmap visualization, the following Data configuration options are available.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" id="heading-data" colspan="2">

Data

</td></tr><tr><td>

Data source

</td><td>

You have selected a Table data source in [Create a heatmap visualization in the Visualization Designer](../task/create-dv-heatmap-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

Metric

</td></tr><tr><td>

Label

</td><td>

Label of the metric. By default it is the same as the name of the data source.

</td></tr><tr><td>

Select an aggregation

</td><td>

Computational method for aggregating data. The default is **Count**, which displays the number of records selected.**Note:** If you select **Count Distinct**, only unique records are counted. For example, you want to generate a report with a distinct number of users who have one or more of the roles in a given list of roles. Users with more than one role would be counted twice unless you use **Count Distinct**.

</td></tr><tr><td>

Field

</td><td>

Field to apply the metric to, for **Average**, **Sum**, or **Count Distinct** aggregations. You may further be able to aggregate on fields from extended tables.The data is shown in a format that matches the field type. For example, if you select an integer field, such as the **Priority** field, the data is expressed as a number. If you select a duration field, such as **Business duration** on the Incident table, the aggregated data is expressed in days, hours, and minutes.

If function fields were created in Report Designer for the table, they are available in the dropdown list. For more information, see [Report on function fields](../concept/function-fields-reporting.md).

</td></tr><tr><td>

Format values

</td><td id="entry_format-values">

Select to open the **Formatting values** dialog. For more information, see [Value formatting in reports](value-formatting-reports.md#).

</td></tr><tr><td class="sub-head" colspan="2">

Formatting values

</td></tr><tr><td>

Use custom formatting

</td><td>

Option to use custom formatting on the component.

</td></tr><tr><td>

Decimal precision

</td><td id="entry_decimal-precision">

Number of decimals to show in the metric. This field is available only when the **Use custom formatting** option is activated.

</td></tr><tr><td>

Rounding

</td><td>

Type of rounding to use to reach the number of decimals in the **Decimal precision** field. Options include:-   Up `UP`
-   Down `DOWN`
-   Ceiling `CEILING`
-   Floor `FLOOR`
-   Half up `HALF_UP`
-   Half down `HALF_DOWN`
-   Half even `HALF_EVEN`

 **Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Use the thousands group separator

</td><td>

Option to use a comma to separate groups of thousands.**Note:** Only available when **Use custom formatting** is true

</td></tr><tr><td>

Enable abbreviation

</td><td>

Option to use an alphabetical abbreviation. For example, M to represent million. **Note:** Only available when **Use custom formatting** is true

</td></tr><tr><td>

Example

</td><td>

Example of the final value to show in the component. **Note:** Only available when **Use custom formatting** is true

</td></tr><tr><td>

Show original number in tooltips

</td><td>

Option to include a tooltip to show the unformatted number on point to. **Note:** Only available when **Use custom formatting** and **Enable abbreviation** are true.

</td></tr><tr><td class="sub-head" colspan="2">

Group by, for column and row

</td></tr><tr><td>

Field for \[table\]

</td><td>

The field to group by. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.**Note:** It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.

</td></tr><tr><td>

Max number of groups

</td><td>

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the Others group. You can show that aggregate with the **Show others** option.By default, you cannot show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

</td></tr><tr><td>

Show others

</td><td>

If **Max number of groups** is set and this option is turned on, an aggregate of the groups beyond the maximum number is displayed as the Others group.

</td></tr><tr><td>

Add alternative group by

</td><td>

This selection opens a dialog in which you select additional items that the data in the visualization may be grouped by. The viewer of the visualization can then select which of these items to group the data by. The viewer toggles the visibility of the selector in the visualization's More actions menu. In the additional items dialog, you can set whether this selector is visible by default by toggling **Selector visible by default**.If you select a value in **Group by**, that is the default group-by value. You do not have to select a **Group by** value to specify alternative group-by values. In this case, no default group-by value is used.

For more information about the viewer experience selecting from alternative group-by values, see [Select a group-by value in a data visualization as a viewer](../../performance-analytics/concept/select-group-runtime.md).

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by

</td><td>

Groups or categories to sort by in the specific order. Options include Name, Value, and Group bucket.

</td></tr><tr><td>

Sort by order

</td><td>

Ascending or descending.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show zero

</td><td>

When toggled on, shows empty \(NULL\) values as zero \(0\). Default is true.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Refresh after being away for X min.

</td><td>

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td class="sub-head" colspan="2">

No data message

</td></tr><tr><td>

Set custom message when no data

</td><td>

Option to configure a custom message that displays when no data is returned.

</td></tr><tr><td>

Illustration

</td><td>

An illustration to include in the message.

</td></tr><tr><td>

Heading

</td><td>

Header text of the message that describes why no data was returned.

</td></tr><tr><td>

Content

</td><td>

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment

</td><td>

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>