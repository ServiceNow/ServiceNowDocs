---
title: Specify alternative outbound email addresses for notifications
description: By default, the system sends all outbound email notifications from the default email address of the instance, but you can specify an alternative address.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Specify alternative outbound email addresses for notifications

By default, the system sends all outbound email notifications from the default email address of the instance, but you can specify an alternative address.

## Before you begin

Role required: admin

## About this task

For organizations that need to send email messages from specific email addresses, such as from multiple service desks, or they want to send notifications in different languages, the platform supports configuring multiple outbound addresses.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select an existing notification record for the desired event, such as **Incident Closed**.

3.  Create a copy of this notification for each outbound email address.

4.  Open one of the notification copies, and click the **Advanced view** related link.

5.  In the **What it will contain** section, add an email address to the From field that is different from the default instance address.

    For more information on how to construct the From address, refer to section 3.6.2 of [RFC 2822](https://tools.ietf.org/html/rfc2822#page-21).

6.  Add a different email address than the**From** address to the **Reply to** field if you want replies to this notification to go to a different address.

    The system checks the **From** field for an address. If this field is empty, then the system uses the default address for the instance. If the **Reply to** field is empty, then all replies are sent to the address from which the notification was sent. If the **Reply to** field contains an email address, then the system sends all replies to the notification to this address.

7.  Create mutually-exclusive conditions for notifications of the same type, so only the desired notification is sent when the event is fired.

    For example, if the **Company** is a certain value, then the notification comes from a unique email address entered in the **From** field.

8.  Click **Update**.


**Parent Topic:**[Create an email notification](t_CreateANotification.md)

