---
title: Configure notifications in Service Operations Workspace for ITSM
description: Customize notifications that are sent to an agent to update about various changes.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure notifications in Service Operations Workspace for ITSM

Customize notifications that are sent to an agent to update about various changes.

## Before you begin

Role required: workspace\_admin, notification\_provider\_admin, sn\_sow\_admin.sn\_sow\_admin or admin

For delegation notifications, the Notification Provider for Next Experience plugin \(com.glide.notification.provider.next.experience\) must be installed.

## About this task

An agent is notified in the following scenarios:

-   A change request, incident, or problem assigned to an agent has any updates.
-   A task is delegated to the agent.

The notification icon shows notification alerts. The icon shows a badge with notification count and new notifications for a short duration.![SOW notification alert](../image/sow-notification-alert.png)

Use the notification icon to view the notifications.![SOW notifications](../image/sow-notifications.png)

In email notifications, you can decide where the link to a record is redirected. Instead of a record automatically opening in the classic UI16 interface, the record can be opened in Service Operations Workspace \(SOW\). The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior. The record link in an email notification opens in SOW only if the following conditions are met:

-   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) system property is set to true.
-   The user selecting the incident record link has the sn\_sow\_user role.

This feature is applicable for the following record types:

-   Incident
-   Problem
-   Request

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Administration** &gt; **Notification triggers**.

2.  To modify the notifications for incident, problem, and change updates, perform the following steps:

    1.  From the list of notification triggers, select one of the following:

        -   Incident notification
        -   Problem notification
        -   Change notification
    2.  Edit the required information, such as the notification category, who to send it to and when to send it.

        **Who to send** and **When will receive** tabs contain the notification settings.

        **Note:** Keep in mind the following information when editing these notifications:

        -   You can’t edit the notification header.
        -   The **Category** field of each type of notification must match that notification type so the notifications are categorized correctly for agents. For example, the **Category** field must be **Incident** for incident notifications. This step confirms that the notification is categorized in the notification preferences and agents can easily turn on and off all the notifications categorized under a category.
    3.  Select **Update**.

3.  To modify the delegation notification, perform the following steps:

    1.  From the list of notification triggers, select **Delegation notification**.

    2.  Edit the required notification information, such as who to send it to, when to send it, its header and content.

        **Who to send** and **When will receive** tabs contain the notification settings.

    3.  Select **Update**.


