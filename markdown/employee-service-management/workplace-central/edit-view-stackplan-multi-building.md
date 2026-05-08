---
title: Edit a scenario using the stack plan
description: Edit a scenario using the stack plan to allocate spaces to departments, cost centers, workplace entities, or neighborhoods.
locale: en-US
release: australia
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2026-03-25"
reading_time_minutes: 3
breadcrumb: [Viewing or editing a scenario, Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Edit a scenario using the stack plan

Edit a scenario using the stack plan to allocate spaces to departments, cost centers, workplace entities, or neighborhoods.

## Before you begin

Ensure that you have created a scenario, and it is in the Draft state. For more information, see [Create a scenario](create-a-scenario.md).

**Important:** If allocation changes in your instance impact the scenario, the system displays a warning on the Space Details panel. You must review the changes, edit the scenario accordingly, then select **Move to valid** before continuing. For more information about allocation changes, see [Reviewing allocation changes](../../workplace-space-management/concept/reviewing-allocation-changes.md).

![Space details panel displaying a warning about reviewing allocation changes.](../images/wsd-central-review-changes.png)

Role required: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.scenario\_reader \(read only; to view a scenario\)

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center by navigating to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select All scenarios, then select the scenario that you want to edit.

    By default, the scenario opens in the **Stack plan** tab.

3.  On the Space details pane, on the View options card, select **Edit scenario**.

    The **Group by** option is automatically filled based on the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property.

4.  Select the Accordion panel icon \(![Accordion icon for a building to show or hide floors within a building.](../images/wsd-building-accordion-icon.png)\) for the building that you want to edit.

    You can expand an accordion to display the floors of a building. If your scenario contains multiple buildings, the accordion of the last building is expanded by default.

    -   When you select a building to see the floors, the borders of the selected building are highlighted.
    -   When you select a floor on the Stack plan to view the spaces or allocations, the borders of the selected floor are highlighted.
    -   When you select a bar or space to view the number of allocated spaces, the borders of the selected bar or space are highlighted.
5.  Edit the stack plan based on your requirement.

<table id="choicetable_ej5_fmc_kfc"><thead><tr><th align="left" id="d164667e195">

Action

</th><th align="left" id="d164667e198">

Steps

</th></tr></thead><tbody><tr><td id="d164667e204">

**Zoom in or out on the stack plan**

</td><td>

Use the zoom options \(![Zoom options.](../images/zoom-options.png)\) on the stack plan.

</td></tr><tr><td id="d164667e219">

**Resize a bar**

</td><td>

1.  Select the bar that you want to resize.
2.  On the map legend card, select **Resize**.
3.  In the Space Count field, enter the number of spaces that you want to allocate to the bar.
4.  In the **Allocate added spaces from** or **Allocate remaining space to** field, select a parent entity or unallocated spaces.

The spaces are allocated from or added to the selected entity.

This step is applicable if the Group by option is Workplace Entity.

5.  Select **Apply**, then save the scenario.

</td></tr><tr><td id="d164667e265">

**Move a bar to a different floor**

</td><td>

1.  Select the bar that you want to move.
2.  On the map legend card, select **Move**.
3.  In the **Assign to building** field, select the building that you want to move the bar to.
    -   You can only select buildings that are added to the scenario based on the space selection criteria.
    -   You can also move the bar temporarily to the Clipboard.
4.  In the **Assign to floor** field, select the floor that you want to move the bar to.

This field can't be edited if **Assign to building** value is **Clipboard**.

5.  In the **Space allocation** field, select a parent entity or unallocated space.

The spaces are allocated from the selected entity.

This field is applicable if the Group by option is Workplace Entity.

6.  Select **Apply**, then save the scenario.

</td></tr><tr><td id="d164667e334">

**Drag a bar to a different floor**

</td><td>

1.  Drag the bar to the floor that you want to move it to.
2.  On the space selection pop-up, select unallocated spaces or a parent entity.

This step is applicable if the Group by option is Workplace Entity.

</td></tr></tbody>
</table>
**Parent Topic:**[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

**Related topics**  


[Edit a scenario using the floor map](edit-scenario-floor-map.md)

[Edit user assignments of a neighborhood](add-or-edit-user-assignments-of-a-neighbourhood.md)

