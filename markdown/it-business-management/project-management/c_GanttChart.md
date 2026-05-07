---
title: Gantt chart
description: A Gantt chart on the planning console is a visual representation of a project timeline that shows start and end dates of tasks, and the dependencies between tasks.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Gantt chart

A Gantt chart on the planning console is a visual representation of a project timeline that shows start and end dates of tasks, and the dependencies between tasks.

Use Gantt charts to add and delete tasks, change task dates and dependencies, and assess the progress of the overall project.

## The critical path

The critical path is highlighted in red on the Gantt chart to differentiate critical path tasks from standard tasks in blue. Not all tasks are part of the critical path, only those tasks that directly affect the finish date. Use the critical path to determine which tasks are driving the finish date. If schedule adjustments are necessary, consider making resource or other changes to those tasks on the critical path.

The tasks that are not part of the critical path and can therefore be delayed are commonly called **slack** or **float** tasks. The Gantt chart shows the slack/float tasks by default, but calculations that deal with these tasks, such as how long they can be delayed without impacting the project, is not available.

## Milestones

A milestone is a project task with a duration of **0**. Use milestones to indicate important dates in a project. If necessary, create dependencies between tasks and milestones so that a task does not start until a milestone has been reached.

## Color coding

The colors of the task bars on the Gantt chart are based on the percent complete and state of the task. The default color coding available for project and tasks is shown:

|Color|Explanation|
|-----|-----------|
|Light blue bar|Task is pending or open.|
|Dark blue bar \(full or partial\)|The percentage complete is between 1% and 100%. The dark blue section indicates the percentage complete. The task can be in the Work in Progress state or Completed state.|

**Note:** The colors of the task bars on the Gantt chart can be configured from [program](../../program-management/task/t_AccessTheProgramWorkbench.md) workbench.

## SDLC phases

Icons appear next to tasks to indicate what phase they belong to.

|Icon|Phase|
|----|-----|
|Agile phase icon|Agile phase.|
|Testing phase icon|Testing phase.|

**Note:** Tasks in the waterfall phase do not display an icon.

-   **[Gantt chart options](../reference/r_EditTasks.md)**  
Use the Gantt chart to quickly change task attributes, such as start and end time, rather than opening every Task form and modifying field values one by one.

**Parent Topic:**[Using Planning console - Legacy](c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console](../task/t_OpenPlanningConsole.md)

[Planning console tasks](../reference/r_PlanningConsoleTasks.md)

[Client side planning console](client-side-planning-console.md)

[Create a parent-child relationship on the planning console](../task/t_CreateParentChildRelatConsole.md)

[Predecessor dependencies in the planning console](../reference/r_ProjectTaskDependencyValues.md)

[Custom columns in the planning console](custom-columns-planning-console.md)

[Create a dependency from the planning console](../task/t_CreateADependency.md)

