---
title: Create an equipment record by using design and assign
description: Create an equipment record using the design and assign function in the Telecommunications Network Inventory application. By creating the equipment and its related inventory records, you can fulfill an order request for an equipment record.DOC1090321
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create an equipment record by using design and assign

Create an equipment record using the design and assign function in the Telecommunications Network Inventory application. By creating the equipment and its related inventory records, you can fulfill an order request for an equipment record.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you instantiate an equipment template, it creates the corresponding configuration item \(CI\) records in the equipment table. To learn more about the equipment tables, see [Equipment extension classes](../reference/equipment-extension-classes.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Create a change request to instantiate an equipment record.

    1.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **All Equipment**.

        **Note:** To create an equipments from the rack record, go to **Inventory** &gt; **Rack**and open the rack record. And then select **Create equipment** from more options menu.

    2.  Select **Create equipment**.

    3.  Select the inventory template in the **Apply inventory template** field.

    4.  On the **Add equipment details** section, fill in the fields.

        For a description of the field valuesTo learn more about the fields, see [Equipment form](../reference/equipment-form.md).

    5.  Select **Next**.

    6.  Confirm the details and select **Create**.

    The equipment record is created.

3.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

4.  Select the **New** button.

5.  Select **Create Inventory Equipment**.

6.  Select **Next**.

    A change request is created.

7.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

8.  Select **Save**.

    A change task is created.

9.  Open the change task.

10. On the **Task Attribute** tab, fill in the fields.

    For a description of the field values, see [Equipment task attribute form](../reference/equipment-task-attribute-form.md).

11. Select **Submit**.


## Result

The equipment record is created along with the associated inventory records. These records are generated depending on the model relationship attached with the inventory model.

**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

**Related topics**  


[Creating an inventory template for a logical composite](../concept/creating-inventory-template-logical-composite.md)

[Add an equipment or rack to logical composite](add-equipment-rack-logical-composite.md)

[Remove an equipment or rack from logical composite](remove-equipment-rack-logical-composite.md)

