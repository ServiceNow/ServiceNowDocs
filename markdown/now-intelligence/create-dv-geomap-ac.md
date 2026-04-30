---
title: Create a geomap visualization in the Visualization Designer
description: A geomap visualization shows the geographical distribution of data for a world, country, region, or province/state. Use Geomaps use table data that contains location information.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Create geomap report, Create geomap visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a geomap visualization in the Visualization Designer

A geomap visualization shows the geographical distribution of data for a world, country, region, or province/state. Use Geomaps use table data that contains location information.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Geomap visualization in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/next-experience/vancouver/shared-components/now-vis-geomap-wrapper/usage). This site gives information about Geomap data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the Geomap visualization type.

4.  Choose a table data source.

    For general descriptions of the data sources, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

    1.  Configure the map settings.

    2.  Enable drill-down to enable or disable map navigation between levels and list redirection.

5.  Configure the **Header and border**. Header and border options are the same for all data sources.

    |Header and border fields|Description|
    |------------------------|-----------|
    |Show header|The visualization header, including title and icons.|
    |Show header separator|Option to display a line separating the header from the rest of the component.|
    |Chart title|Title of the visualization.|
    |Description|A short overview about the visualization that the end user sees.|
    |Wrap title|Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.|
    |Show border|Option to display a line around the component.|
    |Bare|Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.|

6.  Set the options for your data source.

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

Legend location in relation to the chart. Options include:-   Above
-   Below
-   Right
-   Left


</td></tr><tr><td>

Set color type

</td><td>

Type of color scheme to apply to the component. The choices are:

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
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

Enable an event to occur when a user clicks in a chart or one of its segments.

</td></tr><tr><td>

Action

</td><td>

Only the **Go to data view** interaction is available for geomaps. This action opens the underlying records view.

</td></tr></tbody>
</table>9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for Geomap visualizations](../reference/config-dv-geomap-table-data.md)**  
When you select a table data source for a Geomap visualization, the following Data configuration options are available.
-   **[Map sources for geomap data visualizations](../concept/geomap-map-source.md#)**  
Geomap data visualizations are connected to location tables in a special map source.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

