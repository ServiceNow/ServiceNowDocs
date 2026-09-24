---
title: Create a pivot table data visualization in the Visualization Designer
description: Create a pivot table visualization to summarize large data sets by breaking them down by multiple dimensions in a single table. Cells show each row and column value combination and can also show subtotals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/create-dv-pivot-ac.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 12
keywords: [Create pivot table report, Create pivot table visualization]
breadcrumb: [Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Create a pivot table data visualization in the Visualization Designer

Create a pivot table visualization to summarize large data sets by breaking them down by multiple dimensions in a single table. Cells show each row and column value combination and can also show subtotals.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/report-view-access-control.md) and [Platform Analytics roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/platform-analytics-roles.md).

## About this task

For information about the use of a Pivot visualization in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/now-components/sn-multipivot/usage). This site gives information about Pivot data visualization components in the UI Builder, and some configuration options may differ from the Visualization Designer.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

2.  Select **Create data visualization**.

3.  Select the Pivot Table \(\[Omitted image "inline-data-vis-pivot-table.png"\] Alt text: Pivot table icon\) visualization type.

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

Option to show or hide the refresh option from data visualizations. If cache is enabled on a dashboard, the Refresh option is hidden.

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

    For general descriptions of the data sources, see [Data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/data-sources-visualizations.md).

    -   Table \(available in the base system\). When you select a table, you can filter it by custom or preconfigured conditions. Custom conditions can include questions or Service Catalog variables.

        Configured report sources appear in the **Predefined conditions** list. For more information, see [Report sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/c_ReportSources.md).

        To help you create a custom filter, there is a preview list of records that would be included in the visualization. You can change which fields are shown as columns and the width of columns in the list actions.

        \[Omitted image "dv-preview-edit-cols.png"\] Alt text: Preview record list for table source data visualization with list actions shown.

    -   Indicator \(available in the base system\). You can filter the indicator scores by breakdowns and elements. Automated indicators can be configured with selected breakdowns. Formula indicators inherit their breakdowns from the parent indicators. Data snapshots indicator breakdowns are configured in the indicator. In both cases, only those breakdowns are available when you configure a visualization based on those indicators.

        **Note:** Benchmark indicators aren't supported.

        \[Omitted image "dv-ind-source-con-filter.png"\] Alt text: Conditional filter for indicator data source on data visualization.

        **Note:**

        You might have a multiple select \(is one of\) or dynamic \(is \(dynamic\)\) operator on the breakdown element filter. These operators require the indicator and breakdown to support them. For more information about the configurations that support these operators, see ["Is one of" and "Is \(Dynamic\)" operators on breakdown conditions in data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/condition-operators-ind-bkdowns.md).

        Indicator types include Automated, Formula, and Manual indicators as well as Automated and Formula Data Snapshots. The Indicator Preview shows an example of the visualization and a list of the indicator's properties.

        \[Omitted image "dv-indicator-source-preview.png"\] Alt text: Indicator preview example with visualization example and list of properties including source type, indicator source, indicator type, additional conditions and available breakdowns.

    -   Usage Insights \(available with the User Experience PAR Integration application, to users with a required role\). Choose one of up to three KPIs included with this application, depending on the visualization type. For more information, see [Usage Insights data sources for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/uxa-data-sources.md).
    **Note:** You can choose multiple data sources for this visualization. However, all data sources must be of the same type: table, indicator, or Usage Insights. For more information, see [Multiple data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/multiple-data-sources.md).

6.  Duplicate the data source.

    1.  Select the data source's More Actions menu \[Omitted image "more-actions-menu-icon.png"\] and choose **Duplicate**.

        \[Omitted image "dv-duplicate-data-source.png"\] Alt text: Data source's More Actions menu with Duplicate selected

    2.  Select the copy of the data source and edit it.

        For example, if the original data source has multiple conditions, you can duplicate it if you want to add more conditions and not lose the original configuration.

    Both the original data source and duplicated and edited data source apply to the visualization.

7.  Select the options for your data source.

    -   If your visualization represents table data, go to [Table data options for pivot table visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-table-data.md).
    -   If your visualization represents indicator data, go to [Indicator data options for pivot table data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-ind-data.md).
    -   If your visualization represents Usage Insights data, go to [Usage Insights data options for pivot table data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-uxa-data.md).
8.  Under **Presentation**, provide display and color information.

<table id="table_gvk_2mr_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Freeze row header

</td><td>

Allows users to keep the header visible while scrolling to another area in the visualization.

</td></tr><tr><td>

Freeze row footer

</td><td>

Allows users to keep the footer visible while scrolling to another area in the visualization.

</td></tr><tr><td>

Freeze first column

</td><td>

Keeps the first column visible while scrolling.

</td></tr><tr><td>

Show alternative row colors

</td><td>

Toggles a background color for alternative rows to make reading the visualization easier.

</td></tr><tr><td>

Show alternative column colors

</td><td>

Toggles a background color for alternative columns to make reading the visualization easier.

</td></tr><tr><td>

Display row lines

</td><td>

Displays border lines to separate rows.

</td></tr><tr><td>

Display column lines

</td><td>

Displays border lines to separate columns.

</td></tr><tr><td>

Show pivot expanded

</td><td>

Show the fully expanded pivot table. Otherwise only the first level of row grouping is shown.

</td></tr><tr><td class="sub-head" colspan="2">

Table layout settings

</td></tr><tr><td>

Pivot layout

</td><td>

-   **Grouped**

\(Default\) All row dimensions after the first are nested.

-   **Flat**

Shows one row per unique combination of all dimensions from the second row dimension onward. All remaining dimensions are shown as individual flat columns with no nesting or hierarchy.

</td></tr><tr><td class="sub-head" colspan="2">

Table size settings

</td></tr><tr><td>

Truncate first column \[truncateFirstColumn\]

</td><td>

When true, limits the width of the first column. First column contents beyond this width are truncated. First column headers aren't truncated. Specify this width limit in **First Column max width, in px**.

</td></tr><tr><td>

Truncate first column \[truncateFirstColumn\]

</td><td>

When true, limits the width of the first column. First column contents beyond this width are truncated. First column headers aren't truncated. Specify this width limit in **First Column max width, in px**.

</td></tr><tr><td>

First Column max width, in px

</td><td>

The maximum width of the first column, beyond which its contents are truncated. This maximum width can't be less than the width of the first column header, which is never truncated. Values lower than the header width are ignored.Only takes effect when **Truncate first column** is active. Default value is 200px.

</td></tr><tr><td>

Wrap column headers

</td><td>

Breaks header text into lines matching content width, with a minimum limit of 100px. Does not apply to first column.You can't both wrap and truncate column headers.

</td></tr><tr><td>

Truncate column headers

</td><td>

Truncates header text into lines matching content width, with a minimum limit of 100px. Does not apply to first column.You can't both wrap and truncate column headers.

</td></tr><tr><td class="sub-head" colspan="2">

Colors

</td></tr><tr><td>

Set color type

</td><td>

-   Default: A color or set of colors that come from the UX Theme that is applied to the instance. For more information, see [Working with themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-theming.md).
-   Single color/Colors per metric: Select a single color in the **Set value color** field. Interacting with that field opens a selector where you can choose the color from either a set of icons or from a list. You can also search for a color. Entering a search value has the selector show you a list of colors filtered by that search value.

If the visualization has more than one metric, you see the Colors per metric option instead. This option lets you select a single color for each metric.

Alternatively, you can add a rule to define a dynamic color. For more information, see [Create coloring rules for data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/colors-dv.md).

</td></tr></tbody>
</table>9.  Under **Chart interaction**, set what if anything happens when a viewer selects a chart or a chart segment on the visualization.

<table id="table_qnp_d2d_b1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow chart interaction

</td><td>

Enable an event to occur when a user selects a visualization or one of its segments.

</td></tr><tr><td>

Action

</td><td>

Choose the event that occurs when a user selects in a visualization or one of its segments. Choices depend on the visualization type and data source. Applies only when **Allow chart interaction** is on. For more information, see [Chart interactions in a data visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/dv-chart-interactions.md).

-   **Go to data view** opens a list view, KPI Details page, or Usage Insights overview page relevant to the associated segment or visualization. For table data, a system property determines whether a Core UI list or a Platform Analytics list opens. For more information, see [Data views for different data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/visualization-drilldown-in-config-ws.md).
-   **Go to URL** opens the specified URL, which can be on the instance or external. You have the option of specifying a page name to appear in the tooltip, for those visualizations with tooltips.
-   **Drill down to chart** \(Visualization Designer only\) Opens a different data visualization that is filtered by the selected data. You can add a drill-down visualization for each metric on the parent visualization.

**Note:** The last level of drill down in the Platform Analytics experience is always a Core UI list. Records don't open in Workspace embedded lists.

**Drill down to chart** supports only table data sources.

</td></tr></tbody>
</table>10. Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the data visualization list.


## Pivot table with multiple data sources

Consider a case where you want to present the following information, split up for each assignment group:

-   Number of assigned open incidents
-   The average age of the assigned open incidents
-   The average number of times an incident was reassigned

You can present this information in a single pivot table. Each set of information is going to come from a different data source. You have to find either three tables or three Performance Analytics indicators with this information. You can't mix and match different types of data sources! Fortunately, you find three appropriate indicators already defined in your instance. You select them as your data sources for a pivot table.

\[Omitted image "pivot-example-data-sources.png"\] Alt text: Data sources selected in pivot table visualization config panel

You want to see these indicator scores broken down by assignment group. Therefore, you select Assignment Group under Group By. Your three data sources are going to show as three columns, so you skip the **Column** field and select Assignment Group as a row.

\[Omitted image "pivot-example-group-by.png"\] Alt text: Assignment Group selected as a breakdown to group by in pivot table config panel

Now you're done. Save the data visualization and use it in a dashboard.

\[Omitted image "pivot-example-on-dashboard.png"\] Alt text: Completed pivot table on a dashboard

## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/share-dv-ac.md)
-   [Bookmark a visualization in the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/bookmark-dv-ac.md)

-   **[Table data options for pivot table visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-table-data.md)**  
When you select a table data source for a pivot table visualization, the following Data configuration options are available.
-   **[Indicator data options for pivot table data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-ind-data.md)**  
When you select an indicator data source for a pivot table visualization, the following Data configuration options are available.
-   **[Usage Insights data options for pivot table data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/config-dv-pivot-uxa-data.md)**  
When you select a Usage Insights data source for a pivot table visualization, the following Data configuration options are available.
-   **[Pivot visualization example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/dv-example-pivot.md)**  
Pivot tables show multiple dimensions or variables of a data set. This visualization displays separate cells for each row and column value combination, as well as a column subtotal for each first-level row. Aggregate information is presented in the upper left.

**Parent Topic:**[Creating data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/creating-data-visualizations.md)

