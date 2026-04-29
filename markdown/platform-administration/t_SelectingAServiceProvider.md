---
title: Select a service provider
description: You can configure how a device's service provider affects the construction of the device's email address.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a service provider, Subscription-based notifications, Preferences in Core UI, Notification Preferences, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Select a service provider

You can configure how a device's service provider affects the construction of the device's email address.

## Before you begin

Role required: admin

## Procedure

1.  From the user menu, navigate to **Preferences** &gt; **Notifications** and then select the **Advanced Preferences** link.

2.  Select the **Delivery Channels** tab.

3.  If no devices are configured, follow these steps to add an SMS device and select a service provider.

    1.  In the SMS channel section, select **+Add**.

    2.  Expand the **Channel Info** section and provide the Channel Name and Phone number in the fields.

    3.  From the **Service provider** drop-down list, select the appropriate service provider.

        The service providers are stored in the Notification Service Provider \[cmn\_notif\_service\_provider\] table. Only active service providers are visible.

    4.  Select **Save**.


**Parent Topic:**[Create a service provider](t_CreateAServiceProvider.md)

