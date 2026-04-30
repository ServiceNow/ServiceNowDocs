---
title: Managing work order tasks
description: Use work order tasks to define separate activities that must be done to complete a work order.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing work orders and work order tasks, Using Field Service Management, Field Service Management]
---

# Managing work order tasks

Use work order tasks to define separate activities that must be done to complete a work order.

A [Managing work orders and work order tasks](../../field-service-management/concept/managing-work-orders.md) contains one or more work order tasks. These tasks allow qualifiers to define separate activities that must be done to complete a work order.

When a user with the wm\_qualifier role or a qualifier combination role moves a work order from **Draft** to **Awaiting Qualification**, a work order task is automatically created and populated with information from the work order. This user can edit existing tasks or create new tasks at any time.

A key feature in Field Service Management is the ability to create multiple work order tasks under a single work order. Splitting a work order into separate tasks, when necessary, enables qualifiers to:

-   Assign different aspects of a single work order to different agents.
-   Assign work to agents with different skill sets.
-   Assign work to agents in different locations.
-   Schedule parts of the work at different times.
-   Schedule tasks so they are done one after another.
-   Schedule tasks so they are done at the same time by different agents.
-   Schedule additional tasks, if necessary, to complete the work order.
-   Coordinate the arrival and usage of the parts required to complete a work order.

-   **[Create a work order task](../task/t_CreateAWorkOrderTask.md)**  
Create a work order task from a work order.
-   **[Clone a work order task](../task/t_CloneAWorkOrderTask.md)**  
Clone existing tasks to quickly create new tasks.
-   **[Delete a work order task](../task/t_DeleteAWorkOrderTask.md)**  
Work order tasks can be deleted by users with the wm\_admin role.
-   **[Assign preferred agents to tasks](../../field-service-management/task/assign-preferred-agents-tasks.md)**  
Identify the agents most preferred for working on a customer account and assign them to tasks.
-   **[Exclude Field Service agents from being assigned work order tasks](../../field-service-management/task/exclude-agents-from-being-assigned-tasks.md)**  
Exclude Field Service agents from being assigned work order tasks with dynamic scheduling, or Schedule Optimization.
-   **[Create dependencies between work order tasks](../task/t_SetAnUpstreamTask.md)**  
If a work order contains multiple tasks, you can create dependencies between the tasks that determine the order in which tasks are performed.
-   **[Create a work order task dependency using a work order template](../task/t_CrtWOTskDpdWOTmplt.md)**  
In addition to creating work order task dependencies that are inherited from the associated work orders, you can also create work order templates that contain task dependencies.
-   **[Create work order tasks in CSM Agent Workspace](../../field-service-management/task/create-workorder-tasks-workspace.md)**  
Create work order tasks to track the work created for a work order.
-   **[Qualify work order tasks in CSM Agent Workspace](../../field-service-management/task/qualify-workorder-tasks-workspace.md)**  
Qualify work order tasks associated with a work order to dispatch them to agents who can work on the task.
-   **[Prioritize a work order task for Schedule Optimization](../../field-service-management/task/prioritize-a-work-order-task-for-schedule-optimization.md)**  
Add penalties and values to a work order task to define the importance of the task.

**Parent Topic:**[Managing work orders and work order tasks](../../field-service-management/concept/managing-work-orders.md)

