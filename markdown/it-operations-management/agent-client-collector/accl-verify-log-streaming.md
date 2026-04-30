---
title: Identify and resolve log streaming issues
description: Make sure that your ACC data inputs are streaming data properly by identifying and resolving log streaming issues.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Identify and resolve log streaming issues

Make sure that your ACC data inputs are streaming data properly by identifying and resolving log streaming issues.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

In the ACC data input record, the Streaming Sources related list shows the streaming data of that data input's sources. This data enables you to identify streaming issues and their possible cause.

For example, if the last event time for a data input's endpoint server is yesterday, the server might be down or configured incorrectly. A streaming issue might also be caused by the data input configuration file not being installed on the endpoint.

**Note:** You can view the streaming data of all data inputs and the MID Servers that receive logs from them in the Streaming Sources page. For more information, see [Identify and resolve log streaming issues](../../health-log-analytics-admin/task/hla-data-input-streaming.md) in the ServiceNow Health Log Analytics application documentation.

## Procedure

1.  Navigate to **All** &gt; **ACC Data Inputs** and select a data input record.

2.  On the data input form, select the Streaming Sources related list.

3.  Review the streaming data of that data input's sources.

    For a description of the filters, see [ACC data input streaming sources](../reference/accl-streaming-sources-ref.md).

4.  Resolve any data streaming issues.

    1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Alerts**.
    2.  Open alerts and address the specified issues.

## What to do next

Proceed to the next step in the Health Log Analytics data input setup flow. For more information, see [Set up additional ACC data inputs](accl-data-input-setup.md).

