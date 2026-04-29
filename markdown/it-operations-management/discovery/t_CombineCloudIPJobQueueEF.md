---
title: Configure a single queue for Cloud-based and IP-based events
description: Configure Cloud-based and IP-based events to share a single queue, which helps reduce the impact of Discovery on app nodes.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Optimizing Discovery load for Event Framework, Configure Discovery to use Event Framework, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure a single queue for Cloud-based and IP-based events

Configure Cloud-based and IP-based events to share a single queue, which helps reduce the impact of Discovery on app nodes.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace is using version 1.9.0 or later.
-   ServiceNow AI Platform® is using XP9, YP4, or later than YP4.
-   The **discovery.use.event.processing** system property is turned on. For more information, see [Configure Discovery to use Event Framework](t_ConfigureDiscoveryEventFramework.md).

Role required: discovery\_admin

## About this task

When using a single queue, Cloud Discovery jobs frequently have higher priority than IP-based Discovery jobs. Separating Cloud-based and IP-based job queues helps avoid interference between Discovery types. However, balancing Discovery throughput and instance impact involves trade-offs.

|Separate queues|Single queue|
|---------------|------------|
|More worker threads, which means more database activity|Fewer worker threads, which means less database activity|
|More impact on jobs unrelated to Discovery|Less impact on jobs unrelated to Discovery|
|Cloud Discovery doesn't impact IP Discovery|Cloud Discovery can preempt IP Discovery|

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the System Properties \[sys\_properties\] table, select the **discovery.event.separate.cloud.events** property.

3.  Set the **Value** field to **false**.

4.  Select **Update**.


**Parent Topic:**[Optimizing Discovery load for Event Framework](../concept/c_FineTuneDiscoLoadEF.md)

