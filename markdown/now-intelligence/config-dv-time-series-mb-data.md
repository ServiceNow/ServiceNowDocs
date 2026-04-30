---
title: MetricBase data options for time series visualizations
description: The following data options are available for all time series type visualizations of MetricBase data.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Create time series visualizations, Data visualizations in Platform Analytics, Platform Analytics]
---

# MetricBase data options for time series visualizations

The following data options are available for all time series type visualizations of MetricBase data.

<table id="table_wqy_sjr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data source

</td><td>

You have selected a MetricBase data source in [Create time series visualizations](../task/create-dv-time-series-ac.md).

</td></tr><tr><td class="sub-head" colspan="2">

MetricIf there is more than one metric, you can change the time series chart type for that metric by clicking the Change chart type icon. Also, if there is more than one metric, you can use the More options list to select a main metric and to add a Y-axis for each metric. Lastly, if you have the latest version of the Data Visualizations application from the ServiceNow Store, you can set dashboard filters to apply only to specific metrics. For more information, see [Chart options for multiple metrics](../concept/chart-options-multi-metrics.md).

</td></tr><tr><td>

Label

</td><td>

Label of the metric. By default it is the same as the name of the data source.

</td></tr><tr><td>

Metric

</td><td>

Metrics determined in your MetricBase database.

</td></tr><tr><td>

Transform

</td><td>

Option to apply a transform to the data. For example, you can select **Envelope** to show the minimum and maximum \(envelope\) value within the dataset. For more information, see [MetricBase transforms](metricbase-transforms.md).

</td></tr><tr><td>

Dynamic period based on time range

</td><td>

When enabled, the aggregation period is set according to the time range. Time range &lt; 4 hours: minute aggregation. Time range 4 hours - 3 days: hourly aggregation. Time range &gt; 3 days: daily aggregation.

 Applies only when the Transform is Resample.

</td></tr><tr><td>

Label

</td><td id="entry_transform-label">

Label to apply to the transform. This property only applies when when **Transform** is Label.

</td></tr><tr><td>

Model

</td><td>

Prediction model to use to transform the data. If a model does not already exist, you can create one. To learn more, see [Detect anomalies in MetricBase data using predictive models](https://www.servicenow.com/docs/access?context=train-a-model&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).This property applies only when **Transform** is Predict.

</td></tr><tr><td>

Count

</td><td>

Specified number of values to show in the metric dataset.This property applies only when **Transform** is Top or Bottom.

</td></tr><tr><td>

Summand

</td><td>

Specified value to add to the data points in the dataset.This property applies only when **Transform** is Add.

</td></tr><tr><td>

Subtrahend

</td><td>

Specified value to subtract from the data points in the dataset.This property applies only when **Transform** is Subtract.

</td></tr><tr><td>

Factor

</td><td>

Value to multiply the data points in the dataset by. This property applies only when **Transform** is Multiply.

</td></tr><tr><td>

Divisor

</td><td>

Value to divide the data points in the dataset by. This property applies only when **Transform** is Divide.

</td></tr><tr><td>

Duration

</td><td>

Specified duration of new data points used to calculate an outcome.This property applies only when **Transform** is Interpolate.

</td></tr><tr><td>

Fractions

</td><td>

Percentiles of the underlying data to create a new dataset.This property applies only when **Transform** is Fractiles.

</td></tr><tr><td>

Function

</td><td>

Aggregation function used to calculate a new dataset. This property applies only when **Transform** is Resample, Filter, or Partition.

</td></tr><tr><td>

Period

</td><td>

New time period to apply to the dataset.This property applies only when **Transform** is Resample.

</td></tr><tr><td>

Window

</td><td>

Sliding time window of the given duration to create the new dataset. This property applies only when **Transform** is Filter or Partition.

</td></tr><tr><td>

Base

</td><td>

A timestamp to align the partition window.This property applies only when **Transform** is Partition.

</td></tr><tr><td>

Format values

</td><td id="entry_format-values">

Select to open the **Formatting values** dialog. For more information, see [Value formatting in reports](value-formatting-reports.md#).

</td></tr><tr><td class="sub-head" colspan="2">

Formatting values

</td></tr><tr><td>

Formatting

</td><td>

Select default, number, or duration format

</td></tr><tr><td class="sub-head" colspan="2">

--Number format

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

</td></tr><tr><td class="sub-head" colspan="2">

--Duration format

</td></tr><tr><td>

Unit format

</td><td>

Option to abbreviate the time unit or use full words

</td></tr><tr><td>

Maximum duration unit

</td><td>

Largest time unit in display

</td></tr><tr><td>

Minimum duration unit

</td><td>

Smallest time unit in display

</td></tr><tr><td>

Hide seconds when duration is greater than one minute

</td><td>

When Seconds are the minimum duration unit, toggling this on hides the second after the duration exceeds one minute.

</td></tr><tr><td>

Show original value in tooltip

</td><td>

Pointing to a displayed metric value shows the default formatted value in a tooltip.

</td></tr><tr><td>

Example

</td><td>

An example metric value as formatted

</td></tr><tr><td class="sub-head" colspan="2">

Group by

</td></tr><tr><td>

Group by

</td><td>

The field on the MetricBase data source to group by. For example, for a visualization of the Monitorable Item data source, you can group by Created by, Name, Primary, Tags, Type, or Updated by.

</td></tr><tr><td>

Add alternative group by

</td><td>

This selection opens a dialog in which you select additional items that the data in the visualization may be grouped by. The viewer of the visualization can then select which of these items to group the data by. The viewer toggles the visibility of the selector in the visualization's More actions menu. In the additional items dialog, you can set whether this selector is visible by default by toggling **Selector visible by default**.If you select a value in **Group by**, that is the default group-by value. You do not have to select a **Group by** value to specify alternative group-by values. In this case, no default group-by value is used.

For more information about the viewer experience selecting from alternative group-by values, see [Select a group-by value in a data visualization as a viewer](../../performance-analytics/concept/select-group-runtime.md).

</td></tr><tr><td class="sub-head" colspan="2">

Date range

</td></tr><tr><td>

Set absolute period

</td><td>

Option to set absolute start and end date.Available when **Apply date range** is selected.

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

Date format

</td><td>

Defines the date format for the X axis. -   Default `default`
-   Date `date`
-   Month `month`

</td></tr><tr><td>

Allow change date range

</td><td>

When turned on, the viewer has a date range selector control with a set of predefined options.

</td></tr><tr><td>

Show range picker by default

</td><td>

When turned on, the date range selector is shown to the viewer without the viewer needing to open it. When off, the viewer has to open the date range selector in the More options menu.

 Default: off \(false\)

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Show forecast

</td><td>

Option to display forecast data in the chart based on current trend data. Requires licensed Performance Analytics.**Note:** If there is not enough historical data to generate a forecast, no forecast or error is displayed.

</td></tr><tr><td>

Configure forecast

</td><td>

Opens a dialog for configuring forecasting on this data visualization. A forecast configuration on the data visualization overrides any configuration set on the data source, such as an indicator. This override applies only to the specific data visualization.This option is available only when Show forecast is turned on. For more information, see [Configure a forecast in a time series visualization](../task/configure-forecast-ts-viz.md#).

</td></tr><tr><td>

Show forecast range

</td><td>

Option to display the 95% confidence interval of the forecast. Available only when Show forecast is turned on.

</td></tr><tr><td class="sub-head" colspan="2">

Data update

</td></tr><tr><td>

Follow filters

</td><td>

Follow filters set for a page. When enabled, the visualization displays on a workspace with the filters set by the page. Toggle off to disable a visualization from accepting any filter input.

</td></tr><tr><td>

Follow filter per metric

</td><td>

If the visualization shows multiple metrics, toggle filter following on and off for each metric. Default: All metrics follow filters if Follow filters is on.Requires the latest Data Visualization application from the ServiceNow Store.

</td></tr><tr><td>

Show filter icon

</td><td>

Option to show the filter icon and the number of filters impacting the visualization. If a filter is not selected to apply to a visualization, the icon does not show. Toggle off to hide the filter icon and number of filters applied.

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