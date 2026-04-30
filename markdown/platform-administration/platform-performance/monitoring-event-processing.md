---
title: Monitoring event queue efficiency through Application Insights
description: You can monitor event queue performance in Application Insights by comparing and analyzing the rate at which events are logged and processed.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Monitoring event queue efficiency through Application Insights

You can monitor event queue performance in Application Insights by comparing and analyzing the rate at which events are logged and processed.

You can monitor the relationship between events logged and events processed by viewing the **Events** graph on the **Overview** tab.

Use the **Events** graphs to do the following:

-   Monitor the rate of incoming events
-   Monitor the rate of processed events
-   Detect anomalies in processing events

You access the Events graphs by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Overview**.

-   Look for bottlenecks by comparing the **Events Logged** and **Events Processed** totals. A spike in the **Events Logged** number without a corresponding spike in the **Events Processed** number indicates a problem with processing events.
-   A high and consistent spike in both the **Events Logged** and **Events Processed** figures indicates the system is receiving and processing a large load of events. Look for loops or conditions that might be causing a continuous stream of incoming events.

Dig deeper into potential performance issues by drilling down to analyze issues at the node-level in the detail graphs.

-   Analyze the processing of events over time by comparing processed events to the **1-Day Moving Average** shown on the **Events Processed** graph.
-   Look for patterns in event logging over time. Determine whether the same spike is happening at the same time every week.
-   Look for correlations between the count of events logged and system activities by overlaying diagnostic events on the graph. For example, if you see a spike in the Events Logged number and you notice that it coincides with the installation of an update set, you can investigate the update set to determine why it caused the spike in events logged.
-   Investigate the cause of an issue by selecting a data point at the start of spike to view a list of events created 5 minutes before and 5 minutes after the issue.
-   Analyze the rate of incoming events by comparing logged events to the **1-Day Moving Average** total on the **Events Logged** graph.
-   Identify potential performance issues by comparing metrics for individual event queues in the Event Queue table.
    -   Focus on a 1-day, 7-day, or 30-day period by selecting a day range.
    -   Identify which queue had the most logged events by sorting on the **Logged events in range** column. An event is logged when it is inserted into the Events \[sysevent\] table.
    -   Identify which queue had the most queued events by sorting on the **Queued events in range** column. An event is queued when it is assigned to a specific event queue in the Events \[sysevent\] table.
    -   Identify which queue had the most unprocessed events by sorting on the **Unprocessed events in range** column.
    -   Identify which queue took the most amount of time processing events in the selected day range by sorting on the **Processing duration in range** column.
    -   Identify which queue processed the most events in the selected day range by sorting on the **Processed events in range** column.
    -   Identify which queue took the most amount of time processing events on average in the selected day range by sorting on the **Average processing duration in range** column.

**Parent Topic:**[Application Insights](application-insights.md)

