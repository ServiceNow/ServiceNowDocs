---
title: Create an Indicator Scorecard
description: The Indicator Scorecard component enables users to visualize and compare data between multiple Performance Analytics indicators. It highlights the information regarding the last score collected, the change from the previous data point, the trend over time, and the value of the target to achieve.​
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Data visualizations in Platform Analytics, Platform Analytics]
---

# Create an Indicator Scorecard

The Indicator Scorecard component enables users to visualize and compare data between multiple Performance Analytics indicators. It highlights the information regarding the last score collected, the change from the previous data point, the trend over time, and the value of the target to achieve.​

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../concept/report-view-access-control.md) and [Platform Analytics roles](../../par-for-workspace/reference/platform-analytics-roles.md).

## About this task

For information about the use of an Indicator Scorecard in a dashboard, see [the Developer Site](https://developer.servicenow.com/dev.do#!/reference/now-experience/xanadu/shared-components/sn-scorecard-list/usage). This site gives information about Indicator scorecard components in the UI Builder, and some configuration options may differ from the Visualization Designer.

**Note:** You aren’t able to sort by previous scores in UI Builder.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Select **New**.

3.  Select the Indicator Scorecard \(![Indicator scorecard icon](../image/inline-data-vis-scorecard.png)\) visualization type.

4.  Configure the filtering and sorting capabilities of the Indicator Scorecard.

<table id="table_j2v_zll_4nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scorecard Type

</td><td>

List to select from scorecard types. Options include:-   **List**: Shows the list of indicators and metrics as columns.
-   **Pivot**: Shows indicators as rows and breakdown as columns or vice versa.


</td></tr><tr><td>

Show Header

</td><td>

Toggle to show or hide header.

</td></tr><tr><td>

Title

</td><td>

Component title.

</td></tr><tr><td>

Description

</td><td>

Component description displayed in the info icon during runtime.

</td></tr><tr><td>

Source definition

</td><td>

Select how to set which indicators to show. Options include:-   **Condition based**: Allows you to set a condition to determine which indicators to display.
-   **Manually selected**: Allows you to manually add indicators through the **Add data source** pane.

You can select a breakdown and element to filter the indicator for each indicator you manually select.

If you select only one indicator, you can set **Show only breakdowns** to show the elements of that indicator without the indicator score.

-   **Indicator group**: Sets an indicator group as the source.


</td></tr><tr><td>

Filter

</td><td>

Encoded query string for filtering which indicators to show. To create a filter statically, use the condition builder that is provided.**Note:** Only available if **Source definition** is Condition based.

</td></tr><tr><td>

Indicator group

</td><td>

Filter the table based on an indicator group from the list.**Note:** Only available if **Source definition** is Indicator group.

</td></tr><tr><td>

Breakdown

</td><td>

Select the breakdowns that you want to display. You can drag breakdown tiles to reorder them.

</td></tr><tr><td>

Max number of groups

</td><td>

The maximum number of elements to show for a breakdown. If you do not select the elements to show in **Filter elements**, the elements that are shown depend on the breakdown source and the value of **Sort direction**. For example, consider the Assignment Group breakdown, which uses the Name field from the Group \[sys\_group\] table. If the **Max number of groups** is the default 5, you show either the first 5 group names or the last 5 group names alphabetically, depending on whether the sort direction is ascending or descending. In such cases, consider selecting the elements in the **Filter elements** field.Default: 5

</td></tr><tr><td>

Filter elements

</td><td>

Select the elements to show for the relevant breakdown. If you don’t select any elements, all elements up to the max number of groups are shown.

</td></tr><tr><td>

Show breakdowns as columns

</td><td>

When true, breakdown elements are shown as columns on the pivot table. When false, breakdown elements are shown as rows. Supports only one breakdown and applies only to Pivot scorecards.Default: false

</td></tr><tr><td>

Show only breakdowns

</td><td>

If set to true, hides indicator total and shows only breakdown elements and the metrics selected. Available only on List scorecards when Source Definition is **Manually Selected** and only one indicator is selected.Default: false

</td></tr><tr><td>

Allow change breakdown

</td><td>

When true, the viewer can change the breakdown that is displayed. Available only when **Show only breakdowns** is true.Default: false

</td></tr><tr><td>

Breakdown visibility selector

</td><td>

When true, the breakdown selector is visible to viewers of the scorecard. When false, the breakdown selector has to be opened from the More options menu. Only available when **Allow change breakdown** is true.

 Default: false

</td></tr><tr><td>

Metrics

</td><td>

Select analytics to show in the indicator list. You can drag and drop metrics tiles to reorder them.Default: lastScore, changeAndChangePercent, target, trend

</td></tr><tr><td>

Time series aggregation

</td><td>

Time series aggregation to apply to all Indicators selected. To learn more about time series aggregations, see [Applying time series aggregations](../../performance-analytics/concept/applying-time-series-aggregations.md#).

</td></tr><tr><td>

Sort by

</td><td>

The column to sort the indicators by. Values: Name, Latest Score, Target, Change, changePercent, indicator\_group

**Note:** You cannot sort by previous scores.

 Default: Name

</td></tr><tr><td>

Sort Direction

</td><td>

The sorting direction for the indicators and/or breakdown elements. The effect on breakdown elements varies depending on the breakdown source. For example, breakdown elements from the Choice \[sys\_choice\] table are sorted according to the value of the Sequence field, whereas breakdown elements from Group \[sys\_group\] are sorted alphabetically according to the Name field.Values: Ascending \(Asc\) or Descending \(Desc\)

 Default: Asc

</td></tr><tr><td class="sub-head" colspan="2">

Additional settings

</td></tr><tr><td>

Follow filters

</td><td>

Turn on to have filters set on the dashboard apply to the Indicator Scorecard.Default: true

</td></tr><tr><td>

Show filter icon

</td><td>

Show the filter icon and the number of dashboard filters impacting the visualization. If a filter isn’t selected to apply to a visualization, the icon doesn’t show. Toggle off to hide the filter icon and number of filters applied.Default: true

</td></tr><tr><td>

Enable drilldown

</td><td>

Redirects user to underlying data when they select a data point. Toggle off to prevent this interaction.Default: true

</td></tr><tr><td>

Show filter element

</td><td>

Option to show the applied filter elements next to the indicator name. If a filter cannot apply to a visualization, the element\(s\) do not show. Toggle off to hide the filter elements and show only the indicator name.Default: true

</td></tr><tr><td>

Show bookmark

</td><td>

Toggle to show or hide a column of bookmarks. When on, users can bookmark indicators and breakdowns for themselves.Default: true

</td></tr><tr><td>

Show indicator info

</td><td>

Toggle to show or hide the indicator information icon. When shown, indicator information includes information about the last collection date, frequency of collection, and direction.Default: true

</td></tr><tr><td>

Show bookmarked items only

</td><td>

Toggle on to show only bookmarked indicators or breakdown elements.Default: false

</td></tr><tr><td class="sub-head" colspan="2">

Display settings

</td></tr><tr><td>

Max elements per page

</td><td>

The page size as determined by the maximum number of indicators or breakdown elements that the page can show. The increments are 10, 20, 50, and 100 indicators/elements. Default: 10

​

</td></tr><tr><td>

Target color scheme

</td><td>

Select a target color scheme. By default, the value defined in the **Default indicator target color scheme** property on the Performance Analytics Properties page is applied.

</td></tr><tr><td>

Show alternate row colors

</td><td>

Alternates colors of rows.

</td></tr><tr><td>

Show row lines

</td><td>

Adds dividers between rows.

</td></tr><tr><td>

Show column lines

</td><td>

Adds dividers between columns.

</td></tr><tr><td class="sub-head" colspan="2">

Chart interaction

</td></tr><tr><td>

Allow chart interaction

</td><td>

Enable navigation to the KPI Details page of an indicator what that indicator's name is selected.

</td></tr><tr><td>

Action

</td><td>

Only the **Go to data view** interaction is available. This action opens the indicator in KPI Details.

</td></tr></tbody>
</table>5.  Select **Save**.

    Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** to return to the Data Visualization list.


## What to do next

-   [Add a visualization to a dashboard from the Visualization Designer](add-dv-new-db.md)
-   [Share a data visualization in the Visualization Designer](share-dv-ac.md#)
-   [Bookmark a visualization in the Visualization Designer](../../dashboards/task/bookmark-dv-ac.md)

