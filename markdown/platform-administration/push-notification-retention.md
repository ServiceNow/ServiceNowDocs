---
title: Push notification retention
description: You can archive and eventually destroy push notifications that you no longer need or if your Push Notification table is excessively large.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Push notification retention

You can archive and eventually destroy push notifications that you no longer need or if your Push Notification table is excessively large.

Push notification retention is available starting with the Jakarta release.

## Push notification archive and destruction plugins

The push notification archiving and destruction feature uses the Data Archiving and Push Retention plugins. The Data Archiving plugin must be active to archive and destroy push notification records. The Push Retention plugin provides a set of rules that specify when the system archives and destroys push notification records.

In new instances, the Push Retention plugin and associated archive and destroy rules are active by default. On upgraded instances, you must manually activate both the plugin and the archive and destroy rules. Be sure to review and approve the archive and destroy rules before activating them.

If your instance already has a process for managing push notification records, you do not need to activate the Push Retention plugin. If you want to replace your current process with Push Retention, be sure to deactivate the current process before activating the archive and destroy rules.

## Archiving and destroying push notification records

Archiving means moving records from the Push Notification \[sys\_push\_notification\] table to the Push Notification Archive \[ar\_sys\_push notification\] table when they exceed the archive rule time limit. Destroying means deleting records in the Push Notification Archive table when they exceed the destroy rule time limit.

## Default archive and destroy rules

Push retention provides the following push archive rules:

-   **Push Notification - Over a year old:** archives push notification records that were created more than 365 days prior to the current date.
-   **Push Notification Archive - Over a year old:**destroys push notification records that have been archived for more than 365 days prior to the current date.

With these default settings, your messages are kept on the instance for a total of two years: one year in the Push Notification table, and one year in the Push Notification Archive table. At the end of the period, the system deletes the expired notification records from the Push Notification Archive table.

**Note:** By default these rules are active on new instances and inactive on upgrades. The system runs archive and destroy rules when you activate them.

## Compatibility with other record management implementations

If you are already using another method for managing push notification records, such as table cleaners, you do not have to use the Push Retention feature. To prevent unexpected record deletion, avoid using multiple push notification management processes on the same instance at the same time.

**Note:** For assistance replacing your existing record management implementation with push notification retention, contact your professional services or sales representative.

-   **[Activate the Push Retention plugin](../task/activate-push-retention-plugin.md)**  
The Push Retention plugin \(com.glide.push\_retention\) provides the retention policy for push notifications, so that you can specify when the system archives and destroys push notification records.
-   **[Archive push notifications manually](../task/archive-push-notification-manually.md)**  
You can manually archive push notifications on demand instead of waiting for the instance to archive them based on a scheduled job.

**Parent Topic:**[Push notifications](c_PushNotifications.md)

**Related topics**  


[Push notification system](../reference/r_PushMessageArchitecture.md)

[Activate push notifications](../task/t_ActivatePushNotifications.md)

[Installed with push notifications](../reference/r_InstalledWithPushNotifications.md#)

[Push notification properties](../reference/r_PushNotificationProperties.md)

[Push notification setup with the ServiceNow mobile app](../reference/r_PushNotificationSetupSN.md)

[Push notification setup with a custom push application for ServiceNow mobile apps](../reference/r_PushNotificationSetupCustom.md)

[Requeue failed push notification messages](../task/t_HandlingFailedPushMessages.md)

