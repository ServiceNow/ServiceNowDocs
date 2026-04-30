---
title: Configuring Schedule Optimization
description: Schedule Optimization enables you to optimize task scheduling, auto-assign tasks, and adapt to changing conditions. By applying policies, you can create the best possible schedule that maximizes task assignment and minimizes travel time.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configuring Schedule Optimization

Schedule Optimization enables you to optimize task scheduling, auto-assign tasks, and adapt to changing conditions. By applying policies, you can create the best possible schedule that maximizes task assignment and minimizes travel time.

## Configuration overview

The Schedule Optimization configuration comprises four main elements: Policies, Scheduling attributes, Batches, and Scopes. The workflow involves configuring policies and scheduling attributes, creating batches to execute optimizations, and scopes optimized by the appropriate method. There are additional configurations that will trigger optimization to run throughout the day as scheduling conditions change. By following these steps, you can effectively optimize schedules based on your specified criteria and constraints.

1.  Activate the Schedule Optimization plugin. For more information, see [Activate Schedule Optimization](../task/schedule-optimization-engine-plugin.md).
2.  [Set the properties](../reference/schedule-optimization-properties.md) of the schedule optimization engine to tailor its behavior and functionality to your organization's specific needs.
3.  Create policies to determine how to optimize agent schedules based on defined objectives or constraints. For instance, if a company has 20 technicians with appointments in a city, you can configure a policy to minimize driving time. By running a batch the night before, the system evaluates all tasks and generate an optimized schedule that minimizes agents' driving time. For more information, see [Create a policy for Schedule Optimization](../task/create-policies-schedule-optimization.md).
4.  Configure the scheduling attributes to create reusable sets of common optimization settings like the default travel estimate provider and task conditions to consider when optimization runs. For more information, see [Create a scheduling attribute for Schedule Optimization](../task/configure-scheduling-attributes.md).
5.  Create optimization batches with the desired schedules and settings. For more information, see [Create a batch for Schedule Optimization](../task/create-an-optimization-batch.md#).
6.  Create optimization scopes to associate batches with existing scheduling attribute configurations, optimizing either by assignment groups or territories. For more information, see [Create a scope for Schedule Optimization](../task/create-an-optimization-job-soe.md)
7.  Schedule batches to run automatically to assign tasks to agents and optimize schedules.
8.  Optionally, create intraday configurations to automatically update agents schedules in response to events, such as an agent running late.

## Schedule Optimization based on territories

Consider the following points while implementing Schedule Optimization based on territories.

-   **Plugin dependencies**

    Optimize tasks based on territories with Schedule Optimization when the Territory Planning plugin is installed.

    -   If the Territory Planning plugin isn't installed or the Territory Model is inactive, the optimization seamlessly continues relying on assignment groups.
    -   If both the Field Service Territory Planning and Schedule Optimization plugins are installed, but the Territory Model is inactive, tasks are optimized based on assignment groups. Keep territory-related batches inactive until the Territory Planning plugin is activated.
    -   If both the Territory Planning and Schedule Optimization plugins are installed and the Territory Model is active, tasks are exclusively optimized based on territories. You can create scopes specifically for territories.
-   **Activation prerequisite**

    Before activating the Field Service Territory Model, ensure batches optimized by assignment groups are inactive, and batches optimized by territories are active.

-   **Post-activation**

    After activating the Field Service Territory Model, tasks need territories selected for Schedule Optimization to assign them to agents.

-   **Territory-Centric optimization**

    With both plugins active and the Field Service Territory Model enabled, tasks are exclusively optimized based on territories.

-   **Intraday efficiency**

    Resolves complexities of agents handling multiple territories in a day, especially during multiple shifts.

-   **Overlapping Territories management**

    In the Field Service Territory Model, territories can overlap either in geography or with shared agents. Machine learning-driven capabilities consider these overlaps for effective assignment and management in task optimization.

-   **Agent start location**

    When utilizing the Field Service Territory Model, the agents' start locations can be temporarily adjusted to a different location, with a specified start and end date. This temporary start location is utilized when assigning tasks, ensuring that logistics are optimized based on the agent's temporarily set start location. If a temporary start location is not set, or after the specified end date, the agent's location will revert to their home location. Additionally, during the agent relocation process, you can customize attributes related to agent membership and availability, allowing for flexible and efficient management of resources. For more information, see [Move agents between territories in the Territory Planning console](../task/relocate-agents-territories.md).


## Schedule Optimization with Workforce Optimization for Field Service

Schedule Optimization considers an agent's schedule and events from the Workforce Optimization for Field Service application to auto-assign tasks only when the **Enable Shift Scheduling for FSM to Determine Availability** option is enabled. For more information, see [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md) and [Activate Workforce Optimization for Field Service](../task/activate-wfo-fsm.md).

## Schedule Optimization for Planned Crews

Use Schedule Optimization to optimize task assignments to planned crews. There are two types of crews: planned crews, which are pre-created, and dynamic crews, which are dynamically created as needed. Schedule optimization only supports planned crews. To ensure effective Schedule Optimization, the Field Service Crew Operations plugin must be active, planned crews must be created in the system, and each planned crew should have a designated location and schedule.

**Related topics**  


[Activate Schedule Optimization](../task/schedule-optimization-engine-plugin.md)

