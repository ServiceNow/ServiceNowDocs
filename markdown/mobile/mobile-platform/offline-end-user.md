---
title: Offline mode for mobile
description: Access and submit actions to records in your mobile apps, even if you don't have an internet connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-end-user.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 3
breadcrumb: [Mobile app settings, Using the mobile apps, Mobile Platform]
---

# Offline mode for mobile

Access and submit actions to records in your mobile apps, even if you don't have an internet connection.

Plan ahead when you use offline mode. If you're working in an area with no internet access, download what you want to work on ahead of time while you're still connected to the internet.

When you're in offline mode, the changes that you make to your records are logged in your outbox. Your outbox tracks all the actions that you made on your cached records. After your device has internet access, you can synchronize your device with the instance. The cached changes in your outbox update to the instance.

## Enable offline mode

Enable offline mode in your **Settings** tab. Tap **Offline** and then toggle on **Offline Mode**.

If you have not already downloaded the offline cache, you see a dialog box that asks you to download it. Tap **Download cache** and then select **Offline mode**.

\[Omitted image "mobile-enable-offline.png"\] Alt text: Enabling offline mode in mobile

## Navigate the mobile app in offline mode

When you're in offline mode, a banner that reads Offline Mode displays across the top of all screens.

<table id="table_a2w_vp1_mjc"><tbody><tr><td>

\[Omitted image "mobile-offline1.png"\] Alt text: Launcher screen in offline mode

</td><td>

\[Omitted image "mobile-offline3.png"\] Alt text: Record in offline mode

</td></tr></tbody>
</table>Depending on how your administrator configures the mobile app, you're unable to submit certain actions while you're in offline mode. These actions are hidden from the user interface.

|Online with actions available|Offline with some actions unavailable|
|-----------------------------|-------------------------------------|
|\[Omitted image "mobile-offline-grey1.png"\] Alt text: Online with all actions available|\[Omitted image "mobile-offline-grey2.png"\] Alt text: Offline mode with some actions not listed in the menu|

When you submit an action while you're in offline mode, the change gets marked with a cloud offline icon. Changes remain marked until your device synchronizes to the server.

\[Omitted image "mobile-offline-action.png"\] Alt text: Offline Action: Saved to Outbox

## Disable offline mode and synchronize outbox

To turn off offline mode and sync pending actions, do the following:

-   Navigate to **Settings** &gt; **Offline** in the mobile app. Then deselect **Offline Mode**.
-   Tap **Sync all** from the outbox items list.

Once connectivity is restored, a pop-up displays prompting you to select **Go Online and Sync** to upload any pending changes from the outbox.

**Note:** After the synchronization completes, you're back online and your offline cache is deleted.

<table id="table_gv1_135_ljc"><tbody><tr><td>

\[Omitted image "mobile-offline-outbox.png"\] Alt text: Changes remain in the outbox until synced to the server.

</td><td>

\[Omitted image "mobile-offline-goonline-sync.png"\] Alt text: Pop up listing option to go online and sync

</td><td>

\[Omitted image "mobile-offline-cache-button.png"\] Alt text: Offline cache page

</td></tr></tbody>
</table>## Cache expiration

Your administrator configures a default length of time after which your offline cache expires.

When a cache expires, you must go online and sync your changes. Warning messages appear periodically to remind you to synchronize your cache before it expires.

**Note:** Always synchronize your cache before and after going offline.

\[Omitted image "cache-expiration.png"\] Alt text: Warning message to prevent cache expiration.

## Resolve synchronization errors

Problematic changes that you made in offline mode don't synchronize to the instance. They remain in the outbox until they are resolved.

You can't synchronize changes that contradict changes made by other users while you were offline. For example, you may receive an error message if you try to synchronize changes to a record that another user closed while you were working in offline mode.

To view the errors in your cached changes, navigate to **Settings** &gt; **Offline** &gt; **Outbox**. Error messages indicate where errors occurred in your cached records while you were offline. You can resolve any of the listed issues directly from your outbox. Tap **Resolve** to fix the error or tap **Delete** to remove the issue from the list.

<table id="table_hmj_3k5_ljc"><tbody><tr><td>

\[Omitted image "mobile-offline-error-banner.png"\] Alt text: Pop up banner with error message

</td><td>

\[Omitted image "mobile-offline-error-sync.png"\] Alt text: Options listed to delete or resolve listed error

</td></tr></tbody>
</table>You can either tap **Resolve** to fix the error or tap **Delete** to remove the issue from the list.

## Scheduled offline caching

\[Omitted image "offline-mode-user-setting.png"\] Alt text: Offline mode user settings

Enable scheduled offline caching to automatically download your cache according to your work schedule. Scheduled caching works in the background, so you can continue to use the app while the download completes. You can enable or disable this feature in your app settings.

**Note:** To download content only when connected to Wi-Fi, enable the **Wi-Fi only** option.

