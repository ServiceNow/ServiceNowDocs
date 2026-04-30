---
title: Set up table notifications for non-task tables
description: Table notifications are supported for all task tables by default, and you can set up a table notification for any other table.
locale: en-US
release: yokohama
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up table notifications for non-task tables

Table notifications are supported for all task tables by default, and you can set up a table notification for any other table.

## Before you begin

Role required: live\_feed\_admin or chat\_admin

## Procedure

1.  Navigate to **System Definition** &gt; **Business Rules**.

2.  Open the **Live Feed events** business rule.

3.  In the Advanced section,select and copy the text in the **Script** field.

4.  Click the back arrow on the top, left to exit the record and return to the Business Rules list.

5.  Click **New**.

6.  Enter the following values at the top of the form.

    -   **Name**: Enter a name, such as `Live Feed events for my table`.
    -   **Table**: Select the table for which you are setting up a notification.
    -   **Active** and **Advanced**: Select these check boxes.
7.  In the **When to run** section, enter the following values.

    -   **When**: Select **before**.
    -   **Insert**, **Update**, and **Delete**: Select the check boxes.
8.  In the **Advanced** section, paste the script from the **Live Feed events** business rule into the script box.

9.  Click **Submit**.

    The **Live Feed events** business rule runs on the non-task table. It fires the **live\_feed.update** event, which is associated with the **Live Feed Update** script action. The script action sets up variables and processes the table notifications.


## What to do next

After saving the business rule, create a [Live Feed table notification record](t_SetUpATableNotifForATaskTable.md) for the new table as you would for a task table.

**Parent Topic:**[Live Feed table notifications](../concept/c_SetUpLiveFeedTableNotifications.md)

**Related topics**  


[Set up table notifications for task tables](t_SetUpATableNotifForATaskTable.md)

[Live Feed table notification examples](../concept/c_LFTableNotifiExamples.md)

