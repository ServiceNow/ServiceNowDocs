---
title: Gantt chart options
description: Use the Gantt chart to quickly change task attributes, such as start and end time, rather than opening every Task form and modifying field values one by one.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Gantt chart, Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Gantt chart options

Use the Gantt chart to quickly change task attributes, such as start and end time, rather than opening every Task form and modifying field values one by one.

From a Gantt chart, you can modify the following task attributes:

<table id="table_skt_4fc_br"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned start date for project tasks

</td><td>

Move the task along the timeline to change the start time and to impose a Time constraint of Start on a specific date. You can also drag a task to change its start date if the task Time constraint is set to Start on a specific date \(not Start ASAP\) and the task has not yet started. The start date of a task cannot be modified if the task already started \(has an actual start date\), the task has already ended \(has an actual end date\), or the task time constraint is set to Start ASAP.You can also modify the dates in the **Planned start date** column on the console.

</td></tr><tr><td>

Planned start date for the project

</td><td>

Modify the dates in the **Planned start date** column on the console.

 You can add tasks that start earlier than the project's planned start date. By default, the planned start date shifts earlier or later when you add tasks to align with the earliest task start date. However, you can enable the [project property](r_InstalledWithProjectManagement.md#project_application_properties) **Rollup project start date from tasks** to retain the planned start date of the project even if you add tasks with a planned start date that is earlier or later.

</td></tr><tr><td>

Planned end date

</td><td>

Drag the right edge of the task bar to extend the planned end date. You can extend the planned of date only for tasks that are not parent tasks and that have not yet ended.

</td></tr><tr><td>

Dependencies

</td><td>

To edit or delete a dependency, double-click an existing dependency connector line between two tasks and update the settings in the Planned Task Relationship popup. The relationship Type for planned tasks is Predecessor of::Successor of and should not be changed.

</td></tr><tr><td>

Lag time and lead time

</td><td>

Lag time is an interval of time between the end of a predecessor task and the start of a successor task. The lag time delays the predecessor by an amount that you specify. Lead time is an interval of time that the predecessor task is allowed to start before it normally would. It is essentially a negative lag time. The value in the **Lag** field specifies both lag and lead time.

 To edit the **Lag** value, double-click a connector and update the settings in the Planned Task Relationship form. Enter a negative value to specify a lead time.

</td></tr><tr><td>

Resources

</td><td>

To change a user resource for an existing task or add a resource to a new task, double-click the task bar and edit the Assigned to field in the Project Task form.**Note:** The resources in **Assigned to** column can be constrained to be derived only from the allocated resource plans associated with the project or any of its task.

</td></tr></tbody>
</table>The Project Management application provides several properties that control how tasks are calculated and behave. See [Project property](r_InstalledWithProjectManagement.md#project_application_properties) for more information.

**Parent Topic:**[Gantt chart](../concept/c_GanttChart.md)

