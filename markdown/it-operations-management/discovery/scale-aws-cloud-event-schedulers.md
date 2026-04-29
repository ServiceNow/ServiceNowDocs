---
title: Scale the AWS cloud event schedulers
description: Scale the cloud event schedulers to improve the Amazon Web Services \(AWS\) event processing rate of the ServiceNow instance.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AWS events-driven discovery, Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Scale the AWS cloud event schedulers

Scale the cloud event schedulers to improve the Amazon Web Services \(AWS\) event processing rate of the ServiceNow instance.

## Before you begin

Role required: cloud\_admin

## About this task

If the instance receives a huge number of events and it doesn’t process them within a reasonable time, create additional Cloud Event Schedulers. Running multiple cloud event schedulers in parallel helps to improve the event processing rate of the instance. When the event inflow rate reduces, you can deactivate some of the Cloud Event Schedulers. For more information, see [AWS events-driven discovery](../concept/aws-events-driven-discovery.md).

## Procedure

1.  Configure the number of Cloud Event Schedulers that you want to use.

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

    2.  In the Name column, search for **sn\_cmp.cloud\_event.parallel\_scheduler\_count**.

    3.  On the **sn\_cmp.cloud\_event.parallel\_scheduler\_count** property form, set the **Value** field to an appropriate value.

        **Important:**

        -   Make sure that the value of the **sn\_cmp.cloud\_event.parallel\_scheduler\_count** property doesn’t exceed the count of available worker nodes.
        -   If you have multiple domains where cloud events are configured, use the **sn\_cmp.cloud\_event.parallel\_scheduler\_count** property with caution because each cloud event scheduler has multiple iterations for each domain in which cloud events are active.
    4.  Select **Update**.

2.  Execute the Cloud Event Scheduler Count Monitor scheduled job.

    The Cloud Event Scheduler Count Monitor scheduled job manages the count of Cloud Event Schedulers per the value specified in the **sn\_cmp.cloud\_event.parallel\_scheduler\_count** property.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

    2.  Open the Cloud Event Scheduler Count Monitor scheduled job.

    3.  Select **Execute Now**.


