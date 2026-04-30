---
title: Create a facilities request task
description: Facilities request tasks are created from facilities requests.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Facilities request tasks, Facilities service management process, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Create a facilities request task

Facilities request tasks are created from facilities requests.

## Before you begin

Role required: facilities\_admin or facilities\_qualifier

## Procedure

1.  Navigate to **All** &gt; **Facilities** &gt; **Requests** &gt; **All Facility Requests**.

2.  Open the desired request.

3.  Click the **Add Task** related link.

4.  Fill in the fields on the form.

<table id="table_ptc_455_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the task.

</td></tr><tr><td>

State

</td><td>

Current state of the task, such as **Accepted** or **Closed Complete**. States progress automatically as users complete the work for each successive state and appears on the subway map at the top of the form.

</td></tr><tr><td>

Parent

</td><td>

Facilities request that this task is associated with.

</td></tr><tr><td>

Assignment group

</td><td>

Group from which an individual facilities staff member is selected to complete the task. The lookup list shows only the assignment groups associated with the selected **Location**. If the **Assignment Group** field is empty, the system searches for the group covering the territory that includes the location of the task.

</td></tr><tr><td>

Cloned from

</td><td>

Record number of the task this task was cloned from, if any.

</td></tr><tr><td>

Assigned to

</td><td>

The individual staff member to complete the task, selected from the **Assignment group**. The **Assigned to** field lookup list shows only those staff members in the assignment group who have all the **Skills** required. If no exact match of skills is found, the lookup list shows all assignment group members.

</td></tr><tr><td>

Override schedule conflict

</td><td>

 

</td></tr><tr><td>

Location

</td><td>

The geographical area of the request. The location is critical for determining which staff member is assigned to the task.

</td></tr><tr><td>

Template

</td><td>

 

</td></tr><tr><td>

Skills

</td><td>

Abilities necessary to execute the task. The system automatically completes the **Skills** field based on the selection in the **Affected CI** field on the associated request. If you change the affected CI on the request, the system adds any skills required by the new CI to the skills already listed here.

</td></tr><tr><td>

Short description

</td><td>

Brief explanation of the task.

</td></tr><tr><td>

Description

</td><td>

Exact technical description of the unit of work to be performed. Provide as much detail about the problem as possible to avoid extra communication with the caller in later stages of the request.

</td></tr><tr><td>

Work notes

</td><td>

Information about the task as it progresses through each state. Work notes are not visible to customers.

</td></tr><tr><td colspan="2">

**Schedule**

</td></tr><tr><td>

Scheduled start

</td><td>

Date and time that work on the task is expected to begin. The scheduled start time is set automatically to one hour after the scheduled travel start time. For example, if **Scheduled travel start** is 10:00 AM, the **Scheduled start** time is set to 11:00 AM. When the task reaches the **Pending Dispatch** stage, the default value can be edited. A staff member cannot be scheduled for two tasks at the same time. If a specified time is already allocated to another task, an error message is displayed. This field is required when the task is assigned or when the state is **Assigned**, **Accepted**, **Pending Dispatch**, or **Work In Progress**.

</td></tr><tr><td>

Estimated end

</td><td>

\[Read-only\] Date on which work on the task ends. The date is automatically calculated based on the **Scheduled start** and **Estimated work duration**.

</td></tr><tr><td>

Estimated work duration

</td><td>

Estimated amount of work time. One hour is set by default. The default value can be edited during the **Draft** or **Pending Dispatch** stage. When defining the estimated work duration, it cannot exceed the total time of the window.

</td></tr><tr><td>

Actual work start

</td><td>

Time when work began. This field is not available until **Actual travel start** time is added manually or the **Start Travel** button is clicked.

</td></tr><tr><td>

Actual work end

</td><td>

Time when work on the task was completed.

</td></tr><tr><td>

Actual duration

</td><td>

\[Read-only\] Total amount of time spent traveling to the site and completing the task. This value is automatically calculated based on the **Actual travel start** and **Actual work end** times.

</td></tr></tbody>
</table>5.  Click **Submit**.


-   **[Task windows](../reference/r_TaskWindows.md)**  
A task window is the time period, bordered by start and end times, in which a task is performed.

**Parent Topic:**[Facilities request tasks](../concept/c_FacRequestTasks.md)

