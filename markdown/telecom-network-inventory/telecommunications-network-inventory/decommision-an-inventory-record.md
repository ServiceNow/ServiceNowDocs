---
title: Decommission an inventory record
description: Decommission an inventory record that you want to remove from Telecommunications Network Inventory.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Manually creating and reviewing your network asset instances, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Decommission an inventory record

Decommission an inventory record that you want to remove from Telecommunications Network Inventory.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, and sn\_ni\_core.inventory\_template\_manager

## About this task

When you decommission a CI record, all the related tables of the CI are removed and the **Life Cycle Stage**, **Life Cycle Stage Status** of this CI changes.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory**.

3.  Open the inventory list and select an inventory CI record that you want to decommission.

4.  Select the more options icon \(![More Options icon.](../image/options-icon.png)\) and then select **Decommission**.

    All the related tables are removed. Also, the **Life Cycle Stage** field is set to **End of Life** and the **Life Cycle Stage Status** field is set to **Retired** if the **Asset** is not used by the CI. Otherwise, the **Life Cycle Stage** field is set to **Inventory** and the **Life Cycle Stage Status** field is set to **Available**.

    **Note:** Decommission fails if the selected CI has any child CIs as follows.

    |Inventory name|Relationship that fails decommission|
    |--------------|------------------------------------|
    |Network site|Site, equipment, or equipment holder|
    |Interface card|Interface used by any physical or logical connection|
    |Network interface|Interface linked with physical or logical connection|
    |Physical/Logical connection|Any connection that is used by another connection as a connection element.|
    |Equipment holder|Rack linked with an equipment or shelf, a shelf linked to an equipment, slot, or subslot linked to a card.|
    |Equipment|Physical or logical interface linked to a connection or to a physical interface that has a logical connection.|


**Parent Topic:**[Manually creating and reviewing your network asset instances](../concept/creating-telecommunications-network-inventory.md)

