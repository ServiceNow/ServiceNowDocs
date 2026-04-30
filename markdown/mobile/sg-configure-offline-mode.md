---
title: Configure offline mode behavior
description: Create system properties to customize the offline mode behavior of the mobile application.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Offline mode, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure offline mode behavior

Create system properties to customize the offline mode behavior of the mobile application.

## Before you begin

Install or request installation of the SG Offline support plugin \(com.glide.sg.offline\).

Role required: admin

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`

2.  Verify that the property does not exist by searching for the property name in the System Properties table.

3.  Click **New**.

4.  Complete the System Property form using the property names listed in this table.

    Use the information in the description to determine a value for the property.

    **Note:** For more detail on creating system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

<table id="table_myv_c2n_vnb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.sg.offline.attachment.allowed\_content\_types

</td><td>

A comma-separated list of allowed file types for attachments in offline mode. The default list includes these types: image/png, image/jpg, image/gif, video/quicktime. The default is empty. If empty, offline mode does not download any files.

</td></tr><tr><td>

glide.sg.offline.attachment.max\_size

</td><td>

The maximum size, in bytes, for attachments that are cached while in offline mode. If no download, a placeholder displays. The default size is 50 MB.

</td></tr><tr><td>

glide.sg.offline.attachment.max\_total\_bytes

</td><td>

Maximum space allocated for all attachments in cache. Default value is 400 MB, max is 2 GB. The property value is in MB.​

</td></tr><tr><td>

glide.sg.offline.enabled

</td><td>

Enable offline capabilities on your instance. Offline mode is enabled by default. To disable offline mode, create a system property with this name and set the value to false.

</td></tr><tr><td>

glide.sg.offline.expiration

</td><td>

The length of time before cached data is expired. The default length is 48 hours. After 48 hours, the system deletes the data due to security protocol.

 The property value is in milliseconds.

</td></tr><tr><td>

glide.sg.offline.incremental.client\_polling\_interval

</td><td>

Determines minimum polling frequency. The property value is in minutes. The default value is 1, the minimum value is 0.

</td></tr><tr><td>

glide.sg.offline.incremental.enabled

</td><td>

Enable the incremental offline for all users. Incremental offline is disabled by default.

</td></tr><tr><td>

glide.sg.offline.incremental.record\_watcher\_expiration

</td><td>

Defines how long a record watcher is active but offline payload is not retrieved before it is removed. The property value is in minutes. The default value is 30.​

</td></tr><tr><td>

glide.sg.offline.incremental.silent\_push.max\_pushes\_per\_hour

</td><td>

Limits the number of silent pushes to send per 60 minutes per user. The property value is in minutes. The default value is 3. The maximum value is 10

</td></tr><tr><td>

glide.sg.offline.incremental.silent\_push.min\_wait\_time

</td><td>

Determines minimum time between silent pushes per user. The property value is in minutes. The default value is 1. The maximum value is 1440.

</td></tr><tr><td>

glide.sg.offline.roles

</td><td>

A comma-separated list of role names that are allowed to work in offline mode. If empty, all users may use offline mode.

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.cachesync\_offset

</td><td>

Number of minutes before a user's schedule to begin payload generation. The property value is in minutes.​**Note:** Be sure not to set the value of this property to a value that was less than the interval that the Mobile Offline Scheduling job is running. Doing so will prevent offline payloads from being generated.

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.enabled

</td><td>

Enable scheduled downloading for all Agent app users​

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.reminder\_offset

</td><td>

Number of minutes before a user's schedule that they receive a manual download reminder. If there is no cache or the cache is expired, offline mode sends a reminder for the user to manually download a cache. Offline mode sends this reminder once a day before the start of the users schedule.

</td></tr><tr><td>

glide.sg.offline\_payload.refresh\_frequency

</td><td>

The number of minutes before a cached record is flagged for refresh. The default is 240 minutes. The property value is in minutes.​

</td></tr></tbody>
</table>5.  Click **Submit**.


## Result

For a view of the offline mode end-user experience, see: [Working offline in mobile](../concept/offline-end-user.md).

**Parent Topic:**[Offline mode](../concept/mobile-offline-mode.md)

