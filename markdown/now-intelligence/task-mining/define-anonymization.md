---
title: Define Task Mining anonymization
description: Replace personally identifiable information with alias data to protect sensitive user information.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2024-09-05"
reading_time_minutes: 1
breadcrumb: [Configure, Task Mining, Platform Analytics]
---

# Define Task Mining anonymization

Replace personally identifiable information with alias data to protect sensitive user information.

## Before you begin

Set the application scope to Task Mining core using the application picker.

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

**Note:** You can't add new anonymization configuration records.

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Configuration icon\(![Task Mining Configuration icon](../image/task-mining-configuration-icon.png)\).

3.  Under **Configuration**, select **Anonymization**.

4.  Select the anonymization configuration record that you want to modify.

    The available records are:

    -   **Event Field Replacement Value**

        Determines the replacement term for any event fields when the replaced event filter is applied. The default value is **BLOCKLISTED**. For more information, see [Avoid capturing and displaying application details](replace-application-details.md).

    -   **Minimum level of anonymization**

        Determines at the system level the minimum available level of anonymization when setting up a Task Mining project. This value defines how users are identified for the project that you're creating. The default value is **LOGIN NAME**. The other possible values are **INITIALS** for the user's initials or **ANONYMIZED CODE**.

5.  Modify the **Value** field.

6.  Select **Save**.


