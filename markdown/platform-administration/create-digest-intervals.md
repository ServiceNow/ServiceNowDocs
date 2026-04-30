---
title: Create or modify email digest intervals
description: Admins can create or modify the email digest intervals \(length of time\) during which activity for a selected notification is accumulated in an email digest. Users select a digest interval when they enable an email digest in their notification preferences.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Email digests, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create or modify email digest intervals

Admins can create or modify the email digest intervals \(length of time\) during which activity for a selected notification is accumulated in an email digest. Users select a digest interval when they enable an email digest in their notification preferences.

## Before you begin

Role required: admin

## About this task

Before adding an email digest interval, review the base system digest intervals in the Digest Intervals \[sys\_email\_digest\_interval\] table. You can modify intervals, including the base system intervals, which are one day \(24 hours\), one hour, every four hours, and seven days \(weekly\).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Digest Intervals**.

    |Action|Description|
    |------|-----------|
    |To add an interval|Click **New**.|
    |To modify an interval|Select the interval to be changed.|

2.  Enter the new or changed interval information:

    |Field|Description|
    |-----|-----------|
    |Name|Interval name that describes the interval length of time, for example: Every 2 hours.|
    |Interval|Length of the interval, either number of **Days** or **Hours** \(hours, minutes, and seconds\). The minimum time length allowed is one hour, and the maximum time length allowed is seven days \(one week\).|

3.  If you created an interval, click **Submit**, or if you changed an interval, click **Update**.

    The system updates the Digest Intervals \[sys\_email\_digest\_interval\] table with the new or modified interval. The digest interval is listed as an option in the notification preferences \(**Notifications** tab in the System Settings window\) when a user enables a digest for the notification. For example:

    ![Example notification settings for a notification with the email digest enabled](../image/NotifPrefEnableDigest.png)

4.  To delete an interval, select the interval to be deleted in the Digest Intervals \[sys\_email\_digest\_interval\] table and click **Delete**.

    **Note:** If the interval is in use, the system does not remove the interval.


## What to do next

Determine the email notifications that can be delivered in a digest and [configure the email digest content](configure-email-digest.md) for those notifications.

**Parent Topic:**[Email digests](../concept/email-digests.md)

**Related topics**  


[Email digest properties](../concept/email-digest-properties.md)

