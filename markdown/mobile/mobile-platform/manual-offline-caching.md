---
title: Manual offline caching
description: Users can manually download or refresh the offline cache at any time. This option gives users control over when their device data is updated, before working without connectivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/manual-offline-caching.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Manual offline caching

Users can manually download or refresh the offline cache at any time. This option gives users control over when their device data is updated, before working without connectivity.

The manual download option allows users to initiate or refresh the offline cache directly from their device. This is particularly useful when users know in advance that they will be working in an area without network connectivity and want to prepare their device with the latest available data.

## General guideline

Manual cache downloads should not be used regularly by the user, as frequent downloads can place unnecessary load on the server. Consider setting up scheduled and incremental updates that align with your users' workflows.

## User performance of manual caching

<table id="table_kmz_klf_njc"><thead><tr><th>

Description of process

</th><th>

Mobile screen view

</th></tr></thead><tbody><tr><td>

-   **Initial download**

The Download Cache option initiates a full on-demand download of the offline cache. Use this option when no cache exists on the device. When selected, the mobile app:

    -   Downloads all data and resources configured for offline use.
    -   Stores the data securely on the device for use without connectivity.
    -   Displays a progress indicator while downloading. The mobile app can still be used at this time.
    -   Does not affect existing local drafts, saved forms, or outbox items.

</td><td>

\[Omitted image "mobile-enable-offline.png"\] Alt text: Download cache option displayed

</td></tr><tr><td>

-   **Update cache**

Once an offline cache already exists, the Update Cache option allows users to refresh the data manually. Use this option to update cached content with the latest data from the ServiceNow instance.


</td><td>

\[Omitted image "mobile-offline-cache-button.png"\] Alt text: Option to update cache or to clear cache

</td></tr></tbody>
</table>**Parent Topic:**[Configure offline cache downloads to user devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-cache.md)

