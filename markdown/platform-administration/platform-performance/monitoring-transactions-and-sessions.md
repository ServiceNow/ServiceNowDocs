---
title: Monitoring users and transaction performance through Application Insights
description: Maintain the health and performance of your instance by monitoring key metrics related to users and transactions through the Application Insights Users and Transactions graph.
locale: en-US
release: xanadu
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Monitoring users and transaction performance through Application Insights

Maintain the health and performance of your instance by monitoring key metrics related to users and transactions through the Application Insights Users and Transactions graph.

You can detect anomalies and performance deviations in your instance by monitoring the relationship between users, transactions, and average transaction response time in the Users and Transactions graph on the **Overview** tab.

Use the Users and Transactions graph to do the following:

-   Monitor the performance of transactions on your instance.
-   View the transaction load on your instance.
-   Track the number of logged-in users.

You access the graph by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Overview**.

-   Analyze system slowness by comparing the **Transaction Count** and **Logged in Users** figures. Note that a spike in the **Transaction Count** that has a corresponding spike in the **Logged in Users** count might be a false alarm.
-   Determine whether a heavy transaction load is affecting system performance by comparing the **Average Response Time** figure to the **Transaction Count** amount. Look for spikes in the **Transaction Count** amount relative to the **Average Response Time** figure.

Dig deeper into a potential performance issue by drilling down to analyze issues at the node-level in the detail graphs on the **Session Info** tab.

-   Look for spikes that indicate a bottleneck or loop condition in the **Transaction Count** detail graph. An upward trend line indicates the system is becoming overloaded. Select a data point on the graph to view a list of transactions in a 10-minute range.
-   Look for spikes that indicate times of heaviest traffic on the instance in the **Logged in Users** detail graph. Monitor the trend lines to determine when the system is busiest.
-   Determine whether performance degradation is happening on one node, across all nodes, or on a set of nodes that are consolidated using the **Group by Performance** option. Compare the node metrics to the **1-Day Moving Average** amount. If you don’t see any obvious issues, look for anomalies in execution counts or high execution times on the **Slow Patterns** tab. If you see both, start your investigation there.

**Parent Topic:**[Application Insights](application-insights.md)

