---
title: Configure scheduled offline caching
description: Configure offline caching so your field technicians can receive scheduled updates to their offline data cache. Scheduled downloads are based on the user's work schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/mobile-platform/scheduled-offline-caching.html
release: australia
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2026-06-09"
reading_time_minutes: 2
breadcrumb: [Scheduled offline caching, Configure offline cache to devices, Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure scheduled offline caching

Configure offline caching so your field technicians can receive scheduled updates to their offline data cache. Scheduled downloads are based on the user's work schedule.

## Activate the Agent Schedule plugin

To enable and configure scheduled offline caching, the Agent Schedule plugin \[com.snc.agent\_schedule\] must be activated. For details on plugin activation, see Activate a plugin.

## Create work schedules for offline caching

For mobile clients other than Mobile Agent, verify that an entry in offline download schedule \(sys\_sg\_offline\_download\_schedule\) exists for the client type, for example, Request. This entry specifies the table that has the offline download schedules for the agents or technicians. Mobile uses the schedule from this table for scheduling offline cache generation. To populate schedules for each user, a scheduler script can be used like in Field Service Mobile.

For the Mobile Agent app, the entry is created when the plugin is activated. After activating the plugin, you must create work schedules for the agents or technicians to enable users to automatically receive scheduled offline caches. This can be done directly through the Agent Work Schedules \[agent\_work\_schedule\] table. For more information on how to create schedules through this table, see Create a work schedule for an agent or technician.

Based on the records from the Agent Work Schedules table, your instance runs background scheduled jobs that create schedules in the Agent Daily Schedules \[agent\_daily\_schedule\] table. Within these schedules, agents will receive a silent push sometime throughout their scheduled day.

The offline payloads that your instance generates are based on the times recorded in the Agent Daily Schedules. These can be found in the Events \[sysevent\] table. Use the records in the Event table to track these payloads, and info about when they are created and when they are sent to the agents.

## Scheduled Jobs associated with offline caching

These scheduled jobs are automatically scheduled for only users who enable background downloading on their app. For information on how users can enable this feature, see [Offline mode for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-end-user.md).

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

Defines the number of minutes before the user's scheduled time that the instance begins generating the offline payload.

</td></tr><tr><td>

glide.sg.offline.scheduled\_download.reminder\_offset

</td><td>

Define the number of minutes before the user's scheduled offline time that a reminder is sent to download the cache manually.

</td></tr><tr><td>

glide.sg.offline\_payload.refresh\_frequency

</td><td>

Define a fixed interval between the initial scheduled cache download and when the cache should be refreshed.

</td></tr><tr><td>

glide.sg.offline.attachment.max\_total\_bytes

</td><td>

Defines the total amount of storage the offline cache can use for attachments in bytes.

</td></tr></tbody>
</table>For information on other related offline system properties, see [System properties in offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/mobile-system-properties.md).

-   **[General guidelines for scheduling offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/general-guidelines-schedule-caching.md)**  
When scheduling offline caches keep these general guidelines in mind for usability and a good user experience.

**Parent Topic:**[Scheduled offline caching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/mobile-platform/offline-caching-scheduled.md)

