---
title: Bubble data visualization example
description: The bubble data visualization is used to do compare fields and see their relationships.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 4
breadcrumb: [Bubble visualization, Create, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Bubble data visualization example

The bubble data visualization is used to do compare fields and see their relationships.

## Before you begin

Role required: Anyone with access to data can create a visualization of that data on any dashboard that they can edit. Users with the itil, report\_user, admin, or viz\_creator role can create a visualization in the Visualization Designer. When you create a visualization in the Visualization Designer, it is saved to the Library. For more information on access, see [Report\_view access control](../../reporting/concept/report-view-access-control.md) and [Platform Analytics roles](../reference/platform-analytics-roles.md).

## About this task

Use a bubble visualization to show two ordinal fields, such as Priority and Age, as circles of different sizes along an x-y axis. Use the relative size and position of the circles to compare fields and see their relationships. You can also group the data by a third field, which can be qualitative. The third field is differentiated by color.

In this example, you create a bubble visualization that shows the number of open incidents and color code the visualization to highlight the value's desirability.

## Procedure

1.  Follow the first steps to [Create a bubble data visualization in the Visualization Designer](../../reporting/task/create-dv-bubble-ac.md):

    1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**, or open an in-line dashboard and select **Edit**.

    2.  Select **Create data visualization**.

    3.  Select the **Bubble** visualization type from Multidimensional charts.

2.  For the moment, skip the header and border section and move to the data source.

    1.  Select **Add data source**.

    2.  Choose the Incident \[incident\] table.

    3.  Because this visualization shows open incidents, let's add the predefined condition Incidents.Open in the Filters section.

        With this filter selected, the visualization only shows the number of active incidents.

    4.  Select **Run** to preview the records that the visualization will be based on.

    5.  Select **Add this source**.

    A bubble visualization with the current values of the selected data appears in the Visualization Designer.

    ![Animation showing selection of data source, application of filter and result](../../reporting/image/dv-ex-bubble-data-source.gif)

3.  Now that you can see the visualization, let's add some context for the user.

    1.  Expand the Header and border section.

    2.  Select **Show header** and provide the title `Resolution time by state`.

        When **Show header** is selected, you can add a title and a description. The chart title isn't necessarily the same as the visualization name. The visualization name identifies it in the Visualization Designer and in a list. The chart title appears within the visualization.

    3.  Enter a description of the visualization: `Bubble report showing incident resolution times with state`.

        While the description and title fields aren't required, this information makes the visualization easier to understand on a dashboard and easier to identify in a list.

4.  Skip the Data source sections

    While the bubble report does support multiple data sources, you're just working with incidents. Because we only want to see the number of open incidents, you don't need to change the default metric, Count, or its label, Incident.

5.  In the Dimensions section, keep the X axis field, Business resolve time, and select `State` for the Y axis field.

    Select **Apply**

    ![Bubble report with X axis set to Business resolve time and Y axis set to State](../../reporting/image/dv-ex-bubble-dimensions.png)

6.  Under Data update, configure how the audience interacts with the visualization.

    1.  Select **Follow filters**.

        This option enables the visualization to follow interactive filters on the dashboards it's placed on that are based on the same table.

    2.  Select **Show filter icon** to show the number of filters applied to the visualization.

        For example, if dashboard filters limit the value of the visualization, the icon indicates that you're seeing the number of open incidents that match the filters. You can then check to see which filters are in effect.

    3.  Under Chart interaction, select **Allow chart interaction**.

        From the Action menu, select **Drill down to chart** to let viewers navigate to relevant information by selecting a data point in the chart. Some visualizations only drill down to the list of associated data. Table data is generally restricted by access control lists \(ACLs\) and viewers may not see all of the associated records.

7.  Under **Presentation** &gt; **Colors**, Choose the **Default** color type for the visualization.

    -   **Default** applies the colors associated with your UX theme.
    -   **Single** specifies the same color for each bubble. All data visualizations that use fixed element colors show the same element in the same color.

## Result

You have created a bubble visualization sorted on two values. You have also configured the visualization's colors.

**Parent Topic:**[Create a bubble data visualization in the Visualization Designer](../../reporting/task/create-dv-bubble-ac.md)

