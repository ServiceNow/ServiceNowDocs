---
title: Monitoring MID server performance through Application Insights
description: You can monitor the performance of a MID Server by tracking the status of entries in the ECC queue.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Monitoring MID server performance through Application Insights

You can monitor the performance of a MID Server by tracking the status of entries in the ECC queue.

Application Insights enables you to monitor the performance of the ECC queue, which is a communication log between your instance and an MID Server. For details, see [MID Server ECC Queue](https://www.servicenow.com/docs/access?context=ecc-queue-mid-server&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

You can monitor the relationship between the number of ready, processing, and processed records by viewing the ECC queue graphs. Use the ECC queue graphs to monitor the following:

-   Load handling, viewing the number of entries in your ECC input and output queues
-   Processing efficiency, by tracking entries in the ready, processing, and processed states in both of the ECC queues

You access the graphs by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Overview**.

-   Look for a spike in the ready state without a corresponding spike in the processing and processed states. This pattern indicates a potential problem with reading the queue.
-   Look patterns or trends that indicate worsening performance over time. A steady increase in ready entries with a flat or declining processing rate indicates a bottleneck or performance issue that merits further investigation.

Dig deeper into potential performance issues by drilling down to analyze issues for an agent or group of agents in the detail graphs.

-   Make the detail graphs easier to read by grouping agents with similar performance metrics by selecting the **Group by Performance** check box. Look for groups with higher counts or spikes in the selected time range. View and compare trend lines for a group of agents in a separate graph by selecting a data point. Look for anomalies by comparing the individual agents to the **1-Day Moving Average** number.
-   Analyze ECC queue efficiency by tracking the number of entries in the ready, processing, and processed states over time. Output metrics measure the number of jobs leaving the instance. Input metrics measure the number of jobs sent to the instance from the MID Server or another system.

**Parent Topic:**[Application Insights](application-insights.md)

