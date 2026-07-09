---
title: Gantt chart
description: A Gantt chart on the planning console is a visual representation of a project timeline that shows start and end dates of tasks, and the dependencies between tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/project-management/c\_GanttChart.html
release: yokohama
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Planning console - Legacy, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Gantt chart

A Gantt chart on the planning console is a visual representation of a project timeline that shows start and end dates of tasks, and the dependencies between tasks.

Use Gantt charts to add and delete tasks, change task dates and dependencies, and assess the progress of the overall project.

## Gantt charts

\[Omitted image "gantt\_chart\_planning\_console.png"\] Alt text: Example Gantt chart

## The critical path

The critical path is highlighted in red on the Gantt chart to differentiate critical path tasks from standard tasks in blue. Not all tasks are part of the critical path, only those tasks that directly affect the finish date. Use the critical path to determine which tasks are driving the finish date. If schedule adjustments are necessary, consider making resource or other changes to those tasks on the critical path.

The tasks that are not part of the critical path and can therefore be delayed are commonly called **slack** or **float** tasks. The Gantt chart shows the slack/float tasks by default, but calculations that deal with these tasks, such as how long they can be delayed without impacting the project, is not available.

## Milestones

A milestone is a project task with a duration of **0**. Use milestones to indicate important dates in a project. If necessary, create dependencies between tasks and milestones so that a task does not start until a milestone has been reached.

\[Omitted image "milestone\_between\_two\_tasks.png"\] Alt text: Milestone example

## Color coding

The colors of the task bars on the Gantt chart are based on the percent complete and state of the task. The default color coding available for project and tasks is shown:

<table id="table_o5w_ysm_2s"><thead><tr><th>

Color

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

Light blue bar\[Omitted image "light\_blue\_bar.png"\] Alt text: Screenshot for Light blue bar

</td><td>

Task is pending or open.

</td></tr><tr><td>

Dark blue bar \(full or partial\)\[Omitted image "dark\_blue\_bar.png"\] Alt text: Screenshot for dark blue bar

</td><td>

The percentage complete is between 1% and 100%. The dark blue section indicates the percentage complete. The task can be in the Work in Progress state or Completed state.

</td></tr></tbody>
</table>**Note:** The colors of the task bars on the Gantt chart can be configured from [program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/program-management/t_AccessTheProgramWorkbench.md) workbench.

## SDLC phases

Icons appear next to tasks to indicate what phase they belong to.

|Icon|Phase|
|----|-----|
|\[Omitted image "agile\_icon.png"\] Alt text: screenshot for Agile phase icon|Agile phase.|
|\[Omitted image "testing\_phase\_icon.png"\] Alt text: screenshot for testing phase icon|Testing phase.|

**Note:** Tasks in the waterfall phase do not display an icon.

-   **[Gantt chart options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/r_EditTasks.md)**  
Use the Gantt chart to quickly change task attributes, such as start and end time, rather than opening every Task form and modifying field values one by one.

**Parent Topic:**[Using Planning console - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console]()

[Planning console tasks]()

[Client side planning console]()

[Create a parent-child relationship on the planning console]()

[Predecessor dependencies in the planning console]()

[Custom columns in the planning console]()

[Create a dependency from the planning console]()

