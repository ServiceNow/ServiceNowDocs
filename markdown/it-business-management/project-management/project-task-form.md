---
title: Project task form
description: Learn about the fields of project task form. The fields appear when the Project Portfolio Management is active and the Project form is in the Basic view. Configure the form to display the fields.
locale: en-US
release: yokohama
product: Project Management
classification: project-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Form field information for Project Management, Reference, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Project task form

Learn about the fields of project task form. The fields appear when the Project Portfolio Management is active and the Project form is in the **Basic** view. Configure the form to display the fields.

<table id="table_ibj_35d_br"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Brief description of the project task.

</td></tr><tr><td>

Number

</td><td>

System-generated number with a configurable prefix.

</td></tr><tr><td>

Status

</td><td>

Status of the project task.

 The status updates automatically based on the difference of the planned end date of the task from the current date. The color of the status changes as the planned end date approaches:

-   **Green**: The planned end date for the project task is more than the offset working days that you defined.
-   **Yellow**: The planned end date for the project task is less than the offset working days that you defined.
-   **Red**: The planned end date for the project task is past the offset working days that you defined.

 The default offset for status calculation is 3 working days. You can update the **com.snc.ppm.yellow\_status\_duration** property to change the offset duration. Your project schedule determines the working days.

**Important:** The status of the project task does not affect the overall status of the project, meaning the project task status does not roll up to the project. Also, the status of the child tasks does not affect the status of the parent task.

 Execute the **Update Active Project Task Status** scheduled job to update the status of your existing tasks. This scheduled job runs daily by default, however you can execute this job on demand also.

 If you do not want the status of a task to update automatically, you can change the status of the task manually. Changing the status manually, overrides the automatic update and the execution of the scheduled job does not change the status of the project task.

 **Note:** Configure the property **com.snc.status\_process\_planned\_task\_entities** to include or exclude task types for automatic status updates.

</td></tr><tr><td>

Override status

</td><td>

Indicates if the project task status is updated manually. By default, this check box is deselected. When you change the **Status** field manually, this check box becomes selected.

</td></tr><tr><td>

State

</td><td>

Current state of the project. The states include: Pending, Open, Work in Progress, Closed Complete, Closed Incomplete, Closed Skipped.The state is automatically rolled up from the project tasks. For more information, see [Project calculation](../concept/c_ProjectWorkbenchProjectCalc.md) and [Parent-child rollup task calculations](../concept/c_ParentChildRollupTaskCalcs.md).

</td></tr><tr><td>

Description

</td><td>

Detailed description of the project task.

</td></tr><tr><td>

Assigned to

</td><td>

User assigned to the project task. The following conditions apply:-   If an assignment group is defined, only users in the assignment group appear in the lookup list.
-   If skills are defined, only users with those skills appear in the lookup list.
-   If no assignment groups or skills are defined, only users with one of the Project Management application user roles appear in the lookup list.
-   Users with `timecard_user` role also appear in the lookup list.

</td></tr><tr><td>

Assignment group

</td><td>

User group assigned to the project task.

</td></tr><tr><td>

Additional assignee list

</td><td>

Additional users assigned to the project task.

</td></tr><tr><td>

Percent complete

</td><td>

Percentage of the work that has been completed for the project task.

</td></tr></tbody>
</table><table id="table_s3b_p2g_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Milestone

</td><td>

Option for converting the task to a milestone.

</td></tr><tr><td>

Key milestone

</td><td>

Option for converting the task to a key milestone.

</td></tr><tr><td>

Allow dates outside schedule

</td><td>

Indicates whether the project task is set to start and end on a non-schedule day \(outside regular project schedule\) such as on a weekend. An off-schedule task can start any time during the day and on any day of the week.For example, if you use the project schedule Monday to Friday, 8:00 to 17:00 and a project task of duration 2 days should start on Saturday, then an off-schedule task is allowed to be scheduled on Saturday and end on Sunday. Similarly, if a task of duration 3 days starts on Friday, then an off-schedule will end on Sunday instead of ending on Tuesday.

 The option is not enabled for a parent task. The value of this field on the parent task is derived from the child tasks.

 **Note:**

-   There is no difference between an off-schedule and an on-schedule task if there is no schedule defined at the project.
-   1 day is 8 hours for a task in regular schedule and 24 hours for a task outside schedule.

</td></tr></tbody>
</table><table id="table_kls_t2g_mcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Planned start date

</td><td>

Estimated date and time for the project task to start. You can edit this date when the **Time constraint** is **Start on Specific Date**, **Start no earlier than**, or **Start no later than**.If the constraint type is **Start ASAP** or **Start no later than**, changing the planned start date for a task changes the constraint type to **Start no earlier than**.

</td></tr><tr><td>

Planned end date

</td><td>

Estimated date and time for the project task to end.For a manual project, any update to the actual start date does not update the planned end date of the project task. Enable the project property **Enable alter of planned date with Actual for Manual Project** to update planned end date from the actual start date and planned duration.

</td></tr><tr><td>

Planned duration

</td><td>

Estimated length of time \(from start time to end time\) of the project task.

</td></tr><tr><td>

Planned effort

</td><td>

Estimate of how much time it will take to complete this task. After you add child tasks, this field becomes read-only, rolls-up calculation and overwrites any earlier entry that you made.

</td></tr><tr><td>

Constraint date

</td><td>

A read-only field that determines the start date for tasks with **Start no earlier than**, **Start no later than**, and **Start on specific date** constraints. Use the **Move project** related link to change this date. For more information, see [Change the planned start date of a project](../task/change-planned-start-date-of-project.md).

</td></tr><tr><td>

Original start date

</td><td>

Original planned date and time for the task to start.

</td></tr><tr><td>

Actual start date

</td><td>

Date on which the project task started. The task is set to **Work in Progress** when the actual start date is populated.When you change the **State** or **Percent complete** of the task, the actual dates are auto-populated with the date component copied from the planned dates.

 When you populate the actual start and end dates, the time component in actual dates is defaulted to the date component in planned dates when the derive time component from planned dates field on Project form is set to True.

</td></tr><tr><td>

Actual end date

</td><td>

Date on which the project task ended. The task is set to **Closed Complete** when the actual end date is populated.

</td></tr><tr><td>

Actual duration

</td><td>

Duration of the task from task start to task closure. As with planned duration, the actual duration shows total task time.

</td></tr><tr><td>

Actual effort

</td><td>

Actual number of hours charged from the resources on this project task. If you are using the Time Card Management application, the value for the field comes from the application automatically. The application calculates the actual effort on the task by taking the total time worked from all approved time cards of all resources who worked on the task.

</td></tr><tr><td>

Time constraint

</td><td>

When the project task begins:-   **Start ASAP**: The task starts as soon as possible as determined by the relationships and dependencies. The dates for these tasks are derived from the constraint date of the project.
-   **Start on specific date**: The task starts on a date that you specify. The task dependencies are not considered for date calculation.
-   **Start no earlier than**: The task starts on or after the constraint date.
-   **Start no later than**: The task starts on or before the constraint date. The start date is determined by the relationships and dependencies.

 **Note:** If the **Calculation** field on the Project form is set to Manual, you cannot change the constraint type for such projects. To change the constraint type, change the project to Automatic.

</td></tr><tr><td>

Original end date

</td><td>

Original planned date and time for the task to end.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Activity / Work notes / Additional comments|Information about the milestones, impediments, or changes as the project progresses. Enter notes or comments in the **Activity** field and click **Additional comments** or **Work notes**. The text appears in the feed.|

|Field|Description|
|-----|-----------|
|Checklist|[Checklist](../task/t_CreateAProjectTaskChecklist.md) to track items that must be completed for the task.|

**Related topics**  


[Create a project task from a project](../task/t_CreateATaskFromAProject.md)

