---
title: Configuring Field Service Capacity and Reservations Management
description: Configure Field Service Capacity and Reservations Management to manage the distribution and assignment of the work capacity for work order tasks.
locale: en-US
release: xanadu
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Configuring Field Service Capacity and Reservations Management

Configure Field Service Capacity and Reservations Management to manage the distribution and assignment of the work capacity for work order tasks.

## Configuration overview

The steps for configuring Field Service Capacity and Reservations Management are:

1.  [Activate Field Service Capacity and Reservations Management](../task/capacity-management-plugin.md)

    You can activate the Field Service Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management \) for Field Service Management if you have the admin role.

2.  [Create capacity allocation schedule](../task/allocate-schedule-for-capaity-definition.md#)

    The capacity allocation schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks.

3.  [Create a capacity definition](../task/create-capacity-definitions.md)

    Allocate work to different task attributes based on their reserved capacity percentage and defined source of capacity.

4.  [Create a demand channel](../task/create-a-demand-channel.md)

    Demand channels help organize and manage work by efficiently distributing resources. When creating a reservation rule, you can allocate a specific percentage of capacity to a particular demand channel. By tagging work orders or tasks with demand channels, you ensure they are routed correctly, improving resource allocation and scheduling accuracy.

5.  [Create a capacity assignment](assign-work-based-on-the-defined-capacity-.md)

    Create the assignment of work based on the selected source, such as agent schedules, tasks, or hours.

6.  [Override capacity assignment for a changed work schedule](../task/override-capacity-assignment.md)

    Change the default capacity assignment rules for any change in plan within a capacity definition. You can update the capacity assignments for the existing capacity definition rule at different time intervals and for different capacity buckets rather than creating a new capacity definition.


**Related topics**  


[View Capacity Usages information](../reference/capacity-usage.md)

[Field Service Capacity and Reservations Management components](../reference/capacity-management-components.md)

[Field Service Territory Capacity Analytics dashboard](../../../use/dashboards/application-content-packs/capacity-dashboard.md)

