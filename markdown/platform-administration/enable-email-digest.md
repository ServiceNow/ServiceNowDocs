---
title: Enable an email digest in Core UI
description: Reduce the number of notifications you receive for a selected target record during a specified time interval by enabling an email digest. The digest is a single email that collects individual notifications for a targeted record generated during the specified interval. The email digest of two different target records will not be clubbed in a single email.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Email digests, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable an email digest in Core UI

Reduce the number of notifications you receive for a selected target record during a specified time interval by enabling an email digest. The digest is a single email that collects individual notifications for a targeted record generated during the specified interval. The email digest of two different target records will not be clubbed in a single email.

## Before you begin

Role required: none

## About this task

The email digest option is available only if your admin configured email digest content for that notification.

## Procedure

1.  Select the gear icon \(![System Settings gear icon](../image/IconUI16Gear.png)\) in the banner frame to open the System Settings window, and select the **Notifications** tab.

2.  Select the notification:

    1.  In the Notifications By Category section, select the row or right arrow \(**&gt;**\) of the category that you want to view.

    2.  In the list of notifications for the category, select the row or right arrow \(**&gt;**\) next to the notification that you want to edit.

3.  To enable or disable an email digest for the notification, if an email digest is available:

    1.  Select the **Email Digest** switch.

        The email digest is enabled when the switch is green and disabled when the switch is grey.

    2.  If you enabled the digest, select the **Interval** \(length of time\) during which the notifications are accumulated.

        The digest interval begins with the first occurrence of notification activity. For example, if you select the daily \(1 Day\) interval and the first notification occurs at 07:00, the system begins accumulating notifications at 07:00 and stops at 07:00 the next day.

    Soon after the interval ends, the system sends the email digest to you instead of sending the individual notifications generated during the digest interval. If you disabled the digest, the system immediately stops accumulating the notifications for the digest and does not send the email digest. The system resumes sending the notifications as they are generated.


**Parent Topic:**[Email digests](../concept/email-digests.md)

**Related topics**  


[Apply notification conditions](apply-notification-conditions.md)

[Email digests](../concept/email-digests.md)

[Configure email digests](configure-email-digest.md)

