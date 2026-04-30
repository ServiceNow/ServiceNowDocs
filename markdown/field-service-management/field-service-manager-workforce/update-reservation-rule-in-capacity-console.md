---
title: Update capacity value and reservation for a territory in capacity console
description: The Capacity Console provides flexibility for capacity planners and managers to modify capacity value and reservation rule for better allocation of resources. Reservations determine the demand channels applicable and the percentage allocation of capacity for each channel on a given day.
locale: en-US
release: zurich
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [View territory and demand channel summary, Capacity Console, Capacity, Workforce, Use, Field Service Management]
---

# Update capacity value and reservation for a territory in capacity console

The Capacity Console provides flexibility for capacity planners and managers to modify capacity value and reservation rule for better allocation of resources. Reservations determine the demand channels applicable and the percentage allocation of capacity for each channel on a given day.

## Before you begin

Role required: fsm\_adv\_cap\_mgmt.wm\_capacity\_planner, sn\_fsm\_capacity\_mg.wm\_capacity\_write

## About this task

Use contextual side panel \(CSP\) to:

-   **Update capacity value**: Capacity values can be modified for hours and tasks but not for agent schedules. Agent schedule values are dynamically calculated and cannot be adjusted manually.
-   Create or modify reservation: The CSP allows two types of reservation updates:

    -   **Create a new reservation**: Use this option to define a new reservation and apply it to the selected context.
    -   **Override reservation**: Replace the current reservation with another from the existing list.
    **Note:** The **Copy &amp; Modify Reservation** option is available only in the Territory Summary section.


## Procedure

1.  Navigate to **All** &gt; **CSM/FSM configurable workspace** &gt; **Capacity console**.

2.  Select the **Group by** filter and choose **Territory**.

3.  Locate the **Summary** row or an event for a specific duration within the territory.

4.  Click on an event or data row in the calendar.

    The Territory summary page appears in the contextual side panel.

5.  To update the capacity value, select the Edit ![Edit icon](../image/edit-mobile-icon.png) icon and change the value in terms of hours or tasks in whichever way the capacity definition is defined.

6.  To change the applied reservation, select the Actions ![Actions icon.](../image/more_actions.png) icon and click **Override Reservation**.

    1.  In the **Reservation** field, select an existing reservation from the drop-down menu.

        Example: Base Rule for All Territories.

    2.  Click **Apply Override** to enforce the selected rule.

7.  To create a new reservation by making a copy of current reservation, select **Copy &amp; Modify Reservation**.

    1.  In the **New reservation name** field, enter the reservation name.

    2.  Change the values of the reservation as needed or add and remove demand channels.

        Example: Fiber Repair: 25% with a maximum overflow of 100%.

    3.  Click **Apply modified reservation**.


## Reservation Modifications

1.  Capacity assignment of type agent schedule - Scenario: Aurora \(Daily assignment\)
    -   Adjust the reservation to allocate 10% capacity for Copper Repair and 30% for Fiber Repair.
    -   Save the modified reservation to apply changes for the selected day.
2.  Capacity assignment of type hours - Scenario: San Diego \(Monthly assignment\)
    -   Modify the fixed capacity value \(e.g., reduce from 200 hours to 180 hours\).
    -   Change the reservation to better align with the long-term capacity plan.
3.  Capacity assignment of type tasks - Scenario: Chicago \(Daily assignment\)
    1.  Modify the fixed capacity value \(e.g., reduce from 20 tasks to 10 tasks\).
    2.  Change the reservation to better align with the long-term capacity plan.

The following snapshots showcases the actions performed in the contextual side panel of the capacity console.

![Capacity console contextual side panel showcasing the options to open the reservation record and override reservation.](../image/reservation-rule-update.png)

![Capacity console contextual side panel showcasing the option to copy and modify the reservation.](../image/copy-reservation.png)

