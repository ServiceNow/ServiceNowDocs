---
title: Reviewing top processes by resource usage in incident investigation with DEX
description: Reviewing the top processes by CPU and memory usage on Digital End-User Experience \(DEX\) monitored devices helps you identify processes causing device issues.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Incident diagnostics and suggested resolutions, DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Reviewing top processes by resource usage in incident investigation with DEX

Reviewing the top processes by CPU and memory usage on Digital End-User Experience \(DEX\) monitored devices helps you identify processes causing device issues.

The Top processes by CPU and Memory usage section in the **Investigation** tab of incident records for DEX monitored devices displays the processes using the most CPU and memory resources on a device. When expanded, this section shows a graph with data points for snapshots captured during the selected time range. The X-axis of the graph shows the time and the Y-axis shows the CPU and memory usage percentages.

**Note:** When a device is offline, the graph displays data points with a value of zero or shows no data points.

Every snapshot captures the top 10 processes by CPU usage, top 10 processes by memory usage, and their combined average usage percentages. Selecting a data point on the graph shows the data from the corresponding snapshot. By default, the graph displays the latest snapshot data.

## Time ranges for viewing top processes by resource usage

The Timeframe drop-down list provides different time range options for viewing snapshots of the top resource-using processes. Selecting a time range and then selecting **Go** displays the graph for the chosen period.

By default, the graph shows the date and time of the latest snapshot. Selecting a data point on the graph shows the corresponding date and time of that snapshot.

Some time ranges display individual snapshot data on the graph, while others display aggregated data.

-   The following time ranges display non-aggregated data:
    -   **At incident creation**: Snapshots are captured every 30 minutes from six hours before the incident to incident creation time. This time range option is selected by default.

        **Note:** The graph doesn't show snapshots for incidents created more than seven days ago.

    -   **Last 6 hours**: Snapshots are captured every 30 minutes for the last six hours. In addition to automated snapshots, selecting the Refresh icon ![](../image/icon-dex-refresh.png) captures the latest snapshot on demand.

        **Note:** The Refresh icon is enabled only for the **Last 6 hours** time range and when the device is online.

    -   **Custom**: Snapshots are captured every 30 minutes for a custom date and time range within the last seven days, selected using the **Day** and **Slot** drop-down lists.
-   Time ranges displaying aggregated data:

    -   **Last 12 hours**: Data is captured every 30 minutes and aggregated hourly.
    -   **Last 24 hours**: Data is captured every 30 minutes and aggregated every two hours.
    -   **Last 2 days**: Data is captured every 30 minutes and aggregated every four hours.
    -   **Last 7 days**: Data is captured every 30 minutes and aggregated every 24 hours.
    The graphs for time ranges showing aggregated data display data points for each aggregation interval.

    **Note:** Availability of data points for aggregated time ranges depends on how long the device is connected and the aggregation period for that time range. For example, if a device was connected less than 24 hours ago, data points might be available for shorter time ranges such as **Last 24 hours** or **Last 2 days**. However, for the **Last 7 days** time range with an aggregation interval of 24 hours, the graph shows no data points.


## Average CPU and memory usage calculation for top processes

Each snapshot captures the top processes by CPU and memory usage. The process name, CPU usage percentage or memory usage value \(in MB\), and the latest process ID \(PID\) are shown for every process. The combined average CPU and memory usage percentages for these processes are also displayed.

For time ranges that show individual snapshot data, the combined average memory and CPU usage percentages are calculated using the following formulas:

-   Average CPU usage percentage = `Sum of CPU usage percentages by top 10 processes / 10`
-   Average memory usage percentage = `((Total memory used by top 10 processes / total device memory) * 100) / 10`

For time ranges that display snapshots of aggregated data, the average CPU and memory usage across all data points is calculated based on the following data:

-   Graph data aggregation based on CPU and memory usage percentages: The average CPU and memory usage percentages by the top 10 processes in each individual snapshot during the aggregation period are combined and displayed in the corresponding data point on the graph.

    For example, when you select the **Last 12 hours** time range, data is aggregated hourly and shown as a data point on the graph. If three individual snapshots are captured in an hour with average memory usage of 88.88%, 92.97%, and 90.53% respectively, then the aggregated average memory usage for that data point is 90.79%.

-   Table data aggregation based on process name: If the same process is listed more than once in the top processes tables across multiple snapshots within the aggregation period, its CPU usage or memory usage values are combined. The process with its combined usage value is then listed as a single entry for the corresponding data point. As a result, the top process tables might show fewer than 10 unique processes.

    For example, in the **Last 12 hours** time range with hourly data aggregation, Google Chrome Helper is listed as a top memory-using process in three snapshots within an hour. The process name and memory usage values from the three snapshots are combined into a single table entry. The Top 10 processes by Memory table might then display fewer than 10 processes.


