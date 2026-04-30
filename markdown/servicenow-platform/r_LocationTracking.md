---
title: Location tracking
description: Geolocation adds the Geolocation tracked field to the User form. In the default view of a user record, select the Geolocation tracked check box to enable location tracking for the user.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Geolocation, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Location tracking

Geolocation adds the **Geolocation tracked** field to the User form. In the default view of a user record, select the **Geolocation tracked** check box to enable location tracking for the user.

When a user has geolocation tracking enabled, the system updates the user's geographic coordinates whenever the user opens, or loads, a record from the Task \[task\] table or from a table that extends Task. After this initial update, the system continues to update the user's geographic coordinates at a recurring interval if the user does not close or reload the record. To edit the length of this interval, navigate to **Geolocation** &gt; **Administration** &gt; **Geolocation Properties** and change the setting for the [property](r_GeolocationHistory.md) that regulates the update interval for the user's location. The default setting for this property is **300** seconds \(5 minutes\).

**Note:**

-   The system can update geographic coordinates only for users who have location services enabled in their browsers. Even users who have the **Geolocation tracked** check box selected may be prompted by their browsers to share or withhold their location.
-   A user's geo\_history will not be logged if the user remained at approximately the same location, even if the Minimum distance an agent must move to be considered in a new location \(in meters\) property is set to 0.

**Parent Topic:**[Geolocation](../concept/c_Geolocation.md)

**Related topics**  


[Geolocation](../concept/c_Geolocation.md)

