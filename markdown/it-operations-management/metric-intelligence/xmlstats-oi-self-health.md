---
title: View self-health monitoring statistics for Metric Intelligence
description: Monitor the status of components and processes of Metric Intelligence. Use the XMLStats page to view statistics and diagnostic details that can help with troubleshooting issues with Metric Intelligence.
locale: en-US
release: australia
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# View self-health monitoring statistics for Metric Intelligence

Monitor the status of components and processes of Metric Intelligence. Use the XMLStats page to view statistics and diagnostic details that can help with troubleshooting issues with Metric Intelligence.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Open a browser and enter the URL to the instance.

    Type in: `http://<instance name>.service-now.com`

2.  Append the following text to the instance URL: `xmlstats.do?include=XMLStatsOI`.

    The complete URL format is: `http://<instance name>.service-now.com/xmlstats.do?include=XMLStatsOI`

3.  Hit Enter.


## Result

Details are separated between two sections, instance level statistics and node level statistics. Details in the node section are specific to the node in the URL.

|Entry|Description|
|-----|-----------|
|batches\_recieved|Number of batches of metrics that the node received from the MID Server.|
|batches\_processed|Number of batches of metrics processed on the node.|

Details in the instance section are for the entire instance, showing the status of the self-health monitors.

|Entry|Description|
|-----|-----------|
|scheduled\_jobs\_monitor|Status of the self-health monitor that checks if the essential Metric Intelligence scheduled jobs are active.|
|distributed\_cluster\_monitor|Status of the self-health monitor that checks if the Metric Intelligence MID Server distributed cluster is running properly.|
|oi\_extension\_monitor|Status of the self-health monitor that checks if the Metric Intelligence extension is running properly.|
|metrics\_collection\_monitor|Status of the self-health monitor that checks if metrics are being collected by active connectors that are configured for metrics collection.|

**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

