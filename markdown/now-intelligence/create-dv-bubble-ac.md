---
title: Create a bubble visualization in the Visualization Designer
description: Use a bubble visualization to show multiple separate metrics on a single chart. Use bubble charts to answer binary questions, such as whether two fields have a relationship, and to highlight patterns.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [Create bubble report, Create bubble visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a bubble visualization in the Visualization Designer

Use a bubble visualization to show multiple separate metrics on a single chart. Use bubble charts to answer binary questions, such as whether two fields have a relationship, and to highlight patterns.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Bubble visualization in a dashboard, see [the Developer Site.](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-bubble-wrapper/usage) This site gives information about Bubble data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

Bubble visualizations aggregate information over three different metrics, using the X axis, Y axis, and bubble size.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the Bubble \(![bubble chart icon](../image/inline-data-vis-bubble.png)\) visualization type.

4.  Configure the **Header and border**. Header and border options are the same for all data sources.

    |Header and border fields|Description|
    |------------------------|-----------|
    |Show header|The visualization header, including title and icons.|
    |Show header separator|Option to display a line separating the header from the rest of the component.|
    |Chart title|Title of the visualization.|
    |Description|A short overview about the visualization that the end user sees.|
    |Wrap title|Option to wrap long titles onto a second line. If false, displays an ellipsis to truncate long titles.|
    |Wrap labels|Select to wrap long elements labels on the axis.|
    |Max label size, px|Specify the maximum label size for element names on the axis. Default=100 px.|
    |Truncation type|Specify where to truncate long labels with an ellipsis. Options are Beginning, Middle, and End.|
    |Show border|Option to display a line around the component.|
    |Bare|Option to remove padding around data visualization to provide more compact positioning on the page. Only available when **Show border** is turned off.|

5.  Choose a data source.

    For general descriptions of the data sources, see [Data sources for data visualizations](../../par-for-workspace/reference/data-sources-visualizations.md).

    You can choose one or more tables \(available in the base system\). When you select a table, you can filter it by conditions.

    **Note:** You can choose to define a data source manually in JSON. However, this method is intended only for experts.

6.  Select the options for your data source.

    Go to [Table data options for bubble visualizations](../reference/config-dv-bubble-table-data.md).

7.  Under **Presentation**, provide display and color information. In the **Colors** section, configure the colors and color rules.

<table id="table_b5f_w23_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show data table

</td><td>

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td>

Show legend

</td><td>

Available when you configure a group by or have more than one metric. Select to display the legend.

</td></tr><tr><td>

Legend position

</td><td>

Legend location relative to the chart: Above, Below, Right, or Left.

</td></tr><tr><td>

Set color type

</td><td>

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
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

Enable an event to occur when a user clicks in a chart or one of its segments.

</td></tr><tr><td>

Action

</td><td>

Choose the event that occurs when a user clicks in a chart or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** is on. For more information, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

-   **Go to data view** opens the records view in a Core UI list or KPI Details relevant to the associated segment or visualization. Records do not open in Workspace embedded lists.

Not supported for User Experience Analytics data sources.

-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Drill down to chart** \(Visualization Designer only\) Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization.

**Note:** The last level of drill down in the Platform Analytics experience is always a Core UI list. Records do not open in Workspace embedded lists.

**Drill down to chart** supports only table data sources.

</td></tr></tbody>
</table>9.  Select **Save** to continue editing the visualization, or **Save and close** to return to the Analytics Center main screen.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   Select the More actions menu icon \(![More actions menu icon](../../dashboards/image/icon-vert-3dot-p.png)\) to duplicate, share, export, schedule, or bookmark the visualization.

-   **[Table data options for bubble visualizations](../reference/config-dv-bubble-table-data.md)**  
When you select a table data source for a bubble visualization, the following Data configuration options are available.
-   **[Bubble visualization example](../../par-for-workspace/task/dv-example-bubble.md)**  
The bubble data visualization is used to do compare fields and see their relationships.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

