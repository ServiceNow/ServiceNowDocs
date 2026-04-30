---
title: Monitoring database performance through Application Insights
description: Maintain the health and performance of your database by monitoring the volume of database transactions and average response time through Application Insights.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Monitoring database performance through Application Insights

Maintain the health and performance of your database by monitoring the volume of database transactions and average response time through Application Insights.

You can detect anomalies and database performance issues by monitoring the database graphs on the **Session Info** tab.

Use the database graphs to monitor the following metrics:

-   Average response time
-   Volume of transactions by analyzing database throughput

You access the graphs by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Session Info**.

-   Look for spikes that indicate delays in response time for each type of database operation \(deletes, inserts, updates, and selects\) in the **Average Database Response Time** graph. View a list of database transactions by selecting a data point in the spike, and then look for outliers in the response time. Review the source record to see whether the transaction can be optimized.
-   Look for spikes or periods of heavy usage for each type of database operation \(deletes, inserts, updates, and selects\) in the **Database Throughput** graph. View a list of database transactions by selecting a data point in the spike, and then look for outliers in SQL count and response time. Review the source record to see whether you can optimize the transaction.


**Parent Topic:**[Application Insights](application-insights.md)

