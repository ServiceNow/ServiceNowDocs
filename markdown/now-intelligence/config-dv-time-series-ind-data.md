---
title: Indicator data options for time series data visualizations
description: The following Data configuration options are available for all time series type visualizations of indicator scores.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Time series visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Indicator data options for time series data visualizations

The following Data configuration options are available for all time series type visualizations of indicator scores.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

You have selected an Indicator data source in [Create time series data visualizations](../task/create-dv-time-series-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

MetricIf there is more than one metric, you can change the time series chart type for that metric by clicking the Change chart type icon. Also, if there is more than one metric, you can use the More options list to select a main metric and to add a Y-axis for each metric. Lastly, you can set dashboard filters to apply only to specific metrics. For more information, see [Options for time series data visualizations with multiple metrics](../concept/chart-options-multi-metrics.md).

</td></tr><tr><td>

Label

</td><td>

Label of the metric. By default it is the same as the name of the data source.

</td></tr><tr><td>

Time aggregation

</td><td>

Time aggregation to apply to the metric, such as 7-day running SUM or By-month AVG. Default is the same as the indicator period. For more information, see [Applying time series aggregations](../../performance-analytics/concept/applying-time-series-aggregations.md#).

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

</td></tr><tr><td>

Add alternative group by

</td><td>

This selection opens a dialog in which you select additional items that the data in the visualization may be grouped by. The viewer of the visualization can then select which of these items to group the data by. The viewer toggles the visibility of the selector in the visualization's More actions menu. In the additional items dialog, you can set whether this selector is visible by default by toggling **Selector visible by default**.If you select a value in **Group by**, that is the default group-by value. You do not have to select a **Group by** value to specify alternative group-by values. In this case, no default group-by value is used.

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

Ascending or descending. The sort by order for all elements in a time series visualization is based on the most recent element. For example, a column visualization that shows incidents per month grouped by priority, the order of priority for all months reflects that of the most recent month.

If some group by fields don’t support the selected sorting, they default to sorting by group bucket for date/time fields such as Age. For all other fields, they default to element order.

If a date filter is applied, the data is sorted by the most recent completed period.

</td></tr><tr><td class="sub-head" colspan="2">

Date range

</td></tr><tr><td>

Show maximum range

</td><td>

Option to show the maximum range of available dates.

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

Number of periods

</td><td>

Number of date periods to display. This property applies only when **Set absolute period** is true.

</td></tr><tr><td>

Period

</td><td>

Time interval for each date period. -   Days `D`
-   Months `M`
-   Years `Y`

 This property applies only when **Set absolute period** is false.

</td></tr><tr><td>

Allow change date range

</td><td>

When turned on, the viewer has a date range selector control with a set of predefined options.

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show target

</td><td>

If it is defined for the indicator, displays the global target value.

</td></tr><tr><td>

Show forecast

</td><td>

Option to display forecast data in the chart based on current trend data.**Note:** If there is not enough historical data to generate a forecast, no forecast or error is displayed.

</td></tr><tr><td>

Configure forecast

</td><td>

Opens a dialog for configuring forecasting on this data visualization. A forecast configuration on the data visualization overrides any configuration set on the data source, such as an indicator. This override applies only to the specific data visualization.This option is available only when Show forecast is turned on. For more information, see [Configure a forecast in a time series data visualization](../task/configure-forecast-ts-viz.md#).

</td></tr><tr><td>

Show forecast range

</td><td>

Option to display the 95% confidence interval of the forecast. Available only when Show forecast is turned on.

</td></tr><tr><td>

Show trend

</td><td>

Option to display the direction that the indicator is moving, or how values have changed over time.

</td></tr><tr><td>

Show confidence band

</td><td>

Option to display the bandwidth between which indicator scores are moving.

</td></tr><tr><td>

Show threshold

</td><td>

Option to display an active threshold set for the selected indicator, such as an all-time high or low. Thresholds appear only if they have been defined for the selected indicator.

</td></tr><tr><td>

Show comment

</td><td>

Option to display comments added to data points.

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

Show filter as separate series

</td><td>

When toggled on, if there is a filter applying multiple elements, these elements are shown as separate lines in the chart. The filter can be a component added to a dashboard or UIB page, or it can be an "is one of" filter condition on the data visualization itself.

 This feature supports only one breakdown at a time. Other breakdown filters have no effect on the chart. Filter precedence works as follows:

-   The first "is one of" filter condition on the data visualization overrides all other filter conditions and all single/multiple select filter components.
-   If there are no "is one of" filter conditions, the first multiple select filter that has a selection made overrides all other single/multiple select filters and all filter conditions.
-   A different multiple select filter can take effect if the first one is cleared.

Default: off. A single aggregate line is shown for all elements.

Requires the latest Data Visualization application from the ServiceNow Store.

 **Note:** Available only when no **Group by** is defined.

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

