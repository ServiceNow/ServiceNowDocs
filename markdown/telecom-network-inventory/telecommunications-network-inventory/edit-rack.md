---
title: Edit rack
description: Added topic as per STRY56040533 - DOC1080161.Edit a rack to remove, add, or move the equipment from the selected rack. Organize and upgrade the components within the rack using the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Create a rack, Create and maintain racks and cabinets, Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Edit rack

Edit a rack to remove, add, or move the equipment from the selected rack. Organize and upgrade the components within the rack using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

By editing a rack, you can see all the equipment added to the rack along with its details.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Rack**.

3.  Select a rack from the displayed list.

    After selecting a KPI \(Key Performance Indicator\), a list of the equipment contributing to that respective metric is displayed.

    A dashboard displays the KPIs \(occupied units, weight capacity, power usage, and equipment types\) along with the front and rear views of the rack.

4.  Select **Edit Rack**.

    A list of all equipment, and the front view of both the edited configuration and the current configuration is displayed.

5.  From the displayed list of equipment, search for the equipment to add in the rack by using either the filters or the search box.

    **Note:**

    -   The existing filters automatically clear on entering a search. And, applying a filter clears your search terms.
    -   The equipment list can also be sorted based on latest creation date, highest number of Rack Units and weight.
    -   The list shows all the equipment records included in the sn\_ni\_core.equipment system property, and the equipment that aren't in the rack. However, the equipment installed within the rack is visible in the list, but remains inactive.
    -   The info \(![info icon](../image/icon-info.png)\) expands and displays the equipment details on selecting an equipment or the info button.
6.  Perform any of the following while editing a rack.

<table id="table_tqd_2yr_lbc"><thead><tr><th>

Actions

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Add

</td><td>

1.  Select **\(![Options icon](../../../common/image/icon-menu.png)\)** &gt; **Add to Rack**.
2.  Fill in the fields and select **Add**.

To learn more about the fields, see add equipment to rack table of [Change request and change task forms](../concept/change_request_forms.md).

 **Note:** You can drag the equipment from the corner to the desired rack unit. For non-TNI, a TNI entity with category as equipment is created. Changes can be undone or redone.

</td></tr><tr><td>

Move

</td><td>

1.  Select **\(![Options icon](../../../common/image/icon-menu.png)\)** &gt; **Move**.
2.  Fill in the fields and select **Move**. To learn more about the fields, see add equipment to rack table of [Change request and change task forms](../concept/change_request_forms.md).
 **Note:**

-   You can also drag the equipment from the corner to the desired rack unit.
-   You can undo or redo the changes


</td></tr><tr><td>

Remove

</td><td>

Select **\(![Options icon](../../../common/image/icon-menu.png)\)** &gt; **Remove**.**Note:**

-   You can undo or redo the changes
-   Multiple change tasks are created on multiple removals of equipment. Additionally, both removed equipment and racks are added under **Affected CIs**.


</td></tr><tr><td>

Reserve a rack unit

</td><td>

Select Options \(![Options icon](../../../common/image/icon-menu.png)\) of the rack unit that you want to reserve and select **Reserve**.**Note:**

-   You can undo or redo the changes
-   On reserving a rack unit, its life-cycle stage is set to Deployed and its life-cycle stage status is set to Reserved.


</td></tr></tbody>
</table>7.  Select **Save**.

    A change request is created with the implemented modifications under the **Change Tasks** tab.The short description of each change task is updated based on the modifications. Once the changes are applied, work notes of the tasks are updated and are marked as closed.

    **Note:**

    -   Select the displayed change request to see change tasks and more.
    -   The short description is updated as `Initiated to add Equipment equipment_name to Rack rack_name.` if the equipment is added to the rack. `Initiated to remove Equipment equipment_name from Rack rack_name.`, if it’s removed from the rack. `Initiated to move the Equipment equipment_name within the Rack rack_name`, if it’s moved within the rack. `Initiated to reserve a unit of Rack rack_name for Equipment equipment_name`, if a rack slot is reserved.
    -   A change request is created only if the rack is modified.
    -   A change request isn’t created in the following situations.
        -   if the same equipment is added and then removed.
        -   if the equipment is removed and added it back to the rack in the same slot.
        -   if the equipment is added and then moved it to another position in the rack, only one add is created with the latest rack slot details.
        -   if any technical error occurs. However, work notes are updated with the error details.
    -   A change request can contain different change tasks.

**Parent Topic:**[Create a rack](edit-a-rack.md)

