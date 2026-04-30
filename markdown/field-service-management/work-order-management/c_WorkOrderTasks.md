---
title: Manage work order tasks
description: Use work order tasks to define separate activities that must be done to complete a work order.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Prepare work orders, Using Field Service Management, Field Service Management]
---

# Manage work order tasks

Use work order tasks to define separate activities that must be done to complete a work order.

A work order contains one or more work order tasks. These tasks allow qualifiers to define separate activities that must be done to complete a work order.

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
-   **[Create task dependency using a work order template](../task/t_CrtWOTskDpdWOTmplt.md)**  
In addition to creating work order task dependencies that are inherited from the associated work orders, you can also create work order templates that contain task dependencies.
-   **[Create advanced task dependency using a work order template](../../field-service-management/task/create-a-work-order-advanced-task-dependency-using-a-work-order-template.md)**  
You can create work order templates that contain advanced task dependencies.
-   **[Create work order tasks in CSM Agent Workspace](../../field-service-management/task/create-workorder-tasks-workspace.md)**  
Create work order tasks to track the work created for a work order.
-   **[Qualify work order tasks in CSM Agent Workspace](../../field-service-management/task/qualify-workorder-tasks-workspace.md)**  
Qualify work order tasks associated with a work order to dispatch them to agents who can work on the task.
-   **[Prioritize a work order task for Schedule Optimization](../../field-service-management/task/prioritize-a-work-order-task-for-schedule-optimization.md)**  
Add penalties and values to a work order task to define the importance of the task.
-   **[Onsite arrival and check-in](../../field-service-management/reference/onsite-arrival-and-check-in.md)**  
The Onsite Arrival and Check-in process ensures accurate task location confirmation and effective time tracking.
-   **[Manage inventory in Field Service Management](../../field-service-management/concept/sourcing-parts.md)**  
Get the parts you need to complete the tasks.
-   **[Review a task](../../field-service-management/task/review-send-task-back.md)**  
As a reviewer, review the details of a work order task. If the details are sufficient, you can close the task. If more information is required, send the task back to the agent so they can add the requested details.
-   **[Using rate types and labor rate cards](../../field-service-management/concept/using-rate-types-labor-rate-cards.md)**  
Use rate types and labor rate cards to define different cost rates for different activities recorded by field service agents.
-   **[Assign a knowledge article to a work order or work order task](../../field-service-management/task/add-knowledge-workorder.md)**  
Add additional information to complete tasks.
-   **[Review and approve time sheets](../../field-service-management/task/field-service-manager-approve-time.md)**  
Managers can review time cards and time sheets for agents in their assignment groups.

**Parent Topic:**[Prepare work orders](../../field-service-management/concept/preparing-work-orders.md)

