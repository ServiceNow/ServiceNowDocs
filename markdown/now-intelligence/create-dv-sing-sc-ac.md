---
title: Create a single score data visualization in the Visualization Designer or on a dashboard
description: Use a single score to show a value as a number or percentage. Visualize how the value compares to a target or benchmark, to track progress, or to identify areas for improvement.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
keywords: [Create single score report, Create single score visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a single score data visualization in the Visualization Designer or on a dashboard

Use a single score to show a value as a number or percentage. Visualize how the value compares to a target or benchmark, to track progress, or to identify areas for improvement.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of a Single Score visualization in a dashboard, see [the Developer Site.](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/now-vis-score-wrapper/usage) This site gives information about Single score data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the Single score \(![Data visualization single score icon](../image/inline-data-vis-single-score.png)\) visualization type.

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
6.  Select the options for your data source.

    -   If your visualization represents table data, go to [Table data options for single score visualizations](../reference/config-dv-sing-sc-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for single score visualizations](../reference/config-dv-sing-sc-ind-data.md).
    -   If your visualization represents User Experience Analytics data, go to [User Experience Analytics data options for Single scores](../reference/config-dv-sing-sc-uxa-data.md).
7.  Under **Presentation**, provide display and color information..

<table id="table_jkm_pcm_t5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Score size

</td><td>

Sets the size of the score. Options include: -   XS `xs`
-   S `sm`
-   M `md`
-   L `lg`
-   XL `xl`
-   XXL `xxl`
-   Auto `auto`: Size adjusts automatically between the preceding sizes depending on the viewport size and the space available after all details have been added in the **Additional settings**.


</td></tr><tr><td>

Score icon

</td><td>

Select one of the icons provided with the design system to precede the score. Optional.

**Note:** See [https://developer.servicenow.com/dev.do\#!/reference/next-experience/xanadu/now-components/now-icon/gallery](https://developer.servicenow.com/dev.do#!/reference/next-experience/xanadu/now-components/now-icon/gallery) for more information.

</td></tr><tr><td>

Icon style

</td><td>

Select "With background" to apply color to the background of the icon. Select "No background" to apply color to the icon itself.

</td></tr><tr><td>

Metric label position

</td><td>

Position for the metric label. Options include:-   Above score `top`
-   Below score `bottom`
 This property applies only with table data sources and when **Show metric label** is true.

</td></tr><tr><td>

Sparkline style

</td><td>

Style of sparkline chart. Options include:-   Area `area`: Option to display the sparkline as a line with the area between its points and the horizontal axis colored in.
-   Line `line`: Option to display the sparkline as a line.
 This property applies only with indicator data sources and when **Show sparkline** is true.

</td></tr><tr class="sub-head"><td colspan="2">

Colors

</td></tr><tr><td>

Set color type

</td><td>

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
-   Single color/Colors per metric: Select a single color in the **Set value color** field. Interacting with that field opens a selector where you can choose the color from either a set of icons or from a list. You can also search for a color. Entering a search value has the selector show you a list of colors filtered by that search value.

Alternatively, you can add a rule to define a dynamic color. For more information, see [Create coloring rules for data visualizations](../../performance-analytics/concept/colors-dv.md#).

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
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

-   **[Table data options for single score visualizations](../reference/config-dv-sing-sc-table-data.md)**  
When you select a table data source for a single score visualization, the following Data configuration options are available.
-   **[Indicator data options for single score visualizations](../reference/config-dv-sing-sc-ind-data.md)**  
When you select an indicator data source for a single score visualization, the following Data configuration options are available.
-   **[User Experience Analytics data options for Single scores](../reference/config-dv-sing-sc-uxa-data.md)**  
When you select a User Experience Analytics data source for a single score visualization, the following Data configuration options are available.
-   **[Single score visualization example](../../par-for-workspace/task/dv-example-single-score.md)**  
Use a single score visualization when you want to show a single value or metric, such as overall revenue or number of open incidents. The basic score visualizes a single value with a descriptive heading and date/time stamp.

**Parent Topic:**[Creating data visualizations](../concept/creating-data-visualizations.md)

