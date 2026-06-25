---
title: General guidelines for handling cache downloads
description: When working with cache downloads keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/offline-cache-general-guidelines.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for handling cache downloads

When working with cache downloads keep these general guidelines in mind for usability and a good user experience.

-   **Cache payload generation and downloaded time limits**
    -   Payload generation time limit: Define the time limit, between 0 to 20 minutes using the parameter `glide.sg.offline.job.maxRuntime`. The default is 10 minutes.
    -   Download time limit: Download time is not controlled by the application but is governed by standard OS and network HTTP timeouts at the device, browser, or infrastructure level.
-   **Payload size limits**
    -   Payload size is unlimited, except for a maximum total size limit on attachments, where a maximum total size can be configured by the admin. For more information, see, [Attachment behavior in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-attachment-behavior.md).
    -   Where possible, keep the offline dataset as a subset of the online data to facilitate faster download times and improved device performance.
-   **Download cache option in the Settings menu**

    When users tap the **Download cache** option in the **Offline** area of the **Settings** menu, the device begins downloading the latest data defined for offline use. A banner indicates that the download is in progress, and the app remains usable throughout. Once complete, offline mode is not enabled automatically. Users must select the option in the **Offline** settings.

    While in offline mode, note the following behavior:

    -   Changes made to cached records are logged in the Outbox.
    -   Once reconnected, tap **Go Online and Sync** to push the changes to the instance.
    -   The local cache then updates to reflect the synced changes.
-   **Enabling background downloading for users**

    Two system properties control whether the Background downloading option appears in the mobile app's Offline settings:

    -   `glide.sg.offline.scheduled_download.enabled`: This is the admin switch for the scheduled downloads feature, which rebuilds the cache at a set time, such as overnight.
    -   `glide.sg.offline.incremental.enabled`: This is the admin switch for the incremental updates feature, which refreshes the cache in small deltas while the app is open.
    Both default to false. The option appears in the app when at least one of these properties are set to true.

    **Note:** Enabling either property does not automatically enroll users. Each user must enable Background downloading in their Offline settings.

-   **Understand how the offline cache updates while online**

    Once the cache has been downloaded \(either through a manual download, scheduled job, or incremental sync\), the app continuously updates it while you're online, regardless of how the initial download was triggered. This means the most current data is available if connectivity is later lost.


**Parent Topic:**[Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-cache.md)

