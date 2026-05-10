---
title: Installed with geolocation
description: Several component types are installed with Geolocation.Business rules are added with activation of Geolocation.Client scripts are added with activation of Geolocation.Geolocation provides the following configurable properties in Geolocation Administration Geolocation Properties .Script includes are added with activation of Geolocation.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Geolocation, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with geolocation

Several component types are installed with Geolocation.

The Geolocation plugin adds a field called [Geolocation tracked](r_InstalledWithGeolocation.md#) to the User `[sys_user]` table. This field allows the system to track individual users by their geographical coordinates.

**Parent Topic:**[Geolocation](../concept/c_Geolocation.md)

## Business rules installed with geolocation

Business rules are added with activation of Geolocation.

<table id="table_r1z_x2p_pp"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GeoLocation Data updated

</td><td>

User \[sys\_user\]

</td><td>

Populates the **Latitude** and **Longitude** fields on the Geolocation History \[geo\_history\] table when the **Latitude** and **Longitude** fields are updated on the User \[sys\_user\] table.

</td></tr></tbody>
</table>**Related topics**  


[Installed with geolocation](r_InstalledWithGeolocation.md#)

## Client scripts installed with geolocation

Client scripts are added with activation of Geolocation.

<table id="table_c1f_j2p_pp"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Update Geolocation on Task

</td><td>

Task \[task\]

</td><td>

Populates the **Latitude** and **Longitude** fields on a user record with GPS coordinates when that user loads any record on the Task table or a table that extends Task. This occurs only when geolocation tracking is enabled for the user.

</td></tr></tbody>
</table>**Related topics**  


[Installed with geolocation](r_InstalledWithGeolocation.md#)

## Properties installed with geolocation

Geolocation provides the following configurable properties in **Geolocation** &gt; **Administration** &gt; **Geolocation Properties**.

The Google Maps plugin provides additional [map properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/set-up-google-maps-api.md) that are used to implement and control specific geolocation features. You must have a [private key](r_GeolocationGoogleKey.md) for Google Maps API for Business to take advantage of the properties listed here.

<table id="table_n35_gbp_pp"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.geolocation.allow.toll.roads

</td><td>

Allow toll roads to be used. Allows the system to use toll roads when auto-routing or optimizing task routes for agents.-   **Type**: True/false
-   **Default value**: True

</td></tr><tr><td>

glide.geolocation.default.start.time

</td><td>

Default start time for all agents when no schedule is set. This value sets the start time for a day other than the current day, when no scheduled task exists or is continued from the previous day. This property uses a 24 hour clock.-   **Type**: String
-   **Default value**: 08:00

</td></tr><tr><td>

glide.geolocation.evening.rush.hours

</td><td>

Evening rush hour span, formatted as 14:30-16:00. All times are expressed as a range, separated by a dash with no spaces. Times not using this format are ignored. This property must be used with the work.management.morning.rush.hours and work.management.rush.travel.buffer properties and uses a 24 hour clock.-   **Type**: String
-   **Default value**: 0

</td></tr><tr><td>

glide.geolocation.history.cleanup

</td><td>

Number of days to keep history data. ServiceNow keeps agent geolocation history records for the number of days specified by this value.-   **Type**: Integer
-   **Default value**: 30

</td></tr><tr><td>

glide.geolocation.morning.rush.hours

</td><td>

Morning rush hour span, formatted as 06:30-08:00. This property uses a 24 hour clock. All times are expressed as a range, separated by a dash with no spaces. Times not using this format are ignored. This property must be used with the work.management.evening.rush.hours and work.management.rush.travel.buffer properties.-   **Type**: String
-   **Default value**: 0

</td></tr><tr><td>

glide.geolocation.proximity

</td><td>

Minimum distance an agent must move to be considered in a new location \(in meters\). This setting establishes a geolocation perimeter that prevents ServiceNow from creating unnecessary history records when an agent has multiple tasks in the same vicinity. An example of this might be when an agent has several tasks in one building. The system assumes that all task activity within the specified radius is part of a single record and does not create additional records when the agent moves from task to task around the building.-   **Type**: Integer
-   **Default value**: 500

For an explanation of how location tracking works, using both the frequency and criteria properties, see the section How location tracking works, at the end of the table.

**Note:** The iOS version of the app updates geolocation only when the mobile device detects a significant location change, which is determined by the your device's operating system. When the operating system updates its location, your app updates with that location change. Distance and time property values are not honored for the iOS version of ServiceNow apps.

</td></tr><tr><td>

glide.geolocation.proximity.location

</td><td>

Maximum distance an agent can be from a specific location and still be placed at that location \(in meters\). This setting defines the maximum distance that an agent can be from a specified location and still be placed at that location by the system.-   **Type**: Integer
-   **Default value**: 200

For an explanation of how location tracking works, using both the frequency and criteria properties, see the section How location tracking works, at the end of the table.

</td></tr><tr><td>

glide.geolocation.rush.travel.buffer

</td><td>

Percentage to add to all rush hour travel times. The system uses this percentage to calculate schedules when auto-routing an agent. Use this property when both morning and evening rush hour times are defined. An example of a valid time buffer percentage is 15.-   **Type**: Integer
-   **Default value**: 0

</td></tr><tr><td>

glide.geolocation.tracking.frequency

</td><td>

Sets the length of the recurring interval, in seconds, that the system waits between attempts to capture a user's geographic coordinates. The system updates geographic coordinates only for users who have geolocation tracking enabled.The property **glide.geolocation.tracking.frequency** defines how long the system waits before updating an agent's location, regardless of task activity or travel. This prevents the ServiceNow AI Platform from creating unnecessary history records if an agent in one location views a task multiple times.

-   **Type**: Integer
-   **Default value**: 60

For an explanation of how location tracking works, using both the frequency and criteria properties, see the section How location tracking works, at the end of the table.

-   **iOS variations**

The iOS version of the app uses both proximity and frequency settings when updating geolocation.

    -   Proximity: A new location is only saved if its distance to the previous location exceeds the configured threshold \(in meters\). This leverages the native iOS distanceFilter functionality.
    -   Frequency: A new location is only saved if its timestamp is later than the previous known location's timestamp by the configured interval \(in minutes\). In iOS, frequency is recorded as the minimum interval to track location updates.
-   **Android variation**

The Android version of the app updates geolocation data at 1 minute intervals. The app collects a user's location using the interval set in this property, but that data is still uploaded to your instance every 1 minute. This interval at which data is sent to the server \(every minute\) is not configurable.

**Note:** Default proximity and frequency values differ based on the tracking type:

    -   Manual tracking
        -   Frequency: 1 minute
        -   Proximity: 100 meters
    -   Action-based tracking
        -   Frequency: 5 minutes
        -   Proximity: 500 meters

</td></tr><tr><td>

glide.geolocation.travel.buffer

</td><td>

Percentage to add to all travel times. An example of a valid percentage value is 15.-   **Type**: Integer
-   **Default value**: 0

</td></tr><tr><td>

glide.geolocation.work.spacing

</td><td>

Amount of time \(in minutes\) to add between the end of a task and the travel start of the next. An example of a valid time value is 10.-   **Type**: Integer
-   **Default value**: 0

</td></tr></tbody>
</table>-   **How location tracking works**

    The location service captures new coordinates based on the configured tracking frequency and stores them in a local table. A separate service then sends all stored coordinates from the local table and send them to the server.

    To determine whether to record a new location update, the system uses both frequency and proximity criteria. When the frequency interval is reached, the location service attempts to capture a new coordinate and automatically compares it with the previous location coordinate. If the difference is less than the configured proximity threshold, the coordinate is discarded and the service checks again after the specified frequency interval.

    For example, if the frequency is set to 5 minutes and the proximity threshold is 50 meters, the service attempts to capture a coordinate every 5 minutes. However, if the new coordinate is within 50 meters of the previous one, it is discarded.


## Script includes installed with geolocation

Script includes are added with activation of Geolocation.

|Name|Description|
|----|-----------|
|GeolocationAJAX|Utilities the system uses when making geolocation AJAX calls.|
|GeolocationUtils|Core utilities for geolocation functionality.|

**Related topics**  


[Installed with geolocation](r_InstalledWithGeolocation.md#)

