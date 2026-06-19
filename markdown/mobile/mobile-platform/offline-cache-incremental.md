---
title: Incremental offline caching
description: Incremental offline synchronization downloads only the changes to records, rather than the full dataset. This approach keeps offline data current while reducing network and battery usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/offline-cache-incremental.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Incremental offline caching

Incremental offline synchronization downloads only the changes to records, rather than the full dataset. This approach keeps offline data current while reducing network and battery usage.

Instead of downloading a full dataset, incremental offline synchronization only changes records that are retrieved, including any additions, updates, and deletions. The system tracks changes only in the specific records defined by the admin through data items, so the device receives targeted updates rather than a full download. This method keeps the offline cache consistent without placing unnecessary load on the network or device.

This method periodically compares the data on your instance with the data cached on the mobile device. When a difference is detected, only the changed records are downloaded, removing the need for users to manually update the entire cache or follow a fixed schedule. This makes incremental sync particularly useful in environments where users frequently or unexpectedly lose network connectivity.

After you enable the incremental updates feature, the user must turn on Background downloading on their device to begin receiving updates. Once enabled, a “Background downloading” section appears under the app’s Offline settings. The user can decide to Enable Wi-Fi only, if they prefer downloads to occur when connected to a Wi-Fi network.

\[Omitted image "mobile-enable-offline.png"\] Alt text: Background downloading option enabled in the Download cache page

The following system properties are available when managing incremental offline caching.

|Property|Description|
|--------|-----------|
|glide.sg.ofﬂine.incremental.enabled|Enable the incremental ofﬂine update option for all users.|
|glide.sg.ofﬂine.incremental.client\_polling\_interval|Defines the interval at which the polling mechanism checks the server for missed changes.|
|glide.sg.ofﬂine.incremental.record\_watcher\_expiration|Specifies how long the record watcher remains active when no changes have occurred to trigger an incremental update.|
|glide.sg.ofﬂine.incremental.silent\_push.max\_pushes\_per\_hour|The number of incremental updates a user can receive in an hour.|
|glide.sg.ofﬂine.incremental.silent\_push.min\_wait\_time|Specifies the minimum interval between consecutive incremental updates sent to the user’s device.|
|glide.sg.offline.job.maxRuntime|Controls how long the server can spend generating the offline cache payload for a user.|

For information on other related offline system properties, see [System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md).

-   **[General guidelines for incremental ofﬂine caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/general-guidelines-increment-offline-cache.md)**  
When working with incremental offline caching keep these general guidelines in mind for usability and a good user experience.

**Parent Topic:**[Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-cache.md)

