---
title: General guidelines for incremental ofﬂine caching
description: When working with incremental offline caching keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/general-guidelines-increment-offline-cache.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Incremental offline caching, Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for incremental ofﬂine caching

When working with incremental offline caching keep these general guidelines in mind for usability and a good user experience.

-   **Enable incremental sync for offline mode**

    Incremental synchronization allows the mobile app to fetch only the changes since the last sync, such as new, updated, or deleted records, without requiring a full cache refresh. Incremental updates are disabled by default and can be enabled by setting the following system property: `glide.sg.offline.incremental.enabled = true`.

    For large datasets, this saves time and reduces bandwidth. For example, if 500 incidents are cached and only 5 changes during the day, incremental sync delivers just those 5 updates rather than re-downloading all 500 incidents.

    **Note:** After a scheduled download is enabled, the user must opt in by turning on the Background downloading toggle in the Offline settings on their device.

-   **Understand the background downloading setting**

    Once an administrator enables incremental updates, a **Background downloading** section displays in the offline settings. Users must select this option to retrieve incremental updates silently in the background and keep the offline cache refreshed with the latest changes from the instance.

-   **Understand incremental sync frequency and limitations**

    Incremental sync uses silent push notifications to keep offline data updated. Two system properties control how frequently updates are delivered.

    |System property|Description|
    |---------------|-----------|
    |`glide.sg.offline.incremental.silent_push.max_pushes_per_hour`|Sets the maximum number of silent pushes a user can receive per hour. If more updates occur than this limit allows, the extra changes are deferred to the next hour.|
    |`glide.sg.offline.incremental.silent_push.min_wait_time`|Defines the minimum number of minutes between consecutive pushes. The app does not send another push until this wait time has passed, even if updates are ready.|

    During periods of frequent changes, users may experience slight delays in receiving the latest data, as the system balances sync responsiveness with device and network performance. For example, if `max_pushes_per_hour` is set to `10` and `min_wait_time` is set to `6` minutes:

    -   The earliest the system can deliver all 10 pushes is over 60 minutes.
    -   Any updates beyond 10 in that hour are deferred to the next hour.
    -   If changes occur in quick succession, the push schedule follows the minimum wait constraint, even if fewer than the maximum pushes have been used.

**Parent Topic:**[Incremental offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-cache-incremental.md)

