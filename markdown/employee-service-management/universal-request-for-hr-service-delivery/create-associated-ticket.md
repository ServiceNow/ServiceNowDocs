---
title: Create associated ticket for primary ticket of UR
description: Agent, working on the primary ticket, requests other departments for assistance in resolving a universal request \(UR\) by creating associated tickets for the UR. Multiple departments can work simultaneously on these associated tickets. These associated tickets are independent of the UR state flow.
locale: en-US
release: yokohama
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Universal Request, Universal Request, Employee Service Management]
---

# Create associated ticket for primary ticket of UR

Agent, working on the primary ticket, requests other departments for assistance in resolving a universal request \(UR\) by creating associated tickets for the UR. Multiple departments can work simultaneously on these associated tickets. These associated tickets are independent of the UR state flow.

## Before you begin

Configure the **sn\_uni\_req.associated\_ticket** property in the **Universal Request properties** page to determine how to handle the creation of the associated tickets. For more information, see [Universal Request properties](../reference/ur-properties.md).

Role required: agent part of the assignment group of the primary ticket or assigned to agent

## About this task

A routing agent of the primary ticket can request other departments for assistance in resolving a UR by creating associated tickets on the primary ticket. Multiple departments can work simultaneously on the associated tickets to resolve the UR.

The following are some key highlights.

-   Pass on the context of the request directly to the other department using the pop-up when creating an associated ticket.
-   Configure the information to be copied from UR to the Associated ticket in Mappings configuration.
-   Agents work on the associated ticket even after the closure of primary ticket / UR as associated tickets are independent of the UR state flow.
-   Configure the Associated ticket tab configuration to view and track the activity of associated tickets from the standard ticket page.

## Procedure

1.  Navigate to the primary ticket record.

    For example, to open an incident primary ticket, navigate to **All** &gt; **Universal Request** &gt; **With Primary Ticket**.

2.  Open the UR and then click the associated primary ticket.

    For example, the Incident ticket associated is displayed as a link in the message.

    The primary ticket record appears on the page.

3.  Click **Create Associated Ticket**.

4.  In the **Create Associated Ticket** dialog box, enter the following details.

    **Note:** Based on the sn\_uni\_req.associated\_ticket property, different fields display on the form. For more information, see [Universal Request properties](../reference/ur-properties.md).

    -   **Department**: Select the department from the list.
    -   **Service**: Select the specific service of the chosen department.
    -   **Short description**: Enter the short description for the new associated ticket.
    -   **Description**: Enter the detailed description for the new associated ticket.
    -   **Work notes**: Enter work notes details.
5.  Click **Create**.

    An associated ticket is created with the descriptions provided and is associated to the existing UR of the primary ticket.


**Parent Topic:**[Using Universal Request](../concept/using-ur.md)

