---
title: Transfer an HR case in Universal Request
description: Transfer an HR case back to the Universal Request, or to another department or service with or without resolution.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Universal Request for HR Service Delivery, Integration of HR Service Delivery with ServiceNow applications, HR Service Delivery, Employee Service Management]
---

# Transfer an HR case in Universal Request

Transfer an HR case back to the Universal Request, or to another department or service with or without resolution.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## About this task

Configure the **sn\_uni\_req.transfer\_type** property in the Universal Request properties page to determine how to handle the primary ticket transfers. For more information, see [Universal Request Properties](../../universal-request/reference/ur-properties.md).

## Procedure

1.  Open the HR case that you want to transfer.

2.  Click **Transfer**.

    **Note:** The **Transfer** option is displayed only if you are a part of the assignment group or if the case is assigned to you.

3.  In the **Transfer Ticket** dialog box, provide the following details.

    **Note:** Based on your transfer type configuration, the given fields are displayed. For more information, see [Universal Request properties](../../universal-request/reference/ur-properties.md).

    -   **Action**: Select if the case should be transferred to another department or back to Universal Request
    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.
    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for routing the primary ticket that you want to pass to the UR Routing agent.
    -   **Copy additional comments and attachments**: Deselect if you do not want to transfer the ticket with additional comments and attachments. By default, all attachments and comments are transferred.

        **Note:** Work notes are not copied while transferring.

4.  Click **Transfer**.


## Result

-   On the HR case form, you can view the reason for transferring in the **Transfer reason** field.
-   The state of the HR case is changed to **Awaiting Acceptance** or **Closed Incomplete based on transfer reason** and the transfer reason and transfer notes are copied to the universal request.
-   The state of the universal request remains **In progress**.

**Note:** The state changes mentioned can be configured. See [Transfer configuration](../../universal-request/task/configure-route-state.md) for more information.

**Parent Topic:**[Universal Request for HR Service Delivery](../concept/universal-request-hr.md)

