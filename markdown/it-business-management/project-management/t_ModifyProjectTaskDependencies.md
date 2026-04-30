---
title: Modify a project task dependency
description: You can modify a dependency when editing the tasks that are linked in the dependency, the dependency type, or the lag time.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Project task dependencies, Project task relationships and dependencies, Project tasks, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Modify a project task dependency

You can modify a dependency when editing the tasks that are linked in the dependency, the dependency type, or the lag time.

## Before you begin

Role required: it\_project\_manager

## About this task

Project task dependencies are saved on the Planned Task Relationship \[planned\_task\_rel\_planned\_task\] table. You can access dependencies from the planning console.

## Procedure

1.  Double-click a dependency on the Gantt chart of the [planning console](../concept/c_TheProjectPlanningConsole.md).

2.  Modify any of the fields \(see table\).

    ![Planned Task Relationship form](../image/planned_task_relationshipform.png "Planned Task Relationship form")

    |Field|Description|
    |-----|-----------|
    |Predecessor|The predecessor, or determiner, in the relationship. You can select a new task. However, it is a good practice to delete the relationship and create a new relationship between the correct tasks.|
    |Successor|The successor in the relationship. The successor depends on the predecessor. You can select a new task. However, it is a good practice to delete the relationship and create a new relationship between the correct tasks.|
    |Type|The type of relationship, which is always **Predecessor of::Successor of**. Do not change this value.|
    |Sub Type|The type of dependency. See [Project task relationships and dependencies](../concept/c_ProjectTaskRelationDepend.md) for a description of each type.|
    |Lag|The lag time between the tasks. The Enter the days, hours, minutes, and seconds for the lag. Lag time can be positive or negative.|

3.  Click **Update**.

    You can view dependencies in the Project Task related list on a Project or Project Task form and from the Project Tasks list on the workbench. These columns show the dependencies:

    -   The **Dependency** column shows the successor task in the relationship.
    -   The **Dependencies** column shows the dependency value. See [Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md) for a description of what you see in this column.

**Parent Topic:**[Project task dependencies](../concept/c_TaskDependencies.md)

