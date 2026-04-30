---
title: Create a slot for equipment
description: Added as per STRY57142377 - DOC1091704Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manually create and review your network asset instances, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create a slot for equipment

Create a slot to provide a designated space for the equipment to maintain, update and access all types of equipment. You can route cables using the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

Slots help a rack to distribute the weight of the equipment across the rack evenly. On creating a slot, a record is created in the Slot \[cmdb\_ci\_container\_slot\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory** &gt; **Slot**.

3.  Create a slot by selecting **New**.

4.  On the Equipment Holder form, fill in the fields.

    To learn more, see [Equipment Holder form](../reference/tni-equipment-holder-form-configuration.md).

5.  Select **Set Inventory Attributes**.

6.  On the TNI CI Attributes form, fill in the fields.

    To learn more about the fields, see [TNI CI Attributes form](../reference/ci-attribue-form.md).

7.  Select **Save**.


**Parent Topic:**[Manually create and review your network asset instances](../concept/creating-telecommunications-network-inventory.md)

