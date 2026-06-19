---
title: System properties in offline mode
description: Use the table to view system properties related to offline mode.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/mobile-system-properties.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: reference
last_updated: "2026-06-08"
reading_time_minutes: 6
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# System properties in offline mode

Use the table to view system properties related to offline mode.

This page lists all system properties related to offline mode. Refer to the individual offline mode topics to learn how each property influences different aspects of the offline experience and how they can be used to customize user behavior and performance.

## Create system properties to customize the ofﬂine mode behavior of the mobile application

**Note:** Install or request installation of the SG Ofﬂine support plugin \(com.glide.sg.ofﬂine\).

1.  Navigate to **All** &gt; **sys\_properties.list**
2.  Verify that the property does not exist by searching for the property name in the System Properties table.
3.  Select **New**.
4.  Complete the System Property form using the property names listed in this table. Use the information in the description to determine a value for the property.

**Note:** For more information on creating system properties, see [Mobile system property configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/additional-mobile-configuration.md).

## System properties used for offline configuration

<table id="table_wdj_211_4jc"><thead><tr><th>

Topic

</th><th>

Sub topic

</th><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activation and deactivation of offline mode

</td><td>

Deactivation

</td><td>

`glide.sg.offline.enabled`

</td><td>

Offline mode is enabled by default. To disable offline mode, create a system property with this name and set the value to false.

</td></tr><tr><td>

Control what data is available in offline

</td><td>

Attachments

</td><td>

`glide.sg.offline.attachment.allowed_content_types`

</td><td>

A comma-separated list of allowed file types for attachments in offline mode.Configuration:

-   Property Type: String
-   Default value: image/png, image/gif, image/jpeg, video/QuickTime

**Note:** The expected value must be a listed MIME type.


</td></tr><tr><td>

Control what data is available in offline

</td><td>

Attachments in offline

</td><td>

`glide.sg.offline.attachment.max_size`

</td><td>

Sets the maximum file size in bytes for attachments downloaded into the offline cache. Attachments that exceed this limit aren't downloaded and display as a placeholder instead.Example: To set a limit of 20 MB, enter `20971520`.

Configuration:

-   Property Type: Integer
-   Default value: 50000 \(50 MB\)
-   Min value: 0
-   Maximum value: 1073741824 \(1 GB\)

</td></tr><tr><td>

Control what data is available in offline

</td><td>

Attachments in offline

</td><td>

`glide.sg.offline.attachment.max_total_bytes`

</td><td>

Defines the total amount of storage the offline cache can use for attachments in bytes.Example: To set a total limit of 100 MB, enter `104857600`.

Configuration:

-   Property Type: Integer
-   Default value: `52428800` \(50 MB\)
-   Min value: 0
-   Maximum value: 2147482548 \(2 GB\)

</td></tr><tr><td>

Security &amp; compliance

</td><td>

Security

</td><td>

`glide.sg.offline.roles`

</td><td>

A comma-separated list of role names that are allowed to work in offline mode. If empty, all users may use offline mode.

</td></tr><tr><td>

Security &amp; compliance

</td><td>

Security

</td><td>

`glide.sg.offline.expiration`

</td><td>

Defines how long offline cached data remains valid on the device before expiring and being automatically deleted in accordance with security policies. Defaults to 48 hours \(2 days\).

 Default value: 172800 \(The property value is in seconds\).

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Incremental updates

</td><td>

`glide.sg.offline.incremental.enabled`

</td><td>

Enables incremental offline updates for all users. Incremental offline is inactive by default.

 Configuration:

-   Property Type: true \| false
-   Default value: false

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Incremental updates

</td><td>

`glide.sg.offline.incremental.client_polling_interval`

</td><td>

Defines the interval at which the polling mechanism checks the server for missed changes.

 Mobile devices can lose connectivity or enter operating system-level sleep modes that block background network activity, causing watcher events to be missed. When the app returns online or is set to active, the polling mechanism asks the server whether any records have changed since the last successful incremental sync, and if so, triggers an incremental update. This acts as a fallback to verify the device catches up with any updates missed while offline or asleep.

 Configuration:

-   Property type: Integer
-   Property value: Duration in minutes
-   Default value: 1
-   Min value: 0

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Incremental updates

</td><td>

`glide.sg.offline.incremental.record_watcher_expiration`

</td><td>

**Note:** This setting is applicable only when the `glide.sg.offline.incremental.enabled` system property is set to true.

 Screens that are marked as available offline are linked to specific data items that determine which records are included for that screen. These records are continuously monitored by a record watcher, which tracks any insert, update, or delete actions. When a change matches the data item filter criteria, the watcher automatically initiates an incremental update to sync the latest data to the user's device.

 This property specifies how long the record watcher remains active when no changes have occurred to trigger an incremental update.

 Configuration:

-   Property Type: Integer
-   Default value: 24 hours

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Incremental updates

</td><td>

`glide.sg.offline.incremental.silent_push.max_pushes_per_hour`

</td><td>

**Note:** This property specifies how long the defined record watcher remains active when no changes have occurred to trigger an incremental update.

The number of incremental updates a user can receive in an hour. If more updates occur than this limit allows, the extra changes are deferred to the next hour.This property works alongside `glide.sg.offline.incremental.silent_push.min_wait_time` \(default: 1 minute\), which enforces a minimum gap between consecutive pushes regardless of the hourly count.

Configuration:

-   Property Type: Integer
-   Default value: 3
-   Maximum value: 10

</td></tr><tr><td>

When data is downloaded for offline usage

</td><td>

Incremental updates

</td><td>

`glide.sg.offline.incremental.silent_push.min_wait_time`

</td><td>

**Note:** This setting is applicable only when the `glide.sg.offline.incremental.enabled` system property is set to `true`.

Specifies the minimum interval, in minutes, between consecutive incremental updates sent to the user's device. Even if new updates are available, the app waits for the defined duration before sending the next update.Configuration:

-   Property Type: Integer
-   Default value: 1
-   Min value: 1
-   Maximum value: 1440

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Scheduled jobs

</td><td>

`glide.sg.offline.scheduled_download.enabled`

</td><td>

Enables scheduled downloading for all mobile app users. Scheduled downloading is inactive by default.Configuration:

-   True \| False
-   Default value: false

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Scheduled jobs

</td><td>

`glide.sg.offline.scheduled_download.cachesync_offset`

</td><td>

Defines the number of minutes before the user's scheduled time that offline payload generation begins. This value offsets the start of generation ahead of the agent's schedule.Example: If the agent schedule is set to 10:00 and `glide.sg.offline.scheduled_download.cachesync_offset` is configured to 30 minutes, offline cache generation starts at 09:30.

Configuration:

-   Property Type: Integer
-   Default value: 60

**Note:** This property should not be set to start earlier than the mobile offline scheduling job run time. Setting it earlier than the job execution prevents offline payloads from being generated.

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Scheduled jobs

</td><td>

`glide.sg.offline.scheduled_download.reminder_offset`

</td><td>

Define how many minutes before the user's scheduled time the download reminder is sent. The reminder appears only when no cache exists or the existing cache has expired.The following two properties work together. This property \(default: 15 minutes\) defines how early the mobile app prompts the agent to download, while glide.sg.offline.scheduled\_download.cachesync\_offset \(default: 60 minutes\) defines how early the server pre-builds the cache.

Configuration:

-   Property Type: Integer
-   Default value: 15

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Scheduled jobs

</td><td>

`glide.sg.offline_payload.refresh_frequency`

</td><td>

Defines a fixed interval between the initial scheduled cache download and when the cache should be refreshed. This allows the device to automatically update its cache at a predictable time, ensuring it stays current when connectivity is available. For example, a device can be configured to refresh its cache during a lunch break, so the cache is already current when work resumes. Example: If the agent's schedule runs daily at 10:00 and the refresh interval is set to 240 \(4 hours\), the cache refreshes automatically at 14:00, provided the device has connectivity at that time.

Configuration:

-   Property Type: Integer
-   Default value: 480 minutes \(8 hours\)

</td></tr><tr><td>

Control when data is being downloaded for offline usage

</td><td>

Manual download / Scheduled jobs / Incremental updates

</td><td>

`glide.sg.offline.job.maxRuntime`

</td><td>

Controls how long the server can spend generating the offline cache payload for a user. If the download does not complete, the user sees an error rather than receiving incomplete or partial data. This applies to both scheduled job and manual downloads.Configuration:

-   Property Type: Integer
-   Default value: 600000 ms \(10 minutes\)
-   Minimum allowed: 5000 ms \(5 seconds\)
-   Maximum allowed: 1200000 ms \(20 minutes\)

</td></tr></tbody>
</table>**Parent Topic:**[Offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-offline-mode.md)

