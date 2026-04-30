---
title: Push notifications, actions, and messages
description: Push notifications, actions, and messages for work order task assignments and reminders.
locale: en-US
release: zurich
product: Mobile Experience for Field Service Management
classification: mobile-experience-for-field-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring push notifications for task assignment, Configure the Now Mobile Agent application, Setting up Field Service Mobile Agent, Configure, Field Service Management]
---

# Push notifications, actions, and messages

Push notifications, actions, and messages for work order task assignments and reminders.

## Push notifications

Adds the following notifications to **System Notification** &gt; **Push** &gt; **Push Notifications**:

-   WorkOrderTaskUpcomingReminder: Sends a notification to the assigned agent as a reminder about an upcoming task.
-   WorkOrderTaskAcceptanceNotification: Sends a notification when a task must be accepted by an agent.
-   WorkOrderTaskGrpAssignmentNotification: Sends a notification when a dispatcher assigns a task to an assignment group.
-   WorkOrderTaskAutoAcceptanceNotification: When auto assignment is enabled, sends a notification when a task is auto accepted by an agent.

## Push notification actions

Adds the following actions to **System Notification** &gt; **Push** &gt; **Push Action**:

-   WO Task-Accept Action
-   WO Task-Reject Action
-   WO Task-Running Late Action

## Push notification messages

Adds the following messages to **System Notification** &gt; **Push** &gt; **Push Messages**:

-   WO Task Acceptance Message
-   WO Task Auto Acceptance Message
-   WO Task Group Assignment Message
-   WO Task Upcoming Reminder Message

## Turn on notification preferences

Field service agents must turn on the following notification preferences:

1.  Navigate to **Self Service** &gt; **My Notifications**.
2.  Turn on the work order task notifications:
    -   WO Task Acceptance Notification
    -   WO Task Auto Acceptance Notification
    -   WO Task Group Assignment Notification
    -   WO Task Upcoming Reminder
3.  Verify that notifications are set to ON on the user profile.

