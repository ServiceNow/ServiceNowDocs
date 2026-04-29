---
title: Transfer a primary ticket
description: You can transfer a primary ticket back to Universal Request, service set \(department\), or service either with or without resolution.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Universal Request, Employee Service Management]
---

# Transfer a primary ticket

You can transfer a primary ticket back to Universal Request, service set \(department\), or service either with or without resolution.

## Before you begin

Role required: agent part of the assignment group of the primary ticket or assigned to the agent

## About this task

Configure the **sn\_uni\_req.transfer\_type** property in the **Universal Request properties** page to determine how to handle the primary ticket transfers. For more information, see [Universal Request properties](../reference/ur-properties.md).

A routing agent can either resolve and close a primary ticket or transfer it to back to Universal Request or another department for review and closure. When a primary ticket is transferred back to UR, the ticket is no longer a primary ticket, and the primary ticket field of the Universal Request becomes empty.

![Click to route the task](../images/route-to-ur.png)

When transferring the ticket, the routing agent can choose the department and a specific service within the department or can select `I'm not sure` when they’re unsure of the correct department or service.

The agent can transfer a ticket with one of the following reasons:

-   **Transfer with resolution**

    The request is resolved and transferred back to UR, a specific department, or a service. Agents can select this option when another departments help is required to fulfill the request.

-   **Transfer without resolution**

    The request isn’t resolved or doesn’t belong to the specific department and transferred back to UR, a specific department, or a service.


![Transfer a ticket by selecting a route reason.](../images/route-ur-dialog.png)

## Procedure

1.  Navigate to the primary ticket record that you want to transfer.

    For example, to open an incident primary ticket, navigate to **All** &gt; **Universal Request** &gt; **With Primary Ticket**.

2.  Open the universal request and then click the associated primary ticket.

    For example, the Incident ticket associated is displayed as a link in the message.

    The primary ticket record appears on the page.

3.  Verify and click **Transfer**.

4.  In the **Transfer Ticket** dialog, provide the following details and then click **Transfer**.

    **Note:** Based on the transfer type configuration, different fields display on the form. For more information, see [Universal Request properties](../reference/ur-properties.md).

    -   **Action**: Select if you want to transfer the ticket to another department or back to the Universal Request.
    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.
    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for routing the primary ticket to the UR Routing agent.
    -   **Copy additional comments and attachments**: Clear the check box if you don’t want to transfer the ticket with additional comments and attachments. By default, all attachments and comments are transferred.

        **Note:** Work notes aren’t copied while transferring.


## Result

The ticket is transferred based on the direct transfer mappings in mapping configuration and transfer type configurations. For more information on configuring routing, see [Transfer configuration](configure-route-state.md) and [Map UR fields with target table fields](transfer-fields-mapping.md).

**Parent Topic:**[Using Universal Request](../concept/using-ur.md)

