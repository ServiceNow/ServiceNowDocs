---
title: Monitoring database performance through Application Insights
description: Maintain the health and performance of your database by monitoring the volume of database transactions and average response time through Application Insights.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Monitoring database performance through Application Insights

Maintain the health and performance of your database by monitoring the volume of database transactions and average response time through Application Insights.

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

You can detect anomalies and database performance issues by monitoring the database graphs on the **Session Info** tab.

Use the database graphs to monitor the following metrics:

-   Average response time
-   Volume of transactions by analyzing database throughput

You access the graphs by navigating to **All** &gt; **Application Insights** &gt; **Application Insights** &gt; **Session Info**.

-   Look for spikes that indicate delays in response time for each type of database operation \(deletes, inserts, updates, and selects\) in the **Average Database Response Time** graph. View a list of database transactions by selecting a data point in the spike, and then look for outliers in the response time. Review the source record to see whether the transaction can be optimized.
-   Look for spikes or periods of heavy usage for each type of database operation \(deletes, inserts, updates, and selects\) in the **Database Throughput** graph. View a list of database transactions by selecting a data point in the spike, and then look for outliers in SQL count and response time. Review the source record to see whether you can optimize the transaction.


**Parent Topic:**[Application Insights](application-insights.md)

