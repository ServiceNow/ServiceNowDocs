---
title: Geolocation history
description: The Geolocation History \[geo\_history\] table contains the history of each tracked user's location over time.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Geolocation, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Geolocation history

The Geolocation History \[geo\_history\] table contains the history of each tracked user's location over time.

To view geolocation history, navigate to **Geolocation** &gt; **Geolocation History**. The record list shows time stamped location data for all users configured for geolocation tracking.

The following system properties, located in **Geolocation** &gt; **Administration** &gt; **Geolocation Properties**, control the data that appears in this table.

-   Minimum distance an agent must move to be considered in a new location \(in meters\): Perimeter that defines a single location in which multiple tasks are present. This property prevents the system from creating unnecessary history records when multiple tasks are in the same general location.

    **Note:** A user's geo\_history will not be logged if the user remained at approximately the same location, even if this property is set to 0.

-   Maximum distance an agent can be from a specific location and still be placed at that location \(in meters\): Distance that a user can be from a specified location and still be placed at that location when the system creates history data.
-   Number of days to keep history data: Time period for which the system retains history data.
-   Minimum amount of time between updating the user's location \(in seconds\): Time period the system waits before updating a user's location, regardless of how often the user accesses tasks.

**Parent Topic:**[Geolocation](../concept/c_Geolocation.md)

