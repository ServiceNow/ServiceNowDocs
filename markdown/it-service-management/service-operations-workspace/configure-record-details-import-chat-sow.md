---
title: Configure the task record information in the MS Teams Import tab
description: Customize the task record fields displayed when you view or import a Microsoft Teams chat conversation.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the task record information in the MS Teams Import tab

Customize the task record fields displayed when you view or import a Microsoft Teams chat conversation.

## Before you begin

Role required: admin

## About this task

When you view or import a Microsoft Teams chat conversation for a task record, the record details are displayed in the **Details** section of the **MS Teams Import** tab. These details are configured in the **Script** field of an implementation corresponding to the task record in the sn\_tcm\_collab\_hook.MSTeamsTaskInfoCardHandler extension point.

For information about collaborating on a task record using Microsoft Teams chat, see [Collaborate on a task record using Microsoft Teams in Service Operations Workspace](start-msteams-chat-sow.md).

![MS Teams Import tab.](../image/ms-teams-chat-page.png "MS Teams Import tab")

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  From the Extension Points list, select **sn\_tcm\_collab\_hook.MSTeamsTaskInfoCardHandler**.

3.  From the Implementations related list, select an implementation associated with the task record and modify the **Script** field.

4.  Edit the **Script** field.

5.  Click **Update**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

