---
title: Project task dependencies
description: A task dependency is created when one task is prevented from starting or finishing based on its relationship with the preceding and succeeding tasks.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Project task relationships and dependencies, Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project task dependencies

A task dependency is created when one task is prevented from starting or finishing based on its relationship with the preceding and succeeding tasks.

The Project Management application supports [several types of dependencies](c_ProjectTaskRelationDepend.md).

## Task time constraints

The Project Task form includes a **Time Constraint** field, which can be one of the following values:

-   If a task is set to **Start ASAP**: The task appears on the Gantt chart as starting when the dependency allows it. However, a task can start on a later date when a lag value is set for the relationship.
-   If a task is set to **Start on specific date**: The task appears on the Gantt chart as starting on the constraint date. The start date of such a task is not impacted even after you put the task in a relation to another task, for example, FS relation.
-   If a task is set to **Start no earlier than**: The task appears on the Gantt chart as starting on or after the constraint date. If the task has no predecessor, the task starts on the specified date. The start date changes to a later date based on the predecessor task end date or if the task is in a relation to another task, for example, FS relationship.
-   If a task is set to **Start no later than**: The task appears on the Gantt chart as starting on or before the constraint date. If the task has any predecessor task, the dependency on the predecessor task determines when the task can start. A scheduling conflict occurs if the predecessor task attempts to move the task beyond the date specified in the **Constraint date** field.

    **Note:** The [project property](../reference/r_InstalledWithProjectManagement.md#table_Project-Properties-system-properties) **Retain start on constraint on tasks after adding relations** controls the behavior for **Start on** selection. The property is set to True by default and is not editable.

-   A task that is not honoring dependency is indicated with a red calendar icon ![task with must start on dependency icon](../image/pc-task-dep-icon.png) on the Planning Console. If you want the task to honor the dependency and adjust the start accordingly, change the constraint type of the task to **Start ASAP**.

-   **[Create a dependency from the planning console](../task/t_CreateADependency.md)**  
You can create a dependency between two tasks on the planning console.
-   **[Modify a project task dependency](../task/t_ModifyProjectTaskDependencies.md)**  
You can modify a dependency when editing the tasks that are linked in the dependency, the dependency type, or the lag time.
-   **[Remove a dependency](../task/t_RemoveDependencies.md)**  
Use the planning console to remove a dependency that is no longer necessary.

**Parent Topic:**[Project task relationships and dependencies](c_ProjectTaskRelationDepend.md)

