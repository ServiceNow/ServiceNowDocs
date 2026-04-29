---
title: Generate visualizations in the Now Assist panel
description: Request generative AI to create a visualization of data that you want to see. If you are on a dashboard that you can edit, you can add the visualization to that dashboard.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Generate visualizations in the Now Assist panel

Request generative AI to create a visualization of data that you want to see. If you are on a dashboard that you can edit, you can add the visualization to that dashboard.

## Before you begin

Role required: now\_assist\_panel\_user and either now\_assist\_analytics\_generation or now.assist.creator.analytics. You need access to the data that you want to see. If you want to add the visualization to a dashboard, you need editing rights to that dashboard.

**Important:** You need the correct entitlements to this skill and to Query Generation.

## Procedure

1.  If you want to add a visualization to a dashboard that you can edit, navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards** and open the dashboard from the library.

2.  Open the Now Assist panel.

    ![Control for opening the Now Assist panel.](../image/nowass-open-nowass-panel.png)

3.  Select **Create a data visualization**.

    ![Now Assist panel showing option to create a data visualization.](../image/nowass-create-dv.png)

4.  Ask for data to see.

    For example, ask "Can I see open incidents by priority?" You then would get a visualization of the count of incidents divided across priorities where active=true. You can specify the chart type, too, but not all charts are supported. For more information about what kind of questions you can ask, see [Guidelines and example questions](../concept/example-questions-generating-dv.md) and [Limitations to generating data visualizations](../reference/limitations-generating-dv.md).

    **Note:** Analytics Generation only returns visualizations of data in tables for which semantic generation is enabled. If you have a question, ask your admin to check the Semantic Table Configurations \[sn\_query\_gen\_table\_config\_list\] under **Query Generation** &gt; **Administration** &gt; **Semantic Table Config**.

5.  To pop out a larger view of the visualization that shows the table name and conditions, select **View details**.

    ![Details of a vertical bar visualization of incident data.](../image/analgen-viz-details.png)

6.  To add the visualization to a dashboard, select **Add to dashboard**.

    A pane opens where you can choose from any of the dashboards that are available to you to edit. You can also create a new dashboard to contain the visualization. Note that technical dashboards are not supported.

7.  To add the visualization to a collaborative workspace in AI Data Explorer, select **Add to exploration**.

    For more information, see [Use AI to explore data with AI Data Explorer](../reference/now-assist-explorer.md).

8.  To edit the visualization, select **Edit visualization**.

    If you have the viz\_creator role, you can save the visualization to the Data Visualizations library. For more information, see [Edit a data visualization in the Visualization Designer](../../dashboards/task/edit-dv-ac-center.md).

9.  Under **What would you like to do next**, you see several suggestions:

    |Suggestion|Description|Example of prompt|
    |----------|-----------|-----------------|
    |Change visualization type or condition|Change a configuration field like Group by, or the filter conditions, or the visualization type.|Change group by to Priority.|
    |Use another table as the data source|Change the data that you want to visualize, according to table name. You may be prompted for the aggregation type, such as Count.|Change table to Problem.|
    |Leave this topic|Select this button to finish work on this visualization|Not applicable|


-   **[Guidelines and example questions](../concept/example-questions-generating-dv.md)**  
This section shows guidelines and some typical questions that you could ask in the Now Assist panel to generate data visualizations.
-   **[Limitations to generating data visualizations](../reference/limitations-generating-dv.md)**  
While data visualization generation is designed to handle a wide range of queries and scenarios, certain cases are not supported or only partially supported.

**Parent Topic:**[Generate or export dashboards and data visualizations in the Now Assist panel](../reference/analytics-assist-landing-page.md)

