---
title: Add an equipment or rack to logical composite
description: Add equipment or rack to a logical composite using design and assign.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Add an equipment or rack to logical composite

Add equipment or rack to a logical composite using design and assign.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

You can add only equipment or rack to a logical composite. The logical composite model must have Multi Chassis to Equipment or Multi Chassis to Rack relationship with the equipment or rack models.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Add Equipment/Rack to Multi Chassis Equipment**.

5.  Select **Next**.

    A change request is created.

6.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

7.  Select **Save**.

    A change task is created.

8.  Open the change task.

9.  On the **Task Attributes** tab, fill in the fields.

<table id="table_jcg_rhy_3dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Multi Chassis Equipment

</td><td>

Logical composite where you add the equipment or rack.

</td></tr><tr><td>

Entity Type

</td><td>

Type of equipment or rack that you want to add to the logical composite. Select one from the following:-   **Equipment Rack**

Select this option to add a rack to the logical composite.

-   **Equipment**

Select this option to add an equipment to the logical composite.

</td></tr><tr><td>

Rack List

</td><td>

List of racks that you want to add to the logical composite.**Note:** This field is available only when you select **Equipment Rack** as **Entity Type**.

</td></tr><tr><td>

Equipment List

</td><td>

List of equipment that you want to add to the logical composite.**Note:** This field is available only when you select **Equipment** as **Entity Type**.

</td></tr></tbody>
</table>10. Select **Submit**.


## Result

The equipment or rack record is added to the logical composite record.

**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

**Related topics**  


[Create an equipment record by using design and assign](create-equipment-record-design-and-assign.md)

[Define a network model relationship](create-network-model-relationships.md)

