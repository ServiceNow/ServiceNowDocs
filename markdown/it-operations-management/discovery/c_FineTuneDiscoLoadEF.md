---
title: Optimizing Discovery load for Event Framework
description: You can optimize Discovery properties to adjust throughput and enhance safety when pinning jobs.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-06-03"
reading_time_minutes: 1
breadcrumb: [Configure Discovery to use Event Framework, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Optimizing Discovery load for Event Framework

You can optimize Discovery properties to adjust throughput and enhance safety when pinning jobs.

|Issue|Action|Related task|
|-----|------|------------|
|Your instance is slow|Decrease the scale factor|[Adjust the scale factor for Event Framework jobs](../task/t_AjustScaleFactorEF.md)|
|Discovery is slow|Increase the scale factor|[Adjust the scale factor for Event Framework jobs](../task/t_AjustScaleFactorEF.md)|
|Discovery is slow when both Cloud and IP Discovery are running|Use a single queue for both Cloud and IP-based events|[Configure a single queue for Cloud-based and IP-based events](../task/t_CombineCloudIPJobQueueEF.md)|
|Discovery is preempting other work|Reduce the worker priority of the background job|[Configure the job priority of background workers for Event Framework](../task/t_ConfigureBackgroundWorkerJobPriorityEF.md)|
|Nodes are executing too many Discovery jobs simultaneously|Configure event processors to execute on specific nodes|[Configure event processors to execute on specific nodes](../task/t_ConfigureEventProcessorsEF.md)|

