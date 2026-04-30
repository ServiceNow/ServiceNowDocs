---
title: Vertical bar visualization example
description: Vertical bar visualizations enable you to show the comparative size or frequency of different categories or groups, for example, sales in different regions or over different periods of time. The X axis of a vertical usually shows a numerical value such years or date ranges, age ranges, or salary ranges.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 7
breadcrumb: [Bar visualization examples, Horizontal and vertical bar visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Vertical bar visualization example

Vertical bar visualizations enable you to show the comparative size or frequency of different categories or groups, for example, sales in different regions or over different periods of time. The X axis of a vertical usually shows a numerical value such years or date ranges, age ranges, or salary ranges.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Use the vertical bar visualization type to compare different categories or groups and clearly show the distribution of a data set. In this example, you show outages by type.

## Procedure

1.  Follow the first steps to [Create a horizontal or vertical bar data visualization](../../reporting/task/create-dv-bar-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  From the Bars section, select the Vertical bar visualization type.

2.  For the moment, we can skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Outage \[cmdb\_ci\_outage\] table.

        This table lists outages of various services.

    3.  Select **Run** to preview the records that the visualization will be based on.

    4.  Select **Add this source**.

    A vertical bar data visualization with the current value of the selected data appears in the Visualization Designer. The visualization is grouped by the first field \(alphabetically\) in the table, Begin. This is useful because it shows the outages distributed by a time measurement.

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the title `Outages by type`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `CMDB outages grouped by when they began and stacked by type.`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

    4.  Select **Save** and give the report the title `Vertical bar - CMDB outages`.

4.  Skip the Metric section.

5.  In the Group by section, select **Add** to differentiate the information in the visualization.

    Select **Type** and choose **Apply**. The columns now show different colors to distinguish the different types of outages.

    ![Vertical bar additional group by selection with the Type field highlighted](../../reporting/image/dv-ex-v-bar-addl-groupby.png)

6.  Under Sorting, maintain the Sort by `Value` and Sort by order `Descending`.

    These options show one logical way of visualizing the data. Change the sorting options to see what works best for you.

7.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Select **Enable drilldown** to let viewers navigate to relevant information by selecting a data point in the chart.

        Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

        This control mirrors **Allow chart interaction**. Under Chart Interaction, you can also select the destination of drilling down.

8.  Chart variations show the data one of three different ways:

    -   **Stacked**

        Shows the grouped elements \(type in this case\) stacked one type over the next.

    -   **Side-by-side**

        Shows a different bar for each type.

    -   **Normalized**

        Shows stacked bars of the same height for each group, with the colors showing the percent of the total.

    |Stacked|Side-by-side|Normalized|
    |-------|------------|----------|
    |![Stacked variation](../../reporting/image/dv-ex-v-bar-char-var-stacked.png)|![Side by side variation](../../reporting/image/dv-ex-v-bar-char-var-sbs.png)|![Normalized variation](../../reporting/image/dv-ex-v-bar-char-var-norm.png)|

9.  Configure the Y axis.

    You can specify several options including the text on the axis, the range of values, and the axis position. You can even select **Hide axis** if you want to hide the axis and its values and show only the comparative sizes of the bars.

    1.  You can give the Y axis the title `Number of outages`, but this information is already in the title of the visualization, so leave it empty.

    2.  You can specify lower and upper ranges for the bars, but because both of these values are useful, leave **Axis range - from** and **Axis range - to** empty.

        There are cases in which a larger **From** value makes sense, but the downside is that the relative sizes of the bars become less accurate. When the **To** value is empty, the highest value in the range is the same as the highest value of the largest bar in the visualization.

    3.  The Show grid and Axis style options are minor aesthetic changes that you can adjust to your own preference.

        In this example, select **Clean** because it's a little bit neater.

        ![Vertical bar visualization with Y axis options](../../reporting/image/dv-ex-v-bar-y-axis.png)

    4.  Change the Max label size to `50`.

        The labels wrap to additional lines. The Truncation type doesn't make a difference, because the labels are wrapped.

10. Configure the X axis.

    You can specify several options including the text on the axis, the range of values, and the axis position.

    X axis configuration addresses how the labels are displayed for the vertical axis. In this example, you have relatively short labels. However, if the maximum label size is smaller than the labels, you can choose to truncate or wrap the label text. You can truncate the text at the beginning of the label or at the end.

    1.  You can give the X axis the title `CMDB Outages`, but this information is already in the title of the visualization, so leave it empty.

    2.  Select **Wrap labels**.

        You don't see any change in the label's display because the Max label size of 0 means that the largest label determines the size.

11. Configure the visualization's legend.

    The legend gives examples of the color coding for each value on the X axis. You can choose whether to show the legend, where to place it and how much to show. Ideal placement depends on the size of its container on a dashboard. If you have more horizontal space, place the legend to the left or right. If you have more vertical space, place it above or below.

    1.  Select **Show legend** and **Show legend value**.

        **Show legend value** adds the number associated with the selected metric. Alternately, you can choose **Show data labels** \(in the Data label section\) to place these value on the bar itself.

    2.  Place the legend above the visualization.

        You can choose to place the legend above, below, or to the right or left of the visualization.

    3.  Select the Center **Horizontal alignment**.

        Start and End move the legend to the left or right of the visualization. \(Start and End are right and left for languages that read from right to left.\)

    4.  Change the Max legend item width to give those values more or less room.

    5.  **Expand legend vertically** provides additional lines to the legend so that users don't have to scroll beyond the default two lines.

        In this example, you only need one line for the three outage types. In a visualization that has bars for 15 or 20 different regions or assignment groups, you might want to show more in the legend without a scrollbar.

12. Choose the **Default** color type for the visualization.

    -   **Default** applies the colors associated with your UX theme.
    -   **Color palette** uses hues of the same color, for example Sequential - Blues Light to Dark.

        ![CMDB outages by type with blue palette applied](../../reporting/image/dv-ex-v-bar-color-palette-blues.png)

    -   **Fixed element color** specifies the same color for each element, such as hardware incidents. All data visualizations that use fixed element colors show the same element in the same color.

## Result

You have created a vertical bar visualization grouped on two fields. You have also configured the visualization's labeling, legend and ranges.

**Parent Topic:**[Bar visualization examples](dv-example-bar.md)

