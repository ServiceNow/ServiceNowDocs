---
title: Offline mode
description: Configure offline mode to enable your users who have no internet connection to continue working from a mobile device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/mobile-offline-mode.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 3
breadcrumb: [Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Offline mode

Configure offline mode to enable your users who have no internet connection to continue working from a mobile device.

Configure specific applications, screens, or functions for users to use offline in your mobile apps. For a description of how offline mode features enhance end users' experience, see [Offline mode for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-end-user.md).

## Plan an offline mode strategy

Offline mode involves a series of configuration and planning decisions. These range from which apps, screens, and functions to enable, to how much data to store on a device. Every item included in the offline payload must be explicitly enabled by an administrator, meaning each configuration choice directly shapes what gets cached. Planning your offline mode strategy helps verify that what you configure is relevant and maintainable.

Before making configuration decisions, identify your target users, the screens they need access to, expected data size, and connectivity patterns such as field versus office use. This gives you the context to make the right choices at each level of the app, screen, and function hierarchy, keeping your offline mode lightweight and aligned with your users’ needs.

The offline mode setup options walk you through the key decisions involved in planning your offline configuration. Review each option to help you determine which approach best fits yours and your users' needs and working patterns, when constructing your offline mode strategy. For more information, see [Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md).

## Offline mode process

<table id="table_sqd_2l5_vnb"><tbody><tr><td>

Offline mode works by creating a cache of records on your mobile device that your users can view and update while offline. This cache is a limited set of data based on the applications your users can access. By default, this cache expires 48 hours after it is downloaded to a mobile device. Any changes your users make to the cache that aren't synchronized within 48 hours are moved to the outbox, where they can be synced to your instance at the user’s next log out.

**Note:** There is a difference in how operating systems display cache expiry time. iOS displays cache expiry time via the **Expires** field. Android displays the cache size and last cached time with no expiry indication.

</td><td>

\[Omitted image "enable-offline.png"\] Alt text: Example screens of downloading data in Offline mode and the Download Complete success message.

</td></tr><tr><td>

While in offline mode, only the parts of the app with cached data are accessible. This depends on which screens are configured to be available offline. For example, if offline mode is enabled only for Tasks and Inventory, all other areas of the mobile app are unavailable while the device is offline.

</td><td>

\[Omitted image "mobile-offline1.png"\] Alt text: Launcher screen in offline mode

</td></tr><tr><td>

While in offline mode, users can create, update, or delete cached records directly from their mobile device. Each action performed is automatically added to the Outbox, which stores all pending operations until the user is back online.

</td><td>

\[Omitted image "mobile-offline-action-comp.png"\] Alt text: Action performed in offline mode

</td></tr><tr><td>

When your users have network access again, they can disable ofﬂine mode and synchronize their data stored in the outbox on their device with the data on the instance. Updates between the mobile and the instance are automatic, unless there is a conflict. Users can resolve conflicts in their outbox.

</td><td>

\[Omitted image "offline-conflict.png"\] Alt text: Screens showing how to synchronize data.

</td></tr></tbody>
</table>-   **[Mobile experience capabilities available in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-capabilities.md)**  
Use the table to view the various capabilities and features that are either fully, partially or not supported in offline mode.
-   **[System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md)**  
Use the table to view system properties related to offline mode.
-   **[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-setup-options.md)**  
Review the setup options to determine which configurations apply to your offline mode requirements. Each option explains what to configure and why, helping you make informed decisions. Before configuring, identify your target users, the screens they need, expected data size, and connectivity patterns such as field versus office use.

**Parent Topic:**[Considerations before implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/imp-considerations.md)

