---
title: Approve or reject an action from a notification in Arc
description: Respond to an action that's waiting for your approval from an in app banner or a desktop notification, without going back to the chat it came from.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/respond-approval-notification.html
release: australia
topic_type: task
last_updated: "2026-10-26"
reading_time_minutes: 1
keywords: [approval notification, in app banner, desktop notification, Approve, Reject]
breadcrumb: [Notifications in Arc, Use, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Approve or reject an action from a notification in Arc

Respond to an action that's waiting for your approval from an in app banner or a desktop notification, without going back to the chat it came from.

## Before you begin

**Desktop notifications** and **Pending approvals** are turned on. For more information, see [Turn notifications on or off in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/manage-notification-settings.md).

Role required: sn\_app\_arc.user

## About this task

If you're in another chat when an action needs your approval, a banner appears at the top of the Arc window. If you're in another app, a desktop notification appears instead. Both show the action, the chat it belongs to, and how long you have before the request expires.

## Procedure

1.  Review the action named in the notification.

2.  Approve or reject the action.

    -   From the in app banner, select **Approve**.
    -   From the in app banner, select **Reject**. Optionally, in **Tell Arc why \(optional\)**, enter a reason, and then select **Confirm reject**.
    -   From the desktop notification, select **Options**, and then select **Approve** or **Reject**.
    To close the banner without responding, select the close icon. The action keeps waiting in its chat until it expires.


## Result

If you approve, Arc continues the task. If you reject, the action doesn't run, the step shows as rejected in the chat, and Arc uses your reason, if you gave one, when it continues.

## What to do next

For more information about approval cards in a chat, see [Respond to approval requests in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/respond-approval-requests.md).

**Parent Topic:**[Notifications in Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/notifications-arc.md)

