---
title: Resource events and schedules
description: Schedules classify time as work time and non-work time and can be associated with resources and with projects.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Resource events, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource events and schedules

Schedules classify time as work time and non-work time and can be associated with resources and with projects.

The [My Calendar](../concept/c_MyCalendar.md) module shows the user's work schedule and non-work time.

When a resource manager makes an allocation, the following takes place automatically:

-   The schedule associated with the specified resource is analyzed.
-   The allocation type changes to **Hard** and calendar events are created for individual resources within the users' schedule. The hours are spread depending upon the [hard allocation spread](rsrc-plan-form.md) type.

Use the Calendar Event Duration property to control the default minimum unit for an event. See [Resource Management properties](r_ResourceProperties.md) for examples.

**Note:** Over-allocation is allowed, starting with the Geneva release. However, no more than 24 hours can be allocated to a user during a given day. See [Resource allocation](r_AllocatingResources.md) for more information.

**Parent Topic:**[Resource events](../concept/c_ResourceEvents.md)

**Related topics**  


[Resource event modifications](../concept/c_ModifyAResourceEvent.md)

[Modify a self-created resource event](../task/t_ModifyASelfCreatedResourceEvent.md)

[Change the resource event color](../task/t_ChangeTheResourceEventColor.md)

