---
title: Set up actionable notifications for ITSM Virtual Agent
description: Administrators and users with the virtual\_agent\_admin role can enable system notifications, trigger Workflow Studio flows for actionable notifications topics, and activate notifications in Virtual Agent.
locale: en-US
release: yokohama
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up ITSM Virtual Agent, ITSM Virtual Agent, IT Service Management]
---

# Set up actionable notifications for ITSM Virtual Agent

Administrators and users with the virtual\_agent\_admin role can enable system notifications, trigger Workflow Studio flows for actionable notifications topics, and activate notifications in Virtual Agent.

## Before you begin

Role required: admin or virtual\_agent\_admin

## Procedure

1.  Enable system notifications.

    1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

    2.  Set the **Active** property to **true** for the conversations you want to activate.

        ![Activate system notifications for conversations.](../image/SystemNotifications.png)

2.  Activate Workflow Studio flows for specific actionable notifications ITSM Virtual Agent conversations.

    These topics are inactive by default. For complete details about activating flows, refer to [Activate a flow](https://www.servicenow.com/docs/access?context=flow-activate&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    The following flows for actionable notifications must be activated if you want to use them with Actionable Notifications:

    -   ITSM Actionable Notifications trigger flow - Approval Reminder
    -   ITSM Actionable Notifications trigger flow - Incident commented
    -   ITSM Actionable Notifications trigger flow - Software Installation
    1.  Select the flow you would like to activate in Workflow Studio.

    2.  Select **Activate**.

3.  [Enable notifications in Virtual Agent.](https://www.servicenow.com/docs/access?context=enable-va-notifications&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)


**Parent Topic:**[Setting up ITSM Virtual Agent](../concept/setting-up-itsm-va.md)

