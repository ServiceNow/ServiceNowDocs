---
title: Schedule blackout periods
description: A blackout period prevents work from being performed in a defined area for a scheduled time period. Blackout periods can be defined for spaces, levels, buildings, campuses, and zones.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Facilities requests, Facilities service management process, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Schedule blackout periods

A blackout period prevents work from being performed in a defined area for a scheduled time period. Blackout periods can be defined for spaces, levels, buildings, campuses, and zones.

Blackout business rules check the **Schedules** field of the **Location** field on a request or task to assess if there are any schedule conflicts with the time span of current.expected\_start to current.estimated\_end.

|Business rule|Action|
|-------------|------|
|Display Space Schedule Conflicts \(facilities\_request business rule\)|If the current.expected\_start and current.estimated\_end are populated and the location is a facilities space, informs the user of any possible schedule conflicts.|
|Display Space Schedule Conflicts \(facilities\_request\_task business rule\)|If the current.expected\_start and current.estimated\_end are populated and the location is a facilities space, informs the user of any possible schedule conflicts.|
|Prevent Space Schedule Conflicts \(facilities\_request\_task business rule\)|If there are any possible schedule conflicts between `now` and `now + estimated_work_duration`, prevent the user from starting work. To override, a facilities\_admin can use a field override\_schedule\_conflict|

-   **[Create a facilities schedule blackout](../task/t_CreateFacScheduleBlackout.md)**  
Blackout periods can be defined for spaces, levels, buildings, campuses, and zones. The Facilities\_admin can override blackout period requests.

**Parent Topic:**[Facilities requests](c_FacilitiesRequests.md)

