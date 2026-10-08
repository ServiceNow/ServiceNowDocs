---
title: Assign a care team case in Care Team Mobile
description: Assign an unassigned care team case to an assignment group and a member of that group so that the right person picks up the work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/cto-mobile-assign-care-team-case.html
release: brazil
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Manage care team cases and tasks using Care Team Mobile, Care Team Mobile, Healthcare Operations, Healthcare and Life Sciences]
---

# Assign a care team case in Care Team Mobile

Assign an unassigned care team case to an assignment group and a member of that group so that the right person picks up the work.

## Before you begin

Role required: sn\_hco.care\_team\_member

## About this task

The **Assignment** action is available only on care team cases that don't have an assignee. After a case is assigned, use [Edit a care team case in Care Team Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/healthcare-life-sciences/cto-mobile-edit-care-team-case.md) to change the assignment.

## Procedure

1.  In Care Team Mobile, navigate to **Track requests** &gt; **Care team**.

2.  Select the unassigned care team case that you want to assign.

    Unassigned cases appear in the **All Active** tab.

3.  Select **Assignment**.

4.  In the **Assignment group** field, confirm or select the group that should own the case.

    The field is filled in with the case's current assignment group, if it has one.

5.  In the **Assigned to** field, select an active member of the assignment group.

    **Note:** The list shows all users, not only members of the selected group. If you select someone who isn't an active member of the group, the assignment is rejected when you submit it.

6.  Select **Assign case**.


## Result

The case's assignment group and assignee are saved, and the **Assignment** action no longer appears on the case.

