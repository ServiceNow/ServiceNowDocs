---
title: Configuring Dynamic Scheduling
description: Configure dynamic scheduling to let dispatchers to easily assign, change, or cancel work tasks. Optimize work order task assignments and streamline field service operations by setting up dynamic scheduling according to your organization's requirements.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Configuring Dynamic Scheduling

Configure dynamic scheduling to let dispatchers to easily assign, change, or cancel work tasks. Optimize work order task assignments and streamline field service operations by setting up dynamic scheduling according to your organization's requirements.

Dynamic scheduling enables dispatchers to auto assign tasks and adapt to changing conditions, as well as needing to focus only on exception cases. Using this feature, you can:

-   Select a set of tasks for scheduling.
-   Prioritize the tasks in the set based on ordering rules \(for example, assign P1 tasks first\).
-   Use ordering rules and unassignment constraints to unassign previously assigned tasks to allow the assignment of higher priority tasks.
-   Use selection criteria such as agent skills and travel time to select agents.
-   Reassign tasks for agent time off.

## Configuration overview

The steps to set up Dynamic Scheduling are:

1.  [Activate dynamic scheduling](../task/activate-dynamic-scheduling-plugin.md): Activate the Dynamic Scheduling plugin \(com.snc.dynamic\_scheduling\) to enable the dynamic scheduling functionality in your system.
2.  [Learn Dynamic Scheduling process engine](dynamic-scheduling-process-engine.md): Dynamic Scheduling optimizes and assign work orders to field service agents in real-time. It involves continuously monitoring the status of tasks and available agents and making intelligent decisions to ensure that tasks are assigned to the most appropriate agent at the most appropriate time.
3.  [Roles and personas required for Dynamic Scheduling](roles-and-personas-for-dynamic-scheduling.md): Manage dynamic scheduling process with administrators, dispatchers, and field service agents.
4.  [Set up agent schedules for dynamic scheduling](agent-schedule-dynamic.md): Set up agent schedules so that dynamic scheduling systematically ensures optimal task allocation.
5.  [Set up Dynamic Scheduling as scheduling mechanism](../task/dynamic-sched-config-field-service.md): Select dynamic scheduling as the preferred task assignment method. This ensures that tasks are automatically assigned to field agents based on predefined criteria and rules.
6.  [Review system properties and components for Dynamic Scheduling](../reference/dynamic-sched-system-properties.md): Review the properties and other installed components related to dynamic scheduling. Customize the settings to align with your organization's specific requirements and business processes.
7.  [Configure dynamic scheduling](../task/create-dynamic-scheduling-config.md#): Create Dynamic scheduling such as task filter, task ordering rule, and unassignment criteria to ensures tasks are allocated to agents with the right expertise who are nearby. This optimizes agent utilization and guarantees that assignments are handled by the most qualified individuals.
8.  [Create a task filter for dynamic scheduling](../task/create-dynamic-scheduling-config.md#): Define criteria to select eligible tasks for dynamic scheduling. Factors like task types, priorities, and attributes determine task eligibility. Task filters help focus on specific tasks for efficient scheduling.
9.  [Create a task ordering rule](../task/create-dynamic-scheduling-config.md#): Create rules to determine the order of task assignments from the selected set of tasks. For instance, designate Priority 1 tasks as the top priority, ensuring swift attention to critical work. These rules enhance task assignments by aligning them with organizational priorities.
10. [Set task unassignment rules for flexibility](../task/create-dynamic-scheduling-config.md#): Create unassignment rules to make task assignments more flexible. This guarantees that service remains uninterrupted by either unassigning or reassigning tasks. It ensures that all tasks are attended to even if someone is absent. For example, if a more important task comes up, you can unassign less critical ones to make room for it. This optimizes resource use and ensures high-priority tasks get the attention they need.
11. Validate configuration to identify any potential issues or misconfiguration that may impact the performance of dynamic scheduling.
12. Optionally, you can also use the advanced configuration options for dynamic scheduling include assigning the same agent to all tasks, priority assignment for critical high-priority work orders, customer preferences for technicians or exclusions, proximity, and more.

## Dynamic Scheduling for Planned Crews

Use Dynamic Scheduling to optimize task assignments to planned crews. There are two types of crews: planned crews, which are pre-created, and dynamic crews, which are dynamically created as needed. Dynamic Scheduling supports both planned crews and dynamic crews. To ensure task assignment to crews, the Field Service Crew Operations plugin must be active, planned crews must be created in the system, and each planned crew should have a designated location and schedule.

**Related topics**  


[Assigning work order tasks to agents using dynamic scheduling](using-dynamic-scheduling.md)

[Dynamic scheduling](dynamic-scheduling.md)

