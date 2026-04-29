---
title: Universal Request data model
description: Universal Request is a task type that supports cross-departmental collaboration and unified employee experience. Universal Request becomes the parent record for departmental primary tickets, such as IT incidents and HR cases, and enables your organization to measure cross-departmental SLAs and OLAs.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Universal Request, Universal Request, Employee Service Management]
---

# Universal Request data model

Universal Request is a task type that supports cross-departmental collaboration and unified employee experience. Universal Request becomes the parent record for departmental primary tickets, such as IT incidents and HR cases, and enables your organization to measure cross-departmental SLAs and OLAs.

The Universal Request \(UR\) is a task that can be created from any of the following sources.

-   Requester-created: An employee uses any of following options to submit a request.
    -   Clicks **Request Help** on the Service Portal or Employee Center.
    -   Taps **Needs Help** on a mobile device.
    -   Uses the virtual agent chat on the portals.
-   Agent created: An IT service desk agent receives a phone call or live chat from an employee, starts a new call record or an Interaction Record, and in some cases, can create a Universal Request instead of a department ticket. The agent can then assign that UR to an appropriate Tier 1 assignment group.
-   System generated: Based on configuration, a universal request is created when an employee submits a Record Producer. The Record Producer is configured to automatically create a Universal Request to enable cross-departmental request transfer and a consistent ticket view for the requester.

The following diagram shows a high-level overview of the Universal Request data model.

![Universal Request data model](../images/ur-datamodel.png)

The Universal Request data model uses a combination of tables to store data:

-   ServiceNow AI Platform tables
-   Tables included with Universal Request

For information, see the list of [Universal Request plugins](ur-plugins.md).

The Task \[task\] table is modified to include the following fields:

-   A Universal Request \(UR\) field points to the parent UR record. This model allows any table extending the Task table to be a child of the UR.
-   Effective Number field \(identifying number\) stores the UR number, if the request has a UR associated with it. If it is not associated with a UR, then the Effective Number stores the current department-specific request number.
-   Transfer Reason field stores the reason for the transfer of the request. The possible options are:
    -   **With resolution**

        Indicates that the request is completed and is transferred back to Universal Request, the specific department or service.

    -   **Without resolution**

        Indicates that the request is not completed and is transferred back to Universal Request, the specific department or service.


The Universal Request table includes:

-   State reasons for the customer-facing states
-   Primary ticket details of the department-specific requests
-   Restricted field to indicate if the request created is sensitive or not

Universal Request also includes user roles and ACLs that customers can use to provide access to different tables. This includes both internal and external user roles.

The Universal Request is a new task type that is extended from the base Task \[task\] table and is uniquely identified by a number prefixed with **UR**.

<table id="simpletable_bpc_mtg_llb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary ticket

</td><td>

References the request that is currently active under the Universal Request. For example, INC1022201.

</td></tr><tr><td>

Opened for

</td><td>

The requester for whom the Universal Request is created.

</td></tr><tr><td>

State

</td><td>

Current state of the Universal Request. A UR can be in any of the following states:-   New
-   In Progress
-   Awaiting Response from user
-   Closed

 For more information on the UR states, see [Universal Request states and reasons](ur-states.md).

</td></tr><tr><td>

State reason

</td><td>

The agent-facing reason for some requester-facing states. The state reason values are as follows:

-   **Triaging:**

A possible state reason when a Universal Request state is **In Progress**, and indicates that the Universal Request is being triaged.

-   **Primary ticket WIP:**

A possible state reason when a Universal Request state is **In Progress**, and indicates that the work for an active primary ticket is in progress.

-   **Confirm response:**

A possible state reason when a Universal Request state is **In Progress**, but the state reason changes to **Confirm Response** notifying the tier 1 agents to either accept or reject the response before closing the ticket for the requester. This happens when the **Needs Review** flag of the Universal Request is set to true.

-   **Accept Resolution:**

A possible state reason when a Universal Request is in **Awaiting Response** state indicating that there is a pending requester’s action to accept the resolution provided.

-   **Action required:**

A possible state reason when a Universal Request is in **Awaiting Response** state that there is an additional action to be performed by the requester.


</td></tr><tr><td>

Restricted

</td><td>

Option for restricting access to a ticket that has sensitive data. If a ticket is marked as Restricted, then only the agents with the sensitive request access can view and resolve the ticket.

</td></tr></tbody>
</table>## Primary Ticket field of the Universal Request table

The Primary Ticket field in the Universal Request determines the UR state and the requester’s ticket view experience. Use the Standard Ticket page configuration of the primary ticket to determine the content that must be displayed in various sections of a standard ticket page. The primary ticket for an UR is a departmental ticket such as an IT incident or an HR case.

**Note:** A Universal Request can have only one primary ticket at a time.

For a Universal Request that is created for the first time, no primary tickets exist. If a child department ticket, such as an IT incident or an HR case is created from the UR, then the child ticket becomes the primary ticket. If the primary ticket is transferred back to UR or to another department, then the primary ticket field becomes empty. This sequence continues as new primary tickets are added and transferred back to UR or to another department.

When a record producer is configured to automatically create a Universal Request, then the UR becomes the parent record. And, when a department ticket is created, then that record becomes the primary ticket and remains until it is transferred back to the UR, to another department, or service.

**Parent Topic:**[Exploring Universal Request](explore-universal-request.md)

