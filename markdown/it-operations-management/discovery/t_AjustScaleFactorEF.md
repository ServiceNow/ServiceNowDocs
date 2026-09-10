---
title: Adjust the scale factor for Event Framework jobs
description: Adjust the scale factor to modify the number of worker threads per app node, which increases or decreases throughput.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-operations-management/discovery/t\_AjustScaleFactorEF.html
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Optimizing Discovery load for Event Framework, Configure Discovery to use Event Framework, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Adjust the scale factor for Event Framework jobs

Adjust the scale factor to modify the number of worker threads per app node, which increases or decreases throughput.

## Before you begin

Confirm the following:

-   You're using Discovery Admin Workspace v1.9.0 or later.
-   You're using the Xanadu Patch 9, Yokohama Patch 4, or later version of the ServiceNow AI Platform®.
-   The **discovery.use.event.processing** system property is turned on. For more information, see [Configure Discovery to use Event Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/t_ConfigureDiscoveryEventFramework.md).
-   The **Job configuration type** field of the Queue Registration form is set to **Scale with nodes**. For more information, see [Queue Registration form reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/r_QueueRegistrationForm.md).

Role required: discovery\_admin

## About this task

If your instance becomes slow while Discovery is running, you can adjust the scale factor to modify the number of worker threads per app node. The default scale factor is set to 2, which corresponds to two worker threads per app node.

For example, if you increase the scale factor to 3, Discovery uses three worker threads per app node, increasing throughput. Conversely, reducing the scale factor to 1 limits Discovery to a single worker thread per app node, which decreases throughput.

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Queue Registry**.

2.  Choose one or more job types for which you want to adjust the scale factor.

    |Job type|Action|
    |--------|------|
    |**IP-based**|Select **discovery.sensors** from the Queue Registry \[sysevent\_queue\] table.|
    |**Cloud-based**|Select **discovery.cloud.sensors** from the Queue Registry \[sysevent\_queue\] table.|

3.  In the **Scale factor** field, set a value.

    **Note:**

    -   On the Queue Registry list view, this field is labeled **Job configuration value**. On the record form, it is labeled **Scale factor**.
    -   The default maximum value is 3. To increase the scale factor beyond 3, open the Queue Provider Param \[sysevent\_queue\_provider\_param\] table, filter by **Provider: Event Provider**, and increase the value in the **max\_thread\_utilization** field. This change affects all jobs in the Queue Registry \[sysevent\_queue\] table where the provider is Event Provider. By default, only `discovery.sensor` and `discovery.cloud.sensors` have scale factor values high enough to be affected.
4.  Select **Update**.


**Parent Topic:**[Optimizing Discovery load for Event Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-operations-management/discovery/c_FineTuneDiscoLoadEF.md)

