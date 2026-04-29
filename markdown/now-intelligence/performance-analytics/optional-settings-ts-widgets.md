---
title: Additional settings for time series widgets
description: Time series widgets have the following optional settings for display, for the date range, and for the axis labels. You can also use these setting to select an elements filter in place of a first-level breakdown element.The visible points of the trend line are used to calculate the confidence band. If you increase the date range, the bands are recalculated using the trend for the new date range.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Time series widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Additional settings for time series widgets

Time series widgets have the following optional settings for display, for the date range, and for the axis labels. You can also use these setting to select an elements filter in place of a first-level breakdown element.

**Important:** This topic is not a guide to creating time series widgets. It is a guide to extra, optional settings that are common across time series widget types. FOR INSTRUCTIONS ON CREATING TIME SERIES WIDGETS, PLEASE SEE THE APPROPRIATE "CREATE" TOPIC:

-   [Create a line visualization for a time series widget](../task/create-line-visualization-ts.md)
-   [Create a column visualization for a time series widget](../task/create-column-visualization-ts.md)
-   [Create an area visualization for a time series widget](../task/create-area-visualization-ts.md)
-   [Create a spline visualization for a time series widget](../task/create-spline-visualization-ts.md)
-   [Create a step visualization for a time series widget](../task/create-step-visualization-ts.md)
-   [Create a stacked column visualization for a time series widget](../task/create-stacked-col-visualization-ts.md)
-   [Create a relative compare visualization for a time series widget](../task/create-relative-compare-ts.md)

The available settings depend on the selected visualization. The following example is for a Area Chart visualization.

![Additional settings for time series widgets.](../image/ts-widget-additional-settings.png)

## Date settings

The date settings are available only if **Previous period chart** is not selected.

<table id="table_a1k_nrp_r1b"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr id="row_widget_period"><td>

Period

</td><td>

Select the date range to display in the widget. Several options are available. -   Select a specific time range. The default is **3m** \(3 months\).
-   Select **max** to use scores up to the current date.
-   Select **between** and then fill in the **From** and **To** fields to define a time period.

 The **Period** field is available with only the following visualizations:

 -   Line
-   Spline
-   Column
-   Area
-   Step
-   Stacked Column
-   Relative Compare

</td></tr><tr id="row_widget_show_date_range_selector"><td>

Show date range selector

</td><td>

Display a date range selector on the widget. Users can then change the selected period when viewing the widget on a dashboard.**Note:**

-   Selecting a date range on a widget does not update the trend line.
-   If you combine a time series aggregation such as By month SUM with a date range selector, the user may see one more time period than they expect. The instance interprets a period such as 3 m as 0-3 months and may show four months of scores.
-   The date range selector is not supported for indicators based on a business calendar.

</td></tr></tbody>
</table>## Axis settings

<table id="table_axis-settings"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Y-axis title

</td><td>

Specify a title to display on the vertical axis of the chart.

</td></tr><tr><td>

Y-axis from

</td><td>

Specify the starting point for the range of values for the vertical axis of the chart.

</td></tr><tr><td>

Y-axis to

</td><td>

Specify the ending point for the range of values for the vertical axis of the chart.

</td></tr><tr><td id="row_2nd-y-axis">

2nd Y-axis title

</td><td>

Specify a secondary title to display on the vertical axis of the chart.

</td></tr><tr><td>

2nd Y-axis from

</td><td>

Specify the starting point for a 2nd range of values for the vertical axis of the chart.The 2nd Y-axis can be used if scores normally move between a limited range, but you have some exceptions that would otherwise distort the chart. For example, scores normally lie from 40 through 60, but there is an exception of 1000.

</td></tr><tr><td>

2nd Y-axis to

</td><td>

Specify the ending point for a 2nd range of values for the vertical axis of the chart.

</td></tr></tbody>
</table>## Display settings

|Setting|Description|
|-------|-----------|
|Show target|Display the target score, if defined. This field appears only if **Previous period chart** is not selected.|
|Show thresholds|Display thresholds such as an all time high or an all time low. Thresholds appear only if they have been defined for this indicator.|
|Show data labels|Display the score for each data point, such as each slice of a pie chart.|
|Show trend|Display the trend line. This field appears only if **Previous period chart** is not selected.|
|Show confidence bands|Display confidence bands in this chart. For information about how the confidence band is calculated, see [Widget confidence bands](optional-settings-ts-widgets.md#).|
|Show forecast|Display forecast data in the chart based on current trend data. Forecasting must be configured on the indicator.|
|Show forecast range|Display the 95% confidence interval of the forecast. Available only when **Select forecast** is enabled.|
|Show comments|Display comments added to data points in the chart.|

## Element settings

|Setting|Description|
|-------|-----------|
|Elements filter|Specify an element filter in place of the first-level [breakdown element](../concept/performance-analytics-glossary.md#). Use an elements filter to personalize which elements appear according to the characteristics of the viewer. For example, you can filter elements of the Assignment Group breakdown to show only the groups to which the viewer belongs. For more information, see [Personalized visuals](../concept/personalized-visuals.md#).|

## Previous Period settings

Previous period settings are available only if **Previous period chart** is selected.

**Note:** Thresholds, trend, confidence bands, and forecasts aren't intended to work when **Previous period chart** is selected.

|Setting|Description|
|-------|-----------|
|Range of periods|Select the range of periods to compare with the current period,|
|Number of periods|Specify the number of previous periods to display.|

## Widget confidence bands

The visible points of the trend line are used to calculate the confidence band. If you increase the date range, the bands are recalculated using the trend for the new date range.

First, the confidence bands are calculated using the standard error of the trend. The width of the band depends on the number of points that are included in the calculation and the mean of the scores. If the standard error is low, the trend line is shown to be accurate. As the number of points decreases, or outliers are recorded, the confidence band widens. The confidence of the trend is less certain with fewer data points or with volatile scores.

