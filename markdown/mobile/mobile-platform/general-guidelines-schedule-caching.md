---
title: General guidelines for scheduling offline caching
description: When scheduling offline caches keep these general guidelines in mind for usability and a good user experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/general-guidelines-schedule-caching.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Configure scheduled offline caching, Scheduled offline caching, Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# General guidelines for scheduling offline caching

When scheduling offline caches keep these general guidelines in mind for usability and a good user experience.

-   **Understand scheduled jobs for offline data refresh**

    A scheduled job automatically refreshes offline data on the device at predefined intervals, such as before the start of a shift

-   **Enable scheduled cache downloads**

    Enable scheduled cache downloads using `glide.sg.offline.scheduled_download.enabled`. Once enabled, configure the following properties.

    -   `glide.sg.offline.scheduled_download.cachesync_offset`: Start preparing data a defined number of minutes before a shift.
    -   `glide.sg.offline.scheduled_download.reminder_offset`: Send users a reminder to download the cache if it has expired.
    These settings verify that users begin their shift with current offline data, even in low-connectivity areas.

    **Note:** After scheduled download is enabled, the user must opt in by selecting the **Background downloading** option in the **Offline settings** on their device.

-   **Configure scheduled job frequency**

    Scheduled jobs can run at any interval configured by the admin, such as hourly or daily. There is no built-in default interval. Consider scheduling jobs to run once per day, as shorter intervals may negatively impact instance performance.

-   **Background refresh behavior**

    Data refreshes automatically without user intervention, provided the device has connectivity.

-   **Scheduled job behavior when offline**

    If the device is offline during a scheduled job, the job is skipped and runs the next time the device has connectivity.

-   **Customize scheduled jobs by user role**

    Scheduled jobs can be tailored to specific user roles or groups by the admin.

-   **User-initiated sync options**

    Scheduled jobs can't be triggered manually by users, but users can run a manual sync at any time.

-   **Scheduled job failure behavior**

    If a scheduled job fails, the app retries at the next scheduled interval. Users can run a manual sync if an immediate update is needed.

-   **Benefits of scheduled jobs over manual syncs**

    Scheduled jobs keep offline data consistently current without relying on user action, allowing users to focus on their work with the latest data available when needed.

-   **Control cache refresh frequency**

    Set `glide.sg.offline_payload.refresh_frequency` to define how often cached records are refreshed with the latest scheduled job payload, helping users verify that they don't see outdated data. If not configured, the cache refreshes every 8 hours, provided the user has an existing cache, a scheduled job is set up, and the user remains logged in.

    Use this property to balance data currency with bandwidth, where shorter intervals provide more current data and longer intervals reduce network usage.


**Parent Topic:**[Configure scheduled offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/scheduled-offline-caching.md)

