---
title: Monitoring queues in Instance Data Replication
description: Monitor the replication record queue, message produced queue, message consumed queue, and the messages processed for all replications sets through the Instance Data Replication \(IDR\) Queue Dashboard.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Monitoring queues in Instance Data Replication

Monitor the replication record queue, message produced queue, message consumed queue, and the messages processed for all replications sets through the Instance Data Replication \(IDR\) Queue Dashboard.

## Accessing the IDR Queue Dashboard

Users with the admin or idr\_admin role can access the dashboard.

Access the IDR Queue Dashboard by navigating to **Instance Data Replication** &gt; **Queue Dashboard**.

## IDR Queue Dashboard

The IDR Queue Dashboard enables you to monitor the following:

-   IDR Queued Producer Records which are hourly records queued for all tables over a 24-hour time period.
-   Outbound Messages Remaining which are messages remaining in the replication queue that are not yet sent to the message queue.
-   Outbound Messages Processed which are messages produced from this instance to the message queue.
-   Inbound Messages Remaining which are messages remaining in the message queue, that have not yet been processed.
-   Inbound Messages Processed which are messages consumed on this instance.

In any chart, select **Last 24 Hours** or **Last 5 Days** as the time period. For the 24-hour period, the number of messages is per hour. For the 5-day period, the number of messages is per day.

Select the legend link under the chart to exclude that data source.

![Queue dashboard.](../image/idr-queue-dashboard.png "IDR Queue Dashboard")

## IDR Queued Producer Records

With the IDR Queued Producer Records chart, you can see the number of records queued for each table over an hourly or daily period. It shows which tables account for the highest amount of traffic within IDR over time. Use this chart to identify activity spikes that cause predictable performance lags on the consumer instance.

For example, if you see that a large spike of activity occurs every day at 3:00 a.m. due to a business rule on a table, you should expect a performance lag to occur on the consumer around that time.

Select **All Tables** or a specific table. Position your cursor over a point in the chart to see the queue count and tables for that point.

## Outbound Messages Remaining

With the Outbound Messages Remaining chart, you can determine whether a producer instance is catching up to real-time replication after a large spike in activity.

When replication is working correctly, the messages remaining count should be very low. If there is a spike in activity, you can expect a large value. For example, when a business rule is changing tens of thousands of records within a minute.

You can also expect messages remaining to decrease over time as the jobs process the messages.

If the messages remaining count continues to grow without resolution, it might indicate:

-   An issue processing the messages. For example, the **IDRProducerJob** is not running, or cannot send messages to the message queue.
-   The instance is recording changes faster than IDR can produce them.

Select **All Sets** or a specific set. Position your cursor over a point in the chart to see the message count and replication set name for that point.

## Outbound Messages Processed

With the Outbound Messages Processed chart, you can see the flow of records from a producer instance to the message queue over time.

Trends for messages processed and the messages remaining over time indicates if replication is recovering from a lag or if there are issues sending data to the message queue.

Along with the Data Replication Queued Producer records chart, you can see if the instance is sending data. If your instance has queued records that are not being sent, it might indicate:

-   The instance is not able to run the producer job. For example, due to other resource-intensive processes running on the instance and all worker threads being busy.
-   There is an issue connecting to the message queue.

To see the message count and replication set name for a graph point, select **All Sets** or a specific set and position your cursor over a point in the chart.

## Inbound Messages Remaining

With the Inbound Messages Remaining chart, you can determine whether a consumer instance is catching up to real-time replication after a large spike in activity.

You can expect a temporary large value when there is a spike in activity. The value normally decreases as the messages are processed.

If this value continues to grow without resolution, it might indicate:

-   An issue processing the messages. For example, the **IDRConsumerJob** is not running, or cannot read messages from the message queue.
-   The instance is recording changes faster than IDR can consume them.

Select **All Sets** or a specific set. Position your cursor over a point in the chart to see the message count and replication set name for that point.

## Inbound Messages Processed

With the Inbound Messages Processed chart, you can see the flow of records for each consumer set over time.

Use the inbound messages chart to determine which replication sets have the most traffic and see trends for messages processed and the messages remaining.

If the producer is sending records to the message queue and the consumer is not processing them, it might indicate issues with the producer or the consumer instance.

Position your cursor over a point in the chart to see the message count and replication set name for that point.

**Parent Topic:**[Administering Instance Data Replication](administering-instance-data-replication.md)

**Related topics**  


[Manage consumer access to replication data in Instance Data Replication](../task/approve-consumer.md)

[Comparing replicated data between instances in Instance Data Replication](comparing-replicated-data.md)

[Deploying a replication configuration from one instance to another in Instance Data Replication](copying-replication-configuration.md)

[Cloning options with Instance Data Replication](cloning-with-instance-data-replicaton.md)

[Monitoring replication status in Instance Data Replication](instance-data-replication-dashboard.md)

[Avoiding insert and update errors in Instance Data Replication](preventing-insert-update-errors.md)

[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

