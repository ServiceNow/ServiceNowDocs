---
title: Modify the Task Mining data retention period
description: Modify the default retention configuration rules to delete data automatically.
locale: en-US
release: zurich
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Modify the Task Mining data retention period

Modify the default retention configuration rules to delete data automatically.

## Before you begin

Set the application scope to Task Mining core using the application picker.

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

**Note:** You can't add new data retention configuration records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Configuration icon ![](../image/task-mining-configuration-icon.png).

3.  Under **Configuration**, select **Retention**.

4.  Select the retention record that you want to edit.

    Task Mining does daily checks for potential deletions.

    The available records are:

    -   **User data retention period**

        User data is the workstation data transferred to Task Mining. The retention period for user data is based on the start date and time value of the record. The default value is 30 days. Only records not associated with any project are deleted.

    -   **Project retention period**

        The project retention period is based on when a project status is set to Closed. Only projects closed for the retention period are deleted. The default retention period is 10 days.

    -   **DataMart retention period**

        A datamart is the mined data with categorization rules applied. The retention period is based on the last opened date for each project. Only data associated with projects that aren't interacted with are deleted. The default retention period is 10 days.

5.  In the **Value** field enter the number of days for the retention period.

6.  Select **Save**.


