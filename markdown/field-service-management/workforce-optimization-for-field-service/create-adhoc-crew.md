---
title: Create ad hoc task-specific crews
description: Create an ad hoc task-specific crew for a task if existing crews are not available to work on the task or the task requires specific skills.
locale: en-US
release: yokohama
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Field Service Crew Operations, Setting up your workforce, Configuring Field Service Management, Field Service Management]
---

# Create ad hoc task-specific crews

Create an ad hoc task-specific crew for a task if existing crews are not available to work on the task or the task requires specific skills.

## Before you begin

Role required: wm\_manager

## About this task

The Create Crew option is available in the work order task form if the following conditions are met:

-   Task is in the Pending Dispatch state.
-   Dispatch Group is selected.
-   The **Needs Crew** option is active.
-   The task is scheduled for the present date or future dates.

**Note:** You can create only one crew for a work order task. If you try creating another crew for a task, the system redirects you to the existing crew.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Manager** &gt; **&gt; Work Order Tasks.**.

2.  Open a work order task that is in the **Pending Dispatch** state.

3.  Click **Create Crew**.

4.  On the form, fill the fields.

5.  <table id="table_ixf_t5q_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the crew. This field is auto-populated based on the work order task for which the crew is created. For example, WOT9001007 Crew.

</td></tr><tr><td>

Description

</td><td>

Description of the crew. This field is auto-populated with a default text message, for example, Crew to work on WOT9001007.

</td></tr><tr><td>

Leader

</td><td>

Name of the crew leader.

</td></tr><tr><td>

Size

</td><td>

Total number of agents, including the leader, in the crew.

</td></tr><tr><td>

Schedule

</td><td>

Working hours of the crew.

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

Option to indicate whether the crew is available for selection when assigning a work order task to the crew.

</td></tr></tbody>
</table>6.  Click **Submit**.


## Result

An ad hoc task-specific crew is created along with the related list records, such as Details, Groups, Skills, and Task Assignees.

