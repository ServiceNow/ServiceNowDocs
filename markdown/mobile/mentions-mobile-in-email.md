---
title: Customize email notifications for mobile activity stream mentions
description: Enable users to alert their contacts by email that they are mentioned in a thread. The user enters the @ character followed by the contact's name in a record's activity stream, for their contact to be alerted. This feature is enabled by default.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure notifications for mobile activity stream mentions, Mobile push notifications, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Customize email notifications for mobile activity stream mentions

Enable users to alert their contacts by email that they are mentioned in a thread. The user enters the `@` character followed by the contact's name in a record's activity stream, for their contact to be alerted. This feature is enabled by default.

## Before you begin

Role required: admin

## About this task

Configure your instance to send an email notification when a user mentions a contact within the activity stream. You can either use the default notification record or create a new notification record. For information about creating a new notification record, see [Create an email notification](https://www.servicenow.com/docs/access?context=t_CreateANotification&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications** in the filter navigator.

2.  Search for the notification record named **Activity Stream @Mention Email**, then select the record to open it.

3.  Verify that **Active** is selected.

4.  Customize the email notification fields.

5.  Select **Update**.

6.  Select the Settings icon \(![Settings icon.](../image/GearIcon.png)\) and select the **Notifications** tab.

7.  Verify that **Allow Notifications** is enabled.


**Parent Topic:**[Configure notifications for mobile activity stream mentions](../concept/notification-activity-stream.md)

