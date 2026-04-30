---
title: Configure event processors to execute on specific nodes
description: Configure the discovery.event.pin.jobs system property to enable event processors to execute on specific nodes and distribute the work evenly. The scale factor calculates the number of nodes but doesn't pin jobs to specific nodes.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-06-03"
reading_time_minutes: 1
breadcrumb: [Optimizing Discovery load for Event Framework, Configure Discovery to use Event Framework, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure event processors to execute on specific nodes

Configure the **discovery.event.pin.jobs** system property to enable event processors to execute on specific nodes and distribute the work evenly. The scale factor calculates the number of nodes but doesn't pin jobs to specific nodes.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace is using version 1.9.0 or later.
-   ServiceNow AI Platform® is using version XP9, YP4, or later than YP4.
-   The **discovery.use.event.processing** system property is turned on. For more information, see [Configure Discovery to use Event Framework](t_ConfigureDiscoveryEventFramework.md).

Role required: discovery\_admin

## About this task

The **discovery.event.pin.jobs** system property determines how jobs are assigned to nodes. When that property is set to **true**, jobs are evenly distributed across specific nodes, but scheduling flexibility is limited. When the property is set to **false**, jobs are randomly assigned, which can increase Discovery throughput.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the System Properties \[sys\_properties\] table, select the **discovery.event.pin.jobs** property.

3.  Set the **Value** field to **true**.

4.  Select **Update**.


**Parent Topic:**[Optimizing Discovery load for Event Framework](../concept/c_FineTuneDiscoLoadEF.md)

