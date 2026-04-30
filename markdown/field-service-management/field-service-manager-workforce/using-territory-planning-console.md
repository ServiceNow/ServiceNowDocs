---
title: Managing territories and agents from Territory Planning console
description: Use the Territory Planning Console to assign work orders or work order tasks to agents or crews in the territories that best match their location based on conditions that you set.
locale: en-US
release: yokohama
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage workforce, Using Field Service Management, Field Service Management]
---

# Managing territories and agents from Territory Planning console

Use the Territory Planning Console to assign work orders or work order tasks to agents or crews in the territories that best match their location based on conditions that you set.

## Territory Planning Console

The territory map in the Territory Planning Console provides a visual representation of a territory so you can easily see the location of the agents and crews assigned to the territory and also assign the work order tasks.

The personas with the role sn\_fsm\_tp.fsm\_territory\_read will only have the view access to Territory Planning console.

**Note:** To identify the best matched territory for a work order task, you must enable the **Field\_Service\_Territories** territory model. For more information, see [Enable the Field Service territory model](../task/enable-territory-model.md).

The following table describes the list of activities you can perform as a territory planner, territory manager, and resource manager in the territory Planning console.

<table id="table_rsw_l3l_stb"><thead><tr><th>

Action

</th><th>

Territory Planner

</th><th>

Territory Manager

</th></tr></thead><tbody><tr><td>

View, manage, and analyze territories and their associated resources.

</td><td>

View territories under **All Territories**, **My Territories**, and **My Selections** categories.

</td><td>

View territories under **My Territories** and **My Selections** categories.

</td></tr><tr><td>

Add or customize data overlays to visualize more data points in the territory.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

View detailed information such as the number of agents, crews, and child territories by clicking the territory geography.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Edit and stretch boundaries to include new data points.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Assign direct agent or crew memberships without assignment groups.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Hide all territory geographies in the map.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Specify the color code using color picker for a territory.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Add child territories**Note:** The child territory ![Child Territory icon.](../image/child-territory-icon.jpg) icon appears only when the territory has child territories.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr><tr><td>

Add child territories to **My Selection** list.

</td><td>

For all territories

</td><td>

Only for assigned territory

</td></tr></tbody>
</table>## Working with territories

Perform the following tasks to work with territories:

-   [Create a work order task](../../planning-and-policy/task/t_CreateAWorkOrderTask.md)
-   [Assign work order tasks to agents or crews from the dispatch queue](../../planning-and-policy/concept/c_DispatchWorkOrderTasks.md#)
-   [Auto-dispatch a work order task](../../planning-and-policy/concept/c_DispatchWorkOrderTasks.md#)
-   [Assign work order tasks to agents](manage-work-order-tasks-dw.md#)
-   [Assign work order tasks to crews on Dispatcher Workspace](../task/assign-wot-to-crew.md)

-   **[View favorite territories on a map](../task/move-territories-to-my-selection.md#)**  
View and manage territories and their associated resource details in the list view and on a map.
-   **[View territory information in contextual side panel](../task/view-territory-details-in-csp.md)**  
The contextual side panel offers valuable insights and easy access to territory information, helping you make well-informed decisions and efficiently manage your territories.
-   **[Change map marker location in the Territory Planning console](../task/change-an-agent-s-location.md)**  
Update the location of your map markers for a dynamic and accurate visual representation of your data entities on the map.
-   **[Change start and end locations for agents](../task/change-agent-start-end-location.md)**  
Change the start-of-day and end-of-day locations for your agents, offering the flexibility needed for specific work order tasks.
-   **[Move agents between territories in the Territory Planning console](../task/relocate-agents-territories.md)**  
Relocate agents between territories to add flexibility to their work.

**Parent Topic:**[Manage workforce](managing-workforce.md)

**Related topics**  


[Configuring Field Service Territory Planning](configuring-territory-planning-fsm.md)

