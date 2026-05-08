---
title: Create time series data visualizations
description: Show changes in data over time. Use different time series visualizations to emphasize different aspects of the data, such as trends or individual values.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create time series data visualizations

Show changes in data over time. Use different time series visualizations to emphasize different aspects of the data, such as trends or individual values.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

A time series is an ordered sequence of metrics taken continuously over time. The following business cases are some of the uses of a time series:

-   Identifying trends, patterns, and outliers in data.
-   Identifying turning points, such as whether a change in policy led to a change in indicator scores.
-   Evaluating the relationships between data sources.

When you are selecting a visualization for a time series, consider whether you want to emphasize the trend in the data or specific changes in the data. Also consider whether you want to show one data source or compare several related data sources.

For information about the use of a Time series visualization in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-timeseries-wrapper/usage). This site gives information about Time series data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

For an example of creating a time series visualization, see [Time series data visualization example](../../par-for-workspace/task/dv-example-line.md).

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Configure the **Header and border**. Header and border options are the same for all data sources.

<table id="table_ly5_djk_c5b"><thead><tr><th>

Header and border fields

</th><th>

Description

</th></tr></thead><tbody><tr id="ac-dv-showborder"><td>

Show border

</td><td>

Option to display a line around the component.

</td></tr><tr id="ac-dv-showheader"><td>

Show header

</td><td>

The visualization header, including title and icons.

</td></tr><tr id="ac-dv-showheadersep"><td>

Show header separator

</td><td>

Option to display a line separating the header from the rest of the component.

</td></tr><tr id="ac-dv-charttitle"><td>

Chart title

</td><td>

Title of the visualization.

</td></tr><tr id="ac-dv-title-align"><td>

Title alignment

</td><td>

Choose Start to align the title with the start of line, End to align it with the end of the line, or Center for center alignment.

</td></tr><tr id="ac-dv-chartdesc"><td>

Description

</td><td>

A short overview about the visualization that the end user sees. Descriptions help users find the visualization.

</td></tr><tr id="ac-dv-wraptitle"><td>

Wrap title

</td><td>

Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.

</td></tr><tr id="ac-dv-wraplabels"><td>

Wrap labels

</td><td>

Select to wrap long elements labels on the axis.

</td></tr><tr id="ac-dv-maxlabelsize"><td>

Max label size, px

</td><td>

Specify the maximum label size for element names on the axis. Default=100 px.

</td></tr><tr id="ac-dv-truncationtype"><td>

Line of truncation

</td><td>

Specify where to truncate long labels with an ellipsis. Options are 1, 2, and 3.

</td></tr><tr id="ac-dv-bare"><td>

Bare

</td><td>

Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.

</td></tr><tr id="ac-dv-showrefreshoption"><td>

Show refresh option

</td><td>

Option to show or hide the refresh option from data visualizations. If cache is enabled on a dashboard, the Refresh option is always hidden.

</td></tr><tr id="ac-dv-show-export-option"><td>

Show export options

</td><td>

Option to show or hide the visualization's export types.

</td></tr><tr><td>

Header background color

</td><td>

Specify the color behind the title of the visualization.

</td></tr><tr><td>

Title color

</td><td>

Specify the text color of the title. The default title color is black, but you can choose a color that contrasts better with the header background. Only available when **Header background color** is selected.

</td></tr></tbody>
</table>4.  Choose a data source.

    For general descriptions of the data sources, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

    -   Table \(available in the base system\). When you select a table, you can filter it by custom or preconfigured conditions. Custom conditions can include questions or Service Catalog variables.

        Configured report sources appear in the **Predefined conditions** list. For more information, see [Report sources](../concept/c_ReportSources.md#).

        To help you create a custom filter, there is a preview list of records that would be included in the visualization. You can change which fields are shown as columns and the width of columns in the list actions.

        ![Preview record list for table source data visualization with list actions shown.](../../par-for-workspace/image/dv-preview-edit-cols.png)

    -   Indicator \(available in the base system\). You can filter the indicator scores by breakdowns and elements.

        **Note:** Benchmark indicators are not supported.

        ![Conditional filter for indicator data source on data visualization.](../../performance-analytics/image/dv-ind-source-con-filter.png)

        **Note:**

        You might have a multiple select \(is one of\) or dynamic \(is \(dynamic\)\) operator on the breakdown element filter. These operators require the indicator and breakdown to support them. For more information about the configurations that support these operators, see ["Is one of" and "Is \(Dynamic\)" operators on breakdown conditions in data visualizations](../../performance-analytics/concept/condition-operators-ind-bkdowns.md#section_breakdown-operators).

    -   MetricBase \(available if MetricBase is enabled\). When you select a MetricBase data source, you have the option of constructing a custom filter for it using conditions and related list conditions, as with Table data sources.
    -   Usage Insights \(available with the User Experience PAR Integration application, to users with a required role\). Choose one of up to three KPIs included with this application, depending on the visualization type. For more information, see [Usage Insights data sources for data visualizations](../../performance-analytics/concept/uxa-data-sources.md).
    **Note:** You can select multiple data sources for this visualization, but they must be of the same type: table, indicator, Usage Insights, or MetricBase. For more information, see [Multiple data sources](../../par-for-workspace/reference/multiple-data-sources.md#).

5.  Select the options for your data source.

    -   If your visualization represents table data, go to [Table data options for time series data visualizations](../reference/config-dv-time-series-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for time series data visualizations](../reference/config-dv-time-series-ind-data.md).
    -   If your visualization represents Usage Insights data, go to [Usage Insights data options for time series data visualizations](../reference/config-dv-time-series-uxa-data.md).
    -   If your visualization represents MetricBase data, go to [MetricBase data options for time series data visualizations](../reference/config-dv-time-series-mb-data.md).
6.  Under **Presentation**, provide display and color information.

<table id="table_gvk_2mr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Display settings: Each visualization type, such as Area and Column, has a different set of display settings. See [Display settings for different time series data visualizations](../reference/display-settings-ts-charts.md).

</td></tr><tr><td class="sub-head" colspan="2">

Y axis

</td></tr><tr><td>

Hide axis

</td><td>

Option to hide the primary axis.

</td></tr><tr><td>

Primary axis title

</td><td>

Title to display on the vertical axis of the visualization.This property applies only when **Hide primary axis** is false.

If there is more than one Y-axis, you have additional axis titles, representing the properties yAxis1Title, yAxis2Title, etc.

Add a Y-axis scale for a metric in the **More options** menu for the metric.

</td></tr><tr><td>

Axis range - from

</td><td>

Starting point for the values on the primary axis.

</td></tr><tr><td>

Axis range - to

</td><td>

End point for the values on the primary axis.

</td></tr><tr><td>

Show grid

</td><td>

Shows a grid of fine lines perpendicular to the primary axis, to help align values against that axis.

</td></tr><tr><td>

Axis style

</td><td>

Style of the primary axis. -   Clean `clean`: Adds a straight line to the primary axis.
-   No tick lines `noTicks`: Option to remove all marks from the primary axis.
-   Standard `default`: Adds a line and tick marks to the primary axis.


</td></tr><tr><td class="sub-head" colspan="2">

X axis

</td></tr><tr><td>

X axis title

</td><td>

Title to display on the horizontal axis of the visualization.

</td></tr><tr><td>

Show grid

</td><td>

When enabled, grid lines appear on the visualization.

</td></tr><tr><td class="sub-head" colspan="2">

Legend

</td></tr><tr><td>

Show legend

</td><td>

Option to display the legend. Activated automatically at 400% zoom.

</td></tr><tr><td>

Show legend value

</td><td>

Option to display the value corresponding to the area of the chart you hover on. The value displays as a tooltip and in the chart legend.

</td></tr><tr><td>

Legend position

</td><td>

Legend location relative to the chart: Above, Below, Right, or Left

</td></tr><tr><td>

Horizontal alignment

</td><td>

Horizontal alignment of elements in the legend: Start, Center, or End

</td></tr><tr><td>

Max legend item width, px

</td><td>

Number of pixels after which the item in the legend is truncated.

</td></tr><tr><td>

Expand legend vertically

</td><td>

When turned on, the legend contents take as much space as needed to fit the legend without scrolling, instead of the maximum 2 lines.

</td></tr><tr><td class="sub-head" colspan="2">

Data label

</td></tr><tr><td>

Show data labels

</td><td>

Option to display the score for each data point.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr><td>

Set color type

</td><td>

Type of color scheme to apply to the component. Options include:

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see Working with themes in Next Experience.
-   Color palette: List of color palettes to select from predefined system palettes in the Chart Color Scheme \[pa\_chart\_color\_schemes\] table. For grouped or stacked data, the colors apply in order from highest value to lowest. For multiple data sources, palette colors apply in the order of data sources. For example, the first color of a palette applies to the first data source, and the second palette color applies to the second source. All visualizations that use the same color palette show the same colors, regardless of what data they display.
-   Fixed element color: Use a specific color from the Chart Colors table \[sys\_report\_chart\_color\] for each element. All data visualizations that use fixed element colors show the same element, such as critical incidents in the Global scope, in the same color.

This option is available only for Table data sources and only if no more than one data source or metric is added, and a Group by is defined.

 **Note:** Single color is only available when no **Group by** is selected.

</td></tr></tbody>
</table>7.  Under **Chart interaction**, set what if anything happens when a viewer clicks a chart or a chart segment on the visualization.

<table id="table_qnp_d2d_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow chart interaction

</td><td>

Enable an event to occur when a user clicks in a visualization or one of its segments.

</td></tr><tr><td>

Action

</td><td>

Choose the event that occurs when a user clicks in a visualization or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** is on. For more information, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

-   **Go to data view** opens a list view, KPI Details page, or Usage Insights overview page relevant to the associated segment or visualization. For table data, a system property determines whether a Core UI list or a Platform Analytics list opens. For more information, see [Data views for different data sources](../../dashboards/reference/visualization-drilldown-in-config-ws.md).
-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Drill down to chart** \(Visualization Designer only\) Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization.

**Note:** The last level of drill down in the Platform Analytics experience is always a Core UI list. Records do not open in Workspace embedded lists.

**Drill down to chart** supports only table data sources.

</td></tr></tbody>
</table>8.  Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the Data Visualization list.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Use cases for different time series visualization types](../reference/time-series-visualization-types.md)**  
Time series visualizations can emphasize the trend in the data or specific changes in the data. They can show one data source or compare several related data sources.
-   **[Table data options for time series data visualizations](../reference/config-dv-time-series-table-data.md)**  
The following Data configuration options are available for all time series type visualizations of table data.
-   **[Indicator data options for time series data visualizations](../reference/config-dv-time-series-ind-data.md)**  
The following Data configuration options are available for all time series type visualizations of indicator scores.
-   **[Usage Insights data options for time series data visualizations](../reference/config-dv-time-series-uxa-data.md)**  
The following Data configuration options are available for all time series type visualizations of Usage Insights data.
-   **[MetricBase data options for time series data visualizations](../reference/config-dv-time-series-mb-data.md)**  
The following data options are available for all time series type visualizations of MetricBase data.
-   **[Display settings for different time series data visualizations](../reference/display-settings-ts-charts.md)**  
Each time series visualization type has a different set of display settings.
-   **[Configure a forecast in a time series data visualization](configure-forecast-ts-viz.md#)**  
If a time series visualization is configured to show forecasts, you can configure the forecasts for that visualization.
-   **[Options for time series data visualizations with multiple metrics](../concept/chart-options-multi-metrics.md)**  
If you are showing multiple metrics in a time series data visualization, you can set the group by, visualization type, and Y-axis scale for each metric. You can also have filters on a dashboard apply only to specific metrics.
-   **[Time series data visualization example](../../par-for-workspace/task/dv-example-line.md)**  
Time series visualizations show the changes in data over time. This example starts with a single indicator data source and adds more complexity.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

