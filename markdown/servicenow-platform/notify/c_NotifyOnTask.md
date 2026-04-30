---
title: Using Notify with tasks
description: Notify allows you to initiate conference calls and send SMS alerts from task records.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Using Notify with tasks

Notify allows you to initiate conference calls and send SMS alerts from task records.

This functionality is available for all tables that extend the Task table, such as incident, problem, or change request. All calls and messages made from tasks are initiated using a single Notify phone number \(E.164 or short code\). You can configure which phone number is used by setting the property **glide.notify.task.phone\_number**.

-   **[Start a conference call from a task](../task/t_StartAConferenceCallFromATask.md)**  
Use Notify to start conference calls from a task record.
-   **[Manage conference calls on task](../task/manage-conf-call.md)**  
Add and manage multiple participants on the conference including self-joining in to the conference call and end the conference call when the discussion is over.
-   **[Send an SMS alert from a task](../task/t_SendAnSMSFromATask.md)**  
Use Notify to send information related to a call through SMS alerts from a task record.

**Parent Topic:**[Using Notify](using-notify.md)

