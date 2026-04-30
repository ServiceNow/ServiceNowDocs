---
title: Offline mode for mobile
description: Access and submit actions to records in your mobile apps, even if you do not have an internet connection.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Mobile app settings, Using the mobile apps, Mobile Platform]
---

# Offline mode for mobile

Access and submit actions to records in your mobile apps, even if you do not have an internet connection.

Video showing how offline mode works in the ServiceNow Agent mobile app.This video shows how offline mode works in your mobile apps. Learn how to download data, enable and disable offline mode, synchronize your outbox, and resolve synchronization errors.

Plan ahead when you use offline mode. If you will be working in an area with no internet access, download what you want to work on ahead of time while you are still connected to the internet.

When you are in offline mode, the changes that you make to your records are logged in your outbox. Your outbox tracks all the actions that you made on your cached records. After your device has internet access, you can synchronize your device with the instance. The cached changes in your outbox update to the instance.

## Enable offline mode

Enable offline mode in your **Settings** tab. Tap **Offline** and then toggle on **Offline Mode**.

If you have not already downloaded the offline cache, you see a dialog box that asks you to download it. Tap **Download and Go Offline**.

![Enabling offline mode in mobile](../image/mobile-enable-offline.png)

## Navigate the mobile app in offline mode

When you are in offline mode, a banner that reads "Offline Mode" appears across the top of all screens.

![Applications homepage offline mode](../image/mobile-offline1.png)

![List screen offline mode](../image/mobile-offline2.png) ![Record offline mode](../image/mobile-offline3.png)

Depending on how your administrator configures the mobile app, you are unable to submit certain actions while you are in offline mode. These actions are grayed out on the user interface.

![Certain actions are disabled in offline mode.](../image/mobile-offline-grey1.png) ![Certain actions are disabled in offline mode.](../image/mobile-offline-grey2.png)

When you submit an action while you are in offline mode, the change gets marked with a patterned background. Changes remain marked until your device synchronize to the server.

![Offline Action: Saved to Outbox](../image/mobile-offline-action.png)

## Disable offline mode and synchronize outbox

To return online in the mobile app, navigate to **Settings** &gt; **Offline Mode**. On the offline mode screen, toggle off **Offline Mode**.

![Changes remain in the outbox until synced to the server.](../image/mobile-offline-outbox.png)

You can synchronize your changes while in offline mode in one of the following ways:

-   From the Offline Mode screen, toggle off the **Offline Mode** button.
-   From the Outbox screen, tap **Sync All**.

**Note:** After the synchronization completes, you are back online and your offline cache is deleted.

## Cache expiration

Your administrator configures a default length of time after which your offline cache expires.

When a cache expires, you lose all the data that you saved to the cache. If you do not synchronize the cache to an instance before the cache expires, none of your changes show on the instance.

Warning messages appear periodically to remind you to synchronize your cache before it expires. To avoid losing your data due to a cache expiration, always synchronize your cache before and after going offline.

![Warning message to prevent cache expiration.](../image/cache-expiration.png)

## Resolve synchronization errors

Problematic changes that you made in offline mode do not synchronize to the instance. They remain in the outbox until they are resolved.

You cannot synchronize changes that contradict changes made by other users while you were offline. For example, you may receive an error message if you try to synchronize changes to a record that another user closed while you were working in offline mode.

To view the errors in your cached changes, navigate to **Settings** &gt; **Offline Mode** &gt; **Outbox**. Error messages indicate where errors occurred in your cached records while you were offline. You can resolve any of the listed issues directly from your outbox.

![Error messages in the outbox.](../image/outbox-error.png)

You can either tap **Resolve** to fix the error or tap **Delete** to remove the issue from the list.

## Scheduled offline caching

![Offline mode user settings](../image/offline-mode-user-setting.png)

Enable scheduled offline caching to automatically download your cache according to your work schedule. Scheduled caching works in the background, so you are able to continue to use the app while the download completes. You can enable or disable this feature in your app settings.

**Note:** Enable **Wi-Fi only** to allow downloads only when you are connected to Wi-Fi.

