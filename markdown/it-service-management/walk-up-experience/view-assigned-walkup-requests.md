---
title: Manage Walk-up Experience interactions manually
description: Agents supporting walk-up locations can manually manage queue requests with several Walk-up Experience interaction-related modules.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage Walk-up Experience queue and interaction, Walk-up Experience, IT Service Management]
---

# Manage Walk-up Experience interactions manually

Agents supporting walk-up locations can manually manage queue requests with several Walk-up Experience interaction-related modules.

## Before you begin

Role required: sn\_walkup.walkup\_technician

## About this task

Manage interactions manually using the Walk-up Experience Technician modules found in the application navigator. To manage automatically assigned interactions from the Agent Workspace inbox, refer to [Manage automatically assigned Walk-up Experience interactions](view-auto-assigned-walkup-requests.md).

Walk-up queues support requesters in the order that they check into the queue — first come, first served. The agents supporting the queue can decide who will work on the first interaction. As new requesters enter the queue and submit interactions, technicians share the workload, assigning queued interactions to themselves.

Certain requesters are considered VIPs. The system recognizes this when they check into the queue. An interaction for a VIP shows **true** for **VIP** in the Interactions list. The agents can move VIP requesters to the front of the queue by assisting them first.

**Note:**

Creating walk-up type interactions manually is not supported. A walk-up interaction is considered valid for check-in or appointment only if created via the check-in or appointment booking interfaces, and not via a table. Agents cannot check-in to a walk-up location on behalf of an end-user.

View walk-up queue interactions using several Walk-up Experience modules:

<table id="table_x1b_z4b_qdb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My Assigned Walk-ups

</td><td>

Interactions you assign to yourself when you accept an active interaction or that are assigned to you. Agents assign interactions to themselves when they accept a queued interaction. Managers can assign interactions to specific agents.

 These interactions are in a Work in Progress state. Once assigned, an agent can transfer the interaction to another agent or queue to complete the work, if necessary.

</td></tr><tr><td>

Open — Unassigned

</td><td>

All open but unassigned interactions associated with your specific walk-up queue location. When a requester checks into a walk-up queue, an interaction is created. The interaction is Queued until an agent accepts it or is assigned the interaction. At that point, the state changes to Work in Progress.

</td></tr><tr><td>

Closed Walk-ups

</td><td>

All Closed Complete and Closed Abandoned interactions assigned to a specific walk-up location queue. Agents can abandon an interaction when a requester leaves the queue before receiving support.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **** &gt; **Walk-up Experience** &gt; **** &gt; **Agent** &gt; **Opened - Unassigned**.

2.  Find the requester name under the **Opened for** column of the Interactions list.

3.  Click the interaction **Number** associated with the requester.

4.  Enter your name in the **Assigned to** field on the form, change the **State** to **Work in Progress**, and select **Update**.

    1.  To close an interaction if the requester has left the queue, click **Abandon** in the form header or choose **Closed Abandoned** from the **State** form field and click **Update**

    2.  Alternatively, you can associate the interaction with another record by clicking the **Associate Record** button in the interaction header.

5.  To resolve the interaction, navigate to **Walk-up Experience** &gt; **Agent** &gt; **My Assigned Walk-ups**.

6.  Click the interaction number from the list to open the Walk-up Interaction form.

7.  Resolve the issue or fulfill the request.

    1.  Change the interaction status to **On Hold** if the requester is not present for an appointment or if the interaction entails a lengthy process, for example, an OS upgrade.

    2.  To view the walk-up location stockroom for fulfillment requests, click the **Stockroom Consumables** related link.

    3.  If you cannot resolve the issue or fulfill the request, click either the **Create Incident** or **Create Request** related link to create an incident or access the Service Catalog.

    When you create an associated incident or request through the Service Catalog, the associated related lists on the form populate accordingly. Related lists include the following details:

    -   Incidents for Interaction: Incidents associated with the interaction
    -   Requests for Interaction: Service Catalog requests associated with the interaction
    -   Incidents by Same Caller: Incidents created for a walk-up requester
    -   Requests by Same Caller: Requests created for a walk-up requester
8.  Set the interaction **State** to **Closed Complete** and select **Update** to update the interaction, when you are finished resolving the interaction.

    Alternatively, you can click **Close** to complete the interaction.


**Parent Topic:**[Manage Walk-up Experience queue and interaction](../concept/use-walkup-to-manage-demand.md)

**Related topics**  


[Use platform view to fulfill a Walk-up Experience request from a stockroom](fulfill-walkup-stockroom-request.md)

[Create an incident](../../incident-management/task/create-an-incident.md)

