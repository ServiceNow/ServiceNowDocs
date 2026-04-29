---
title: Planning console tasks
description: You can perform several tasks on the planning console that you can perform on lists and forms, such as creating project tasks and copying projects. You can also perform several tasks unique to the console.
locale: en-US
release: australia
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Planning console tasks

You can perform several tasks on the planning console that you can perform on lists and forms, such as creating project tasks and copying projects. You can also perform several tasks unique to the console.

<table id="table_ukw_ftd_2s"><thead><tr><th>

Task

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Display a project in the planning console

</td><td>

Select the project from the list in the project workspace banner. ![Project list.](../image/project_selection.png "Project list")

</td></tr></tbody>
</table><table id="table_m3q_lsy_fdc"><thead><tr><th>

Task

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Create a project task

</td><td>

Select the add task below icon \(![Add task icon](../image/add_task_icon.png)\) on the row to create a new task.

 You can also select an existing task to determine the insertion point for the new task, and then select the add task above icon \(![Add task icon.](../image/add_task_above.png)\) or the add task below icon \(![Add task icon.](../image/add_task_below.png)\).

</td></tr><tr><td>

Move a task up or down in the hierarchy

</td><td>

Select an existing task, and then select the move up \(![Move up icon](../image/move_up_icon.png)\) or move down \(![Move down icon](../image/move_down_icon.png)\) icons.

</td></tr><tr><td>

Indent or unindent a task in the hierarchy

</td><td>

Select an existing task, and then select the unindent \(![Unindent icon.](../image/promote_icon.png)\) or indent \(![Indent icon.](../image/demote_icon.png)\) icons.

</td></tr><tr><td>

Edit a task record

</td><td>

Right-click a task and select **Edit**. The Project Task form appears in the overlay. You can also edit a field directly in one of the columns in the planning console. You can also edit project tasks that represent phases in the project workbench.

</td></tr><tr><td>

Edit the **State** field

</td><td>

Double-click the value in the **State** column to select a new state. The value of the **State** field also changes automatically when % complete is changed for a task.

</td></tr><tr><td>

View and modify task status

</td><td>

View the status of the project task based on the difference of the planned end date of the task from the current date. The status of the task updates automatically from Green to Yellow to Red as the planned end date approaches.You can manually update the task status by double-clicking the **Status** column and selecting a different task status. For more information, see **Status** field description in the [Create a project task from a project](../task/t_CreateATaskFromAProject.md) topic.

</td></tr><tr><td>

Add an agile phase or a test phase

</td><td>

Right-click a project and select **Add Agile Phase** or **Add Test Phase**. The agile phase icon or test phase icons appear next to the task in the **Name** column. See [phase icons](../concept/c_GanttChart.md#phase_icons). **Note:**

-   The **Add Agile Phase** option is available only for Agile and Hybrid projects. You must also have the Agile Development 2.0 plugin installed.
-   You can add multiple agile phases and multiple test phases to a project.
-   You can add only one test phase for a test plan in a project. You must have the Test Management plugin installed to view the **Add Test Phase** option.
-   An agile phase cannot overlap another agile phase for an assignment group in a project.
-   While creating a story, if a project has only one phase, then the story is tagged to the phase.

</td></tr><tr><td>

Open a test plan or story

</td><td>

Right-click a task \(a task that represents a phase in the workbench\) and then select **Manage Test Plan**. Select **View Stories** to view the stories list. If you have the scrum\_product\_owner role, select **View Stories** to navigate to the **Backlog** tab of the **Agile Board**.**Note:** The **View Stories** option is available only for Agile and Hybrid projects. You must also have the Agile Development 2.0 plugin installed.

</td></tr><tr><td>

Cancel a resource plan for a Closed project

</td><td>

Right-click the project and select **Cancel Resource Plans**. All past and future allocations for the selected [resource plan are canceled](../../resource-management/task/cancel-resource-plan-from-project-or-demand.md).The option is available only for a project in any of the Closed states.

</td></tr><tr><td>

Complete a resource plan for a Closed project

</td><td>

Right-click the project and select **Complete Resource Plans**. All the requested and resource allocations for the resource plan post the completion date are deleted.The option to [complete resource plans](../../resource-management/task/complete-resource-plan-from-project-or-demand.md) is available only for a project in any of the Closed states.

</td></tr><tr><td>

Add an external dependency between tasks of different projects

</td><td>

Right-click a task and select **Add External Dependency**. Select the project and task to which the [dependency is added](../task/create-external-dependency-planning-console.md).

</td></tr><tr><td>

View the project name of an external dependency

</td><td>

Point to the link icon \(![Link icon](../image/link-icon.png)\) beside the external dependency task to display a tooltip which shows the name of the project to which the external dependency is added.

</td></tr><tr><td>

Change the time constraint for a task

</td><td>

Double-click a task under the **Constraint type** column and select an option: **Start ASAP**, **Start on specific date**, **Start no earlier than**, or **Start no later than**.-   You can change the **Constraint type** for Automatic projects only.
-   When you change the time constraint for a task from **Start on specific date** to **Start ASAP** or vice versa, the planned start date and planned end date of the task are recalculated accordingly.
-   The **Constraint date** column displays the start date for all the constraint types other than **Start ASAP** tasks. This column is not available by default, you must add this column to the Planning Console from the Configuration menu.
-   The option is not available for a parent task. If a task has child tasks, the option is available only for the child tasks.
-   You cannot create a parent task with **Start no later than** or **Start on specific date** time constraint. When a new child task is added to a task with these time constraints, the time constraint for the parent task is converted to **Start ASAP**.
-   You cannot change constraint type for projects with **Calculation** type set as Manual.

</td></tr><tr><td>

Allow task dates outside schedule

</td><td>

Right-click a project task and select **Allow outside schedule**. The selected task is allowed to start and end on a non-schedule day \(outside the regular project schedule\) such as on a weekend. The off schedule task icon \(![Off-schedule task icon](../image/OffScheduleTaskIcon.png)\) appears next to the task in the **Short description** column.For example, if you use the project schedule Monday to Friday, 8:00 to 17:00 and a project task of duration 2 days should start on Saturday, then an off-schedule task is allowed to be scheduled on Saturday and end on Sunday. Similarly, if a task of duration 3 days starts on Friday, then an off-schedule will end on Sunday as opposed to ending on Tuesday.

 -   The option is not available for a parent task. When a task is made off-schedule, its parent also becomes off-schedule. The project also operates as out of schedule if any of the children is set to out of schedule.
-   Once a task is allowed outside the schedule, the **Follow schedule** option is available for the task. Right-click the task and select **Follow schedule** to follow the schedule for the task.

 **Note:**

-   There is no difference between an off-schedule and an on-schedule task if there is no schedule defined at the project level.
-   1 day is 8 hours for a task in a regular schedule and 24 hours for a task outside the schedule.

</td></tr><tr><td>

Convert a task to milestone

</td><td>

Right-click a task and select **Convert to milestone**. -   You can convert a task to a milestone only until it is not in **Work in Progress** state. Once work in progress, the option appears as greyed out for the task.
-   The option is not available for a parent task. If a task has child tasks, the option is available only for the child tasks.

</td></tr><tr><td>

Show or hide external dependencies

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select the **Hide External Dependencies** switch. When this option is enabled, the external dependencies are not displayed when you add an external dependency between two projects. However, the **Dependency** column in the WBS section of the successor project still shows the value of external dependency.

</td></tr><tr><td>

Show external dependency notifications

</td><td>

Select the notification bell icon ![Notification bell icon.](../image/NotificationIcon.png) to display the notifications raised in the successor project. The notifications are triggered as a result of changes made in the predecessor project.![External dependency notification example.](../image/ExternalDependNotification.png)

-   For a [soft dependency](../concept/external-dependency-types.md), select **Accept** or **Reject** to accept or reject the changes in the notification.
-   For a hard dependency, view the displayed notification to review the changes in the notification.

</td></tr><tr><td>

Save changes to the server

</td><td>

Select the save icon ![Save icon.](../image/save_icon.png) to commit changes made in the planning console. The option is available only when [Client Side Planning Console](../concept/client-side-planning-console.md) is enabled.

</td></tr><tr><td>

Expand or contract column width

</td><td>

Select the side of the column and drag it right or left.

</td></tr><tr><td>

Show or hide columns in the planning console

</td><td>

Select the show or hide columns in gantt icon \(![Show or hide columns in gantt icon.](../../project-workspace/image/gear_icon.png)\), and then select or clear the check boxes for the columns available. Admin can [customize](../concept/custom-columns-planning-console.md) which columns appear in this list. The selection is saved in the user preference. The next time you open the planning console, the same columns you selected will appear.

</td></tr><tr><td>

Select WBS levels to show

</td><td>

Select the show or hide columns in gantt icon \(![Show or hide columns in gantt icon.](../../project-workspace/image/gear_icon.png)\), and then select the level from the [WBS](../concept/c_WorkBreakdownStructure.md) **Depth** list.

</td></tr><tr><td>

Expand or collapse sublevels for any level

</td><td>

Select the arrow to expand or collapse any task that has one or more subtasks.

</td></tr></tbody>
</table><table id="table_anw_lsy_fdc"><thead><tr><th>

Task

</th><th>

How to perform the task

</th></tr></thead><tbody><tr><td>

View a summary of a task

</td><td>

Point to a task.![Tooltip shows the summary of the task.](../image/task_summary.png "Tooltip for summary of the task")

</td></tr><tr><td>

Change the planned start or end dates of a task

</td><td>

Select the task, and then drag the left or right edge of the task bar.

</td></tr><tr><td>

Move a task to a new date

</td><td>

Select the task, and then drag the whole task bar to a new location.

</td></tr><tr><td>

Create a dependency between tasks

</td><td>

Find the successor task in the relationship and double-click the value in the **Predecessor** column and enter a value that specifies the relationship. See [Predecessor dependencies in the planning console](r_ProjectTaskDependencyValues.md) for examples.Alternatively, you can create a relationship between two tasks by connecting the ends of the corresponding task bars in the timeline view.

</td></tr><tr><td>

Select a baseline

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select a baseline from the baselines list.

</td></tr><tr><td>

Create a baseline

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Create new baseline**. See [Create baseline of a project](../task/t_CreateAProjectBaseline.md) for more information.

</td></tr><tr><td>

Compare schedule baselines

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select a schedule baseline from the baselines list. Select the show or hide columns in gantt icon \(![show or hide columns in gantt icon.](../../project-workspace/image/gear_icon.png)\), and then select the following columns to compare schedule baselines:-   Baseline start date
-   Baseline end date
-   Baseline variance

</td></tr><tr><td>

Display the critical path

</td><td>

Select the critical path icon \(![Critical path icon](../image/critical_path_icon.png)\). For more information on the critical path, see [Gantt chart](../concept/c_GanttChart.md).

</td></tr><tr><td>

Show date change

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select the **Show Date Change** switch. When this option is enabled, the start and end dates of the task are displayed when you drag the task bar.![Start and end dates on the task bar.](../image/date_change.png "Start date and end dates on task bar")

</td></tr><tr><td>

Show duration change

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select the **Show Duration Change** switch. When this option is enabled, the duration of the task is displayed when you drag either end of the task bar.![Duration on the task bar.](../image/duration_change.png "Task duration")

</td></tr><tr><td>

Show weekends on the calendar

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select the **Show Weekends** switch. The weekends appear as light-blue vertical bars in the Gantt chart.![Light-blue colored vertical bar indicates a Weekend on the task bar.](../image/weekend_gantt_chart.png "Weekend on task bar")

</td></tr><tr><td>

Zoom the calendar in or out

</td><td>

On the top of the calendar, select one of the time periods, such as the month or day. Then select a **Zoom Level** from the calendar.![Calendar zoom options.](../../test-management2/images/zoom_level.png "Calendar zoom")

When the zoom level in calendar is selected as **Auto Fit**, the Gantt view fits in one page to display the entire timeline for the project in one go without using the scrollbar.

</td></tr><tr><td>

Open the tutorial

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Walkthrough**.

</td></tr><tr><td>

Open list of keyboard shortcuts

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Keyboard Shortcuts**.

</td></tr></tbody>
</table><table id="table_u3d_msy_fdc"><thead><tr><th>

Task

</th><th>

How to perform the task

</th></tr></thead><tbody><tr><td>

Open the project workbench

</td><td>

Select the **Planning Console** selection arrow on the banner and select **Project Workbench**. For more information, see [Using Project workbench - Legacy](../concept/c_ProjectWorkbench.md).

</td></tr><tr><td>

Open live feed

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Show live feed**.

</td></tr><tr><td>

Export project data in MPP, CSV, or XML format

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Export Planning Console**. For more information, see [Export project data](../task/t_ExportAProjectWithTheProjectForm.md).

</td></tr><tr><td>

Print the gantt timeline

</td><td>

Select the more options icon \(![More options icon.](../../planning-and-policy/image/gannt_chart_icon.png)\), and then select **Print**.**Note:**

-   Printing on a smaller paper size might result in the gantt chart image being cut off. You may either zoom out using the gantt chart calendar, or increase paper size to print the gantt timeline for projects and tasks.
-   If the colored bars in gantt chart area are not visible in Print preview, then select the option for background graphics in the Print dialog.

</td></tr></tbody>
</table>**Related topics**  


[Using Planning console - Legacy](../concept/c_TheProjectPlanningConsole.md)

