---
title: Create a rack
description: Added as per STRY57142377 - DOC1091704Create a rack to add, organize equipment, rack units, and manage all assets. You can also edit a rack using the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and maintain racks and cabinets, Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create a rack

Create a rack to add, organize equipment, rack units, and manage all assets. You can also edit a rack using the Telecommunications Network Inventory application.

## Before you begin

-   Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager
-   You must create slots as Rack Units and create a relationship with the rack to represent the rack with rack units.

## About this task

A rack contains rack units represented as slots having shelves, and equipment in it. When you create a rack record, it creates a corresponding configuration item \(CI\) record in the Rack \[cmdb\_ci\_container\_rack\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Rack**.

3.  Select **New**.

4.  On the Equipment Holder form, fill in the fields.

    To learn more, see [Equipment Holder form](../reference/tni-equipment-holder-form-configuration.md).

5.  Select **Set Inventory Attributes**.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.


## Result

A rack record is created and related tabs are created. To learn more, see [Related tabs in the network inventory forms](../reference/inventory-related-tab.md).

## What to do next

See [Optimizing rack and cabinet usage](subsequent-actions.md) to learn about the next steps.

-   **[Edit rack](edit-rack.md)**  
Edit a rack to remove, add, or move the equipment from the selected rack. Organize and upgrade the components within the rack using the Telecommunications Network Inventory application.

**Parent Topic:**[Create and maintain racks and cabinets](../concept/create-and-maintain-rack-and-cabinet.md)

