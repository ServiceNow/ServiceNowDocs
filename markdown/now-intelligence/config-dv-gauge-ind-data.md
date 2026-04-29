---
title: Indicator data options for gauge data visualizations
description: When you select an indicator data source for a gauge visualization, the following Data configuration options are available.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Gauge visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Indicator data options for gauge data visualizations

When you select an indicator data source for a gauge visualization, the following Data configuration options are available.

**Note:** Fields that apply to Data snapshots indicators apply only to native Data snapshots indicators, not classic indicators with Data snapshots enabled.

The data source for a native Data snapshots indicator has the indicator type **Automated - Data Snapshots** or **Formula - Data Snapshots**.

![Data source properties for a native Data snapshots indicator](../../par-for-workspace/image/ds-source-native.png)

The data source for a classic indicator with Data snapshots enabled has the indicator type of either **Automated** or **Formula**.

![Data source properties for an enabled Data snapshots indicator](../../par-for-workspace/image/ds-source-enabled.png)

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

You have selected an indicator data source in [Create a gauge data visualization in the Visualization Designer](../task/create-dv-gauge-ac.md).

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

Date range

</td></tr><tr><td>

Apply date range

</td><td>

When turned on, this option allows date filters on the dashboard or UIB page to apply to this visualization. The date range can also be configured in the visualization, but date filters override visualization settings.

</td></tr><tr><td>

Show data for selected period as

</td><td>

Available when **Apply date range** is selected.The indicator aggregation logic for how scores from the selected period are shown, such as Latest score, Sum, or Average.

</td></tr><tr><td>

Set absolute period

</td><td>

Option to set absolute start and end date.Available when **Apply date range** is selected.

</td></tr><tr><td>

Period start

</td><td>

Start date for the absolute period.This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period end

</td><td>

End date for the absolute period.This property applies only when **Set absolute period** is true.

Select **Use current date for period end** to automatically update the end date to the current date. \(Not available if the start date is in the future.\)

</td></tr><tr><td>

Period

</td><td>

Time interval for each date period. -   Days `D`
-   Months `M`
-   Years `Y`

 This property applies only when **Set absolute period** is false.

</td></tr><tr><td>

Number of periods

</td><td>

Number of date periods to display. This property applies only when **Set absolute period** is true.

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

</td></tr><tr><td>

Real-time update

</td><td>

Option to update score in real time.**Note:**

-   This setting is available for automated, non-scripted indicators with a non-scripted breakdown mapping.
-   Real-time score updating does not support MIN, MAX, or COUNT DISTINCT aggregations.

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

Content

</td><td>

Secondary text of the message that provides additional detail.

</td></tr><tr><td>

Alignment

</td><td>

The alignment of the illustration and text in the message.

</td></tr></tbody>
</table>**Parent Topic:**[Create a gauge data visualization in the Visualization Designer](../task/create-dv-gauge-ac.md)

