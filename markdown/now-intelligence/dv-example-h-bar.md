---
title: Horizontal bar visualization example
description: Horizontal bar visualizations enable you to show the comparative size or frequency of different categories or groups, such as incident priority or sales group. You can also add a group by or stack by to a bar visualization, such as the assignment group.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Bar visualization examples, Horizontal and vertical bar visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Horizontal bar visualization example

Horizontal bar visualizations enable you to show the comparative size or frequency of different categories or groups, such as incident priority or sales group. You can also add a group by or stack by to a bar visualization, such as the assignment group.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Use the horizontal bar visualization type to compare different categories or groups and clearly show the distribution of a data set. In this example, you show incidents by priority and stack them by assignment group.

## Procedure

1.  Follow the first steps to [Create a horizontal or vertical bar data visualization](../../reporting/task/create-dv-bar-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

    2.  Select **New**.

    3.  Select the Horizontal bar \(![Horizontal bar icon](../../reporting/image/inline-data-vis-96px-bar-horizontal.png)\) visualization type.

        ![Animation showing workspace and visualization designer selection, and choosing to create a horizontal bar visualization](../../reporting/image/dv-ex-h-bar-select.gif)

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the Incidents.Open condition in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A horizontal bar data visualization with the current value of the selected data appears in the Visualization Designer. Because the only information you've given is that the visualization represents active incidents, you see only a single block. You add priority and assignment group in step 4.

    ![Animation showing selection of data source, application of filter and result](../../reporting/image/dv-ex-h-bar-data-source.gif)

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the chart title `Number of open incidents - Priority and Assignment Group`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Number of open incidents of all priorities grouped by assignment group`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

    4.  Select **Save** and give the report the title `Horizontal bar - Open incidents`.

4.  Skip the Metric section.

5.  Add a Group by to differentiate the information in the chart.

    Under Group by, select **Active** and change the grouping to `Priority`.

6.  Under Sorting, choose the field to sort by and the order of the sorting.

    1.  Choose to sort by `Name`.

        The priority names each start with a number so that the bars are 1 - Critical, 2 - High, and so forth.

    2.  Choose `Ascending` for the sort order.

        The bars are ordered with 1 - Critical at the top followed by 2 - High, 3 - Moderate, and so forth.![Horizontal bar report sorted by name in ascending order](../../reporting/image/dv-ex-h-bar-sort-by.png)

7.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Select **Enable drilldown** to let viewers navigate to relevant information by selecting a data point in the chart.

        Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

        This control mirrors **Allow chart interaction**. Under Chart Interaction, you can also select the destination of drilling down.

8.  Configure the X axis.

    You can specify several options including the text on the axis, the range of values, and the axis position. You can even select **Hide axis** if you want to hide the axis and its values and show only the comparative sizes of the bars.

    1.  You can give the X axis the title `Open Incidents`, but this information is already in the title of the visualization, so leave it empty.

    2.  Keep the default of 0 for the Axis range's **From** value.

        There are cases in which a larger value makes sense, but the downside is that the relative sizes of the bars become less accurate, and may be misleading.

    3.  Keep the default empty value for the Axis range's **To** value.

        When this value is empty, the highest value in the range is the same as the highest value of the largest bar in the visualization. In this example, that value is 17.

    4.  The Show grid and Axis style options are minor aesthetic changes that you can adjust to your own preference.

        In this example, select **No tick lines** because they extend the grid, which is shown.

        ![Horizontal bar visualization with X axis options](../../reporting/image/dv-ex-h-bar-x-axis.png)

9.  Configure the Y axis.

    Y axis configuration addresses how the labels are displayed for the vertical axis. In this example, you have relatively short labels. However, if the maximum label size is smaller than the labels, you can choose to truncate or wrap the label text. You can truncate the text at the beginning of the label or at the end.

    1.  You can give the Y axis the title `Priority`, but this information is already in the title of the visualization, so leave it empty.

    2.  Select **Wrap labels**.

        You don't see any change in the label's display because the Max label size of 0 means that the largest label determines the size.

    3.  Change the Max label size to `50`.

        The labels wrap to additional lines. The Truncation type doesn't make a difference, because the labels are wrapped.

    4.  Clear the **Wrap labels** option.

        When you change the Truncation type, you can see that End replaces the ends of the longer labels with three dots. Select Start and the three dots replace the first part of the longer labels. And the same happens when you select middle.![Animation showing Y axis options](../../reporting/image/dv-ex-h-bar-y-axis-options.gif)

10. Configure the visualization's legend.

    The legend gives examples of the color coding for each value on the Y axis. You can choose whether to show the legend, where to place it and how much to show. Ideal placement depends on the size of its container on a dashboard. If you have more horizontal space, place the legend to the left or right. If you have more vertical space, place it above or below.

    1.  Select **Show legend** and **Show legend value**.

        **Show legend value** adds the number associated with the metric. In this case, 17 is added to the **1 - Critical** incidents because that is how many Critical incidents there are. Alternately, you can choose **Show data labels** \(in the Data label section\) to place this value on the bar itself.

    2.  Place the legend above the visualization.

        You can choose to place the legend above, below, or to the right or left of the visualization.

    3.  Select the Center **Horizontal alignment**.

        Start and End move the legend to the left or right of the visualization. \(Start and End are right and left for languages that read from right to left.\)

    4.  Change the Max legend item width to give those values more or less room.

    5.  **Expand legend vertically** provides additional lines to the legend so that users don't have to scroll beyond the default two lines.

        In this example, you only need one line for the five incident priorities. In a visualization that has bars for 15 or 20 different regions or assignment groups, you might want to show more in the legend without a scrollbar.

11. Add an additional Group by to provide more information in the visualization.

    Remember that you called this visualization `Number of open incidents - Priority and Assignment Group`. Add the assignment group.

    1.  Under Group by, select **+ Add**, choose `Assignment group`, and select **Apply**.

        ![Additional group by option with Assignment group selected.](../../reporting/image/dv-ex-h-bar-addl-groupby.png)

    2.  Show the data labels in the middle.

        With the additional group by, you have stacked values: Assignment group on top of Priority. You can choose to show the data value as the individual number of incidents per assignment group, as a cumulative value \(each segment added to the previous value\), or simply show the total. Choose Individual to show each segment's value.

    3.  Hide the X Axis.

        Because you added the values to each segment, the values on the axis are redundant.

        ![Incidents grouped by priority and assignment group with data labels on each segment](../../reporting/image/dv-ex-h-bar-data-labels-applied.png)

12. Choose the **Default** color type for the visualization.

    -   **Default** applies the colors associated with your UX theme.
    -   **Color palette** uses hues of the same color, for example Blue Light to Dark.

        ![Open critical incidents with blue palette applied](../../reporting/image/dv-ex-h-bar-color-palette-blues.png)

    -   **Fixed element** specifies the same color for each element, such as hardware incidents. All data visualizations that use fixed element colors show the same element in the same color.

## Result

You've created a horizontal bar visualization grouped on two fields. You've also configured the visualization's labeling, legend and ranges.

**Parent Topic:**[Bar visualization examples](dv-example-bar.md)

