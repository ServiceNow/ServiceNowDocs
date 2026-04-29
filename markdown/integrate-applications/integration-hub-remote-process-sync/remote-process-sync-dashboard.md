---
title: Remote Process Sync Dashboard
description: View detailed statistics for your Remote Process Sync integrations. The Remote Process Sync Dashboard helps you monitor the health and performance of RPS by collecting and visualizing metrics such as records processed, queue sizes, processing times, and error states.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Remote Process Sync Dashboard

View detailed statistics for your Remote Process Sync integrations. The Remote Process Sync Dashboard helps you monitor the health and performance of RPS by collecting and visualizing metrics such as records processed, queue sizes, processing times, and error states.

The Remote Process Sync Dashboard provides visibility into your Remote Process Sync integration performance. Use this dashboard to:

-   Monitor remote systems and queue health
-   Track record processing metrics
-   Identify performance bottlenecks
-   Troubleshoot integration issues

The dashboard consists of three tabs: **Overview**, **Inbound Queue**, and **Outbound Queue**

## Before you begin

-   You must install the plugin com.glide.hub.process.sync.dashboard to be able to view the Remote Process Sync Dashboard.
-   The [glide.hub.process.sync.record.successful.status](../reference/remote-process-sync-system-properties.md) property must be set to true for data to show on this dashboard.

To access the Remote Process Sync Dashboard, navigate to **All** &gt; **Integration Hub** &gt; **Dashboards** &gt; **Remote Process Sync Dashboard**. You must have the integration\_admin or admin role to view the dashboard.

## Overview tab

The Overview tab shows high-level health metrics and processing trends.

![Overview tab of Remote Process Sync Dashboard](../images/rps-dashboard-overview.png)

The Overview tab includes these components:

1.  Remote systems in error: Count of remote systems where the inbound or outbound status is marked as Error.
2.  Inbound queues in error: Count of inbound queue records with state = Error.
3.  Outbound queues in error: Count of outbound queue records with state = Error.
4.  Outbound Records Processed: Line graph showing the count of outbound queue records processed over the last 24 hours.
5.  Inbound Records Processed: Line graph showing the count of inbound queue records processed over the last 24 hours.

## Inbound Queue tab

The Inbound Queue tab shows detailed metrics for records being synchronized from remote systems into ServiceNow.

![Inbound Queue tab of Remote Process Sync Dashboard](../images/rps-dashboard-inbound-queue.png)

Use the **Record Processing Overview** dropdown to filter metrics by specific process events \(for example, Issue Created, Incident Updated\), or select **All Process Events** to view aggregate metrics.

The Inbound Queue tab includes these components:

1.  Records processed: Count of inbound records processed within the selected time range. Select from last minute, last hour, or last day using the dropdown.
2.  Records in queue: Current count of unprocessed records in the inbound queue.
3.  Avg. processing times over 24h: Average time \(in milliseconds\) to process inbound records over the last 24 hours.
4.  Latest time in queue: Time elapsed since the most recent record was added to the inbound queue.
5.  Last processed time: Time elapsed since the last record in the inbound queue was processed.
6.  Processing Times Over Last 24h: Line graph showing the processing time \(Subflow Runtimes\) for inbound records over the last 24 hours.

## Outbound Queue tab

The Outbound Queue tab shows detailed metrics for records being synchronized from ServiceNow to remote systems.

![Outbound Queue tab of Remote Process Sync Dashboard](../images/rps-dashboard-outbound-queue.png)

Use the **Record Processing Overview** dropdown to filter metrics by specific process events, or select **All Process Events** to view aggregate metrics.

The Outbound Queue tab includes these components:

1.  Records processed: Count of outbound records processed within the selected time range. Select from last minute, last hour, or last day using the dropdown.
2.  Records in queue: Current count of unprocessed records in the outbound queue.
3.  Avg. processing times over 24h: Average time \(in milliseconds\) to process outbound records over the last 24 hours.
4.  Latest time in queue: Time elapsed since the most recent record was added to the outbound queue.
5.  Last processed time: Time elapsed since the last record in the outbound queue was processed.
6.  Processing Times Over Last 24h: A line graph showing the processing time \(Subflow Runtimes\) for outbound records over the last 24 hours.

