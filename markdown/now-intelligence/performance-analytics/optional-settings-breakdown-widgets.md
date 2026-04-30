---
title: Additional settings for breakdown widgets
description: Breakdown widgets have the following optional settings for the date range, the display, the grouping breakdown, and for the column contents. Not all options are available for all visualizations.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Breakdown widgets, Performance Analytics widgets, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Additional settings for breakdown widgets

Breakdown widgets have the following optional settings for the date range, the display, the grouping breakdown, and for the column contents. Not all options are available for all visualizations.

The available settings depend on the selected visualization. The following example is for a Scorecard visualization.

![Additional settings for breakdown widgets.](../image/bkdown-widget-additional-settings.png)

## Date settings

<table id="table_edt_jbf_kqb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr id="row_widget_period"><td>

Period

</td><td>

Select the date range to display in the widget. Several options are available.-   Select a specific time range. The default is **3m** \(3 months\).
-   Select **max** to use scores up to the current date.
-   Select **between** and then fill in the **From** and **To** fields to define a time period.

The **Period** field is available only if you select **Line**, **Columns and Total**, or **Stacked Column** as the **Visualization**

</td></tr><tr id="row_widget_show_date_range_selector"><td>

Show date range selector

</td><td>

Display a date range selector on the widget that enables users to change the selected period when viewing the widget on a dashboard.**Note:**

-   Selecting a date range on a widget does not update the trend line.
-   If you combine a time series aggregation such as By month SUM with a date range selector, the user may see one more time period than they expect. The instance interprets a period such as 3m as 0-3 months and may show four months of scores.

</td></tr></tbody>
</table>## Axis settings

**Note:** Axis settings are not available when Stacked column is the visualization.

<table id="table_bqq_kjf_kqb"><thead><tr><th>

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

Specify the starting point for a 2nd range of values for the vertical axis of the chart.The 2nd Y-axis can be used if scores normally move between a limited range, but you have some exceptions that would otherwise distort the chart, such as a range of 40 to 60, with an exception of 1000.

</td></tr><tr><td>

2nd Y-axis to

</td><td>

Specify the ending point for a 2nd range of values for the vertical axis of the chart.

</td></tr></tbody>
</table>## Display settings

<table id="table_qt2_qjf_kqb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show target

</td><td>

Display the target score, if defined. This field appears only if **Previous period chart** is not selected.

</td></tr><tr><td>

Show thresholds

</td><td>

Display thresholds such as an all time high or an all time low. Thresholds appear only if they have been defined for this indicator.

</td></tr><tr id="row_widget_show_data_labels"><td>

Show data labels

</td><td>

Display the score for each portion of the chart, such as for each slice of a pie chart.

</td></tr><tr><td>

Show trend

</td><td>

Display the direction the indicator is moving. The trend is shown in a mini-chart on the dashboard.

</td></tr><tr><td>

Show confidence bands

</td><td>

Display confidence bands in this chart. For information about how the confidence band is calculated, see [Widget confidence bands](optional-settings-ts-widgets.md#).

</td></tr><tr><td>

Show forecast

</td><td>

Display forecast data in the chart based on current trend data. Forecasting must be configured on the indicator.

</td></tr><tr><td>

Show comments

</td><td>

Display comments added to data points in the chart.

</td></tr><tr id="row_widget_show_visualization_selector"><td>

Show visualization selector

</td><td>

Display a choice list on the widget that enables users to change the selected visualization from a dashboard.**Note:** You cannot select the **Pivot Scorecard** visualization from a dashboard. You must configure the widget record to use this visualization.

</td></tr><tr id="row_widget_show_breakdown_selector"><td>

Show breakdown selector

</td><td>

Display a choice list on the widget that enables users to change the selected breakdown from a dashboard. There must be more than 1 breakdown available for the widget for the breakdown choice list to appear.

</td></tr><tr><td>

Positive color

</td><td>

When the **Visualization** is **Treemap**, select the color used to indicate a score moving in the desired direction, based on the indicator **Direction** value. If **Color based on** is set to **Target**, the positive color indicates values closer to the target.

</td></tr><tr><td>

Negative color

</td><td>

When the **Visualization** is **Treemap**, select the color used to indicate a score moving in the wrong direction, based on the indicator **Direction** value. If **Color based on** is set to **Target**, the negative color indicates values further away from the target. This field is not available when **Color based on** is **Score**.

</td></tr><tr><td>

Show legend

</td><td>

When the **Visualization** is **Treemap**, select this option to display a legend for the positive and negative colors.

</td></tr><tr><td>

Include elements without data in the legend

</td><td>

Shows the breakdown name in the legend of the widget even when no records match the elements of the breakdown.

</td></tr></tbody>
</table>## Breakdown settings

<table id="table_kqt_rkf_kqb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Breakdown on Y axis

</td><td>

Pivot Analytics Hub breakdown widgets display [breakdown elements](../concept/performance-analytics-glossary.md#) as the X axis and indicators as the Y axis by default. Select this check box to display breakdown elements as the Y axis and indicators as the X axis.

</td></tr><tr><td id="row_widget_show_total">

Show total

</td><td>

If you selected **Scorecard** in the **Visualization** field, an extra row can be included in the breakdown chart showing the totals of all selected breakdowns.

</td></tr><tr><td>

Show bar

</td><td>

Represent the score for each instance by a bar.

</td></tr></tbody>
</table>## Element settings

<table id="table_mp4_bvg_v1b"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Elements filter

</td><td>

Specify if only a certain subset of breakdown elements are available for this widget. By default all elements are available.For example, elements of the breakdown **Priority** can be: **Critical**, **High**, **Moderate**, **Low** or **Planning**.

</td></tr><tr><td>

Manual elements

</td><td>

Breakdown elements can be selected automatically or manually. Select the **Manual elements** check box to display the **Widget Elements** related list for adding elements. Clear the **Manual elements** check box to automatically use the elements that belong to the breakdown.

</td></tr><tr><td>

Show top x

</td><td>

Show only the elements with the x highest scores, according to the **Sort by** field, to make the chart easier to read.In case of ties, the first element listed in the scoresheet is shown. For example, if you have a widget where **Show top x** is 3 and the third-highest value for the Priority breakdown is tied between High and Moderate, the widget shows High, not Moderate.

 ![Scoresheet with two elements tied for 3rd highest value.](../image/bkdown-widget-tied-top-x.png)

 ![Breakdown widget with Show Top x = 3 and the elements 2 - high and 3 - Moderate tied for third highest, with 2 - High showing.](../image/bkdwn-widget-show-top-3.png)

 The order in which the scoresheet lists elements depends on the table containing the elements. For example, for elements on the Choice \[sys\_choice\] table, this order follows the value in the Sequence field. For elements on the Group \[sys\_group\] table, the order is alphabetical based on the Name field.

 **Note:** The top elements are selected from the most recent scores. If the widget has a line visualization, the top elements are still selected from the most recent scores, even if other elements have a higher average score across the timespan shown.

</td></tr><tr><td>

Percentages

</td><td>

If you select **No percentages**, no score percentages are shown for the instances. If you select **Percentage of elements**, a score percentage is shown for each instance. For example, 6.4% of the total incidents are Critical, 11.8% are High, and so on.

</td></tr></tbody>
</table>## Column settings

<table id="table_cpx_jlf_kqb"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Current score

</td><td>

Display the score from the latest data collection.

</td></tr><tr><td>

Trend

</td><td>

Display the direction the indicator is moving. The trend is shown in a mini-chart on the dashboard.

</td></tr><tr><td>

Multiple scores

</td><td>

Adds scores to the Analytics Hub. Select the number of additional scores to display in **Number of periods**. Select the length of each period in **Period step**. If **Current Score** is also selected, the Score column is counted as the most recent period and N-1 periods are added.

</td></tr><tr id="row_widget_change"><td>

Change

</td><td>

Display the change from the previous score.

</td></tr><tr id="row_widget_change_percent"><td>

Change %

</td><td>

Display the percentage change from the previous score.

</td></tr><tr id="row_widget_target"><td>

Target

</td><td>

Display the target for the indicator if a target has been defined.

</td></tr><tr><td>

Gap

</td><td>

Display the difference between the current and the target scores. Gap can be either positive \(moving towards the target\) or negative \(moving away from the target\).

</td></tr><tr><td>

Gap %

</td><td>

Display the percentage difference between the current and target scores. Gap % can be either positive \(moving towards the target\) or negative \(moving away from the target\).

</td></tr></tbody>
</table>## Latest score settings

|Setting|Description|
|-------|-----------|
|Compare score with|This tab is shown when the visualization type is Latest Score. Select Previous Score or Periods Back. You can specify any number of previous periods.|

