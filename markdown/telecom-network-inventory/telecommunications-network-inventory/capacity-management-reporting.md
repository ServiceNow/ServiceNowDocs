---
title: Capacity management
description: Capacity management in Telecommunications Network Inventory enables you to calculate the capacity of physical entities in your network. By effectively managing the capacity, you can plan, monitor, and optimize the resources to make sure that the network can meet your current and future demands efficiently.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Capacity management

Capacity management in Telecommunications Network Inventory enables you to calculate the capacity of physical entities in your network. By effectively managing the capacity, you can plan, monitor, and optimize the resources to make sure that the network can meet your current and future demands efficiently.

## Introduction to capacity management

The capacity management in Telecommunications Network Inventory uses functions and definitions to calculate and report the capacity of your network assets. The capacity metric estimates the maximum, occupied, and available network resources such as ports, slots, or racks in a telecommunication network. You can use this metric result to report the capacity of a network asset that can be used for future expansion of the network design.

## Capacity calculation use cases

When you create a configuration item \(CI\) using the design and assign function, the system automatically calculates the available capacity of the associated CIs. The Telecommunications Network Inventory application uses predefined definitions and functions to calculate the capacity. So, whenever there’s a modification in the current design, the system automatically triggers the capacity calculation, and updates the metrics. The metrics shows estimated maximum, occupied, available, and usage values for an entity. This approach makes sure that resource consumption is effectively managed. Also, this calculation improves the accuracy of the design and assign function.

For example, When you add a new piece of equipment to a rack, it's important to determine the available racks within the equipment holder. When you create an equipment record, the predefined capacity definition runs, and the metric automatically updates the rack availability data. The capacity definition includes functions that determine the maximum and occupied racks. Subsequently, it calculates the difference between the maximum and occupied racks. For instance, if the maximum number of racks is 10 and the occupied racks are 7, there are 3 available racks. If the maximum number of racks are 10 and the occupied racks are 10, the available rack count is 0, which indicates no racks are available. Then the system consolidates the result in the capacity metric. This process provides you with the accurate capacity and availability information of the racks.

You can customize the capacity calculation for each type of Configuration Item \(CI\). This feature enables you to create and configure the function, definition, and metric to calculate the capacity. To learn more about configuring the capacity function and creating the metric, see [Configuring capacity management](configuring-capacity-management.md).

## Capacity management workflow

Capacity management uses function, definition, and metric tables to calculate and report the capacity. In the Telecommunications Network Inventory application, the system runs the capacity function and aggregates the results into the capacity metric table. It creates an available metric for capacity and a usage metric where the percentage value of available capacity is stored. Whenever a design change is happened, the system triggers an API to calculate the capacity using predefined functions and definitions. You can also manually calculate the capacity by selecting the **Calculate capacity** button in the inventory record.

To learn more about capacity function, definition, and metric, see [Configuring capacity management](configuring-capacity-management.md).

