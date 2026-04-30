---
title: Manage conference calls on task
description: Add and manage multiple participants on the conference including self-joining in to the conference call and end the conference call when the discussion is over.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Notify with tasks, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Manage conference calls on task

Add and manage multiple participants on the conference including self-joining in to the conference call and end the conference call when the discussion is over.

## Before you begin

-   Role required: notify\_view, itil, itil\_admin, or notify\_setup\_admin
-   A conference call is already initiated.

## About this task

The **Manage Conference Calls** UI action is available for any table that extends the Task \[task\] table. If at least one conference call is active on a task record, the link appears on the related links section of the form. Out of the tables that extend the task table, the **Manage Conference Calls** UI action is intentionally hidden for Incident Communication Plan \[incident\_alert\] table and Communication Task \[comm\_task\] table. For these two tables, the functionality is already available as **Join conference call** and **End conference call** UI actions.

## Procedure

1.  Navigate to any task record such as Incident, Problem, or Change Request.

2.  Open the record on which the conference all is active.

3.  In the related links, click **Manage Conference Calls**.

4.  In the Manage Conferences window, you can perform the following activities:

    |Options|Description|
    |-------|-----------|
    |Join Conference Call|If the logged in user is not already a part of the conference call, the user can join the conference.|
    |Add Participants|Add participants to the conference who can contribute to the discussion.|
    |End Conference Call|End the conference when the discussion is over.|

5.  In the Manage Conferences window, click the conference call number to know the details of the conference.


**Parent Topic:**[Using Notify with tasks](../concept/c_NotifyOnTask.md)

**Related topics**  


[Start a conference call from a task](t_StartAConferenceCallFromATask.md)

[Send an SMS alert from a task](t_SendAnSMSFromATask.md)

