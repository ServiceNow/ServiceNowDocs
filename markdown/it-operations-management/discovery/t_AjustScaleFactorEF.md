---
title: Adjust the scale factor for Event Framework jobs
description: Adjust the scale factor to modify the number of worker threads per app node, which increases or decreases throughput.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Optimizing Discovery load for Event Framework, Configure Discovery to use Event Framework, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Adjust the scale factor for Event Framework jobs

Adjust the scale factor to modify the number of worker threads per app node, which increases or decreases throughput.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace is using version 1.9.0 or later.
-   ServiceNow AI Platform® is using version XP9, YP4, or later than YP4.
-   The **discovery.use.event.processing** system property is turned on. For more information, see [Configure Discovery to use Event Framework](t_ConfigureDiscoveryEventFramework.md).
-   The **Job configuration type** field of the Queue Registration form is set to **Scale with nodes**. For more information, see [Queue Registration form reference](../reference/r_QueueRegistrationForm.md).

Role required: discovery\_admin

## About this task

If your instance becomes slow while Discovery is running, you can adjust the scale factor to modify the number of worker threads per app node. The default scale factor is set to 2, which corresponds to two worker threads per app node.

For example, if you increase the scale factor to 3, Discovery uses three worker threads per app node, increasing throughput. Conversely, reducing the scale factor to 1 limits Discovery to a single worker thread per app node, which decreases throughput.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Queue Registry**.

2.  Choose one or more job types for which you want to adjust the scale factor.

    |Job type|Action|
    |--------|------|
    |**IP-based**|Select **discovery.sensors** from the Queue Registry \[queue\_registry\] table.|
    |**Cloud-based**|Select **discovery.cloud.sensors** from the Queue Registry \[queue\_registry\] table.|

3.  In the **Scale factor** field, set a value.

    **Note:** The default maximum value is 3. To increase the scale factor beyond 3, configure the **com.glide.processing.framework.max\_thread\_utilization\_percentage** property. For more information about this property, see [Discovery properties](../reference/r_DiscoveryProperties.md). For instructions on how to create a property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

4.  Select **Update**.


**Parent Topic:**[Optimizing Discovery load for Event Framework](../concept/c_FineTuneDiscoLoadEF.md)

