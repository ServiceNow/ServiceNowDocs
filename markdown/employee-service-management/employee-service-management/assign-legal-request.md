---
title: Assign a legal request
description: Assign a legal request to yourself or to someone in your assignment group.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Assign a legal request

Assign a legal request to yourself or to someone in your assignment group.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

When an employee submits a legal request, it is automatically assigned to a group or user in the legal department. The assignment is done based on the [assignment rules](create-assignment-rules-intake-form.md) configured for the intake form of the associated practice area. If the request is assigned to a legal group, any member from the group can triage the request themselves or assign it to another member of the group.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Legal Requests**, click **Unassigned**.

4.  In the list of unassigned requests, open a request by clicking the request number.

5.  Update the **Assignment group permission** to change the permission level of the legal request for the users.

    -   **No Access**: Only the practice area lead, group manager, and user in the **Assigned to** field can access the legal request and assign it to one of the members in the assignment group. The assigned user can then work on the legal request.
    -   **Read**: All members from the assignment group can only view the legal request. This option is the default permission level.
    -   **Edit**: All members from the assignment group can view and work on the legal request. The Assigned To field becomes optional if this option is set.
    Assignment Group Permission field of a active Legal Request Record can be edited by:

    -   Practice area lead, Assignment group manager, Assigned to, and delegated users.
    -   Any Assignment group member, if the record is in New state or Assignment group permission is edit or Configured options have assigned\_to\_field\_not\_mandatory in it.
6.  Based on the permission option, assign the request to yourself or to another member from the assigned group.

    -   To assign the request to yourself, click **Assign to me**.
    -   To assign the request to another member, on the **Details** tab, select a user in the **Assigned to** field and click **Save**.

## Result

The state of the request updates to Assigned.

## What to do next

The assigned user can start [working on the legal request](work-on-legal-request.md).

