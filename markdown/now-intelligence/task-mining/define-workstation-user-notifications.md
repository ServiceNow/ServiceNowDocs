---
title: Customize Task Mining notifications for workstation users
description: Use Task Mining notifications to notify workstation users that their work is being monitored, request consent, and inform them if they have any actions to take.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Customize Task Mining notifications for workstation users

Use Task Mining notifications to notify workstation users that their work is being monitored, request consent, and inform them if they have any actions to take.

## Before you begin

Set the application scope to Task Mining core using the application picker.

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

**Note:** You can't add new notification configuration records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Configuration icon ![](../image/task-mining-configuration-icon.png).

3.  Under **Configuration**, select **Notifications**.

4.  Select the notification configuration record that you want to modify.

    The available records are:

    -   **Consent text**

        Determines the text displayed to users when assigned to a project.

    -   **Private Startup Text**

        Determines the text displayed to users when switching to private mode.

        **Note:** If you leave the private startup text empty, workstation users can't use private timeout.

    -   **Private Timeout Text**

        Determines the text that is displayed to users before the private mode timeout.

        **Note:** If you leave the private timeout text empty, workstation users can't extend their private timeout.

5.  Modify the **Value** field.

    If the **Value** field is empty, the notification will not appear on workstations.

6.  Select **Save**.


