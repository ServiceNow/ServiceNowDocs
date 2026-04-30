---
title: Close a complete work order task on a mobile device
description: Close work order tasks to complete a task for which the issue is fixed or resolved through the Field Service Contractor for mobile application.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor for mobile, ServiceNow Agent mobile app, Use, Field Service Management]
---

# Close a complete work order task on a mobile device

Close work order tasks to complete a task for which the issue is fixed or resolved through the Field Service Contractor for mobile application.

## Before you begin

Role required: wm\_ext\_agent

## Procedure

1.  Access your instance using the ServiceNow Agent mobile application.

2.  On the **My work** navigation tab, tap **Today's tasks**.

3.  Open a work order task that is already in progress.

4.  Tap **Close Complete**.

5.  Enter the notes describing the closure in the **Closure Notes** field.

    The Closure Notes information is copied to the Activity Stream tab in a work order task form.

6.  Automatically create a work order task to follow up on any pending work from the current work order task by enabling the **Create a Follow-up Task** option.

    The new work order task will be assigned to your group.

7.  Tap **Submit**.

    Confirmation messages are displayed depending on whether you enabled the **Create a Follow-up Task** option.

    -   If you have not enabled the option, the confirmation message `Task closed successfully` is displayed.
    -   If you have enabled the option, the message `You have 2 messages` is displayed. Tapping **View** on the message displays the success confirmation message and a message providing the number of the follow-on task that was created.

## Result

The task is closed. If you created a follow-up work order task, you can access it by navigating to **My work** &gt; **My group tasks**.

