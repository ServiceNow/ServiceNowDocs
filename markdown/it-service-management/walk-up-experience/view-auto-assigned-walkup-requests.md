---
title: Manage automatically assigned Walk-up Experience interactions
description: The agents supporting Walk-up Experience locations can view and manage interactions automatically pushed to the Agent Workspace inbox.
locale: en-US
release: australia
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Manage Walk-up Experience queue and interaction, Walk-up Experience, IT Service Management]
---

# Manage automatically assigned Walk-up Experience interactions

The agents supporting Walk-up Experience locations can view and manage interactions automatically pushed to the Agent Workspace inbox.

## Before you begin

Role required: sn\_walkup.walkup\_technician

## About this task

Walk-up Experience interactions can be automatically pushed to a personal inbox in Agent Workspace based on agent schedules and assignment rule configurations in the Advanced Work Assignment feature. The agents fulfill interactions on a first-come-first-served basis as they appear in the inbox.

To manually assign and manage interactions using the Walk-up Experience Agent modules found in the application navigator, refer to [Manage Walk-up Experience interactions manually](view-assigned-walkup-requests.md).

The Agents set a status in the Agent Workspace inbox to indicate readiness to accept interactions. Status choices are **Available**, **Away**, and **Offline**.

Even though interactions are automatically pushed to the walk-up inbox, agents can work with anyone in the walk-up queue at any time.

View walk-up queue interactions assigned to you automatically in your walk-up inbox or in your **My Assigned Walk-ups** list. You can also view all **Open - Unassigned** interactions for the queue you support.

With Agent Workspace you can view lists of all your related walk-up interactions and appointments, your cases, requester accounts and contacts, incidents, requests, and more using one convenient interface. The Walk-up Experience related interaction list includes the following items:

<table id="table_x1b_z4b_qdb"><thead><tr><th>

List item

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

All Closed Complete and Closed Abandoned interactions assigned to a specific walk-up location queue. Agents can abandon an interaction when a guest leaves the queue before receiving support.

</td></tr></tbody>
</table>## Procedure

1.  To begin supporting a walk-up queue requester, navigate to **** &gt; **Workspace Experience** &gt; **Agent Workspace Home**.

    The Agent Workspace homepage opens, greeting you with your name.

2.  Click **Inbox** and ensure your status is set to **Available**.

    View interactions in your inbox automatically pushed to you.

3.  Select the interaction at the top of the list and begin resolving the issue or fulfilling the request.

    When you create an associated incident or request through the Service Catalog, a **New Incident** tab or a **New Catalog Item** tab opens next to the **Details** tab of the original interaction. Fill out the new incident form or order assets. Click **Save** to save the new incident or complete the order confirmation. You receive a Request Number for your ordered item.

    1.  If an interaction requires an unusual amount of time to resolve or if the closure depends on resources not readily available, you can place the interaction on hold.

        The requester does not lose position in the queue and you can help another requester simultaneously. Placing an interaction on hold does not affect your capacity for new interactions. To put an interaction on hold, click the **Put on Hold** button.

    2.  You can associate the interaction with another record by selecting **Associate Record** from the more UI actions icon ![more UI actions icon](../../../common/image/Form_MoreOptions.png) in the interaction header.

    3.  To view the walk-up location stockroom for fulfillment requests, click **List** in the left navigation panel of the Agent Workspace interface, then click **My Stockrooms**.

    4.  If you cannot resolve an issue, click the **Create Incident** button in the interaction header.

        If you cannot fulfill a request from the stockroom, click the more UI actions icon ![more UI actions icon](../../../common/image/Form_MoreOptions.png) in the interaction header to view more actions. Select **Create Request** from the list to access the Service Catalog.

4.  When you are finished resolving the interaction, select the **Close** button in the interaction header.

    Closing an interaction affects your capacity because a new interaction will be pushed to your inbox.


**Parent Topic:**[Manage Walk-up Experience queue and interaction](../concept/use-walkup-to-manage-demand.md)

**Related topics**  


[bundle-platux.workspace-landing-page]

[Service Operations Workspace](../../service-operations-workspace/concept/explore-sow.md)

[Create an incident](../../incident-management/task/create-an-incident.md)

[bundle-sm4e.t_CreateARequestThroughTheCatalog]

