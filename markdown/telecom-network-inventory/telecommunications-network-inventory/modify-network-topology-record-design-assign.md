---
title: Modify a network topology record using design and assign
description: Modify a network topology record using the design and assign function in the Telecommunications Network Inventory application. You can add or delete the elements in an existing network topology record and visualize how the network elements are organized and connected to one another.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a change request from Network Inventory Workspace, Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Modify a network topology record using design and assign

Modify a network topology record using the design and assign function in the Telecommunications Network Inventory application. You can add or delete the elements in an existing network topology record and visualize how the network elements are organized and connected to one another.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Add/Remove member to Topology**.

5.  Select **Next**.

6.  In the **Select topology** field, select the network topology record that you want to modify.

    You can add or delete the following field values:

    -   Topology nodes
    -   Topology sites
    -   Root nodes
    -   Topology connections
7.  Select **Submit**.


## Result

When modifying a network topology record, the following actions occur:

-   When you remove a topology site, all nodes and connections associated with that site within the topology are removed from the relationship.
-   When you remove a topology or root node, all connections associated with the node within the topology are removed from the relationship.
-   When you remove a topology connection, it’s removed from the relationship.
-   When a node is removed from the relationship, if it’s part of a root node, that entry will also be removed.

**Parent Topic:**[Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md)

**Related topics**  


[Visualization of network topology](../concept/visualization-of-topology.md)

[Using the network topology](../concept/using-network-topology.md)

