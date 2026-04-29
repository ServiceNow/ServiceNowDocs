---
title: Geolocation
description: The geolocation feature uses Google Maps to track users, plan efficient routes between locations, and assist in finding accurate travel times for applications that require this information, such as Work Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Geolocation

The geolocation feature uses Google Maps to track users, plan efficient routes between locations, and assist in finding accurate travel times for applications that require this information, such as Work Management.

The system locates users from latitude and longitude information provided by their mobile devices or browsers. Tracking the location of certain users can improve business processes such as the completion of work order tasks. For example, in work management geolocation, the system updates an agent's position each time that agent updates a task record. When the system updates an agent's location frequently, agents and dispatchers can use features like auto-routing to create efficient schedules.

Geolocation features can be configured by users with the admin role.

-   **[Activate geolocation](../task/t_ActivateGeolocation.md)**  
An administrator can activate the Geolocation plugin.
-   **[Installed with geolocation](../reference/r_InstalledWithGeolocation.md#)**  
Several component types are installed with Geolocation.
-   **[Geolocation Google key](../reference/r_GeolocationGoogleKey.md)**  
Geolocation functions in the ServiceNow AI Platform® require a Google Maps API for Business license, or a Google Maps Javascript API Key, to enable use of Google Maps.
-   **[Geolocation history](../reference/r_GeolocationHistory.md)**  
The Geolocation History \[geo\_history\] table contains the history of each tracked user's location over time.
-   **[Location tracking](../reference/r_LocationTracking.md)**  
Geolocation adds the **Geolocation tracked** field to the User form. In the default view of a user record, select the **Geolocation tracked** check box to enable location tracking for the user.

**Parent Topic:**[Exploring Service Administration](../../service-administration/concept/c_ServiceAdministration.md)

**Related topics**  


[Geolocation Google key](../reference/r_GeolocationGoogleKey.md)

[Geolocation history](../reference/r_GeolocationHistory.md)

[Location tracking](../reference/r_LocationTracking.md)

[Activate geolocation](../task/t_ActivateGeolocation.md)

