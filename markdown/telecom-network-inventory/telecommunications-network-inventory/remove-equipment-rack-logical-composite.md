---
title: Remove an equipment or rack from logical composite
description: Remove a rack or equipment from a logical composite using design and assign.
locale: en-US
release: yokohama
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Remove an equipment or rack from logical composite

Remove a rack or equipment from a logical composite using design and assign.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Remove Equipment/Rack from Multi Chassis Equipment**.

5.  Select **Next**.

    A change request is created.

6.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

7.  Select **Save**.

    A change task is created.

8.  Open the change task.

9.  On the **Task Attributes** tab, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Multi Chassis Equipment|Logical composite from where you remove the equipment or rack.|
    |Equipment / Rack|Equipment or rack that you want to remove from logical composite.|
    |Attachments|Select **Add** to add any attachments.|

10. Select **Submit**.


## Result

The equipment or rack record is removed from the logical composite record.

**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

**Related topics**  


[Create an equipment record by using design and assign](create-equipment-record-design-and-assign.md)

[Define a network model relationship](create-network-model-relationships.md)

