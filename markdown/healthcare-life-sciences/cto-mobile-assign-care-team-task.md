---
title: Assign a care team task in Care Team Mobile
description: Assign an unassigned care team task to an assignment group and a member of that group in one step, directly from your mobile device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/cto-mobile-assign-care-team-task.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Manage care team cases and tasks using Care Team Mobile, Care Team Mobile, Healthcare Operations, Healthcare and Life Sciences]
---

# Assign a care team task in Care Team Mobile

Assign an unassigned care team task to an assignment group and a member of that group in one step, directly from your mobile device.

## Before you begin

Role required: sn\_hco.care\_team\_member

## About this task

The **Assignment** action is available only on care team tasks that don't have an assignee. After a task is assigned, use [Edit a care team task in Care Team Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/cto-mobile-edit-care-team-task.md) to change the assignment.

## Procedure

1.  In Care Team Mobile, navigate to **Track requests** &gt; **Care team**.

2.  Select the care team case that contains the task.

3.  Select the **Tasks** tab, and then select the care team task.

    The task details open, including its assignment, description, priority, location, time window, SLA, and related work order and case details.

4.  Select **Assignment**.

5.  In the **Assignment group** field, confirm or select the group that should own the task.

    The field is filled in with the task's current assignment group, if it has one.

6.  In the **Assigned to** field, select an active member of the assignment group.

    **Note:** The list shows all users, not only members of the selected group. If you select someone who isn't an active member of the group, the assignment is rejected when you submit it.

7.  Select **Assign task**.


## Result

The task's assignment group and assignee are saved, and the **Assignment** action no longer appears on the task. The task's state is set to **Assigned**.

