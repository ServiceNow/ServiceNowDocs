---
title: Create a network topology model
description: Create a network topology model in the Telecommunications Network Inventory application to define the metadata for the topology according to your recommendations. You can use a topology model to create a record by using the design and assign function.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create inventory models, Use, Telecommunications Network Inventory]
---

# Create a network topology model

Create a network topology model in the Telecommunications Network Inventory application to define the metadata for the topology according to your recommendations. You can use a topology model to create a record by using the design and assign function.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a network topology model record, it creates a model in the Network Topology Models \[sn\_ent\_network\_topology\_model\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then go to **Inventory Models** &gt; **Network Topology Models**.

3.  Select **New**.

4.  On the **Details** tab, fill in the fields.

<table id="table_xxp_hq1_dtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Behavior

</td><td>

Type of topology structure. Select one from the following options.-   **Ring**

Each node is linked with its neighbor to form a closed network.

-   **Linear Bus**

All the nodes are connected one after the other in a sequential chain.

-   **Mesh**

The nodes are connected directly, dynamically, and non-hierarchically to as many other nodes as possible and cooperate with one another to route data.

-   **Star**

All nodes are connected to a central hub using a communication link.

-   **Tree**

The nodes are arranged in a configuration that resembles a tree’s leaves, branches, and trunk.

</td></tr><tr><td>

Number of allowed nodes

</td><td>

Total number of nodes that are allowed in the topology.

</td></tr><tr><td>

Type

</td><td>

Type of topology. Select one from the following:-   Generic
-   Product


</td></tr></tbody>
</table>    To learn more about common fields, see [Inventory Model form - General](../reference/tni-model-form-general.md).

5.  Select **Save**.

    The related tabs appear on the form. You can view or modify the tabs information. To learn more about the related tabs, see [Inventory models additional tabs](../reference/additional-tabs-of-inventory-models.md).


## What to do next

You use the design and assign function to create a topology record. To learn more, see [Create a network topology record by using design and assign](../task/instantiate-network-topology-design-assign.md).

**Parent Topic:**[Create inventory models](creating-your-inventory-models.md)

**Related topics**  


[Network topology](visualization-of-topology.md)

[Network inventory models](using-inventory-models-tni.md)

