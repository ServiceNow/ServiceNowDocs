---
title: Monitoring platform performance
description: The ServiceNow AI Platform includes tools that administrators can use to monitor platform performance. Monitoring platform performance enables administrators to proactively identify and solve issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/platform-performance/monitoring-platform-performance.html
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Platform performance, Maintain and monitor, Administer]
---

# Monitoring platform performance

The ServiceNow AI Platform includes tools that administrators can use to monitor platform performance. Monitoring platform performance enables administrators to proactively identify and solve issues.

## Overview of monitoring platform performance

Administrators have access to various logs and dashboards that can be used to monitor how a ServiceNow AI Platform instance is performing. These logs and dashboards can be accessed and reviewed at any time to identify indicators of performance degradation. If you notice abnormally slow response times or an unusually high volume of cancelled transactions, you might have performance issues that need to be resolved.

-   **[Reviewing transaction logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/c_TransactionLogResponseTimes.md)**  
The instance automatically logs the vital statistics of every transaction that it processes, and that information is available to you as an administrator. Reviewing transaction logs can help identify latency and performance issues.
-   **[Reviewing response time on forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/c_ResponseTimeOnForms.md)**  
A response time indicator \(clock\) appears at the end of many forms and lists.
-   **[Transaction call chains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/transaction-call-chains.md)**  
Identify and debug the root causes for a problematic transaction by recording, and then reviewing, its call chain. A call chain consists shows the ordered series of scripts executed during the life cycle of a transaction.
-   **[Thread performance monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/c_MonitorPerformanceOnThreads.md)**  
The instance tracks the performance of individual threads, which administrators can view in the transaction log.
-   **[Monitoring instance usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/usage-analytics-module-subscription.md)**  
You can track application usage on your instance through the Application Usage Overview and the ServiceNow Store Usage overview dashboards.
-   **[Application Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/application-insights.md)**  
The ServiceNow® Application Insights application available in the ServiceNow Store, provides a centralized location where you can visualize and monitor system health.

**Parent Topic:**[Maintaining and monitoring the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/maintain-monitor-now-platform.md)

