---
title: Configure offline cache downloads to user devices
description: Control when and how the offline cache is refreshed on user devices to maintain relevance, performance, and bandwidth efficiency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/offline-cache.html
release: australia
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline cache downloads to user devices

Control when and how the offline cache is refreshed on user devices to maintain relevance, performance, and bandwidth efficiency.

ServiceNow mobile supports four refresh options, which can be used individually or in combination. Combine incremental updates, scheduled refreshed, triggered downloads, and manual on-demand update refreshes, for a balance of data relevance and preservation of battery life.

-   **Scheduled offline caching**

    -   Downloads data automatically at defined intervals, such as once a day at midnight.
    -   Verify devices have current data without requiring user action.
    This method provides a predictable, admin-controlled refresh cycle. For more information, see [Scheduled offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-caching-scheduled.md).

-   **Incremental automatic download**

    -   Automatically downloads only the changes since the last sync, rather than the full dataset. Changes include the addition, deletion, or updates of records.
    -   Runs in the background more frequently without heavy data loads.
    This method keeps data current with minimal bandwidth and faster syncs. For more information, see [Incremental offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache-incremental.md).

-   **Button-triggered download**

    -   Buttons can be configured to initiate a cache refresh after it is tapped. The flow is when the user taps the button, the action completes, and the app automatically updates the offline data cache.
    -   Useful in offline-first environments where stale cached data could lead to invalid operations, helping keep the offline cache current and reliable.
    This method reduces the risk of errors such as referencing outdated records by ensuring the cache is updated before the transition to offline mode. For more information, see [Cache updates triggered by user actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/cache-update-user-action.md).

-   **On-demand manual download**

    -   The user manually triggers a cache download or refresh as needed.
    -   Useful when users need control over when data is updated, for example before entering an area without connectivity.
    This method saves bandwidth by updating data only when the user chooses. For more information, see [Manual offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/manual-offline-caching.md).


-   **[General guidelines for handling cache downloads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache-general-guidelines.md)**  
When working with cache downloads keep these general guidelines in mind for usability and a good user experience.
-   **[Scheduled offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-caching-scheduled.md)**  
Schedule automatic cache downloads at defined intervals, to keep offline data current and consistent. This approach prepares users for working offline at specific times without requiring them to manually download the cache.
-   **[Incremental offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache-incremental.md)**  
Incremental offline synchronization downloads only the changes to records, rather than the full dataset. This approach keeps offline data current while reducing network and battery usage.
-   **[Cache updates triggered by user actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/cache-update-user-action.md)**  
Use action-triggered cache updates to define specific user actions that automatically refresh the offline cache in the background. This process reduces reliance on manual cache updates and helps to verify that users have current data when its needed.
-   **[Manual offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/manual-offline-caching.md)**  
Users can manually download or refresh the offline cache at any time. This option gives users control over when their device data is updated, before working without connectivity.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-setup-options.md)

