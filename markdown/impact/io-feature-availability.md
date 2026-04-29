---
title: Feature availability based on package
description: The table outlines the access permissions for Performance Analytics features across production and sub production instances.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-06"
reading_time_minutes: 2
keywords: [Feature availability, Impact Package]
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Instance Observer, Platform Health, Using Impact, Impact]
---

# Feature availability based on package

The table outlines the access permissions for Performance Analytics features across production and sub production instances.

Each feature is evaluated against three license tiers — Total, Advanced, and Guided — with values indicating full access \(Y\), restricted access \(lock\), or feature unavailability \(N/A\). It also covers anomaly-based alert configurations and the adjusted range function for fine-tuning anomaly tolerance thresholds.

|Entry through Performance|Instance|Total|Advanced|Guided|
|-------------------------|--------|-----|--------|------|
|Instance level metrics|
| |Production|Y|Y|Y|
| |Sub production|Y|Y|Y|
|Node level metrics|
| |Production|Y|Y|Y|
| |Sub production|Y|Y|Y|
|Anomaly|
| |Production|Y|lock|lock|
| |Sub production|N/A|N/A|N/A|
|Instance alert card \(with anomaly\)|
| |Production|Y|lock|lock|
| |Sub production|N/A|N/A|N/A|
|Node alert card|
| |Production|Y|lock|lock|
| |Sub production|N/A|N/A|N/A|
|User session instance alert card \(without anomaly\)|
| |Production|Y|Y|lock|
| |Sub production|Y|Y|lock|
|User session node alert card|
| |Production|Y|Y|lock|
| |Sub production|Y|Y|lock|

-   Anomalies and their respected anomaly based alert are only valid for production instance. This is available for Total package customers.
-   Node level alerts are configured through performance page for transaction count, server response time, and user session logged in metrics. It is not included in config alert section. This is available currently for production instances and Total package customers in current release except user session logged in metrics.

## Adjusted range \(anomaly tolerance\)

Allows you to adjust an anomaly tolerance by manipulating the percentage range of a normal distribution that involves modifying the standard deviation or variance of the data distribution. This function enables you to increase or decrease the deviation of the data by selecting the percentage from drop down of the **Adjusted range**. This would widen or narrow the range considered as normal. A larger standard deviation means a wider tolerance for anomalies, while a smaller one means a narrower tolerance. Altering the range of a normal distribution directly impacts what the system identifies \(predefined algorithms\) as anomalous.

-   This capability will act as an AND condition with the anomaly persistence condition under Anomaly based condition.
-   If you want the system identified anomalous points, keep the default range as it is. For metrics like Transaction count, Server response time, Database response time by default value is 0, whereas for Semaphore mean and Node memory it's 50%.
-   If the alert is saved with the adjusted range, the condition remains until you change it.
-   When you hover over the chart following the alert, the normal range and adjusted data range distribution \(upper boundary and lower boundary\) will be displayed for quick comparison.
-   If the lower boundary value exceeds the upper boundary, the range width will prevent the lower limit from surpassing the upper limit.

**Parent Topic:**[Overview of Instance Observer metrics](../concept/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Data Replication](instance-observer-metrics.md)

[Instance Observer reports overview](i-o-reports.md)

[Anomaly insights](addl-inf-io-anomaly.md)

