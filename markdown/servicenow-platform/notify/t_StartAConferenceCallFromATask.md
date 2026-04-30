---
title: Start a conference call from a task
description: Use Notify to start conference calls from a task record.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Notify with tasks, Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Start a conference call from a task

Use Notify to start conference calls from a task record.

## Before you begin

Role required: notify\_view, or itil

Notify must be set up before you can use Notify on task. Ensure there are Notify phone numbers \(E.164 or short code\) in number groups with phone call workflow.

Use **glide.enable.notify\_on\_task** property to enable Notify integration for Task table and its extensions. Entering phone number in **glide.notify.task.phone\_number** property is equivalent to setting **glide.enable.notify\_on\_task** to true.

## Procedure

1.  Navigate to any task record, such as an incident or change request.

2.  Click the **Start conference call** related link.

3.  Select one or more **Recipients** to participate in the conference call.

4.  Click **Start**.

    Any conference call records created from a task are associated with that task. You can view associated conference calls from the task record in the **Conference calls** related list. You may need to configure the form to add the related list.


**Parent Topic:**[Using Notify with tasks](../concept/c_NotifyOnTask.md)

**Related topics**  


[Manage conference calls on task](manage-conf-call.md)

[Send an SMS alert from a task](t_SendAnSMSFromATask.md)

