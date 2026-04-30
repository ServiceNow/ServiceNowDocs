---
title: Archive push notifications manually
description: You can manually archive push notifications on demand instead of waiting for the instance to archive them based on a scheduled job.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Push notification retention, Push notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Archive push notifications manually

You can manually archive push notifications on demand instead of waiting for the instance to archive them based on a scheduled job.

## Before you begin

Role required: admin

## About this task

Push retention provides these push notification archive rules:

-   **Push Notification - Over a year old:** archives push notification records that were created more than 365 days prior to the current date.
-   **Push Notification Archive - Over a year old:**destroys push notification records that have been archived for more than 365 days prior to the current date.

You can manually archive push notification messages that meet the default archive and destroy rules or any additional archive rules that you create.

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Open the push notification archiving rule, for example Push Notification - Over a year old

3.  Click **Recalculate Estimate** to see how many records in the Push Notification \[sys\_push\_notification\] table are going to be archived.

    The estimate appears in the **Record estimate** field.

4.  Click **Run Archive Now**.


**Parent Topic:**[Push notification retention](../concept/push-notification-retention.md)

