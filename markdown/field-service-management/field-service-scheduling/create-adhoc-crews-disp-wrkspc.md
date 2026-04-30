---
title: Create ad hoc crews in Dispatcher Workspace
description: Create ad hoc crews for a task if no existing crews are available to work on the task or the task requires specific skills to complete the job.
locale: en-US
release: yokohama
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Dispatcher Workspace for crew operations, Using Dispatcher Workspace, Assigning work order tasks to agents from Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Create ad hoc crews in Dispatcher Workspace

Create ad hoc crews for a task if no existing crews are available to work on the task or the task requires specific skills to complete the job.

## Before you begin

Role required: wm\_dispatcher

## About this task

The Create Crew option is available in the work order task form if the following conditions are met:

-   The task is in the Pending Dispatch state.
-   **Dispatch Group** is selected.
-   The **Needs Crew** option is active.
-   Task is scheduled for the present date or future dates.

**Note:** You can create only one crew for a work order task. If you try creating another crew for a task, the system redirects you to the existing crew.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click **Dispatcher Workspace**.

3.  Search for and open a work order task for which you want to create a crew.

    For more information, see [Search for tasks that need a crew on Dispatcher Workspace](search-crew-task.md).

4.  Click **Create Crew**.

5.  On the form, fill the fields.

<table id="table_xs1_fj4_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the crew. This field is auto-populated based on the work order task for which an ad hoc crew is created. For example, WOT9001007 Crew.

</td></tr><tr><td>

Description

</td><td>

Description for the crew. This field is auto-populated with a default text message, for example, "Crew to work on WOT9001007."

</td></tr><tr><td>

Leader

</td><td>

Name of the crew leader.

</td></tr><tr><td>

Size

</td><td>

Read-only field. The value of this field is reference from the crew membership table.

</td></tr><tr><td>

Initiated From

</td><td>

The work order task number for which you are creating a crew. This field is auto-populated with the work order task number for which an ad hoc crew is created. For example, WOT9001007.

</td></tr><tr><td>

Schedule

</td><td>

Read-only field. Working hours of the crew. The value of this field is reference from the Schedule travel start and Estimated end fields in the work order task.

</td></tr><tr><td>

Location

</td><td>

Location of the crew.

</td></tr><tr><td>

Maximum Travel Radius

</td><td>

Radius in selected distance unit \(miles or kilometers\).

</td></tr><tr><td>

Distance Unit

</td><td>

Unit of distance covered in miles or kilometers.

</td></tr><tr><td>

Active

</td><td>

Option to indicate whether the crew is available for selection when assigning a work order task.

</td></tr></tbody>
</table>6.  Click **Save**.


## Result

An ad hoc task-specific crew is created along with the related list records, such as Details, Groups, Skills, and Task Assignees.

**Parent Topic:**[Using Dispatcher Workspace for crew operations](../concept/using-disp-wrkspc-crew-operations.md)

