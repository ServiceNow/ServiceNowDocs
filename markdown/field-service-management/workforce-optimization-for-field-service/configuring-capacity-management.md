---
title: Configuring Field Service Capacity and Reservations Management
description: Configure Field Service Capacity and Reservations Management to manage the distribution and assignment of the work capacity for work order tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/workforce-optimization-for-field-service/configuring-capacity-management.html
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Set up workforce, Configure, Field Service Management]
---

# Configuring Field Service Capacity and Reservations Management

Configure Field Service Capacity and Reservations Management to manage the distribution and assignment of the work capacity for work order tasks.

## Configuration overview

The steps for configuring Field Service Capacity and Reservations Management are:

1.  [Activate Field Service Capacity and Reservations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/capacity-management-plugin.md)

    You can activate the Field Service Capacity and Reservations Management plugin \(com.snc.fsm\_capacity\_management\) for Field Service Management if you have the admin role.

2.  [Activate Field Service Advanced Capacity and Reservations management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/capacity-console-plugin.md) to have the Capacity Console in the CSM/FSM Configurable workspace for capacity planners.
3.  [Capacity reservation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/capacity-reservations.md)

    Create capacity reservation rules to use in the capacity definition.

4.  [Create capacity allocation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/allocate-schedule-for-capaity-definition.md)

    The capacity allocation schedule helps manage and distribute your resource capacity over a set period, ensuring that a certain percentage of your resources are reserved for high-priority or same-day tasks.

5.  [Create a capacity definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/create-capacity-definitions.md)

    Allocate work to different task attributes based on their reserved capacity percentage and defined source of capacity.

6.  [Create a demand channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/create-a-demand-channel.md)

    Demand channels help organize and manage work by efficiently distributing resources. When creating a reservation rule, you can allocate a specific percentage of capacity to a particular demand channel. By tagging work orders or tasks with demand channels, you ensure they’re routed correctly, improving resource allocation and scheduling accuracy.

7.  [Associate technicians with demand channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/map-resource-demand-channel.md)

    Associate a technician with the required demand channel to accurately assign the tasks to the technician.

8.  [Create a capacity assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/assign-work-based-on-the-defined-capacity-.md)

    Create the assignment of work based on the selected source, such as agent schedules, tasks, or hours.

9.  [Create a capacity assignment override](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/override-capacity-assignment.md)

    Change the default capacity assignment rules for any change in plan within a capacity definition. You can update the capacity assignments for the existing capacity definition rule at different time intervals and for different capacity buckets rather than creating a new capacity definition.


**Related topics**  


[View Capacity Usages information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-manager-workforce/capacity-usage.md)

[Field Service Capacity and Reservations Management components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/capacity-management-components.md)

[Field Service Territory Capacity Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/capacity-dashboard.md)

