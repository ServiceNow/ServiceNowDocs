---
title: Monitoring semaphore queue efficiency through Application Insights
description: Monitor semaphore queue efficiency by tracking the queue depth and number of rejected transactions through the Application Insights semaphore graphs.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Monitoring semaphore queue efficiency through Application Insights

Monitor semaphore queue efficiency by tracking the queue depth and number of rejected transactions through the Application Insights semaphore graphs.

You can monitor performance of the semaphore queues in your instance by comparing the semaphore queue depth and rejection count in the semaphore graphs on the **Overview** tab.

Through the semaphore graphs, you can monitor the following metrics:

-   The semaphore queue depth, which enables you to help prevent backlogs
-   Rejection counts, which enables you to identify processing bottlenecks

Semaphores control the number of simultaneous transactions that can execute on a node. Low available semaphores indicate that the instance is running close to full transaction capacity. Incoming transactions will wait until the semaphores are available.

You access the semaphore graphs by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Overview**.

-   Monitor the load level by comparing the queue depth to the queue depth limit that appears as a red line on each semaphore graph.
-   Look for correlations or trends by comparing the queue depth metric to the rejection count metric over time.

Dig deeper into semaphore processing efficiency by drilling down to analyze issues at the node-level in the detail graphs on the **Session Info** tab.

-   Look for spikes in the queue depth graphs. A high transaction count indicates the node might be overloaded. Select a data point in the detail graph to view a list of transactions. In the table, look for long-running transactions on the semaphore and stop them. Reduce the transaction count if the queue depth is consistently high.
-   Look for spikes in the rejection count graphs. A high rejection count indicates an unexpected proliferation in calls. If the queue depth is reached, all subsequent requests are rejected, which results in a rejected requests \(HTTP 429\) error message. Reduce the number of calls or stop long-running transactions that might be backing up the queue.

**Parent Topic:**[Application Insights](application-insights.md)

