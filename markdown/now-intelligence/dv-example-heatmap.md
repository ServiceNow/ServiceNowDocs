---
title: Heatmap visualization example
description: The heatmap data visualization shows the relationship between two table fields or indicator breakdowns as a spectrum of shading between two colors. The changes in color as you move along the axes reveal patterns in the value of one or both fields or breakdowns.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 5
breadcrumb: [Heatmap visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Heatmap visualization example

The heatmap data visualization shows the relationship between two table fields or indicator breakdowns as a spectrum of shading between two colors. The changes in color as you move along the axes reveal patterns in the value of one or both fields or breakdowns.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

By observing how cell colors change across each axis, you can observe if there are any patterns in value for one or both variables.

## Procedure

1.  Follow the first steps to [Create a heatmap data visualization](../../reporting/task/create-dv-heatmap-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  From the Multidimensional charts, select the Heatmap visualization type.

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the Incidents.Open condition in the Filters section.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A heatmap data visualization with the current value of the selected data appears in the Visualization Designer. Because the only information you've given is that the visualization represents open incidents, you see only a single block indicating closed incidents. You add columns and rows in the next step.

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the title `Open incidents - Priority and Assignment Group`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Open incidents of all assignment groups grouped by priority and assignment group`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

    4.  Select **Save** and give the report the title `Heatmap - Open Incidents - Priority and Assignment Group`.

4.  Skip the Metric section.

5.  Under Group by, add one column and multiple rows to show the data from multiple perspectives.

    1.  Add the **Priority** column to show the top level of information.

    2.  Add the row **Assignment group**.

6.  Under Sorting, choose the field to sort by and the order of the sorting.

    1.  Choose to sort by `Value`.

    2.  Choose `Descending` for the sort order.

        The columns are ordered with those assignment groups having the highest number of incidents at the top. ![Heatmap report sorted by value in descending order with the legend](../../reporting/image/dv-ex-heatmap-sort-by.png)

7.  Under Additional settings, select **Show 0 when no data available**.

    When you show zero, no cells are left empty. The cells with no open incidents also get a color coding.![Heatmap row with zeroes shown for columns with no associated incidents](../../reporting/image/dv-ex-heatmap-show-zero.png)

8.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Select **Enable drilldown** to let viewers navigate to relevant information by selecting a data point in the chart.

        Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

        This control mirrors **Allow chart interaction**. Under Chart Interaction, you can also select the destination of drilling down.

9.  Choose how to show what the cells in the heatmap describe.

    -   **Show data labels** controls whether the value is shown in the heatmap's cells. This option is enabled by default. When it's inactive, only the colors give an idea of the cells' relative values.
    -   **Show Legend** gives examples of the color coding for each cell in the visualization and its associated value. You can choose whether to show the legend and where to place it.
    1.  Select **Show legend** to enable legend options.

    2.  Play with where to place the legend around the visualization.

        You can choose to place the legend above, below, or to the right or left of the visualization.

10. Play with the color settings.

    The default color type has shades of blue. You can also choose a custom color range with specified colors for upper and lower values.


## Result

You have created a heatmap visualization sorted on two values and configured its values, labels, and data updates. You have also configured the visualization's colors.

**Parent Topic:**[Create a heatmap data visualization](../../reporting/task/create-dv-heatmap-ac.md)

