---
title: Monitoring API performance
description: Monitor the performance of your integrations with the Application Insights API metrics graphs. You can monitor how these integrations are performing over time and how those APIs perform over time.
locale: en-US
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitor, Platform performance, Maintain and monitor, Administer]
---

# Monitoring API performance

Monitor the performance of your integrations with the Application Insights API metrics graphs. You can monitor how these integrations are performing over time and how those APIs perform over time.

Starting with the Zurich release, Application Insights is no longer deployed, enhanced, or supported. It is recommended to evaluate the [Overview of Instance Observer](https://www.servicenow.com/docs/access?context=io-overview&version=zurich&pubname=zurich-impact&ft:locale=en-US) product available with the ServiceNow Impact packages. Work with your Account team to review Impact packages.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

**Note:** admin and sn\_app\_insights.admin are the roles required to experience this improved visibility.

When you select the **API metrics** tab, the list of endpoints is displayed in tabular format. For each API endpoint and request method \(GET, POST, PUT, PATCH, and DELETE\), the following metrics are captured:

-   Response time \(ms\)
-   Requests per minute
-   Payload size \(bytes\)
-   Failure rate \(%\)

-   **[Configure API metrics](../task/configure-api-metrics.md)**  
Configure the API metrics feature in Application Insights to enable instance administrators to proactively monitor instance performance.

**Parent Topic:**[Application Insights](application-insights.md)

