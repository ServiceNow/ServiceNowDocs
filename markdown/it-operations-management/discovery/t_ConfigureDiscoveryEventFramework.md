---
title: Configure Discovery to use Event Framework
description: Configure Discovery to process jobs using the Event Framework method, which enables you to manage discovery throttling effectively and prioritize tasks based on their importance in the queue.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure Discovery to use Event Framework

Configure Discovery to process jobs using the Event Framework method, which enables you to manage discovery throttling effectively and prioritize tasks based on their importance in the queue.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace is using version 1.9.0 or later.
-   ServiceNow AI Platform is using version XP9, YP4, or later than YP4.

Role required: discovery\_admin

## About this task

When not using the Event Framework method, Discovery creates a one-time Schedule Item \[sys\_trigger\] record for each External Communication Channel \(ECC\) queue sensor or pattern input record. After the task is processed, the system scheduler deletes the sys\_trigger. This approach introduces additional overhead and can lead to significant database churn, while offering limited control over how sensors are processed.

The Event Framework reduces database churn by cycling through multiple event tables over time. Instead of deleting old records one by one, it clears out entire tables when they’re no longer needed and reuses them. This approach is much more efficient and helps keep the system running smoothly.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the System Properties \[sys\_properties\] table, select the **discovery.use.event.processing** property.

3.  Set the **Value** field to **true**.

4.  Select **Update**.


## Result

When an input record is added to the ECC Queue, a business rule is triggered, which fires an event. The system processes these events at regular intervals with a default priority of 100.

**Note:** To update a job priority, configure the **com.glide.queue.discovery.sensors.processing\_jobs.priority** and **com.glide.queue.discovery.cloud.sensors.processing\_jobs.priority** system properties. For more information, see [Configure the job priority of background workers for Event Framework](t_ConfigureBackgroundWorkerJobPriorityEF.md).

-   **[Optimizing Discovery load for Event Framework](../concept/c_FineTuneDiscoLoadEF.md)**  
You can optimize Discovery properties to adjust throughput and enhance safety when pinning jobs.

**Parent Topic:**[Advanced Discovery configuration](../concept/c_DiscoveryExtendedCapabilities.md)

