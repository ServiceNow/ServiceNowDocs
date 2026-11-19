---
title: Time zones in resource plans
description: Time zones are important in resource management when the users and groups doing the resource tasks are located in different locations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/resource-management/c\_TimeZonesInResourcePlans.html
release: yokohama
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Resource plans, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Time zones in resource plans

Time zones are important in resource management when the users and groups doing the resource tasks are located in different locations.

Users maintain their time in the [My Calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/resource-management/c_MyCalendar.md) module and resource managers use the resource workbench or resource plan to assign tasks to various users.

All users are assigned a schedule. If a user schedule changes, all time calculations change automatically. The schedules can be floating or time zone-specific.

-   A floating schedule is the same in any time zone. For example, if a resource manager in Amsterdam sets a floating schedule for 08:00–17:00, a user in San Jose sees the schedule as 08:00–17:00.

-   When a schedule is defined in a specific time zone, users in different time zones see the schedule with their own time zone applied. For example, suppose the resource manager sets a time zone-specific schedule for 08:00–17:00 in Amsterdam. The San Jose user then sees the schedule as 23:00 of the previous day to 07:00 on the current day. This is because the San Jose time zone is nine hours behind the Amsterdam time zone.

**Parent Topic:**[Resource plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/resource-management/c_ResourcePlans.md)

**Related topics**  


[Create a resource plan]()

[Use Resource Finder to analyze resource availability]()

[Create an operational resource plan]()

[Request resources]()

[Confirm a resource plan]()

[Confirm and allocate a resource plan]()

[Request a change to a resource plan]()

[Recalculate costs of a resource plan]()

[Update cost plan related to a resource plan]()

[Complete a resource plan]()

[Cancel a resource plan]()

[Delete a resource plan]()

[Extend a resource plan]()

[Request extension of an allocated resource plan]()

[Allocate resources for the extended period]()

[Reduce the duration of a resource plan]()

[Associate a time card with a resource plan]()

