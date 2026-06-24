---
title: Configure notifications for Employee Slate
description: Configure the content, the trigger conditions, and the recipients for the 14 out-of-the-box notifications shipped with Employee Slate for Now Assist.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/eslate-configure-notifications.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
keywords: [notifications, notification content, trigger conditions, recipients, Employee Slate, Now Assist]
breadcrumb: [Notifications, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure notifications for Employee Slate

Configure the content, the trigger conditions, and the recipients for the 14 out-of-the-box notifications shipped with Employee Slate for Now Assist.

## Before you begin

Activate Employee Slate for Now Assist in the instance.

Role required: admin or Employee Slate administrator.

## About this task

Each notification has a content template, an icon, a set of trigger conditions, and a recipient list. Employees view notifications in the bell tray at the top of Employee Slate. Each notification moves through three states: new, viewed, and open. Notifications on the same item group automatically. Employees can mark all as read with a bulk action.

**Note:** Notifications for Moveworks use a separate configuration path.

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Portal Notifications**.

    The page lists the 14 out-of-the-box notifications shipped for Employee Slate for Now Assist.

2.  Select a notification, such as **Incident commented**.

    The notification folder holds the content template, the icon, the trigger conditions, and the recipient list.

3.  Edit the content under **Notification content**.

    Declare the sentences that appear when the notification fires. Use short sentences and active voice.

4.  Set the icon for the notification.

    The icon appears next to the notification in the bell tray and identifies the source.

5.  Set the trigger conditions under **When to send**.

    The trigger conditions describe the system event or the record change that fires the notification.

6.  Set the recipient list under **Who will receive**.

    The recipient list resolves at run time and identifies the employees who receive the notification.

7.  Open the logs table to review notification activity.

    The logs table records every notification sent and the state for each recipient: new, viewed, or open.

8.  Verify the experience from an employee account.

    Trigger the source event, open the bell tray, and confirm that the notification appears with the configured content and icon. Select **Mark all as read** to confirm the toast message and the state change in the log.

9.  Save the configuration.

    The save commits the content, the icon, the trigger conditions, and the recipient list.


## Result

Employees view the configured notifications in the bell tray with the chosen content, icon, and recipient scope. Group updates collapse into one entry. The bulk mark-as-read action clears the tray. The logs table records the activity for review.

