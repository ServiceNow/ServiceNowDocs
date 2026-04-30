---
title: Create a network topology record by using design and assign
description: Create a network topology record using the design and assign function in the Telecommunications Network Inventory application. By creating the network topology, you can visualize how the network elements are organized and connected to one another.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Create a network topology record by using design and assign

Create a network topology record using the design and assign function in the Telecommunications Network Inventory application. By creating the network topology, you can visualize how the network elements are organized and connected to one another.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you instantiate a template, it creates a corresponding configuration item \(CI\) record in the Network Topology \[cmdb\_ci\_network\_topology\] table. And the root nodes are stored in the Topology Root Node \[cmdb\_network\_topology\_root\_node\] table. To learn more about the topology data model, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Design &amp; Assign topology**.

5.  Select **Next**.

6.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

7.  Select **Save**.

    A change task is created.

8.  Open the change task.

9.  On the **Task Attribute** tab, fill in the fields.

    To learn more, see [Task attributes in Topology form](../reference/task-attributes-topology-form.md).

10. Select **Submit**.


## Result

The topology and network topology root node records are created.

## What to do next

You can view the topology in the Network Viewer window. To learn more, see [Viewing a network topology](viewing-network-topology.md).

**Parent Topic:**[Instantiating inventory using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

**Related topics**  


[Create a network topology model](../concept/create-network-topology-model.md)

