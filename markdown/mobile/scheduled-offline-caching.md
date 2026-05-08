---
title: Scheduled offline caching
description: Configure offline caching so your field technicians can receive scheduled updates to their offline data cache. Scheduled downloads are based on the user's work schedule.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Scheduled offline caching

Configure offline caching so your field technicians can receive scheduled updates to their offline data cache. Scheduled downloads are based on the user's work schedule.

## Activate the Agent Schedule plugin

To enable and configure scheduled offline caching, the Agent Schedule plugin \[com.snc.agent\_schedule\] must be activated. For details on plugin activation, see Activate a plugin.

## Create work schedules for offline caching

For mobile clients other than Mobile Agent, ensure that an entry in Offline download schedule \(sys\_sg\_offline\_download\_schedule\) exists for the client type, for example, Request. This entry specifies the table that has the offline download schedules for the agents or technicians. Mobile uses the schedule from this table for scheduling offline cache generation. To populate schedules for each user, a scheduler script can be used like in Field Service Mobile.

For Mobile Agent, the entry is created when the plugin is activated. After activating the plugin, you must create work schedules for the agents or technicians to enable users to automatically receive scheduled offline caches. This can be done directly through the Agent Work Schedules \[agent\_work\_schedule\] table. For more information on how to create schedules through this table, see Create a work schedule for an agent or technician.

Based on the records from the Agent Work Schedules table, your instance runs background scheduled jobs that create schedules in the Agent Daily Schedules \[agent\_daily\_schedule\] table. Within these schedules, agents will receive a silent push sometime throughout their scheduled day.

The offline payloads that your instance generates are based on the times recorded in the Agent Daily Schedules. These can be found in the Events \[sysevent\] table. Use the records in the Event table to track these payloads, and info about when they are created and when they are sent to the agents.

## Scheduled Jobs associated with offline caching

These scheduled jobs are automatically scheduled for only users who enable background downloading on their app. For information on how users can enable this feature, see [Offline mode for mobile](offline-end-user.md).

-   **Populate Agents Daily Schedule Table**

    This job runs once daily for all users with background downloading set to **true**.

-   **Scheduled Download of Offline Payload**

    This job creates an event for the first payload of the day in the \[mobile\_offline\_payload\_gen\_queue\] table.


## Offline scheduling system properties

Use the following properties on the System Properties \[sys\_properties\] table to configure scheduled offline caching.

<table id="table_dtt_lgn_1mb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.sg.offline.scheduled\_download.enabled

</td><td>

Enables scheduled downloading for all Mobile Agent app users.

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.cachesync\_offset

</td><td>

Determines when your instance starts payload generation prior to schedule. Value determines how many minutes before the user schedule payload generation begins.**Note:** Be sure not to set the value of this property earlier than your Mobile Offline Scheduling job is runs. Doing so will prevent offline payloads from being generated.

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.reminder\_offset

</td><td>

Determines when your instance sends your users a daily reminder to manually download a cache. The instance sends this reminder only when there is no cache or the cache is expired. Value determines how many minutes before a user schedule your instance sends this reminder.

</td></tr><tr><td>

glide.sg.offline\_payload.refresh\_frequency

</td><td>

Determines **refreshTimestamp** frequency of payloads. Value represents this frequency in minutes The default value is 480.

</td></tr><tr><td>

glide.sg.offline.attachment.max\_total\_bytes

</td><td>

Determines the maximum size allocated for all attachments in a cache. Value is represented in Megabytes \(MB\). The maximum value is 2048 MB.

</td></tr></tbody>
</table>For information on more offline related system properties, see, [Configure offline mode behavior](../task/sg-configure-offline-mode.md).

**Parent Topic:**[Offline mode](mobile-offline-mode.md)

