---
title: Predecessor dependencies in the planning console
description: In the WBS section of the planning console, you can create dependencies between tasks by specifying a series of values.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Predecessor dependencies in the planning console

In the WBS section of the planning console, you can create dependencies between tasks by specifying a series of values.

The **Predecessor** column on the planning console can specify dependencies between tasks. The values that you put in this column must be in the following format:

`{WBS_number}{dependency_type}+{lag_time}`

Where

-   `WBS_number` is the number of the predecessor task in the relationship.
-   `dependency_type` is one of the [types of dependencies](../concept/c_ParentChildRollupTaskCalcs.md) that the application supports.
-   `lag_time` is the amount of time, in days, to delay the start of the dependent task. This value can be positive or negative integers.

The values are entered without the curly braces \{\}. See the examples in the table.

**Note:** You can also edit tasks from the Gantt chart by clicking the relationship line. See [Gantt chart options](r_EditTasks.md) and [Modify a project task dependency](../task/t_ModifyProjectTaskDependencies.md) for details.

|Dependency type|Example|Additional information|
|---------------|-------|----------------------|
|Finish to start|**1.1fs+0**|The task you are editing starts when task 1.1 is finished.|
|Start to start|**1.1ss+0**|Task 1.1 cannot finish until the task you are editing finishes.|
|Start to finish|**1.1sf+0**|Task 1.1 cannot start until the task you are editing finishes.|
|Finish to finish|**1.1ff+0**|The task you are editing cannot finish until task 1.1 finishes.|

**Parent Topic:**[Using Planning console - Legacy](../concept/c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console](../task/t_OpenPlanningConsole.md)

[Planning console tasks](r_PlanningConsoleTasks.md)

[Client side planning console](../concept/client-side-planning-console.md)

[Gantt chart](../concept/c_GanttChart.md)

[Create a parent-child relationship on the planning console](../task/t_CreateParentChildRelatConsole.md)

[Custom columns in the planning console](../concept/custom-columns-planning-console.md)

[Create a dependency from the planning console](../task/t_CreateADependency.md)

[Using Planning console - Legacy](../concept/c_TheProjectPlanningConsole.md)

