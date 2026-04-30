---
title: Add an external dependency on planning console
description: Add an external dependency between two projects on the planning console. Use the work breakdown structure \(WBS\) column of the planning console to create a dependency between the different projects tasks.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [External dependencies, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add an external dependency on planning console

Add an external dependency between two projects on the planning console. Use the work breakdown structure \(WBS\) column of the planning console to create a dependency between the different projects tasks.

## Before you begin

Role required: it\_project\_manager

## Procedure

1.  Right-click a task in the WBS column of the planning console.

2.  Click **Add External Dependency**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Project|The predecessor project that the dependency is added from.|
    |Task|The task in the predecessor project that the dependency is added from.|
    |Dependency Type|The [type](../concept/external-dependency-types.md) of external dependency: **Hard** or **Soft**.|

4.  Click **OK**.


## Result

-   A shadow task corresponding to the predecessor task appears in the WBS section of the planning console of the successor project. A similar shadow task corresponding to the successor task appears in the WBS section of the planning console of the predecessor project.

    A shadow task is shown as a grayed out task in WBS column.

-   A shadow task corresponding to the predecessor task appears in the **Project Tasks** related list on the successor [project form](t_CreateAProject.md#table_mb3_rfw_1r). A similar shadow task for the successor task appears in the **Project Tasks** related list on the predecessor project form.
-   The **Dependency** column in WBS column of the planning console of the successor project shows the external dependency value between the projects and tasks. The external dependency value has the following format:

    `{project_number}\{WBS_number}{dependency_type}+{lag_time}`

    Where

    -   `project_number` is the number of the predecessor project.
    -   `WBS_number` is the number of the predecessor task in the relationship.
    -   `dependency_type` is the **finish to start** dependency type that the application supports.
    -   `lag_time` is the amount of time, in days, to delay the start of the dependent task. This value can be positive or negative integers.

**Note:** The external dependencies are displayed only when the **Hide External Dependencies** switch on the [planning console](../reference/r_PlanningConsoleTasks.md) is turned off. However, the **Dependency** column in the WBS section of the successor project still shows the value of the external dependency.

## Example

In the example below, an external dependency is created between two projects P1 and P2. P1T1 is a shadow task of predecessor project P1, and PRJ0010127\\1fs+0 is the external dependency value in **the Dependency** column of the planning console of the successor project P2.

![External dependency example](../image/ExternalDependencyExample.png)

## What to do next

Check for any external dependency related [notifications](../reference/r_PlanningConsoleTasks.md) that may impact the project or its tasks.

**Parent Topic:**[External dependencies](../concept/external-dependencies.md)

**Related topics**  


[Types of external dependencies](../concept/external-dependency-types.md)

