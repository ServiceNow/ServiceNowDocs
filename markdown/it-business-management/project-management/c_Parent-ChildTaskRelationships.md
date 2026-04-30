---
title: Parent-child task relationships
description: If a task is relatively large and requires several users with different skills to manage, break the task into subtasks and create parent-child relationships. A child task is a relatively smaller, manageable size of work.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project task relationships and dependencies, Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Parent-child task relationships

If a task is relatively large and requires several users with different skills to manage, break the task into subtasks and create parent-child relationships. A child task is a relatively smaller, manageable size of work.

When you group child tasks together under a parent, values such as **Estimated cost** aggregate and roll up to the parent task. So the parent task takes on the form of a summary task or rollup task for its child tasks. **Planned start date** and **Planned end date** rollup occurs when you create child tasks: the duration of the parent automatically adjusts to cover its child tasks.

A parent-child relationship is different from a dependency relationship. In a dependency, one task must finish before another begins. In a parent-child relationship, any number of tasks can be nested under a parent task with or without any dependencies. When you create a parent-child relationship, the parent task number is saved in the **Parent** field in the Project Tasks table. All project management tasks have a parent: either another project task or the project itself.

Unlike a dependency, a parent-child relationship is not saved as a record in any table. The only modification that takes place when a parent-child relationship is modified is the **Parent** field in the child task record.

You can create predecessor-successor relationships between child tasks with different parents, between two different parent tasks, or between a child task and another parent task. However, if the predecessor task finishes after the successor task starts, creating a dependency between child tasks that have different parents is not allowed.

**Note:** On the Gantt chart, you can drag-and-drop the parent task to move the entire hierarchy to a new location on the schedule.

-   **[Create a parent-child relationship on the Project Task form](../task/t_CreateParentChildRelationship.md)**  
You can create a child task from any project task form.
-   **[Time constraints in parent-child relationships](../reference/r_TimeConstraintsParent-ChildRels.md)**  
Parent-child task relationships have several effects on task time constraints.

**Parent Topic:**[Project task relationships and dependencies](c_ProjectTaskRelationDepend.md)

