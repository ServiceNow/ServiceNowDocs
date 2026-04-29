---
title: Indicator data options for pivot table data visualizations
description: When you select an indicator data source for a pivot table visualization, the following Data configuration options are available.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Pivot table visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Indicator data options for pivot table data visualizations

When you select an indicator data source for a pivot table visualization, the following Data configuration options are available.

**Note:** Fields that apply to Data snapshots indicators apply only to native Data snapshots indicators, not classic indicators with Data snapshots enabled.

The data source for a native Data snapshots indicator has the indicator type **Automated - Data Snapshots** or **Formula - Data Snapshots**.

![Data source properties for a native Data snapshots indicator](../../par-for-workspace/image/ds-source-native.png)

The data source for a classic indicator with Data snapshots enabled has the indicator type of either **Automated** or **Formula**.

![Data source properties for an enabled Data snapshots indicator](../../par-for-workspace/image/ds-source-enabled.png)

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" id="heading-data" colspan="2">

Data

</td></tr><tr><td>

Data source

</td><td>

You have selected an Indicator data source in [Create a pivot table data visualization in the Visualization Designer](../task/create-dv-pivot-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

Metric

</td></tr><tr><td>

Label

</td><td>

Label of the metric. By default it is the same as the name of the data source.

</td></tr><tr><td>

Time aggregation

</td><td>

Time aggregation to apply to the metric, such as 7-day running SUM or By-month AVG. Default is the same as the indicator period. For more information, see [Applying time series aggregations](../../performance-analytics/concept/applying-time-series-aggregations.md#).

</td></tr><tr><td>

Select an aggregation \(Data snapshots indicators only\)

</td><td>

The aggregation is based on the Data snapshots indicator's configuration. You cannot change it in the context of creating a data visualization. **Count** counts the number of records. **Count distinct** counts the number of unique values rather than the total number of records. For example, if the name of a user appears more than once in a list, the user is only counted once. Other choices perform the specified aggregate operation, such as summing the values in a field across records.

</td></tr><tr><td>

Field \(Data snapshots indicators only\)

</td><td>

The field on the Data snapshot's source to which the aggregate is applied. Required for all aggregates except Count.

</td></tr><tr><td>

Show incomplete periods \(Data snapshots indicators only\)

</td><td>

Select to display values from the period in progress. Clear this check box to show only the values for completed periods.

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

Breakdown

</td><td>

List of breakdowns to choose from for grouping indicator scores.**Important:**

-   Scripted breakdowns are not supported in dashboard filters.
-   Only two levels of breakdown are supported in total, including data visualization and dashboard filters.

Data snapshots indicators support only reference, boolean, and choice fields for group bys.

For Data snapshots indicators, breakdowns are configured on the indicator source. For all other indicator data sources, breakdowns are configured on the indicator itself.

</td></tr><tr><td>

Max number of groups

</td><td>

The maximum number of breakdown elements to display in columns. This property does not apply to rows.

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

