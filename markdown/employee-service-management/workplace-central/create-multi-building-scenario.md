---
title: Create a scenario
description: Create a scenario with a building. Add, update, or remove space allocations before publishing and deploying a scenario. Manage and update your scenarios using the Stack plan and Floor map component tabs.
locale: en-US
release: yokohama
product: Workplace Central
classification: workplace-central
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Working with Space Optimization, Use, Workplace Central, Workplace Service Delivery, Employee Service Management]
---

# Create a scenario

Create a scenario with a building. Add, update, or remove space allocations before publishing and deploying a scenario. Manage and update your scenarios using the Stack plan and Floor map component tabs.

## Before you begin

Ensure that the following plugins are installed:

-   Indoor Mapping \(for map-based administration\)
-   Workplace Core
-   Workplace Central
-   Workplace Service Delivery components
-   Workplace Case Management
-   Workplace Space Management

**Important:** You can view spaces based on their workplace entities only for a building. You can’t create or view a scenario based on workplace entities.

Role required: sn\_wsd\_spcmgmt.space\_planner, sn\_wsd\_spcmgmt.scenario\_reader \(read only; to view a scenario\)

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Workplace Central** &gt; **Workplace Central**.
    -   **All** &gt; **Scenario Planning** &gt; **My Scenario Plans**
    You can also open Workplace Central from the Employee Center. Navigate to **Workspaces** &gt; **Workplace Central**.

2.  Select the **Space Optimization** icon \(![Space Optimization icon.](../images/space-optimization-icon.png)\).

    The Space optimization dashboard opens.

3.  Create a scenario by selecting **Create a scenario** from either of the following options.

<table id="choicetable_fwz_mgg_3vb"><thead><tr><th align="left" id="d525934e157">

Path

</th><th align="left" id="d525934e160">

Action

</th></tr></thead><tbody><tr><td id="d525934e166">

**From the Space Optimization tab**

</td><td>

Select **Create scenario**.

</td></tr><tr><td id="d525934e178">

**From a scenarios list section**

</td><td>

Select **Create scenario**.

</td></tr><tr><td id="d525934e190">

**From the Buildings section**

</td><td>

1.  Select a building.
2.  On the building details tab, select **Create scenario**.


</td></tr></tbody>
</table>4.  On the Scenario details form, fill in the fields.

    For a description of the field values, see [Scenario details form](../reference/scenario-details-form.md).

5.  Select **Save scenario**.

6.  Select the Refresh icon \(![Refresh to refresh the scenario.](../images/refresh-icon.png)\) to check if your scenario has moved to the **Draft** state.


## Result

The new scenario is created in the **Processing** state and takes some time to move to the **Draft** state. You can’t open a scenario that is in the Processing state.

![The Scenarios page showing list of scenarios.](../images/wsd-scenario-creation-page.png)

For more information about scenario states, refer to [Scenario and Building - Views, states, settings, and key features](../reference/scenario-planning-views-actions-keyfeatures-.md).

After a scenario moves to the **Draft** state, you can open the scenario and select the view options for the scenario.

-   **Edit Scenario**: You can only edit a scenario using this option. This option is available only when you select a scenario from the Space Optimization page. It isn’t available when you select a building from the Space Optimization page.
-   **View Scenario**: View scenario details \(unassigned spaces, allocated spaces, and user assignment details\) for a selected building, floor, or bar.

## What to do next

To create a copy of an existing scenario, see [Create a copy of an existing scenario](create-copy-of-scenario.md).

View or edit the scenario by using the stack plan or the floor map. For more information, see [Viewing or editing a scenario](../concept/viewing-editing-scenario.md).

**Parent Topic:**[Working with Space Optimization](../concept/working-with-space-optimization.md)

**Related topics**  


[Viewing or editing a scenario](../concept/viewing-editing-scenario.md)

[Review a scenario](review-a-scenario.md)

[Publish a scenario](publish-a-scenario.md)

[Send a scenario for approval](send-a-scenario-for-approval.md)

[Change owner of a scenario](change-owner-of-a-scenario.md)

[Deploy a scenario](deploy-a-scenoria.md)

[View scenario change details](view-scenario-change-details.md)

[Create a copy of an existing scenario](create-copy-of-scenario.md)

[View or edit space allocations of a building](view-or-edit-space-alloctions-of-a-building.md)

[Work on a space assist request](work-on-space-assist-request.md)

[Map based space administration](../concept/map-based-space-administration.md)

