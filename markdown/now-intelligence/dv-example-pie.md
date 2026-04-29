---
title: Pie visualization example
description: The pie data visualization uses a circular shape to show the proportion or percentage of different categories or groups. Each part of the circle \(or "slice"\) represents a different category or group, and the size of each slice is proportional to the size of the group or category it represents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 6
breadcrumb: [Pie and donut visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Pie visualization example

The pie data visualization uses a circular shape to show the proportion or percentage of different categories or groups. Each part of the circle \(or "slice"\) represents a different category or group, and the size of each slice is proportional to the size of the group or category it represents.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Use this visualization type to show the proportion of parts that make a whole, such as the distribution of expenses in a budget or the distribution of incidents across assignment groups.

## Procedure

1.  Follow the first steps to [Create a pie or donut data visualization](../../reporting/task/create-dv-donut-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  From the Pies and Donuts section, select the Pie visualization type.

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the predefined condition Incidents.Open in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A pie visualization with the current value of the selected data appears in the Visualization Designer. Because the only information you've given is that the visualization represents active incidents, you see only a two wedges for Active=True and Active=False. You add priority and assignment group in step 4.

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the title `Open incidents - Assignment Group`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Open incidents of all priorities by assignment group`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

    4.  Select **Save** and give the report the title `Pie - Open incidents`.

4.  Skip the Metric section.

5.  Add a Group by to differentiate the information in the visualization.

    Under Group by, select **Active** and change the grouping to `Assignment group`.

6.  Under Sorting, choose the field to sort by and the order of the sorting.

    1.  Choose to sort by `Name`.

    2.  Choose `Ascending` for the sort order.

        The segments are ordered by the assignment group name starting with Financial, HR, Marketing, and so on.![Pie report on open incidents sorted by Assignment group](../../reporting/image/dv-ex-pie-sort-by.png)

7.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Under Chart interaction, select **Allow chart interaction**.

        From the Action menu, select **Drill down to chart** to let viewers navigate to relevant information by selecting a data point in the chart. Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

8.  Choose how to show what the wedges in the pie describe.

    -   **Show Legend** gives examples of the color coding for each value in the visualization. You can choose whether to show the legend, where to place it and how much to show. Ideal placement depends on the size of its container on a dashboard. If you have more horizontal space, place the legend to the left or right. If you have more vertical space, place it above or below.
    -   **Show data labels** adds the label and value information next to the segments of the visualization.
    1.  Select **Show legend** to enable legend options.

    2.  Select **Show legend value**.

        This option adds the number associated with the metric. In this case, 18 is added to the incidents assigned to the **HR Systems Support** assignment group because that is how many HR Systems incidents there are.

    3.  Select **Show value on the same line** to keep the value with the assignment group name.

    4.  Select **Show legend percentage** to provide more information about the value.

    5.  Play with where to place the legend above of the visualization.

        You can choose to place the legend above, below, or to the right or left of the visualization.

    6.  Select the Center **Horizontal alignment**.

        Horizontal alignment is not available if you place the legend to the right or left of the visualization. Start and End move the legend to the left or right of the visualization. \(Start and End are right and left for languages that read from right to left.\)

    7.  Change the Max legend item width to give those values more or less room.

        ![Open incidents by assignment group pie visualization with legend showing value and percentage options](../../reporting/image/dv-ex-pie-legend-options.png)

9.  Clear **Show legend** and select **Show data labels**.

    1.  Choose the **Data label type**.

        You can choose Value to show the number next to the label, Percent to show the percentage the value represents, or Value and percent to show both.

    2.  Change the Max label size to `50`.

        The labels wrap to additional lines. The Truncation type doesn't make a difference, because the labels are wrapped.

    3.  Clear the **Wrap labels** option.

        When you change the Truncation type, you can see that End replaces the ends of the longer labels with three dots. Select Start and the three dots replace the first part of the longer labels. And the same happens when you select middle.

10. Choose the **Default** color type for the visualization.

    -   **Default** applies the colors associated with your UX theme.
    -   **Color palette** uses hues of the same color, for example Blue Light to Dark.
    -   **Fixed element** specifies the same color for each element, such as hardware incidents. All data visualizations that use fixed element colors show the same element in the same color.

## Result

You have created a pie visualization grouped on one value. You have also configured the visualization's labeling, legend, and colors.

**Parent Topic:**[Create a pie or donut data visualization](../../reporting/task/create-dv-donut-ac.md)

