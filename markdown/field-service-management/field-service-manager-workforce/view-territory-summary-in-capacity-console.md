---
title: View territory and demand channel summary in the contextual side panel
description: The Capacity Console provides a comprehensive summary of territories and demand channels, enabling capacity planners and managers to make informed decisions about resource allocation and management.
locale: en-US
release: yokohama
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using the Capacity Console, Capacity, Manage workforce, Using Field Service Management, Field Service Management]
---

# View territory and demand channel summary in the contextual side panel

The Capacity Console provides a comprehensive summary of territories and demand channels, enabling capacity planners and managers to make informed decisions about resource allocation and management.

## Before you begin

Role required: fsm\_adv\_cap\_mgmt.wm\_capacity\_planner, sn\_fsm\_capacity\_mg.wm\_capacity\_write, sn\_fsm\_capacity\_mg.wm\_capacity\_read

## About this task

When you select an event in the calendar or a specific data row, the contextual side panel \(CSP\) automatically appears on the right side of the screen. This panel provides a dynamic, context-specific interface, displaying relevant information and actionable options tailored to the selected event or capacity data row. It streamlines workflows by offering quick access to key details and actions without requiring navigation to other screens.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM configurable workspace** &gt; **Capacity console**.

2.  View territory or demand channel summary.

<table id="choicetable_awp_znf_c2c"><thead><tr><th align="left" id="d55702e79">

To

</th><th align="left" id="d55702e82">

Do this

</th></tr></thead><tbody><tr><td id="d55702e88">

**View territory summary grouping by territory**

</td><td>

1.  Select **Territory** in the **Group by** filter.
2.  Locate the **Summary** row under the territory section.

**Note:** **Summary** row appears only when **Group By** is set to **Territory**.

3.  Select an event in the calendar to view the territory summary in the CSP.


</td></tr><tr><td id="d55702e128">

**View territory summary grouping by demand channel**

</td><td>

1.  Select **Demand Channel** in the **Group by** filter.
2.  Select an event under the demand channel associated with the selected territory.


</td></tr><tr><td id="d55702e152">

**View each demand channel details by territory**

</td><td>

1.  Select **Territory** in the **Group by** filter.
2.  Select an event under the demand channel associated with the selected territory.


</td></tr></tbody>
</table>
## Result

The contextual side panel opens to display summaries tailored to the selected context, providing key information and enabling actionable insights for users. Depending on the selection, the CSP may display:

-   Territory summary: Provides detailed information about the selected territory, including metrics such as the number of assigned agents, capacity assignment type, or available hours in the specified period based on the capacity definition type of that capacity assignment. This summary supports capacity planners in making informed decisions.
-   Demand channel summary: Displays an overview of demand channel details, including reservation and calculated capacity value for the selected period.

## What to do next

You can change the capacity value and reservation in the contextual side panel.

-   **[Update capacity value and reservation for a territory in capacity console](update-reservation-rule-in-capacity-console.md)**  
The Capacity Console provides flexibility for capacity planners and managers to modify capacity value and reservation rule for better allocation of resources. Reservations determine the demand channels applicable and the percentage allocation of capacity for each channel on a given day.

**Parent Topic:**[Using the Capacity Console](../concept/capacity-and-reservation-management-console.md)

