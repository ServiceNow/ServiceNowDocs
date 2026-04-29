---
title: Table data options for time series data visualizations
description: The following Data configuration options are available for all time series type visualizations of table data.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Table data options for time series data visualizations

The following Data configuration options are available for all time series type visualizations of table data.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" id="heading-data" colspan="2">

Data

</td></tr><tr><td>

Data source

</td><td>

You have selected a Table data source in [Create time series data visualizations](../task/create-dv-time-series-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

MetricIf there is more than one metric, you can change the time series chart type for that metric by clicking the Change chart type icon. Also, if there is more than one metric, you can use the More options list to select a main metric and to add a Y-axis for each metric. Lastly, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](../concept/chart-options-multi-metrics.md).

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

Option to use a comma to separate groups of thousands.**Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Enable abbreviation

</td><td>

Option to use an alphabetical abbreviation. For example, M to represent million. **Note:** Only available when **Use custom formatting** is true.

</td></tr><tr><td>

Example

</td><td>

Example of the final value to show in the component. **Note:** Only available when **Use custom formatting** is true

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Field for \[table\]

</td><td>

The field to group by. For example, in an incident report grouped by **Assignment group**, all incidents that belong to Software, Service Desk, and Network are placed in separate groups. If the table contains variables or question fields, you have the option to group by one of them at the end of the list of fields.**Note:**

-   It is not possible to group or stack data by the **Tags** field, or by certain field types, such as MEDIUMTEXT.
-   If you want to group by a field with continuous values, such as date or integer, the values are automatically grouped according to any report ranges that are defined for the data. For more information, see [Report ranges](../concept/c_ReportRanges.md#).

</td></tr><tr><td>

Add alternative group by

</td><td>

This selection opens a dialog in which you select additional items that the data in the visualization may be grouped by. The viewer of the visualization can then select which of these items to group the data by. The viewer toggles the visibility of the selector in the visualization's More actions menu. In the additional items dialog, you can set whether this selector is visible by default by toggling **Selector visible by default**.If you select a value in **Group by**, that is the default group-by value. You do not have to select a **Group by** value to specify alternative group-by values. In this case, no default group-by value is used.

Data snapshots indicators support only reference, boolean, and choice fields for alternative group bys.

For more information about setting alternative group-bys for multiple metrics, see [Options for time series data visualizations with multiple metrics](../concept/chart-options-multi-metrics.md). For more information about the viewer experience selecting from alternative group-by values, see [Select a group-by value in a data visualization as a viewer](../../performance-analytics/concept/select-group-runtime.md).

**Important:**

-   Only up to three metrics on one visualization support alternative group-by.
-   Alternative group-by does not support data binding on the data source

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

Ascending or descending. The sort by order for all elements in a time series visualization based on table data is based on the entire data set. For example, a column visualization that shows incidents per month grouped by priority, the order of priority for all months is computed across all data points.

If there are multiple group bys added and if all group by fields support the selected sorting option, the selected sorting option applies to all.

If some group by fields don’t support the selected sorting, they default to Name.

If a date filter is applied, the data is sorted by the most recent period, even if that period is hidden.

</td></tr><tr><td class="sub-head" colspan="2">

Trend by

</td></tr><tr><td>

Calendar type

</td><td>

Select the calendar type the aggregation period is based on. Choices include Standard, Gregorian, and various business calendars. The calendar type determines the available aggregation periods.

</td></tr><tr><td>

Aggregation period

</td><td>

The period by which values are aggregated to calculate the trend. Options come from the standard calendar and any business calendars that are defined on the instance, such as the Gregorian. Select **Auto** to have the application infer the aggregation level based on the selected date range. Automatic aggregation respects business calendars and shift schedules.

</td></tr><tr><td>

Interval in minutes \[trendByMinuteInterval\]

</td><td id="entry_interval-minutes">

Number of minutes in each aggregation period. This property applies only when **Aggregation period** is **Minute**.

</td></tr><tr><td>

Date field for \[table\]

</td><td>

The date field on the table to aggregate by. You can only select fields of the following data types:-   Date
-   Date/Time
-   Due Date
-   Precise Time

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Follow filter per metric

</td><td>

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on. For more information, see [Following filters per metric](../concept/chart-options-bars-multi-metrics.md).

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
</table>**Parent Topic:**[Create time series data visualizations](../task/create-dv-time-series-ac.md)

