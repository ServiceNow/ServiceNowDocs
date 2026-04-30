---
title: Single score visualization example
description: Use a single score visualization when you want to show a single value or metric, such as overall revenue or number of open incidents. The basic score visualizes a single value with a descriptive heading and date/time stamp.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Create a single score data visualization, Data visualizations in Platform Analytics, Platform Analytics]
---

# Single score visualization example

Use a single score visualization when you want to show a single value or metric, such as overall revenue or number of open incidents. The basic score visualizes a single value with a descriptive heading and date/time stamp.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. If you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Single score visualizations have the advantage that you can color code them to show if the value is good for your business or requires improvement. For example, the number of open incidents is a value you want to keep low. Revenue, on the other hand, you want to be high. Let's create a single score for open incidents.

In this example, you create a single score visualization that shows the number of open incidents and color code the visualization to highlight the value's desirability.

## Procedure

1.  Follow the first steps to [Create a single score data visualization in the Visualization Designer or on a dashboard](../../reporting/task/create-dv-sing-sc-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

    2.  Select **New**.

    3.  Select the Single score \(![Data visualization single score icon](../../reporting/image/inline-data-vis-single-score.png)\) visualization type.

        ![Animation showing workspace and visualization designer selection, and choosing to create a single score visualization](../../reporting/image/dv-ex-single-score-select.gif)

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the Incidents.Open condition in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A single score data visualization with the current value of the selected data appears in the Visualization Designer.

    ![Animation showing selection of data source, application of filter and result](../../reporting/image/dv-ex-single-score-data-source.gif)

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the chart title `Number of open incidents`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Number of open incidents of all priorities and categories`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

4.  Skip over the Metric section.

    Some data visualizations support multiple data sources, but the single score visualization doesn’t. Because we only want to see the number of open incidents, you don't need to change the default metric, Count, or its label, Incident.

5.  Under Additional settings, configure some extra information about the visualization.

    1.  Leave the **Show metric label** unselected.

        Because the name of the visualization is `Number of open incidents`, the metric label, Incident, is redundant.

    2.  Select **Show score update time**.

        Alone, this option shows the time of day the score was last updated. You can also select Use relative score time to show the elapsed time since the last update, for example just now, five minutes ago, and so on.

        ![Animation showing selection of update time and filter options](../../reporting/image/dv-ex-single-score-show-update.gif)

    3.  Select **Show zero**.

        In some cases, a value of zero isn't interesting to the audience of a visualization. In this case, however, you want to show off having zero open incidents.

6.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Select **Enable drilldown** to let viewers navigate to relevant information by selecting a data point in the chart.

        Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

        This control mirrors **Allow chart interaction**. Under Chart Interaction, you can also select the destination of drilling down.

7.  Under Presentation, configure the size and base color of the score value.

    1.  Under Display settings, change the score size from the default M \(medium\) to XL \(extra large\) to emphasize it.

    2.  Choose a Score icon and an icon style to distinguish this data visualization from others on the dashboard you add it to.

        For example, select the Activity Outline icon with background.

    3.  Select the color type `Single color`.

        ![Animation showing selection of score size, score icon, icon style, and color](../../reporting/image/dv-ex-single-score-show-display.gif)

8.  Configure a color rule for the score.

    Because you want to emphasize the state of open incidents, define a dynamic color rule that changes the score's color based on its value.

    1.  In the Display settings, choose the `Single color` color type.

    2.  Under Color Rules, select **+ Add rule**.

    3.  For the first color rule, choose the **Operator** `lower than`, enter the **Value** `6`, and choose the color `Positive Green` for both the color and the icon color, and select **Apply**.

        The value is up to the specified number but not including it.

        Retain the order 100.

        ![Color rule options with lower than operator selected, value set to 6, and color options set to Positive Green](../../reporting/image/dv-ex-single-score-color-rule-1.png)

    4.  To indicate a value that requires more attention, create a second rule with the **Operator** `between`, the values `5` and `25`, the color and icon color `Warning Orange`, and the order `50`.

    5.  To show values that require the highest attention, create a third rule with the **Operator** `greater than`, the value `25`, the color and icon color `Red`, and the order `25`.

    You've created three rules to show whether the single score value is in line with what you want to see.

    ![Single score in red with XL size, update time, a color that reflects defined coloring rules.](../../reporting/image/dv-ex-single-score-complete.png)

9.  Select **Save**.


## Result

You've created a single score visualization based on a single metric, open incidents. You've also configured user options regarding filters and drilldowns, and configured a color, an icon, and coloring rules.

