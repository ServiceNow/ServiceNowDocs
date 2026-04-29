---
title: Configure the job priority of background workers for Event Framework
description: Configure the job priority of background workers to help prevent noncritical tasks from preempting important work, which promotes system efficiency and stability.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Optimizing Discovery load for Event Framework, Configure Discovery to use Event Framework, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the job priority of background workers for Event Framework

Configure the job priority of background workers to help prevent noncritical tasks from preempting important work, which promotes system efficiency and stability.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace is using version 1.9.0 or later.
-   ServiceNow AI Platform® is using version XP9, YP4, or later than YP4.
-   The **discovery.use.event.processing** system property is turned on. For more information, see [Configure Discovery to use Event Framework](t_ConfigureDiscoveryEventFramework.md).
-   The **com.glide.queue.discovery.sensors.processing\_jobs.priority** and **com.glide.queue.discovery.cloud.sensors.processing\_jobs.priority** system properties are configured. For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

Role required: discovery\_admin

## About this task

By default, Event Framework jobs have a priority of 100. If Discovery is preempting more important work, you can use the **com.glide.queue.&lt;queue\_name&gt;.processing\_jobs.priority** property to adjust the priority.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Choose one or more job types for which you want to adjust the priority.

    |Job type|Action|
    |--------|------|
    |**IP-based**|Select **com.glide.queue.discovery.sensors.processing\_jobs.priority** from the System Properties \[sys\_properties\] table.|
    |**Cloud-based**|Select **com.glide.queue.discovery.cloud.sensors.processing\_jobs.priority** from the System Properties \[sys\_properties\] table.|

3.  In the **Value** field, enter `110`.

    **Note:** Increasing the number in the **Value** field lowers the job's priority, while decreasing the number raises it.

4.  Select **Update**.


**Parent Topic:**[Optimizing Discovery load for Event Framework](../concept/c_FineTuneDiscoLoadEF.md)

