---
title: Create a gauge data visualization in the Visualization Designer
description: A gauge visualization shows where a value lies between expected minimum and maximum values. Use the gauge visualization to follow progress with color-coded value ranges.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Create gauge report, Create gauge visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a gauge data visualization in the Visualization Designer

A gauge visualization shows where a value lies between expected minimum and maximum values. Use the gauge visualization to follow progress with color-coded value ranges.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Gauge visualization in a dashboard, see [the Developer Site.](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-gauge-wrapper/usage) This site gives information about Gauge data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

**Note:** Workflow Data Fabric sources do not support real-time update on single score, dial, and gauge visualizations.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the Gauge \(![dial gauge icon](../image/icon-dial-gauge-ac.png)\) visualization type.

4.  Configure the **Header and border**. Header and border options are the same for all data sources.

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
</table>5.  Choose a data source.

    For general descriptions of the data sources, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

    -   Table \(available in the base system\). When you select a table, you can filter it by custom or preconfigured conditions. Custom conditions can include questions or Service Catalog variables.

        Configured report sources appear in the **Predefined conditions** list. For more information, see [Report sources](../concept/c_ReportSources.md#).

        To help you create a custom filter, there is a preview list of records that would be included in the visualization. You can change which fields are shown as columns and the width of columns in the list actions.

        ![Preview record list for table source data visualization with list actions shown.](../../par-for-workspace/image/dv-preview-edit-cols.png)

    -   Indicator \(available in the base system\). You can filter the indicator scores by breakdowns and elements. Automated indicators can be configured with selected breakdowns. Formula indicators inherit their breakdowns from the parent indicators. Data snapshots indicator breakdowns are configured in the indicator. In both cases, only those breakdowns are available when you configure a visualization based on those indicators.

        **Note:** Benchmark indicators are not supported.

        ![Conditional filter for indicator data source on data visualization.](../../performance-analytics/image/dv-ind-source-con-filter.png)

        **Note:**

        You might have a multiple select \(is one of\) or dynamic \(is \(dynamic\)\) operator on the breakdown element filter. These operators require the indicator and breakdown to support them. For more information about the configurations that support these operators, see ["Is one of" and "Is \(Dynamic\)" operators on breakdown conditions in data visualizations](../../performance-analytics/concept/condition-operators-ind-bkdowns.md#section_breakdown-operators).

        Indicator types include Automated, Formula, and Manual indicators as well as Automated and Formula Data Snapshots. The Indicator Preview shows an example of the visualization and a list of the indicator's properties.

        ![Indicator preview example with visualization example and list of properties including source type, indicator source, indicator type, additional conditions and available breakdowns.](../image/dv-indicator-source-preview.png)

    -   Usage Insights \(available with the User Experience PAR Integration application, to users with a required role\). Choose one of up to three KPIs included with this application, depending on the visualization type. For more information, see [Usage Insights data sources for data visualizations](../../performance-analytics/concept/uxa-data-sources.md).
6.  Select the options for your data source.

    -   If your visualization represents table data, go to [Table data options for gauge data visualizations](../reference/config-dv-gauge-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for gauge data visualizations](../reference/config-dv-gauge-ind-data.md).
    -   If your visualization represents Usage Insights data, go to [Usage Insights data options for gauge visualizations](../reference/config-dv-gauge-uxa-data.md).
7.  Under **Presentation**, provide display and color information.

<table id="table_gvk_2mr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Gauge arc angle

</td><td>

Choice of sizes for the gauge, in degrees.

</td></tr><tr><td>

Value label size

</td><td>

Characters that represent dynamic sizes: small \(S\), medium \(M\), or large \(L\). The actual size of the type changes in proportion to the size of the chart.

</td></tr><tr><td>

Inner radius

</td><td>

Specify the ratio of the visualization's inner radius to the outer. Allowed values are 0.7–0.95.

</td></tr><tr><td>

Show data table

</td><td>

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td class="sub-head" colspan="2">

Range

</td></tr><tr><td>

Min value

</td><td>

Set the lowest value shown on the visualization. If not specified, zero is the default.

</td></tr><tr><td>

Max value

</td><td>

Set the highest value shown on the visualization.

</td></tr><tr><td>

Configure ranges

</td><td>

Specify the number of ranges to divide the gauge into; default 3. You select the number of ranges, the start and end values of each range, the labels, and the color spectrum.

</td></tr><tr><td class="sub-head" colspan="2">

**Legend**

</td></tr><tr><td>

Show legend

</td><td>

Option to display the legend. Activated automatically at 400% zoom.

</td></tr><tr><td>

Legend position

</td><td>

Legend location relative to the chart: Above, Below, Right, or Left

</td></tr><tr><td>

Legend orientation

</td><td>

Options for how to display the register.-   Horizontal `horizontal`: Option to display the legend horizontally.
-   Vertical `vertical`: Option to display the legend vertically up to five lines.
 This property applies only when **Legend position** is Below.

</td></tr><tr><td>

Horizontal alignment

</td><td>

Horizontal alignment of elements in the legend: Start, Center, or End

</td></tr><tr><td>

Max legend item width, px

</td><td>

Number of pixels after which the item in the legend is truncated.

</td></tr><tr><td class="sub-head" colspan="2">

Labels

</td></tr><tr><td>

Score label \[scoreLabel\]

</td><td>

The label of the score in the center of the gauge:

-   No label \(None\)
-   The same label as the visualization metric \(Metric label\)
-   The label that you set for the range that the score falls into, in Configure ranges \(Range label\)
 Labels are disabled and replaced by legends at 400% zoom.

</td></tr><tr><td>

Show range limit \[showRangeLimit\]

</td><td>

When true, the limits that you configured for the ranges are shown. If you did not configure any ranges, the default min and max values are shown.

</td></tr><tr><td>

Show range labels \[showRangeLabels\]

</td><td>

When true, any labels you configured for ranges are shown. This property is available only if you configured ranges and specified labels for them.

</td></tr><tr><td>

Show label as primary

</td><td>

Available when the score label is configured as Range label. Changes the places of the score value and label to make the score value small and emphasize the range value.

</td></tr></tbody>
</table>8.  Under **Chart interaction**, set what if anything happens when a viewer clicks a chart or a chart segment on the visualization.

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

Choose the event that occurs when a user clicks in a chart or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** \[chartInteractionEnabled\] is true. -   **Go to data view** opens the records view in a Core UI list or KPI Details relevant to the associated segment or visualization. Records do not open in Workspace embedded lists.

Usage Insights data sources redirect to the appropriate user, sessions, page, event pages that are based on corresponding usage data.

-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.


</td></tr></tbody>
</table>9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for gauge data visualizations](../reference/config-dv-gauge-table-data.md)**  
When you select a table data source for a gauge visualization, the following Data configuration options are available.
-   **[Indicator data options for gauge data visualizations](../reference/config-dv-gauge-ind-data.md)**  
When you select an indicator data source for a gauge visualization, the following Data configuration options are available.
-   **[Usage Insights data options for gauge visualizations](../reference/config-dv-gauge-uxa-data.md)**  
When you select a Usage Insights data source for a gauge visualization, the following Data configuration options are available.
-   **[Gauge visualization example](../../par-for-workspace/task/dv-example-gauge.md)**  
Like dials, gauges show where a single value lies across a range from minimum to maximum expected values. In addition to dial functionality, you can set colored data ranges to help users understand what the value represents.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

