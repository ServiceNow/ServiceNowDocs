---
title: Schedule Optimization
description: The Schedule Optimization enables you to optimize task scheduling, auto-assign tasks, and adapt to changing conditions. By applying policies, you can create the best possible schedule that maximizes task assignment and minimizes travel time.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Optimizing Scheduling and Dispatching operations, Exploring Field Service Management, Field Service Management]
---

# Schedule Optimization

The Schedule Optimization enables you to optimize task scheduling, auto-assign tasks, and adapt to changing conditions. By applying policies, you can create the best possible schedule that maximizes task assignment and minimizes travel time.

## Key Benefits

-   **Boost customer satisfaction**

    Create more predictable schedules, give preference to high-priority work, and help ensure SLAs are met. Focus on solving exceptional cases while Schedule Optimization handles the majority of tasks.

-   **Decrease costs**

    Coordinate and direct a large number of agents efficiently. Schedule the best resource to help ensure a first-time fix. Reduce travel time and overtime.

-   **Increase revenue**

    Fit more jobs into working hours to boost customer satisfaction and loyalty.

-   **Agent productivity**

    Increase agent productivity by enabling quick transitions between assignments. Minimize travel time to reduce fuel consumption and lower emissions.


## Schedule Optimization workflow diagram

The following figure illustrates the high-level workflow of Schedule Optimization.

![Schedule Optimization flow diagram showing how batches, scopes, and policies work together. See the previous text description for more information.](../image/sched-opt-flow.png "Schedule Optimization workflow")

## Key components in Schedule Optimization

Policies encapsulate your optimization goals by blending objectives and constraints. Knowing your objectives and constraints allows you to tailor your optimization strategies effectively. For example, if your team consists of 20 technicians operating within a city, a policy can be configured to minimize travel time. By running an optimization batch the night prior, the system streamlines tasks, cutting down on commuting time.

Scopes link tasks to policies and can be based on assignment groups or geographical territories. Selecting the appropriate scope is critical to ensure that your policies are applied to the right set of tasks, optimizing your resources where it counts.

Batches are the configurations that set when and how your optimizations occur. Running batches at strategic times allows you to adapt to changes and needs swiftly.

**Note:** Utilize the ‘Schedule Optimization’ Application Scope for setting up and configuring these elements.

## Schedule Optimization based on territories

Use Schedule Optimization with Field Service Territory Planning to schedule complex multi-territory assignments where an agent might be responsible for multiple territories over a longer batch processing period. Assign tasks to agents whether they’re primary or secondary members of a single or multiple territories.

## Intra-day Schedule Optimization

Intra-day Optimization re-optimizes schedules for groups or territories in real-time based on changing conditions. Useful when tasks are canceled, delayed, or new tasks come in. For example:

-   A cable service provider deals with last-minute cancellations.
-   A weather event results in new, high-priority repair tasks.
-   A technician calls out sick for the day.

**Note:** Field Service Scheduling Automation must be installed to use Intra-day Optimization.

## Schedule Optimization based on Capacity and Reservations Management

Use Schedule Optimization with Capacity and Reservations Management to allocate tasks. This integration considers defined capacities and reservations for both internal teams and external contractors before scheduling and allocating tasks.

## Schedule Optimization for Planned Crews

Use schedule optimization to optimize task assignments to planned crews. There are two types of crews: planned crews, which are pre-created, and dynamic crews, which are dynamically created as needed. Schedule optimization only supports planned crews.

## Schedule Optimization with Workforce Optimization for Field Service

Use Schedule Optimization to consider agents' schedule and events from the Workforce Optimization for Field Service application to auto-assign tasks.

## Schedule Optimization with advanced task dependencies

Use Schedule Optimization to efficiently assign tasks considering advanced task dependencies between them.

**Related topics**  


[Configuring Schedule Optimization](schedule-optimization-engine.md)

