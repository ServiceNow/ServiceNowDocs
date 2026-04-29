---
title: Dial visualization example
description: Dial visualizations show where a single value lies across a range from minimum to maximum expected values. Visually, a "needle" points to the value, and the dial is colored in for values up to the needle.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 6
breadcrumb: [Dial visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Dial visualization example

Dial visualizations show where a single value lies across a range from minimum to maximum expected values. Visually, a "needle" points to the value, and the dial is colored in for values up to the needle.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Use the dial visualization when you want to compare a current value to a target or benchmark, such as a company's sales compared to its goal. You can configure the dial visualization with colors to show where the current value lies compared to the goal. In a single score, you can color code the value to show if it's in a positive or negative range. With a dial, you color code the part of the visualization that represents the value.

## Procedure

1.  Follow the first steps to [Create a dial data visualization](../../reporting/task/create-dv-dial-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  Select the dial visualization type from the Scores section.

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the predefined condition Incidents.Open in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A dial data visualization with the current value of the selected data appears in the Visualization Designer![Untitled dial visualization showing the Incident table as data source](../../reporting/image/dv-ex-dial-data-source.png).

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the title `Open incidents - Dial`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Number of open incidents of all priorities and categories`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

4.  Skip over the Metric section.

    Some data visualizations support multiple data sources, but the dial visualization doesn’t. Because you only want to see the number of open incidents, you don't need to change the default metric, Count, or its label, Incident.

5.  Under Additional settings, select **Show 0 when no data available**.

    Because the name of the visualization is `Number of open incidents`, the metric label, Incident, is redundant.

    In some cases, a value of zero isn't interesting to the audience of a visualization. In this case, however, you want to show off having zero open incidents.

6.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Under Chart interaction, select **Allow chart interaction**.

        From the Action menu, select **Drill down to chart** to let viewers navigate to relevant information by selecting a data point in the chart. Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

7.  Under Presentation, configure the sizes of the score and the dial itself, and the visualization's minimum and maximum values.

    1.  Under Display settings, change the score size from the default M \(medium\) to L \(large\) to emphasize it.

    2.  Choose a minimum and maximum value for the dial.

        The default values are 0 and 100. In this case, the minimum is zero if there are no open incidents. Keep the default value for the maximum as well, but consider realistic maximum values when you create your own dial visualizations.

    3.  Ignore the inner radius parameter for the purposes of this example.

        The inner radius is the ratio of the visualization's inner radius to the outer. Allowed values are 0.7–0.95.

8.  Configure a color rule for the score.

    Because you want to emphasize the state of open incidents, define a dynamic color rule that changes the dial's color based on its value.

    1.  In the Display settings, choose the `Single color` color type.

    2.  Under Color Rules, select **+ Add rule**.

    3.  For the first color rule, choose the **Operator** `lower than`, enter the **Value** `6`, and choose the color `Positive Green` for both the color and the icon color \(if available\), and select **Apply**.

        The value is up to the specified number but not including it.

        Retain the order 100.

        ![Color rule options with lower than operator selected, value set to 6, and color options set to Positive Green](../../reporting/image/dv-ex-single-score-color-rule-1.png)

    4.  To indicate a value that requires more attention, create a second rule with the **Operator** `between`, the values `5` and `25`, the color and icon color `Warning Orange`, and the order `50`.

    5.  To show the values that require the highest attention, create a third rule with the **Operator** `greater than`, the value `25`, the color and icon color `Red`, and the order `25`.

    You've created three rules to show whether the single score value is in line with what you want to see.

    ![Dial visualization with Large size and a red arc color that reflects defined coloring rules.](../../reporting/image/dv-ex-dial-complete.png)


## Result

You have created a dial visualization based on a single metric, open incidents. You have also configured user options regarding filters and drilldowns, and configured the visualization's size and coloring rules.

**Parent Topic:**[Create a dial data visualization](../../reporting/task/create-dv-dial-ac.md)

