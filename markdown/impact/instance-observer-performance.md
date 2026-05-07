---
title: Performance
description: Monitor all your instances 24x7 in one place with near real-time metrics and alerts on performance and availability in Instance Observer. Generate various charts of overview Instance Health and Performance Metrics and drill down into specific data points with recommended troubleshooting.​
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Performance

Monitor all your instances 24x7 in one place with near real-time metrics and alerts on performance and availability in Instance Observer. Generate various charts of overview Instance Health and Performance Metrics and drill down into specific data points with recommended troubleshooting.​

Make data-driven decisions based on your users, platform, and applications​, access to near real-time and historical instance performance telemetry, and ​proactively visualize instance performance telemetry across instances with point-in-time metadata​.

## Key benefits

-   View historical trends of performance data.
-   Identify and investigate performance anomalies.
-   View specific jobs and transactions running at a point in time.
-   Access a deep dive into selected performance metrics

## Performance metrics

The **Performance** tab lists many metrics for several key system components. These metrics help in collecting data about your instances, which aids in monitoring the performance of your instances. The metrics are:

-   Transactions or Response Times
-   Database
-   Semaphores
-   Event Queues
-   ECC Queue
-   Emails
-   Schedulers
-   Job Details
-   Node Health
-   Host Health
-   Standby Replica Log
-   Read Replica Log
-   Chat Details
-   Database Growth
-   Cluster Details
-   Load Balancer
-   User Information
-   Instance Data Replication

## Access Instance Observer Performance page

1.  To access the Instance Observer page, navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer**
2.  From the **Performance** menu, select the metric for the key system component.

-   **[Getting started with Performance charts](../task/io-getting-started-perf-charts.md)**  
Follow these steps to generate Performance charts using Instance Observer.
-   **[Anomalies detection](../task/anomalies-detection.md)**  
Instance Observer proactively detects the anomalies for cyclical or non-cyclical metrics under the performance chart for the Impact Total package on production instances. Anomalies represent metrics outliers based on historical patterns. Every anomaly may not represent an issue, but, notifies you and you decide the criticality and configure alerts, accordingly.
-   **[Analyze job details for long pending jobs](../task/io-long-pending-job-alert-card.md)**  
Stay ahead of job delays by identifying and acting on jobs that breach predefined lateness thresholds. The Long Pending Jobs alert card tracks pending jobs by lateness duration, so you can act on the pending jobs before they affect the downstream workflows and miss the SLAs.

**Parent Topic:**[Monitoring instance health with Instance Observer](io-overview.md)

