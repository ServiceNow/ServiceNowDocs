---
title: Create a payload for external third-party providers
description: Create a payload for external third-party providers to send your work items to the external queue.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create a payload for external third-party providers

Create a payload for external third-party providers to send your work items to the external queue.

## Before you begin

Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to **All** &gt; **Advanced Work Assignment** &gt; **Queues**.

2.  Create a queue enabling External Routing.

    For more information about creating a queue with external routing, see [Enable external routing for queues](enable-awa-external-routing.md).

3.  Open the provider record, select the subflow that you created, and select **Save**.

    For more information about creating a subflow, see [Create a subflow](create-subflow-extrnl-route.md).![Select subflow for external routing of the AWA queue item.](../image/subflow-extrnl-routing.png)

4.  In the External Event definition section, create a definition form or modify the existing demo data records by changing the provider name you created.

    ![Select the provider for your work item to be routed to the external queue.](../image/select-provider-extrnl-route.png "Provider for External Routing")

    The payload script in the External event definition \[awa\_external\_event\_definition\] table has the event type and payload information that you send to the third-party providers. Therefore, it is required for you to change all the events' provider to the provider you created.

    ![Payload script for the third-party provider.](../image/payload-extrnl-route.png "Payload for External Routing")

    In the payload script:

    -   `current` refers to the work item glideRecord associated with the queue. You can access all the workitem records from the glideRecord current.
    -   `queueObj` is the glideRecord for the existing awa\_queue record.
    -   `additionalParams` refers to the parameters from the document table.
    **Note:** Before saving the script, verify that you have the required data.

5.  Select **Update**.


