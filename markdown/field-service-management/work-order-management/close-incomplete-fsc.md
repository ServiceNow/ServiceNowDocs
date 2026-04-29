---
title: Close an incomplete work order task on a mobile device
description: You can close a work order task as incomplete if there is work pending on the task through the Field Service Contractor for mobile application.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Close an incomplete work order task on a mobile device

You can close a work order task as incomplete if there is work pending on the task through the Field Service Contractor for mobile application.

## Before you begin

Role required: wm\_ext\_agent

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  On the **My work** navigation tab, tap **Today's tasks**.

3.  Open a work order task that is already in progress.

4.  Tap the more actions \(![More actions icon](../image/OverflowIcon.png)\) icon.

5.  Tap **Close Incomplete**.

6.  Provide the reason in the **Closure Notes**.

    The Closure Notes information is copied to the **Activity Stream tab** in a work order task form.

7.  Automatically create a work order task to follow up on any pending work from the current work order task by enabling the **Create a Follow-up Task** option.

    The new work order task will be assigned to your group.

8.  Tap **Submit**.

    Confirmation messages are displayed depending on whether you enabled the **Create a Follow-up Task** option.

    -   If you have not enabled the option, the confirmation message `Task closed successfully` is displayed.
    -   If you have enabled the option, the message `You have 2 messages` is displayed. Tapping **View** on the message displays the success confirmation message and a message providing the number of the follow-on task that was created.

## Result

The task is closed. If you created a follow-up work order task, you can access it by navigating to **My work** &gt; **My group tasks**.

