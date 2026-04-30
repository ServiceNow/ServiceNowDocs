---
title: Manage Walk-up Experience interactions manually
description: Technicians supporting walk-up locations can manually manage queue requests with several CSM Walk-up Experience interaction-related modules.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Walk-up Experience queue and interaction management, Using Walk-up Experience, Customer communication, Using Customer Service Management, Customer Service Management]
---

# Manage Walk-up Experience interactions manually

Technicians supporting walk-up locations can manually manage queue requests with several CSM Walk-up Experience interaction-related modules.

## Before you begin

Role required: sn\_csm\_walkup.walkup\_technician

## About this task

Manage interactions manually using the CSM Walk-up Experience Technician modules found in the application navigator. To manage automatically assigned interactions from the CSM Configurable Workspace inbox, refer to [Manage automatically assigned Walk-up Experience interactions](csm-walkup-view-auto-assigned-requests.md).

Walk-up queues support guests in the order that they check into the queue — first come, first served. Technicians supporting the queue can decide who will work the first interaction. As new guests enter the queue and submit interactions, technicians share the workload, assigning queued interactions to themselves.

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

All open but unassigned interactions associated with your specific walk-up queue location. When a guest checks into a walk-up queue, an interaction is created. The interaction is Queued until an agent accepts it or is assigned the interaction. At that point, the state changes to Work in Progress.

</td></tr><tr><td>

Closed Walk-ups

</td><td>

All Closed Complete and Closed Abandoned interactions assigned to a specific walk-up location queue. Agents can abandon an interaction when a guest leaves the queue before receiving support.

</td></tr></tbody>
</table>## Procedure

1.  To begin supporting a walk-up queue guest, navigate to **** &gt; **CSM Walk-up Experience** &gt; **** &gt; **Technician** &gt; **Opened - Unassigned**.

    The Interactions list opens.

2.  Find the guest name under the **Opened for** column of the Interactions list.

3.  Click the interaction **Number** associated with the guest.

4.  Enter your name in the **Assigned to** field on the form, change the **State** to **Work in Progress**, and click **Update**.

    1.  To close an interaction if the guest has left the queue, click **Abandon** in the form header or choose **Closed Abandoned** from the **State** form field and click **Update**

    2.  Alternatively, you can associate the interaction with another record by clicking the **Associate Record** button in the interaction header.

5.  To resolve the interaction, navigate to **Walk-up Experience** &gt; **Technician** &gt; **My Assigned Walk-ups**.

6.  Click the interaction number from the list to open the Walk-up Interaction form.

7.  Resolve the issue or fulfill the request.

    1.  Change the interaction status to **On Hold** if the requester is not present for an appointment or if the interaction entails a lengthy process, for example, an OS upgrade.

    2.  If you cannot resolve the issue or fulfill the request, click the **Create Case** related link to create a case.

    When you create a case, the associated related lists on the form populate. Related lists include the following details:

    -   Cases for Interaction: Cases associated with the interaction
    -   Cases by Same Caller: Cases created for a walk-up guest
    When you finish resolving the interaction, change the interaction **State** to **Closed Complete** and click **Update** to update the interaction. Alternatively, you can click **Close** to complete the interaction.

8.  When you finish resolving the interaction, change the interaction **State** to **Closed Complete** and click **Update** to update the interaction.

    You can also click **Close** to complete the interaction.


