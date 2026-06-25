---
title: Resource events and schedules
description: Schedules classify time as work time and non-work time and can be associated with resources and with projects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/resource-management/r\_ResourceEventsAndSchedules.html
release: australia
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource events, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource events and schedules

Schedules classify time as work time and non-work time and can be associated with resources and with projects.

The [My Calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/c_MyCalendar.md) module shows the user's work schedule and non-work time.

When a resource manager makes an allocation, the following takes place automatically:

-   The schedule associated with the specified resource is analyzed.
-   The allocation type changes to **Hard** and calendar events are created for individual resources within the users' schedule. The hours are spread depending upon the [hard allocation spread](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/rsrc-plan-form.md) type.

Use the Calendar Event Duration property to control the default minimum unit for an event. See [Resource Management properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/r_ResourceProperties.md) for examples.

**Note:** Over-allocation is allowed, starting with the Geneva release. However, no more than 24 hours can be allocated to a user during a given day. See [Resource allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/r_AllocatingResources.md) for more information.

**Parent Topic:**[Resource events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/resource-management/c_ResourceEvents.md)

**Related topics**  


[Resource event modifications]()

[Modify a self-created resource event]()

[Change the resource event color]()

