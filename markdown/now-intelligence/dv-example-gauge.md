---
title: Gauge visualization example
description: Like dials, gauges show where a single value lies across a range from minimum to maximum expected values. In addition to dial functionality, you can set colored data ranges to help users understand what the value represents.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 5
breadcrumb: [Gauge visualizations, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Gauge visualization example

Like dials, gauges show where a single value lies across a range from minimum to maximum expected values. In addition to dial functionality, you can set colored data ranges to help users understand what the value represents.

## Before you begin

Role required: No role is required to see the Platform Analytics workspace. With any internal role, you can create a data visualization, but you need the viz\_creator role to save your visualizations to the Visualization Library. To create a meaningful visualization, you must have permission to access the data you want to report on.

## About this task

Use the gauge visualization when you want to compare a value to a target or benchmark, such as a company's sales compared to its goal. You can configure the visualization with colors to show where the current value lies compared to the goal. With a dial, you color code the part of the visualization that represents the value. With a gauge visualization, you color code the ranges and a needle points to the value.

## Procedure

1.  Follow the first steps to [Create a gauge data visualization in the Visualization Designer](../../reporting/task/create-dv-gauge-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  From the Scores section, Select the gauge visualization type.

2.  For the moment, skip the header and border section and move on to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the Incidents.Open condition in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A gauge data visualization with the current value of the selected data appears in the Visualization Designer.![Untitled gauge visualization showing the Incident table as data source](../../reporting/image/dv-ex-gauge-data-source.png)

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the visualization title `Open incidents - Gauge`.

        When **Show header** is selected, you can add a title and a description. The title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The title appears within the visualization.

    3.  Enter a description of the visualization: `Number of open incidents of all priorities and categories`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

4.  Under Additional settings, select **Show 0 when no data available**.

    In some cases, a value of zero isn't interesting to the audience of a visualization. In this case, however, you want to show off having zero open incidents. When you don't select **Show 0 when no data available**, you have the option to configure a message to show when there is no data.

5.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Select **Enable drilldown** to let viewers navigate to relevant information by selecting a data point in the chart.

        Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

        This control mirrors **Allow chart interaction**. Under Chart Interaction, you can also select the destination of drilling down.

6.  Under Presentation, configure the shape of the gauge and the size of the gauge value.

    1.  Under Display settings, choose 180 degrees as the gauge arc angle.

        180 degrees shows the gauge as a semicircle. 240 degrees shows the gauge as three quarters of a circle.

        |180 degree gauge|240 degree gauge|
        |----------------|----------------|
        |![180 degree gauge example](../../reporting/image/dv-ex-gauge-180.png)|![240 degree gauge example](../../reporting/image/dv-ex-gauge-240.png)|

    2.  Change the value label size from the default M \(medium\) to L \(large\) to emphasize it.

    3.  Ignore the inner radius parameter for the purposes of this example.

        The inner radius is the ratio of the visualization's inner radius to the outer. Allowed values are 0.7–0.95.

7.  Under Ranges, choose the minimum and maximum values of the gauge.

    The default values are 0 and 100. In this case, the minimum is zero if there are no open incidents. Keep the default value for the maximum as well, but consider realistic maximum values when you create your own gauge visualizations.

8.  Select **Configure ranges**.

    Ranges are the color bands that show how the value meets the goals associated with the visualization. For the purpose of this example, you configure three ranges to illustrate the value.

    1.  Keep the default number of ranges, `3`, and the default color scheme of `Green to red`.

    2.  Label the first range `Good` and specify **Values less than or equal to** `5`.

    3.  Label the second range `Needs work` and specify **Values less than or equal to** `20`.

        The lower value is taken from the first range.

    4.  Label the third range `We need help`.

        The value of this range is taken from the second range.

    5.  Select **Apply**.

        ![Range configuration with labels and values](../../reporting/image/dv-ex-gauge-config-ranges.png)

9.  Configure the **Labels** for the gauge.

    1.  Choose the Score label `None`.

        The other choices are Metric label and Range label. Because the metric is in the name of the visualization, it's redundant to label the value in the gauge with Incidents. The Range label provides the option to make the label the visualization's primary text rather than the value.

    2.  Select **Show range limit**.

        The range limit adds the lower values of each range, and the upper limit of the gauge to the visualization.

    3.  Select **Show range labels**.

        The range labels that you configured add context for each of the ranges.

    You've created three rules to show whether the single score value is in line with what you want to see.


## Result

You have created a gauge visualization based on a single metric, open incidents. You have also configured user options regarding filters and drill downs, and configured the visualization's size, labeling, and ranges.

**Parent Topic:**[Create a gauge data visualization in the Visualization Designer](../../reporting/task/create-dv-gauge-ac.md)

