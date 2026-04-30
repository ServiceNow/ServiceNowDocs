---
title: Define your inventory numbering
description: Define the numbering for your virtual local area network \(VLAN\) or link aggregation group \(LAG\) connections in the Telecommunications Network Inventory application. By defining these inventory numbers, you can configure your network assets to activate a network connection.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Inventory number allocation, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Define your inventory numbering

Define the numbering for your virtual local area network \(VLAN\) or link aggregation group \(LAG\) connections in the Telecommunications Network Inventory application. By defining these inventory numbers, you can configure your network assets to activate a network connection.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.inventory\_template\_manager, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

The numbering that you define in this process creates VLAN and LAG number ranges, allowing for the assignment of numbers from those ranges to network connections and equipment ports. When you provision a network connection over an Ethernet network interface to fulfill a customer order, you create a VLAN interface to support your network topology. You must assign a VLAN number from 1 through 4096 for this interface. You use this VLAN number to create an interface name so that you can activate the interface on the network.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Number Allocation** &gt; **Inventory Numbers**.

3.  Select **New**.

4.  On the **Details** tab, fill in the general information for inventory numbering.

    To learn more about the fields that are unique to the Inventory Numbers form, see [Inventory Numbers form](../reference/inventory-numbers-form.md).

5.  To add the attachments, such as graphics or documents, select the attachment icon \(![Attachment icon.](../image/attachments-icon.png)\) in the right panel.

6.  Select **Save**.

    The related tabs appear on the form. You can view or modify the related tab information. To learn more about the related tabs, see [Related tabs in the Network inventory forms](../reference/inventory-related-tab.md).


## What to do next

To update or delete an inventory number record, see [Update or delete a record of an inventory number allocation](update_and_delete_ip_address_space.md).

**Parent Topic:**[Inventory number allocation](../concept/vlan_or_lag_number_management.md)

