---
title: Create emergency notifications
description: Create an emergency notification in BCM UIB Workspace. You can then use Everbridge to notify the stakeholders.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create emergency notifications

Create an emergency notification in BCM UIB Workspace. You can then use Everbridge to notify the stakeholders.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager, or sn\_bcm.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace** and select **Crisis events** in the list view.

2.  Select the record in the **Pending** state.

    **Note:** If the **Exercise Method** is **Functional**, then you can create an emergency notification for an exercise event.

3.  Open the event record link from the **Number** column.

4.  Select the **Emergency Notifications** tab and choose **New**.

    The New Notification form is shown in the example.

    ![New notification form.](../image/create-new-notification.png)

5.  On the form, fill in the fields.

    For more information on the fields in the form, see [Create New Notification form](../reference/create-new-notification-form.md).

6.  To save the notification and send it later, select **Save**.

7.  Select **Send**.

    It creates a notification in Everbridge as shown in the example.

    ![Get response status.](../image/get-response-status-notification.png)

    When you create and send a notification for a crisis event in Business Continuity Workspace, a corresponding incident is created along with a notification in Everbridge.

8.  Refresh the page and verify that the notification was sent without any errors.

    If the notification isn’t sent due to an error, the Notification state moves to **Error**.

9.  Select **Get response status** to retrieve the notification status from Everbridge for contacts in the **Communication status** field.

    Before you submit an event for approval, all the notifications that are **In Progress** must be closed.

    1.  Select the link to the emergency notification record in the Number column to delete a notification that is in **Draft** or **Error** state.

        **Note:** You can’t delete a notification that is in the **Attempting to send**, **In Progress**, or **Completed** state.

    2.  Select **Delete** in the **More** actions icon.

10. Select **Save**.

    **Note:** Now that the event is closed and the corresponding incident in Everbridge is also closed, you can’t create any more notifications for this event.


-   **[Create New Notification form](../reference/create-new-notification-form.md)**  
Use the Create New Notification form in BCM UIB Workspace to add details about an emergency notification.

**Parent Topic:**[Sending notifications with Everbridge](../concept/ebn-collective-tasks.md)

