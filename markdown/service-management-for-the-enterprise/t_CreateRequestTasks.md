---
title: Create request tasks
description: Tasks are created in support of requests.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Request task management, Request Management in a Service Management application, Service Management]
---

# Create request tasks

Tasks are created in support of requests.

## Before you begin

Role required: \[SM application\]\_admin or \[SM application\]\_qualifier

## Procedure

1.  Navigate to **All** &gt; **\[SM Application\]** &gt; **Requests** &gt; **All \[SM Application\] Requests**.

2.  Open the request for which you want to create tasks.

3.  Click the **Add Task** related link.

    The Task screen for the SM application opens.

4.  Fill in the fields on the form.

    **Note:** Not all fields display for all SM applications.

<table id="table_ptc_455_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the task.

</td></tr><tr><td>

Parent

</td><td>

Request that this task is associated with.

</td></tr><tr><td>

Cloned from

</td><td>

Record number of the task this task was cloned from, if any.

</td></tr><tr><td>

Location

</td><td>

Geographical area where the work must be done. The location is critical for determining the staff member who is assigned to the task.

</td></tr><tr><td>

Template

</td><td>

Template for creating this request \(optional\). Click the lookup icon and select a template. The description of the selected template populates the **Description** field.

</td></tr><tr><td>

Skills

</td><td>

Abilities necessary to execute the task. This field is automatically completed based on the selection in the **Affected CI** field on the associated request. If you change the affected CI on the request, the system adds any skills required by the new CI to the skills already listed here.

</td></tr><tr><td>

State

</td><td>

Current state of the task, such as **Accepted** or **Closed Complete**. ServiceNow advances the state automatically as users complete the work for each successive state.

</td></tr><tr><td>

Assignment group

</td><td>

Group from which an individual legal staff member is selected to complete the task. The lookup list shows only the assignment groups associated with the selected **Location**. If the **Assignment Group** field is empty, the system searches for a group covering the territory that includes the location of the task.

</td></tr><tr><td>

Assigned to

</td><td>

Individual staff members who should complete the task, selected from the **Assignment group**. If you defined skills and assigned them to staff members, the **Assigned to** field lookup list shows only those staff members in the assignment group who have all the **Skills** required. If no exact match of skills is found, the lookup list shows all assignment group members. **Note:** If state flows are disabled, this field is not mandatory.

</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the task.

</td></tr><tr><td>

Description

</td><td>

Exact technical description of the unit of work to be performed. Qualifiers should provide as much detail about the problem as possible to avoid extra communication with the caller in later stages of the request.

</td></tr><tr><td>

Work notes

</td><td>

Information about the task as it progresses through each state. Work notes are not visible to customers.

</td></tr></tbody>
</table>    **Note:** The workflow appears at the top of the form, with the completed states shown in green.


**Parent Topic:**[Request task management](../concept/c_RequestTasksMgmt.md)

