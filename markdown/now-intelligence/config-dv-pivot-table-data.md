---
title: Table data options for pivot table visualizations
description: When you select a table data source for a pivot table visualization, the following Data configuration options are available.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Pivot table visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Table data options for pivot table visualizations

When you select a table data source for a pivot table visualization, the following Data configuration options are available.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" id="heading-data" colspan="2">

Data

</td></tr><tr><td>

Data source

</td><td>

You have selected a Table data source in [Create a pivot table data visualization in the Visualization Designer](../task/create-dv-pivot-ac.md).

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

Group by

</td></tr><tr><td>

Select columns

</td><td>

The field whose values are each represented in a vertical column.

</td></tr><tr><td>

Max number of groups

</td><td>

Select the maximum number of groups to display. Groups in excess of this number, determined by sorting, are aggregated into the Others group. You can show that aggregate with the **Show others** option.By default, you cannot show more than 50 groups. If you have the admin role, you can change this limit in the **par\_viz.table\_data.max\_groups** system property.

Data for the Max number of groups is evaluated across all periods in the time series to ensure consistent group membership across all dates in the visualization.

</td></tr><tr><td>

Show others

</td><td>

If **Max number of groups** is set and this option is turned on, an aggregate of the groups beyond the maximum number is displayed as the Others group.

</td></tr><tr><td>

Rows

</td><td>

Hierarchy of table fields with values displayed horizontally.

</td></tr><tr><td>

Field for &lt;table&gt;

</td><td>

The field to group by. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   If you want to group by a field with continuous values, such as date or integer, the values are automatically grouped according to any report ranges that are defined for the data. For more information, see [Report ranges](../concept/c_ReportRanges.md#).

</td></tr><tr><td>

Show row total

</td><td>

Option to show a final column with the total of each row

</td></tr><tr><td>

Show column total

</td><td>

Option to show a final row with the total of each column

</td></tr><tr><td>

Show parent row totals

</td><td>

When you have a hierarchy of more than one field in the rows, this option shows the sub total of fields higher up the hierarchy.

</td></tr><tr><td class="sub-head" colspan="2">

Sorting

</td></tr><tr><td>

Sort by

</td><td>

Sorting options of the main and alternative groups set in **Group by**. Options include:-   Name: Sorts the values alphabetically by field or element name.
-   Value: Sorts the values numerically or by count.
-   Element order: If you are grouping by records on the Choice \[sys\_choice\] table, either directly or through a breakdown, this option sorts the groups according to the value of the Sequence field.
-   Group bucket: Sorts the elements by bucket group, when applicable. Only available for indicator data sources and when the breakdown used for the **Group by** is based on a bucket group.
-   Report range: Sorts the table field values by range. Only available for table data sources and when the table field used for the **Group by** has a report range associated with it.

**Note:**

-   The choices of what to sort by are based on the main, default **Group by**, if one is defined. This sorting applies to any alternative group-bys if possible. If the sorting criterion selected for the main group-by cannot apply to an alternative group-by \(such as sorting by Element order when the alternative group-by is not on the Choice table\), sorting for that group-by defaults to Value.
-   If no main **Group by** has been set, but alternative group-bys are defined, you can sort only by Name or Value.
-   Sorting is not available for Pareto bar visualizations. Pareto charts are always sorted by value in descending order.

</td></tr><tr><td>

Sort by order

</td><td>

Ascending or descending.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show 0 when no data is available

</td><td>

When toggled on, shows empty \(NULL\) values as zero \(0\). Default is true.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Show filter icon

</td><td>

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

</td></tr><tr><td>

Refresh after being away for X min.

</td><td>

Triggered when you navigate away from the dashboard that contains the data visualization to another page in the same workspace, includingPlatform Analytics experience. Sets how many minutes you will be on another page before the visualization automatically refreshes when you navigate back.Do not confuse this property with the **Scheduled repetition** setting on inline dashboards. This latter property refreshes the entire dashboard, and applies only while that dashboard is open.

</td></tr><tr><td class="sub-head" colspan="2">

Info messages

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

Heading level

</td><td>

Header text size for the message that describes why no data was returned.

</td></tr><tr><td>

Content

</td><td>

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment

</td><td>

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>**Parent Topic:**[Create a pivot table data visualization in the Visualization Designer](../task/create-dv-pivot-ac.md)

