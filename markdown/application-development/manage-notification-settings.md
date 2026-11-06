---
title: Turn notifications on or off in Arc
description: Choose whether Arc notifies you about approvals, requests for your input, and schedules, and check that macOS lets Arc show notifications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/manage-notification-settings.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [notification settings, desktop notifications, pending approvals, reminders, awaiting input, schedule notifications, notification delay, send test]
breadcrumb: [Notifications in Arc, Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Turn notifications on or off in Arc

Choose whether Arc notifies you about approvals, requests for your input, and schedules, and check that macOS lets Arc show notifications.

## Before you begin

Role required: sn\_app\_arc.user

## About this task

You can turn each type of notification on or off, depending on what you want to hear about.

## Procedure

1.  In Arc, select your name at the bottom of the sidebar, and then select **Settings**.

2.  Select **Notifications**.

3.  Under **Delivery**, turn each setting on or off.

    -   **Desktop notifications**: Turns all notifications on or off.
    -   **Approvals**: Notifies you when an approval is waiting on you.
    -   **Awaiting input**: Notifies you when Arc is waiting for your response, such as when it asks you to confirm a draft before it sends it.
    -   **Notify me**: Sets how long Arc waits before it notifies you about approvals and input requests. Choose **Immediately**, or a delay of 1 to 4 minutes. This setting is available when **Approvals** or **Awaiting input** is on.
    -   **Schedules \(Recommended\)**: Notifies you when a scheduled job or reminder is due. These notifications are always sent at the scheduled time.
    With a delay, you aren't notified about approvals you answer right away in the chat.

4.  On macOS, under **macOS status**, check that **Permission** shows **Enabled**.

    Desktop notifications are available on macOS only. On Windows, this section doesn't appear, and Arc notifies you with in app banners while it's open.

    If macOS doesn't allow Arc to show notifications, select **Open System Settings** and turn on notifications for Arc.

5.  To see what a notification looks like, select **Send test**.

    **Send test** is in the **macOS status** section, so it's available on macOS only.


## What to do next

To respond to an approval from a notification, see [Approve or reject an action from a notification in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/respond-approval-notification.md).

**Parent Topic:**[Notifications in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/notifications-arc.md)

