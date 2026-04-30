---
title: Project task relationships and dependencies
description: The Project Management application enables you a create parent-child relationships between tasks and dependencies, such as finish-to-start and finish-to-finish, between tasks.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project task relationships and dependencies

The Project Management application enables you a create parent-child relationships between tasks and dependencies, such as finish-to-start and finish-to-finish, between tasks.

This table explains the types of task relationships and dependencies that you can create.

|Concept|Description|
|-------|-----------|
|Finish-to-start dependency|A dependency that indicates that a task must not be started until its predecessor finishes.|
|Start-to-start dependency|A dependency that indicates that a successor task must not be started until the predecessor task has started.|
|Start-to-finish dependency|A dependency that indicates that a successor must not be finished until the predecessor task starts.|
|Finish-to-finish dependency|A dependency that indicates that a task must not be finished until another task finishes.|
|Lag time|A manually specified time break between predecessor and successor tasks.|
|Parent task|A project task with smaller tasks, referred to as child tasks, underneath it. Child tasks break down the work of a parent task into more manageable subsets. Certain fields for child tasks, such as planned end date, roll up and affect the same field in the parent task.|
|Child task|A project task that is a subset of a larger task. Child task start dates cannot occur before the start date of the parent task.|
|Rollup task|Another term for a parent task in the context of aggregating child task items, such as effort or resources, into a larger parent task calculation. All fields on rollup task forms are read-only.|
|Roll down|State changes roll down from the project to project tasks, and from parent tasks to child tasks.|

**Note:** Only one relationship can exist between two tasks.

The Project Management application provides several properties that control how tasks are calculated and behave. See [Project property](../reference/r_InstalledWithProjectManagement.md#project_application_properties) for more information.

-   **[Project task dependencies](c_TaskDependencies.md)**  
A task dependency is created when one task is prevented from starting or finishing based on its relationship with the preceding and succeeding tasks.
-   **[Parent-child task relationships](c_Parent-ChildTaskRelationships.md)**  
If a task is relatively large and requires several users with different skills to manage, break the task into subtasks and create parent-child relationships. A child task is a relatively smaller, manageable size of work.
-   **[Parent-child rollup task calculations](c_ParentChildRollupTaskCalcs.md)**  
Date changes, stage changes, and value calculations roll up from child tasks to parent tasks.

**Parent Topic:**[Project tasks](c_ProjectTasks.md)

**Related topics**  


[Scheduling conflicts between project tasks](scheduling-conflicts.md)

[Create a project task](../task/t_CreateAProjectTask.md)

[Create a milestone](../task/t_CreateMilestones.md)

[Change requests and project tasks](c_ChangeRequestsAndProjectTasks.md)

[Project task checklists](c_project-task-checklists.md)

[Accept or reject project task notifications](../task/accept-project-task-notifications.md)

[Task resources](c_TaskResources.md)

