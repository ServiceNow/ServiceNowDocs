---
title: Catalog Task workflow activity
description: The Catalog Task activity creates a service catalog task record.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Task workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Catalog Task workflow activity

The **Catalog Task** activity creates a service catalog task record.

**Note:** This activity is only available when the workflow runs on a table that extends Task.

A user must complete the catalog task. This activity is available only for workflows running on the Catalog Request Item \[sc\_req\_item\] table.

**Note:** Task activities run as the user whose actions complete the task the workflow was waiting for and advances the workflow.

## Results

You can assign a result value using `activity.result` from within a script field of the activity. The final **State** value of the catalog task record determines the result value for the **Create Task** activity. Possible result values are:

-   Closed complete
-   Closed incomplete
-   Closed skipped
-   Deleted
-   Cancelled

## Input fields

The values you enter in the following fields determine the behavior of the activity.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="subhead" colspan="2">

Catalog Task Activity SettingsThe following fields specify the behavior of the Catalog Task Activity.

</td></tr><tr><td>

Task Table

</td><td>

The table on which this activity runs. In most cases, leave set to the default value: \[sc\_req\_item\].

</td></tr><tr><td>

Priority

</td><td>

The value you want assigned to the **Priority** field for the new task.

</td></tr><tr><td>

Wait for completion

</td><td>

If selected, the workflow activity waits for the task to complete before continuing. If cleared, the task is created but the workflow proceeds.

</td></tr><tr><td class="subhead" colspan="2">

Catalog Task Record Settings The following fields specify the field values that this activity sets for the catalog task it creates.

</td></tr><tr><td>

Task value from

</td><td>

Specify how you want to populate fields on the new task. -   **Fields:** a predefined set of fields including **Fulfillment group**, **Assigned to**, **Short description** and **Instructions**.
-   **Template:** an existing template for the selected task table.
-   **Values:** values that you specify using a Set Values widget.

 After you select a value for **Task value from**, additional fields specific to that value appear on the form.

</td></tr><tr id="row_FulfillmentGroup"><td>

Fulfillment groupOnly appears when **Task value from** is set to `Fields`

</td><td>

The group that is responsible for completing the task. Populates the **Assignment group** field on the new task.

</td></tr><tr id="row_AssignedTo"><td>

Assigned toOnly appears when **Task value from** is set to `Fields`

</td><td>

The user who is responsible for completing the task. Populates the **Assignment to** field on the new task.

</td></tr><tr id="row_ShortDescription"><td>

Short descriptionOnly appears when **Task value from** is set to `Fields`

</td><td>

A short description for the task. Populates the **Short description** field on the new task.

</td></tr><tr id="row_Instructions"><td>

InstructionsOnly appears when **Task value from** is set to `Fields`

</td><td>

The task instructions for the user to complete prior to closing the task. Populates the **Description** field on the new task.

</td></tr><tr><td>

Template Only appears when **Task value from** is set to `Template`.

</td><td>

The values in the task will be populated from the values in the template you select.

</td></tr><tr><td>

SetValues Only appears when **Task value from** is set to `Values`.

</td><td>

Select any field on the task record to a value you specify here.

</td></tr><tr id="row_Advanced"><td>

Advanced

</td><td>

Check **Advanced** if you want to use a script to assign values on the catalog task. When you check **Advanced,** a text box appears where you can enter your script.

</td></tr><tr id="row_AdvancedScript"><td>

Advanced Script Only appears when the **Advanced** field is checked.

</td><td>

Set additional values for the task in this script. This script is run after the task values are set using the **Fields**, **Template** or **Values** you have specified. Use the variable *task* when setting additional values, for example:

 `task.short_description = current.short_description;`

</td></tr><tr><td class="subhead" colspan="2">

Catalog Task Variables

</td></tr><tr><td>

Variables on Task Form

</td><td>

Specify optional catalog variables to include on the Catalog task form. The variables you select here will be displayed in a field called **Variable Editor**. If you select no variables here, the **Variable Editor** field in the Catalog Task form will not be visible.

</td></tr><tr><td class="subhead" colspan="2">

Catalog Task Schedule

</td></tr><tr id="row_DueDateBasedOn"><td>

Due date based on

</td><td>

Select how workflow determines the task's duration, due date, and schedule. -   **A user specified duration:** The duration is based on a user specified value.
-   **A relative duration:** The duration is calculated from a relative duration \(such as End of Next Business Day\).
-   **A date/time or duration field:** The duration is based on the value of a field on the current record.
-   **Script:** The duration is returned by a script.

</td></tr><tr id="row_Duration"><td>

Duration Only appears when **Due date based on** is set to `A user specified duration`

</td><td>

The specific number of days and hours.

</td></tr><tr id="row_RelativeDuration"><td>

Relative durationOnly appears when **Due date based on** is set to `A relative duration`

</td><td>

The general number and length of business days.

</td></tr><tr id="row_DueDateField"><td>

Due date fieldOnly appears when **Due date based on** is set to `A date/time or duration field`

</td><td>

The date/time or duration field.

</td></tr><tr id="row_DueDateScript"><td>

Due date scriptOnly appears when **Due date based on** is set to `Script`

</td><td>

The script that sets 'answer' to the number of seconds for the duration.

</td></tr><tr id="row_ScheduleBasedOn"><td>

Schedule based on

</td><td>

The basic schedule the timer uses to count working hours. If a schedule is specified, the duration will only be considered for times that are specified on the schedule. For example, if the duration is 2 hours and the workflow begins at 4:00pm on a schedule that is 8am - 5pm, then it ends at 9:00am the next day. The options are: -   **This workflow's schedule:** The schedule uses workflow context date, time, and an optional **Time zone based on** value.
-   **A specific schedule:** The schedule uses a pre-defined **Schedule** and an optional **Time zone based on** value.
-   **A schedule field:** The schedule uses a value from a table and an optional **Time zone based on** value.

</td></tr><tr id="row_Schedule"><td>

ScheduleOnly appears when **Schedule based on** is set to `A specific schedule`

</td><td>

The predefined **Schedule** from a list.

</td></tr><tr id="row_ScheduleField"><td>

Schedule fieldOnly appears when **Schedule based on** is set to `A schedule field`.

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr><tr id="row_TimeZoneBasedOn"><td>

Time zone based on

</td><td>

The time zone for calculating the duration. The time zone may be based on:-   **No time zone:** Default. Workflow uses the GMT time zone.
-   **A specific time zone:** A specific **Time zone** that you choose from a choice list.
-   **A time zone field:** A **Time zone field** to track time duration from a field on the form.

</td></tr><tr id="row_TimeZone"><td>

Time zoneOnly appears when **Time zone based on** is set to `A specific time zone`

.

</td><td>

Select the time zone you want from the choice list.

</td></tr><tr id="row_TimeZoneField"><td>

Time zone fieldOnly appears when **Time zone based on** is set to `A time zone field.`

</td><td>

A date and time or duration field for the schedule, that is associated with the table. Valid fields appear in blue on the Select the element from a tree dialog.

</td></tr></tbody>
</table>## States

The activity state tells the workflow engine what to do with the activity.

|State|Description|
|-----|-----------|
|Executing|The workflow engine knows to start the onExecute function of the activity.|
|Waiting|The workflow engine ignores the activity until a specific event to restart the activity is fired.|
|Finished|The activity finished running. See the result value for the outcome of the activity.|
|Cancelled|This activity, or the workflow that contains this activity, was canceled.|
|Error|A JavaScript error occurred. Review the logs for error details.|

**Parent Topic:**[Task workflow activities](r_TaskActivities.md)

