---
title: Create a payload for external third-party providers
description: Create a payload for external third-party providers to send your work items to the external queue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/advanced-work-assignment/create-payload-extrnl-provider.html
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-06-21"
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

    For more information about creating a queue with external routing, see [Enable external routing for queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/enable-awa-external-routing.md).

3.  Open the provider record, select the subflow that you created, and select **Save**.

    For more information about creating a subflow, see [Create a subflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/create-subflow-extrnl-route.md).\[Omitted image "subflow-extrnl-routing.png"\] Alt text: Select subflow for external routing of the AWA queue item.

4.  In the External Event definition section, create a definition form or modify the existing demo data records by changing the provider name you created.

    \[Omitted image "select-provider-extrnl-route.png"\] Alt text: Select the provider for your work item to be routed to the external queue.

    The payload script in the External event definition \[awa\_external\_event\_definition\] table has the event type and payload information that you send to the third-party providers. Therefore, it is required for you to change all the events' provider to the provider you created.

    \[Omitted image "payload-extrnl-route.png"\] Alt text: Payload script for the third-party provider.

    In the payload script:

    -   `current` refers to the work item glideRecord associated with the queue. You can access all the workitem records from the glideRecord current.
    -   `queueObj` is the glideRecord for the existing awa\_queue record.
    -   `additionalParams` refers to the parameters from the document table.
    **Note:** Before saving the script, verify that you have the required data.

5.  Select **Update**.


