---
title: Configuring push notifications for task assignment
description: Assign tasks and send reminders to customer service agents and field technicians using push notifications.
locale: en-US
release: australia
product: Mobile Experience for Field Service Management \(Glide Family\)
classification: mobile-experience-for-field-service-management-glide-family
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Now Mobile Agent application, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Configuring push notifications for task assignment

Assign tasks and send reminders to customer service agents and field technicians using push notifications.

Agents and technicians can receive push notifications about tasks on their mobile devices. Dispatchers and managers can use push notifications to assign tasks to groups or to individual agents and to send reminders. Agents and technicians can accept or reject tasks from their mobile devices depending on the configuration.

Push notifications for work order tasks use the **ServiceNow Mobile Application** push application. Use this application to send notifications to both individual users and assignment groups.

Users with the system administrator role can enable and configure push notifications. See Push notifications for more information.

## Push notifications for task assignment

When a dispatcher or manager assigns a task to an individual user:

-   The user receives a notification with an **Approve** or **Reject** action. Approving the notification assigns the task to the user. Rejecting the notification unassigns the task and returns it to the **Pending Dispatch** state.
-   With auto assignment enabled, the user receives a notification about the assigned task and no further action is required.

**Note:** This behavior depends on the setting for the **Agent must accept or reject the assigned task** configuration option. If disabled, the agent does not have the option to reject a task.

When a dispatcher or manager assigns a task to an assignment group, all users in the group receive a notification with an **Approve** or **Reject** action. Agents receive the notification and can accept or reject the task. When an agent clicks **Assign to me**, the state of the task changes to **Assigned**.

## Push notifications as reminders

Notifications can be sent as reminders about upcoming tasks and about SLAs coming due. These notifications are sent to the agent assigned to the task.

Send notifications as upcoming task reminders. Reminders can be set at 15-minute intervals up to one hour. These reminders require the **wm\_notification.upcoming.task.reminder.minutes.before** system property to be set. The default setting is 45 minutes before the task start time. If the value for this property is not defined, the agent does not receive reminders.

Send notifications to the assigned agents and agent managers for the following SLAs:

-   SLA warning
-   SLA breached
-   SLA repair complete

