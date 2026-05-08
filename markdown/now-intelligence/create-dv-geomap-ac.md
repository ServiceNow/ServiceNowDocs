---
title: Create a geomap data visualization
description: A geomap visualization shows the geographical distribution of data for a world, country, region, or province/state. Use Geomaps use table data that contains location information.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Create geomap report, Create geomap visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a geomap data visualization

A geomap visualization shows the geographical distribution of data for a world, country, region, or province/state. Use Geomaps use table data that contains location information.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Geomap visualization in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/shared-components/now-vis-geomap-wrapper/usage). This site gives information about Geomap data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the Geomap visualization type.

4.  Choose a table data source.

    For general descriptions of the data sources, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

    1.  Configure the map settings.

    2.  Enable drill-down to enable or disable map navigation between levels and list redirection.

5.  Configure the **Header and border**. Header and border options are the same for all data sources.

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

</td></tr><tr><td>

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

</td></tr><tr><td>

Line of truncation

</td><td>

Specify where to truncate long labels with an ellipsis. Options are 1, 2, and 3.

</td></tr><tr id="ac-dv-showborder"><td>

Show border

</td><td>

Option to display a line around the component.

</td></tr><tr id="ac-dv-bare"><td>

Bare

</td><td>

Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.

</td></tr><tr id="ac-dv-show-refresh"><td>

Show refresh option

</td><td>

Option to show or hide the refresh option from data visualizations. If cache is enabled on a dashboard, the Refresh option is always hidden.

</td></tr></tbody>
</table>6.  Set the options for your data source.

    Go to [Table data options for Geomap visualizations](../reference/config-dv-geomap-table-data.md).

7.  Under **Presentation**, provide display and color information.

<table id="table_czj_b1d_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show data table

</td><td>

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td>

Show % of total in tooltip

</td><td>

Enable to show the percentage each data point contributes to the total alongside absolute values in the tooltip.

</td></tr><tr id="ac-dv-sortby"><td>

Map

</td><td>

Map to plot the data, such as the world map or the map of a country.

</td></tr><tr id="ac-dv-sortbyorder"><td>

Show data label

</td><td>

Enables the data labels.

</td></tr><tr><td>

Legend

</td><td>

Displays the legend.

</td></tr><tr><td>

Legend position

</td><td>

Legend location in relation to the visualization. Options include:-   Above
-   Below
-   Right
-   Left


</td></tr><tr><td>

Set color type

</td><td>

Type of color scheme to apply to the component. The choices are:

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see Working with themes in Next Experience.
-   Color range: A spectrum of colors between a color for the lowest value and a color for the highest value. You can select these colors from a set of icons, from a list of colors including their icons, or by searching for the color name or hexadecimal value. The colors are taken from the Color Definition \[sys\_report\_color\] table.


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

Only the **Go to data view** interaction is available for geomaps. This action opens the underlying records view.

</td></tr></tbody>
</table>9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Overview main screen.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for Geomap visualizations](../reference/config-dv-geomap-table-data.md)**  
When you select a table data source for a Geomap visualization, the following Data configuration options are available.
-   **[Map sources for geomap data visualizations](../concept/geomap-map-source.md#)**  
Geomap data visualizations are connected to location tables in a special map source.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

