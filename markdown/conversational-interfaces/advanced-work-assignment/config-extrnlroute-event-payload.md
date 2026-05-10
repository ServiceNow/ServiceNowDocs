---
title: Configure External Routing events and payload
description: Configure Advanced Work Assignment with external routing using AWA External Service API for CCaaS and third-party providers to enable them to submit events.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure External Routing events and payload

Configure Advanced Work Assignment with external routing using AWA External Service API for CCaaS and third-party providers to enable them to submit events.

## Before you begin

Role required: admin

## About this task

When AWA Queue is configured for external routing, it enables for setting up a REST endpoint corresponding to the CCaaS entry point for routing, which:

-   Makes the schema changes needed to associate with an AWA External queue with the CCaaS REST endpoint.
-   Provides the following fields to provide the payload for the REST call:
    -   Case \(sn\_customerservice\_case\)
    -   Task \(sn\_customerservice\_case\)
    -   Interaction \(interaction\)

Configuring AWA with external routing enables you to consolidate the routing of ServiceNow channels \(such as Chat, Cases, or Incidents\) and the CCaaS channels. The AWA External Service API involved in the configuration plays a key role:

-   Detects the Work Item \(created or transferred\)
-   Uses the External AWA Service API pushEvent \(EVENT\_TYPE\) function to pass the Work Item.
-   Generates the request payload and constructs the flow object using the The ExternalAWAServiceAPI.
-   Pushes the events to the external system using the Subflow.

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select an existing External Routing Queue item or create one.

3.  Select the **External** check box to create an external routing Work Item.

    **Note:** If you selected an existing AQA Queue item, verify that external routing is enabled with the **External** field checked.

4.  In the External third-party routing section of the queue form, select the Preview this record icon ![Preview this record icon.](../image/preview-record-icon.png) and select **Open record**.

    **Note:** You are notified to save the Queue record for any changes you made upon navigating. Select **Update** for an existing queue or select **Submit** for a new queue.

5.  Select the **Subflow** from the list of flows available to send events to the selected provider.

    ![Select subflow to send events to the provider.](../image/select-awa-exrnl-subflow.png)

6.  Select the required External Event Definitions for the provider.

    The selected External Event Definitions are associated with the provider to define the external events that must be handled by the provider. You can either select from the existing event definitions or create one.

7.  Select an external event definition to see the **Event type** and **Payload** that it contains.

    ![Event type and payload of the subflow associated with the provider.](../image/awa-extrnl-event-defntn.png)

    **Note:** Ensure that you do not add any info message or error message after answer block. Answer should be always return string, if answer is in try block, you can add info/error messages in catch block.

    Use the following items that are available by default, to construct the payload contents you want on the external system:

    -   `current` = Represents the AWA Work item record
    -   `docuemntGR` = Represents the interaction or task referenced by the Work Item.
    -   `additionalParams` = Contains objects with the values of the Work Item document's fields.
    -   payload script = Contains scriptable APIs.
8.  Select **Update**.

    The Agent chat queue is configured to the external routing queue.


## Result

After the configuration, all the incoming chats are routed to the external queue and you can see the list of work items sent to the external queue in the Work Items \[awa\_work\_items\] table. You can find the recorded event logs of the subflows associated with the provider in the Flow engine contexts \[sys\_flow\_context\] table.

To view the execution details of the event payload, open an event record from the Flow engine contexts \[sys\_flow\_context\] table and select **Open in Operations View**. You will see the AWA Post External Routing Events flow with the payload.

![Executed external event payload.](../image/executed-external-routing.png "AWA Post External Routing Events")

