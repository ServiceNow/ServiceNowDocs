---
title: Use Analytics Generation
description: In the Now Assist panel, request generative AI to create a visualization of data that you want to see. If you are on a dashboard that you can edit, you can add the visualization to that dashboard.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics Generation, Platform Analytics]
---

# Use Analytics Generation

In the Now Assist panel, request generative AI to create a visualization of data that you want to see. If you are on a dashboard that you can edit, you can add the visualization to that dashboard.

## Before you begin

Now Assist for Creator must be installed on your instance, and the data visualization skill must be activated. Consult your admin if this does not seem to be the case.

Role required: now.assist.creator and now\_assist\_panel\_user. You need access to the data that you want to see. If you want to add the visualization to a dashboard, you need editing rights to that dashboard.

## Procedure

1.  If you want to add a visualization to a dashboard that you can edit, open that dashboard in **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.

2.  Open the Now Assist panel.

    ![Control for opening the Now Assist panel.](../image/nowass-open-nowass-panel.png)

3.  Select **Create a data visualization**.

    ![Now Assist panel showing option to create a data visualization.](../image/nowass-create-dv.png)

4.  Ask for data to see.

    For example, ask "Can I see open incidents by priority?" You then would get a chart of the count of incidents divided across priorities where active=true. You can specify the chart type, too, but not all charts are supported. For more information about what kind of questions you can ask, see [Guidelines and example questions](../concept/example-questions-generating-dv.md) and [Limitations to generating data visualizations](../reference/limitations-generating-dv.md).

5.  To add the visualization to a dashboard, select **Add to dashboard**.

    A pane opens where you can choose from any of the in-line dashboards that you can edit. You can also create a new dashboard to contain the visualization. However, technical dashboards are not supported.

6.  To edit the visualization, select **Edit in visualization designer**.

    If you have the viz\_creator role, you can save the visualization to the Data Visualizations library. For more information, see [Edit a data visualization in the Visualization Designer](../../dashboards/task/edit-dv-ac-center.md).

7.  You have an optional, iterative process to change the visualization that you see.

    1.  Select **Yes** to the question **Would you like to modify the generated visualization?**

        ![Now Assist panel asking if you want to modify the generated visualization.](../image/nowass-mod-gen-query.png)

    2.  In answer to the prompt **What would you like to modify**, request one of the following:

        -   A different chart in the same group of charts. For example, you could request a change from a horizontal bar to a vertical bar, or from a line chart \(time series\) to a column chart \(time series\). However, you could not change from a horizontal bar to a line chart.
        -   A different group by, if the chart group supports group by.
        -   A different trend by, if you have a time series chart.
        -   A different filter query
    If your modification would require a different chart group, you are notified. You may get a suggestion for a chart type in the same group, or an offer to start over.


## Result

You get a generated data visualization. This visualization is inside the Now Assist panel, if it will fit. You have the option to pop it out in that case. If the visualization would not fit, it is popped out by default.

![Result of the query showing a list of indicators.](../image/nowass-dv-list.png "Example of a generated data visualization")

-   **[Guidelines and example questions](../concept/example-questions-generating-dv.md)**  
This section shows guidelines and some typical questions you could ask in the Now Assist panel to generate data visualizations.
-   **[Limitations to generating data visualizations](../reference/limitations-generating-dv.md)**  
While Analytics Generation is designed to handle a wide range of queries and scenarios, certain cases are currently not supported or only partially supported.

**Parent Topic:**[Analytics Generation](../reference/analytics-assist-landing-page.md)

