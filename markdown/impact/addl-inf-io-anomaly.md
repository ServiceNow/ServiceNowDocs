---
title: Anomaly insights
description: The reference topic gives additional information for anomaly charts.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-30"
reading_time_minutes: 4
keywords: [Anomaly details]
breadcrumb: [Overview of Instance Observer metrics, Instance Observer reference, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Anomaly insights

The reference topic gives additional information for anomaly charts.

## Additional information for anomaly

-   In Anomaly charts, the x axis represents time series and the y-axis represents the actual metrics per date range you select. Anomalies are denoted by red color code on the chart. Each red point represents the occurrence of an anomaly in the data. The specific placement of the red mark depend on the criteria or algorithm used to detect anomalies.
-   In case of node level performance chart \(like semaphore and node memory\), you must select the common grain for x axis \(1 minute roll up\) if you must tally the data between default and anomaly tab. Performance chart is represented at the node level, however, anomalies are aggregated at an instance level.
-   The anomalous points are selectable for semaphore and Node Memory max metrics in Anomaly chart that will be enabled with node metadata beyond the normal range. You must select **View detail** for the same. This Information will not reflect for non-anomalous points. In case of 10-min grain data, the anomaly is calculated based on 15-min average data point. Therefore, this will list all nodes beyond the range in the last 15 minutes.

## Aggregation level of each metric

<table id="table_q2n_2fx_t3c"><thead><tr><th>

Metric Name

</th><th>

Aggregation LevelDefault Chart

</th><th>

Aggregation LevelAnomaly Chart

</th><th>

Aggregation TypeDefault Chart

</th><th>

Aggregation TypeAnomaly Chart

</th></tr></thead><tbody><tr><td>

User Transaction Count

</td><td>

Instance

</td><td>

Instance

</td><td>

Sum

</td><td>

Sum

</td></tr><tr><td>

Average Server Response Time

</td><td>

Instance

</td><td>

Instance

</td><td>

Weighted Average

</td><td>

Weighted Average

</td></tr><tr><td>

SQL Response Time

</td><td>

Instance

</td><td>

Instance

</td><td>

Average

</td><td>

Weighted Average

</td></tr><tr><td>

Semaphore Default Mean

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Node Memory Max

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Semaphore Default Queue Depth

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Semaphore API Int In Use

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Semaphore API Int Queue Depth

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Semaphore AMB Send Queue Depth

</td><td>

Node

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Garbage Collection

</td><td>

Instance

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

CPU Time

</td><td>

Instance

</td><td>

Instance

</td><td>

Sum

</td><td>

Sum

</td></tr><tr><td>

Threads Running

</td><td>

Instance

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

InnoDBrowLock

</td><td>

Instance

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr><tr><td>

Slow Queries

</td><td>

Instance

</td><td>

Instance

</td><td>

Max

</td><td>

Max

</td></tr></tbody>
</table>## Roll up logic

-   **User Transaction Count \| Average Server Response Time \| SQL Response Time**
    -   When selected date range is **less than or equal to 7 days**, metric values are rolled up at the 1-minute level.
    -   When selected date range is **greater than 7 days but less than 30 days**, metric values are rolled up at the 10-minute level.
    -   When selected date range is **greater than 30 days**, metric values are rolled up at the 1-hour level.
    -   Default chart metric values will **not match** with the anomaly chart metric values when data is rolled up at the 10-minute level, because the default chart uses a 10-minute metric value average whereas the anomaly chart uses a 15-minute moving average.
    -   Default chart metric values will **match** with the anomaly chart metric values when aggregation is at the 1-minute level for **User Transaction Count** and **Average Server Response Time**. Values will not match for **SQL Response Time** because the default chart uses **Average** aggregation whereas the anomaly chart uses **Weighted Average**.
    -   Anomaly chart data is available for a **maximum of 28 days** from the current date.
-   **Other metrics**
    -   When selected date range is **less than or equal to 24 hours**, metric values are rolled up at the 1-minute level.
    -   When selected date range is **greater than 1 day but less than 7 days**, metric values are rolled up at the 5-minute level.
    -   When selected date range is **greater than 7 days but less than 30 days**, metric values are rolled up at the 10-minute level.
    -   When selected date range is **greater than 30 days but less than 60 days**, metric values are rolled up at the 1-hour level.
    -   When selected date range is **greater than 60 days but less than 90 days**, metric values are rolled up at the 2-hour level.
    -   When selected date range is **greater than 90 days but less than 120 days**, metric values are rolled up at the 4-hour level.
    -   When selected date range is **greater than 120 days but less than 150 days**, metric values are rolled up at the 8-hour level.
    -   When selected date range is **greater than 150 days but less than 180 days**, metric values are rolled up at the 12-hour level.
    -   Default chart metric values will not match with anomaly chart metric values for node-level metrics, because the default chart aggregates at the node level whereas the anomaly chart aggregates at the instance level. Note that the aggregation type \(Max\) remains the same across both charts for these metrics.
    -   Anomaly chart data is available for a maximum of 28 days from the current date.

**Parent Topic:**[Overview of Instance Observer metrics](../concept/instance-observer-ovr-metric.md)

**Related topics**  


[Instance Data Replication](instance-observer-metrics.md)

[Instance Observer reports overview](i-o-reports.md)

[Feature availability based on package](io-feature-availability.md)

