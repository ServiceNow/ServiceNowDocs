---
title: Email digests
description: An email digest is a single email that summarizes the activity for a selected notification and its target record during a specified time interval. You can enable an email digest to reduce the number of notifications received when frequent updates to the associated record occur within a short time period.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Email digests

An email digest is a single email that summarizes the activity for a selected notification and its target record during a specified time interval. You can enable an email digest to reduce the number of notifications received when frequent updates to the associated record occur within a short time period.

![Email digest example that has a summary of incident comments](../image/EmailDigestExample.png "Example email digest")

**Note:** Email digests apply to email notifications only and are not supported for SMS messages, push notifications, and activity streams.

## How email digests work

In new and upgraded instances, the Email digest \(com.glide.email\_digest\) plugin is activated by default. Your instance must use the Core UI interface, since the email digest feature involves setting [user notification preferences](user-notification-preferences.md) in the System Settings window.

Admins determine which notifications can be delivered in an email digest and configure the digest content for those notifications. Admins can also control the intervals for digests. An interval is the length of time that notifications are collected for the digest, such as daily or hourly.

Users enable the digest and select the digest interval for a specific notification in their notification preferences. The system accumulates the notifications that normally would be sent during the specified interval and summarizes them in the email digest.

When processing an email digest, the system:

-   Stores the digest configuration for the notification in the Notifications \[sysevent\_email\_action\] table.
-   Temporarily stores the notification content accumulated for a user in the Email Digest Parts \[sys\_email\_digest\_part\] table and the Email Digest Part Users \[sys\_email\_digest\_part\_user\] table.
-   Runs an email digest job every 15 minutes to check when a digest is ready to be sent to a user.

    The system uses the digest interval to determine when the digest is ready to be sent. The digest interval begins when the first notification is triggered for the user and stops at the end of the interval time.

-   Sends the email digest to the user soon after the selected digest interval ends.

    For example, if a user selects an hourly digest interval and the first notification is triggered at 08:15, the interval starts at 08:15. When the digest interval ends, the system generates the email digest approximately one hour later, at about 09:15 or shortly after, depending on when the email digest job ran.


## Set up email digests

-   **What to do — admins**
    1.  Review the base system digest intervals and if needed, [create or modify intervals](../task/create-digest-intervals.md).

        The base system digest intervals are one day \(24 hours\), one hour, every four hours, and seven days \(weekly\).

    2.  Determine the email notifications that can be delivered in a digest and [configure the email digest content](../task/configure-email-digest.md) for those notifications.

        When determining which notifications are appropriate for an email digest, consider the notification content and intervals that your users can select. For example, digests that can be generated weekly might be better suited for notifications that are non-urgent.

-   **What to do — all users**

    For a notification that can be delivered in an email digest, [enable the email digest in your notification preferences](../task/enable-email-digest.md) \(**Notifications** tab in the System Settings window\). You also specify the interval time that the notifications are accumulated.

-   **Next step**

    If you are an admin, begin the digest setup process by reviewing the base system email digest intervals and [create or modify the intervals](../task/create-digest-intervals.md).


-   **[Create or modify email digest intervals](../task/create-digest-intervals.md)**  
Admins can create or modify the email digest intervals \(length of time\) during which activity for a selected notification is accumulated in an email digest. Users select a digest interval when they enable an email digest in their notification preferences.
-   **[Configure email digests](../task/configure-email-digest.md)**  
Use the Notification form to create or modify the content of an email digest for a notification. You can also disable the email digest for a notification so that it isn’t available in the notification preferences of your users.
-   **[Enable email digest in Next Experience](../task/enable-email-digest-next-exp.md)**  
Reduce the number of email notifications you receive by enabling email digest notifications. An email digest is a single email that summarizes the activity for a selected notification and its target record during a specified time interval.
-   **[Enable an email digest in Core UI](../task/enable-email-digest.md)**  
Reduce the number of notifications you receive for a selected target record during a specified time interval by enabling an email digest. The digest is a single email that collects individual notifications for a targeted record generated during the specified interval. The email digest of two different target records will not be clubbed in a single email.

**Parent Topic:**[Email and SMS notifications](c_EmailNotifications.md)

**Related topics**  


[Create notification categories](../task/create-notification-categories.md)

[Create an email notification](../task/t_CreateANotification.md)

[Email templates](c_EmailTemplates.md)

[Email layouts](email-layouts.md)

[Email retention](email-retention.md)

[Watermarks on notification emails](c_WorkingWithWatermarks.md)

[Parse an email thread](../task/parse-email.md)

[Domain separation and Notifications](domain-separation-notifications.md)

[Email FAQs and troubleshooting notification emails](troubleshooting-notification-emails.md)

