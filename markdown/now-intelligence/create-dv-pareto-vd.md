---
title: Create a Pareto bar data visualization
description: Use a Pareto bar visualization to Identify the most important dimension in a large set of dimensions. Pareto bar visualization columns show data in descending order. A line shows the cumulative percentage.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-04"
reading_time_minutes: 10
keywords: [Create pareto bar report, Create pareto bar visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a Pareto bar data visualization

Use a Pareto bar visualization to Identify the most important dimension in a large set of dimensions. Pareto bar visualization columns show data in descending order. A line shows the cumulative percentage.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Pareto bar visualization in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-vis-bar-wrapper/usage). This site gives information about Pareto bar data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the Pareto bar visualization \(![pareto bar icon](../image/inline-data-vis-pareto.png)\) visualization type.

4.  Configure the **Header and border**. Header and border options are the same for all data sources.

<table id="table_ly5_djk_c5b"><thead><tr><th>

Header and border fields

</th><th>

Description

</th></tr></thead><tbody><tr id="ac-dv-showheader"><td>

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

Truncation type

</td><td>

Specify where to truncate long labels with an ellipsis. Options are Beginning, Middle, and End.

</td></tr><tr id="ac-dv-showborder"><td>

Show border

</td><td>

Option to display a line around the component.

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

    -   Indicator \(available in the base system\). You can filter the indicator scores by breakdowns and elements.

        **Note:** Benchmark indicators are not supported.

        ![Conditional filter for indicator data source on data visualization.](../../performance-analytics/image/dv-ind-source-con-filter.png)

        **Note:**

        You might have a multiple select \(is one of\) or dynamic \(is \(dynamic\)\) operator on the breakdown element filter. These operators require the indicator and breakdown to support them. For more information about the configurations that support these operators, see ["Is one of" and "Is \(Dynamic\)" operators on breakdown conditions in data visualizations](../../performance-analytics/concept/condition-operators-ind-bkdowns.md#section_breakdown-operators).

    -   User Experience Analytics \(available with the User Experience PAR Integration application, to users with a required role\). Choose one of up to three KPIs included with this application, depending on the visualization type. For more information, see [User Experience Analytics data sources for data visualizations](../../performance-analytics/concept/uxa-data-sources.md).
    **Note:** You can choose multiple data sources for this visualization. However, all data sources must be of the same type: table, indicator, or User Experience Analytics. For more information, see [Multiple data sources](../../par-for-workspace/reference/multiple-data-sources.md#).

6.  Select the options for your data source.

    -   If your visualization represents table data, go to [Table data options for Pareto bar visualizations](../reference/config-dv-pareto-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for pareto bar visualizations](../reference/config-dv-pareto-ind-data.md).
    -   If your visualization represents User Experience Analytics data, go to [User Experience Analytics for Pareto bar visualizations](../reference/config-dv-pareto-uxa-data.md).
7.  Under **Presentation**, provide display and color information.

    Under **Display settings**, you can show the data table. This table shows graph and visualization data for easier screen reader access. You can also select whether hovering on a data value opens a tooltip with all the data values or only the details of the selected data value.

<table id="table_s1z_jyz_bzb"><thead><tr><th>

Field \[Property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide axis

</td><td>

Hides both the bar metric Y-axis and the pareto Y-axis.

</td></tr><tr><td>

Axis style

</td><td>

Style of the X axis.-   Clean `clean`: Adds a straight line to the X axis.
-   No tick lines `noTicks`: Option to remove all marks from the X axis.
-   Standard `default`: Adds a line and tick marks to the X axis.
**Note:** Only available when **Show grid** is true for vertical bar visualizations.

</td></tr><tr><td>

Axis title \(for X axis\)

</td><td id="entry_x-axis-title">

Title to display on the horizontal axis of the visualization.

</td></tr><tr><td>

Wrap labels

</td><td>

Wraps long labels in the horizontal axis.

</td></tr><tr><td>

Max label size, px

</td><td>

Maximum label size for the horizontal axis, in pixels.

</td></tr></tbody>
</table><table id="table_yj3_p4t_zbc"><thead><tr><th>

Field \[Property\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide axis

</td><td>

Hides both the bar metric Y-axis and the pareto Y-axis.

</td></tr><tr><td>

Axis title \(for Y axis\)

</td><td>

Only affects the bar axis and not the Pareto axis.

</td></tr><tr><td>

Show grid

</td><td>

Adds grid lines to the visualization. This option applies only to the Y axis.

</td></tr><tr><td>

Axis style

</td><td>

Style of the Y axis.-   Clean `clean`: Adds a straight line to the Y axis.
-   No tick lines `noTicks`: Option to remove all marks from the Y axis.
-   Standard `default`: Adds a line and tick marks to the Y axis.
**Note:** Only available when **Show grid** is true for vertical bar visualizations.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Show legend|Option to display the legend.|
    |Legend position|Legend location relative to the visualization: Above, Below, Right, or Left|

<table id="table_ktl_jq1_czb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show data labels

</td><td>

Option to display the score for each data point.

</td></tr><tr><td>

Data label position

</td><td>

Location of data labels: at the top, middle, or bottom of the bars.**Note:** Only available when **Show data labels** is true.

</td></tr></tbody>
</table><table id="table_colors"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Set color type

</td><td>

Type of color scheme to apply to the component. Options include:

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   Color palette: List of color palettes to select from predefined system palettes in the Chart Color Scheme \[pa\_chart\_color\_schemes\] table. For grouped or stacked data, the colors apply in order from highest value to lowest. For multiple data sources, palette colors apply in the order of data sources. For example, the first color of a palette applies to the first data source, and the second palette color applies to the second source. All visualizations that use the same color palette show the same colors, regardless of what data they display.
-   Fixed element color: Use a specific color from the Chart Colors table \[sys\_report\_chart\_color\] for each element. All data visualizations that use fixed element colors show the same element, such as critical incidents in the Global scope, in the same color.

This option is available only for Table data sources and only if no more than one data source or metric is added, and a Group by is defined.

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

-   **Go to data view** opens a list view, KPI Details page, or User Experience Analytics overview page relevant to the associated segment or visualization. For table data, a system property determines whether a Core UI list or a Platform Analytics list opens. For more information, see [Data views for different data sources](../../dashboards/reference/visualization-drilldown-in-config-ws.md).
-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Drill down to chart** \(Visualization Designer only\) Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization.

**Note:** The last level of drill down in the Platform Analytics experience is always a Core UI list. Records do not open in Workspace embedded lists.

**Drill down to chart** supports only table data sources.

</td></tr></tbody>
</table>9.  Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the Data Visualization list.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for Pareto bar visualizations](../reference/config-dv-pareto-table-data.md)**  
When you select a table data source for a Pareto bar visualization, the following Data configuration options are available.
-   **[Indicator data options for pareto bar visualizations](../reference/config-dv-pareto-ind-data.md)**  
When you select an indicator data source for a Pareto bar visualization, the following Data configuration options are available.
-   **[User Experience Analytics for Pareto bar visualizations](../reference/config-dv-pareto-uxa-data.md)**  
When you select a User Experience Analytics data source for a Pareto bar visualization the following Data configuration options are available.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

