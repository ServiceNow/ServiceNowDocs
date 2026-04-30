---
title: Create a horizontal or vertical bar data visualization
description: Use bar visualizations to show information in segments that are proportional to the values they represent. Vertical bar and horizontal bar visualizations compare numeric values that represent either nominal or ordinal data.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-04"
reading_time_minutes: 11
keywords: [Create horizontal bar report, Create horizontal bar visualization, Create vertical bar report, Create vertical bar visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a horizontal or vertical bar data visualization

Use bar visualizations to show information in segments that are proportional to the values they represent. Vertical bar and horizontal bar visualizations compare numeric values that represent either nominal or ordinal data.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

For more information about this visualization type, see [Bar Visualization Overview](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-bar-wrapper/overview) on the ServiceNow Developer Site. This site gives information about Horizontal and Vertical bar data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## About this task

In general, use horizontal bars to graph nominal data, such as the number of users in each assignment group. Use vertical bars to graph ordinal data, such as the number of open incidents in different age buckets. For information about the use of a Bar visualization in a dashboard, see [the Developer Site.](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-bar-wrapper/usage)

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the horizontal bar \(![horizontal bar icon](../image/inline-data-vis-bar-horizontal.png)\) or vertical bar \(![vertical bar icon](../image/inline-data-vis-bar-vertical.png)\) visualization type.

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

    -   If your visualization represents table data, go to [Table data options for horizontal and vertical bar visualizations](../reference/config-dv-bar-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for horizontal and vertical bar visualizations](../reference/config-dv-bar-ind-data.md).
    -   If your visualization represents User Experience Analytics data, go to [User Experience Analytics data options for bar visualizations](../reference/config-dv-bar-uxa-data.md).
7.  Under **Presentation**, provide display and color information.

    **Note:** For horizontal bar visualizations, the X axis is the primary. For vertical bar visualizations, the Y axis is primary.

<table id="table_gvk_2mr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Show only one data point in tooltip

</td><td>

When turned on, the tooltip shows only the data point being hovered over. When turned off, the tooltip shows all data points.

Default: Off, except when zoom is 400%, which automatically turns it on.

</td></tr><tr><td>

Show data table

</td><td>

Shows a table with chart and graph data for easier screen reader access. Data includes the percentage of the total for each value, when appropriate.

</td></tr><tr><td class="sub-head" colspan="2">

X and Y axis \(Some options are only available on the primary or secondary axis. On horizontal bar visualizations, the X axis is primary. On vertical bar visualizations, the Y axis is primary.\)

</td></tr><tr><td>

Hide axis

</td><td>

Option to hide the primary axis.

</td></tr><tr><td>

Axis title

</td><td>

Title to display on the X or Y axis.

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


</td></tr><tr><td>

Wrap labels

</td><td>

Wrap long labels in the secondary axis.

</td></tr><tr><td>

Max label size, px.

</td><td>

The length in pixels at which the label of the secondary axis is wrapped or truncated.

</td></tr><tr><td>

Truncation type

</td><td>

Determines where to truncate long labels for the secondary axis. Options include:-   Start `start`
-   Middle `middle`
-   End `end`


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

Type of color scheme to apply to the component. Options include: -   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
-   Color palette: List of color palettes to select from predefined system palettes in the Chart Color Scheme \[pa\_chart\_color\_schemes\] table. For grouped or stacked data, the colors apply in order from highest value to lowest. For multiple data sources, palette colors apply in the order of data sources. For example, the first color of a palette applies to the first data source, and the second palette color applies to the second source. All visualizations that use the same color palette show the same colors, regardless of what data they display.
-   Single color/Colors per metric: Select a single color in the **Set value color** field. Interacting with that field opens a selector where you can choose the color from either a set of icons or from a list. You can also search for a color. Entering a search value has the selector show you a list of colors filtered by that search value.

If the visualization has more than one metric, you see the Colors per metric option instead. This option lets you select a single color for each metric.

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

Enable an event to occur when a user clicks in a chart or one of its segments.

</td></tr><tr><td>

Action

</td><td>

Choose the event that occurs when a user clicks in a chart or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** is on. For more information, see [Chart interactions in a data visualization](../../par-for-workspace/concept/dv-chart-interactions.md).

-   **Go to data view** opens the records view in a Core UI list or KPI Details relevant to the associated segment or visualization. Records do not open in Workspace embedded lists.

Not supported for User Experience Analytics data sources.

-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Apply as filter** filters all data visualizations on the dashboard by the value of the selected segment, where applicable.

**Note:** **Apply as filter** is available only for table and indicator data sources. It does not work when the Group by field is a duration field.

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

-   **[Table data options for horizontal and vertical bar visualizations](../reference/config-dv-bar-table-data.md)**  
When you select a table data source for a horizontal or vertical bar visualization, the following Data configuration options are available.
-   **[Indicator data options for horizontal and vertical bar visualizations](../reference/config-dv-bar-ind-data.md)**  
When you select an indicator data source for a horizontal or vertical bar visualization, the following Data configuration options are available.
-   **[User Experience Analytics data options for bar visualizations](../reference/config-dv-bar-uxa-data.md)**  
When you select a User Experience Analytics data source for a horizontal or vertical bar visualization, the following Data configuration options are available.
-   **[Following filters per metric](../concept/chart-options-bars-multi-metrics.md)**  
If you are showing multiple metrics in a horizontal or vertical bar visualization, you can have filters on a dashboard apply only to specific metrics.
-   **[Bar visualization examples](../../par-for-workspace/task/dv-example-bar.md)**  
Bar visualizations enable you to show the comparative size or frequency of different categories or groups, for example, sales in different regions or over different periods of time.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

