---
title: Application Insights
description: The ServiceNow Application Insights application available in the ServiceNow Store, provides a centralized location where you can visualize and monitor system health.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application Insights

The ServiceNow® Application Insights application available in the ServiceNow Store, provides a centralized location where you can visualize and monitor system health.

Starting with the Xanadu release, Application Insights is being deprecated and will no longer be available on the Store for installation. Support will continue until Zurich release. It is recommended to evaluate the [Impact Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=yokohama&pubname=yokohama-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview

Application Insights enables you to proactively manage the health and performance of your instances. Application Insights provides time-series graphs and data that enable you to visualize performance trends, see correlated events, and access resources to take corrective action.

You can access Application Insights by logging in as a user with the admin or sn\_app\_insights.admin role and navigating to **All** &gt; **Application Insights** &gt; **Application Insights**.

## Key benefits

-   View the health and performance of all your instance nodes in one place.
-   Detect anomalies or deviations in instance performance.
-   Take corrective actions and resolve performance issues on your own without having to involve an administrator.
-   Analyze the root cause of a performance issue by determining the context and correlation with system events such as an upgrade or application install.
-   Proactively mitigate potential risks to the system. Identify and pre-empt risks that would otherwise lead to issues.

![Application Insights home page](../image/app-insights-overview.png "Application Insights")

-   **[Working with Application Insights graphs](working-with-application-insights-graphs.md)**  
View key performance metrics for your instance using Application Insights graphs.
-   **[Monitoring users and transaction performance through Application Insights](monitoring-transactions-and-sessions.md)**  
Maintain the health and performance of your instance by monitoring key metrics related to users and transactions through the Application Insights Users and Transactions graph.
-   **[Monitoring semaphore queue efficiency through Application Insights](monitoring-semaphore-activity.md)**  
Monitor semaphore queue efficiency by tracking the queue depth and number of rejected transactions through the Application Insights semaphore graphs.
-   **[Monitoring database performance through Application Insights](monitoring-database-performance.md)**  
Maintain the health and performance of your database by monitoring the volume of database transactions and average response time through Application Insights.
-   **[Monitoring event queue efficiency through Application Insights](monitoring-event-processing.md)**  
You can monitor event queue performance in Application Insights by comparing and analyzing the rate at which events are logged and processed.
-   **[Monitoring MID server performance through Application Insights](monitoring-mid-server.md)**  
You can monitor the performance of a MID Server by tracking the status of entries in the ECC queue.
-   **[Solving slow patterns](application-insights-slow-patterns.md)**  
You can identify, prioritize, and troubleshoot performance issues related to slow patterns in your instance.
-   **[Troubleshoot a scheduled job through Application Insights](../task/troubleshoot-a-scheduled-job.md)**  
Identify a scheduled job that is causing slow performance or running more often than necessary through the Scheduled Jobs table.
-   **[Monitoring API performance](api-metrics.md)**  
Monitor the performance of your integrations with the Application Insights API metrics graphs. You can monitor how these integrations are performing over time and how those APIs perform over time.
-   **[Application Insights p1 prediction model](app-insights-prediction.md)**  
Application Insights enables you to receive a warning when your instance is about to experience a priority 1 \(p1\) event.
-   **[Configure Application Insights thresholds](../task/config-app-insights-thresholds.md)**  
Configure conditional thresholds to trigger an alert that notifies you when one or more metrics, such as response time, is outside of the desired range.
-   **[Configure Application Insights threshold triggers](../task/conf-app-insights-thresh-triggers.md)**  
Detect that a threshold has been exceeded and create a trigger to perform a sequence of actions.
-   **[Install Application Insights](../task/install-application-insights.md)**  
You can install the Application Insights application \(sn\_app\_insights\) if you have the admin role.
-   **[Application Insights properties](../reference/app-insights-properties.md)**  
These system properties control the behavior of the Application Insights application.
-   **[Application Insights roles](../reference/application-insights-roles.md#)**  
Application Insights is installed with these roles.

**Parent Topic:**[Monitoring platform performance](monitoring-platform-performance.md)

