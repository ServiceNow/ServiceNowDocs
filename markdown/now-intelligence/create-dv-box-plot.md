---
title: Create a box plot data visualization
description: Use a boxplot to show the median and lower and upper quartiles of numeric data along with outliers. You can also compare the distribution of different groups of this data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [create boxplot visualization, create box report]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a box plot data visualization

Use a boxplot to show the median and lower and upper quartiles of numeric data along with outliers. You can also compare the distribution of different groups of this data.

## Before you begin

**Important:** The Boxplot visualization is included in the latest data visualizations application from the ServiceNow® Store.

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

The Boxplot visualization only supports table data. Indicator, MetricBase, and Usage Insights data is not supported.

For information about the use of a Boxplot visualization in a dashboard, see [the Developer Site.](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-boxplot/usage) This site gives information about Box plot components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the Boxplot \(![vertical box icon](../image/inline-data-vis-box.png)\) visualization type.

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
</table>5.  Open the Data Source selector and select a table.

6.  Configure the data settings as described in [Table data options for boxplot visualizations](../reference/config-dv-box-table-data.md).

7.  Under **Presentation**, provide display and color information..

<table id="table_jkm_pcm_t5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display settings

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

Axis position

</td><td>

Position of the primary axis. Options include:-   Left
-   Right
 This property applies only when **Hide axis** is false. If there is more than one primary axis, such as multiple Y axes on a vertical bar visualization, you can set each axis position separately.

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

Wrap labels

</td><td>

Select to wrap long elements labels on the axis.

</td></tr><tr><td>

Max label size, px

</td><td>

Specify the maximum label size for element names on the axis. Default=100 px.

</td></tr><tr class="sub-head"><td colspan="2">

Colors

</td></tr><tr><td>

Set color type

</td><td>

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see Working with themes in Next Experience.
-   Single color/Colors per metric: Select a single color in the **Set value color** field. Interacting with that field opens a selector where you can choose the color from either a set of icons or from a list. You can also search for a color. Entering a search value has the selector show you a list of colors filtered by that search value.


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

Choose the event that occurs when a user clicks in a visualization or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** is on. For more information, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

-   **Go to data view** opens a list view, KPI Details page, or Usage Insights overview page relevant to the associated segment or visualization. For table data, a system property determines whether a Core UI list or a Platform Analytics list opens. For more information, see [Data views for different data sources](../../dashboards/reference/visualization-drilldown-in-config-ws.md).
-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Drill down to chart** \(Visualization Designer only\) Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization.

**Note:** The last level of drill down in the Platform Analytics experience is always a Core UI list. Records do not open in Workspace embedded lists.

**Drill down to chart** supports only table data sources.

</td></tr></tbody>
</table>9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for boxplot visualizations](../reference/config-dv-box-table-data.md)**  
When you select a table data source for a boxplot visualization, the following Data configuration options are available.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

