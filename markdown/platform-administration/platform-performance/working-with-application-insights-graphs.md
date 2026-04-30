---
title: Working with Application Insights graphs
description: View key performance metrics for your instance using Application Insights graphs.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Working with Application Insights graphs

View key performance metrics for your instance using Application Insights graphs.

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Application Insights provides time-series data in a collection of graphs that help you visualize the performance and health of your instance. The graphs are automatically refreshed every five minutes.

## Overview graphs

You can view a summary of the overall health and performance of your instance on the **Overview** tab. It provides in an aggregated instance-level view by combining metrics from the **Events**, **ECC Queue**, and **Session Info** tabs.

Use the overview graphs to do the following:

-   Analyze how metrics have been performing over time individually and in relation to each other.
-   View trends or patterns between different data sets by overlaying metrics and diagnostic events.
-   Closely and proactively monitor the instance when performing any impactful activity such as a system update or during periods of heavy user traffic.
-   Overlay diagnostic events to help you determine causation and correlation.
-   Compare metrics or focus on a specific metric by selecting which graph lines to display from the legend above the graph.
-   Change the time period by selecting a different day range from the date picker. The default value is 1 day, but you can also change the time period to 7 days or 30 days.
-   View the details for all metrics at a point in time by pointing your cursor anywhere on the graph.

    View node-level details for a metric by pointing your cursor and selecting a data point. The corresponding detail graph on the **Events**, **ECC Queue**, or **Session Info** tab is displayed.

-   Narrow the time range by selecting the left or right side of the time line below the graph and dragging across. Shift the time range by dragging this view along the axis.

## Detail graphs

Each graph on the **Events**, **ECC Queue**, and **Session Info** tabs provides a detailed view of metrics for one or more nodes.

Use the detail graphs to do the following:

-   Compare a specific metric to the median, 1-day moving average, or the 95th percentile value
-   View trends or patterns by overlaying metrics and diagnostic events
-   Determine whether performance degradation is happening on one node or across all nodes
-   View detailed statistics for each node to monitor system health over time

Detail graphs include the same controls as overview graphs but provide additional functionality.

-   See trends, issues, and system health for nodes and agents with similar performance values by selecting **Group By Performance**. If there are seven or more lines on the graph, this option is selected by default.
-   Overlay diagnostic events to help you determine causation and correlation.
-   Add a custom filter to display data for specific nodes. For example, display the average transaction time for nodes where the status is online.
-   Compare the performance of different nodes to the 1-day moving average by selecting which graph lines to display from the legend above the graph.

    The **1-Day Moving Average** line represents the average value across all nodes over one day.

-   Change the time period by selecting a different day range from the date picker. The default value is 1 day, but you can also change the time period to 7 days or 30 days.
-   View the details for an agent or node by pointing your cursor anywhere on the graph.

    Compare the metric to the following horizontal lines on the graph:

    -   **Median**: The middle value.
    -   **95th percentile**: The 95th percentile value. A metric with a data point above this line is likely a cause for concern.
    View a list of associated events or transactions within a 10-minute period by pointing your cursor and selecting a data point.

-   Narrow the time range by selecting the left or right side of the time line below the graph and dragging across. Shift the time range by dragging this view along the axis.

The median, average, and 95th percentile values for each node are displayed in the table below the detail graph.

-   To sort records in the list, select the column header.
-   To filter the list using a value in a field, right-click in the field and select **Show Matching** or **Filter Out**.
-   To group records in the list by label, select the column options menu and then select **Group by**.
-   To filter records in the list, select the column options menu and then select **Filter**. Enter a condition and value.

-   **[Application Insights overview graphs and metrics](overview-graphs-and-metrics.md)**  
The Application Insights overview graphs provide consolidated views of key metrics.
-   **[Application Insights detail graphs and metrics](detail-graphs-and-metrics.md)**  
The Application Insights detail graphs provide views of individual metrics at the node level.

**Parent Topic:**[Application Insights](application-insights.md)

