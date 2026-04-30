---
title: Offline mode
description: Configure offline mode to enable your users who have no internet connection to continue working from a mobile device.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Offline mode

Configure offline mode to enable your users who have no internet connection to continue working from a mobile device.

Video showing how offline mode works in the ServiceNow Agent mobile app.This video shows how offline mode works in Mobile Agent.

Configure specific applications, screens, or functions for users to use offline in your mobile apps. For a description of how offline mode features enhance end users' experience, see [Offline mode for mobile](offline-end-user.md).

## Supported screens in offline mode

Offline mode is supported in the following screens. For more information about screen types in mobile, see [Mobile screen types](sg-mobile-applet.md).

-   Input form screen
-   Calendar screen
-   Sections screen
-   List screen
-   Related list screen
-   Record screen
-   Map screen
-   Details screen
-   Activity list screen

## Offline mode process

<table id="table_sqd_2l5_vnb"><tbody><tr><td>

Offline mode works by creating a cache of records on your mobile device that your users can view and update while offline. This cache is a limited set of data based on the applications your users can access. By default, this cache expires 48 hours after it is downloaded to a mobile device. This means that any changes your users make to the cache that are not synchronized to your instance within 48 hours are lost.

</td><td>

![Example screens of downloading data in Offline mode and the Download Complete success message.](../image/enable-offline.png)

</td></tr><tr><td>

While in offline mode, only parts of the app with cached data are available. For example, if you have only enabled offline mode for tasks and inventory, all other parts of your mobile app are unavailable while offline.

</td><td>

![Example screen showing only apps with cached data is displayed.](../image/offline-disabled-apps.png)

</td></tr><tr><td>

When your users have network access again, they can disable offline mode and synchronize their cached data with the data on your instance. Updates between the instance and the mobile device are automatic, unless there is a conflict. Users can resolve conflicts in their outbox.

</td><td>

![Screens showing how to synchronize data.](../image/offline-conflict.png)

</td></tr></tbody>
</table>## Incremental Offline

Incremental offline mode periodically compares the data on your instance and data cached on your mobile device. When the record watcher detects a difference, it triggers an update that contains only the changed files. Using this option, your users are not required to update the entire cache manually or according to a fixed schedule. These smaller updates are ideal in situations where users frequently or unexpectedly lose network connectivity.

-   **[Configure offline mode for mobile](../task/setup-mobile-offline.md)**  
Setup offline mode for your mobile applications so that users can work without an internet connection.
-   **[Request offline mode](../task/sg-request-work-offline.md)**  
To activate this feature, request activation of the SG Offline support plugin \(com.glide.sg.offline\).
-   **[Configure offline mode behavior](../task/sg-configure-offline-mode.md)**  
Create system properties to customize the offline mode behavior of the mobile application.
-   **[Define the number of displayed records in offline mode](../task/config-offline-record-number.md)**  
Define the number of records to display to users in offline mode. Choose between 0 through 1000 records. This range gives you the flexibility to display different amounts to the user in online and offline modes.
-   **[Configure data items in offline mode](../task/config-offline-data-item.md)**  
Define a separate data item for offline mode, giving you the flexibility to define the amount of data to display when a user is offline.
-   **[Configure offline mode properties for action functions](../task/config-offline-properties-action-funct.md)**  
Determine which fields and functions are available to users when working in offline mode.
-   **[Configure action items and action steps in offline mode](../task/configure-action-item-offline.md)**  
Configure action items to execute actions like create, edit and delete records while in offline mode. For an action item to perform multiple processes you must define separate action steps.
-   **[Register associated records in the offline cache](../task/register-assoc-records-offline-cache.md)**  
Admins can configure offline mode to include associated records in the offline cache when a user performs an action in online mode on their Mobile Agent.
-   **[Configure reference inputs for input form screens in offline mode](../task/reference-fields-offline-mode.md)**  
Configure reference inputs so that users can see a list of records in offline mode on their Mobile Agent.
-   **[Configure offline mode properties for function instances](../task/config-offline-property-function-instance.md)**  
Determine if the function instance available to users in online mode is also available in offline mode. This option gives you more control over how users manage their offline tasks.
-   **[Scheduled offline caching](scheduled-offline-caching.md)**  
Configure offline caching so your field technicians can receive scheduled updates to their offline data cache. Scheduled downloads are based on the user's work schedule.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

