---
title: Resource schedules
description: Understand the default schedules used in Resource Management and learn how to create your own custom schedules.Check the default schedule associated to a resource and apply custom schedules to those resources who require it.Choose the default schedule to be applied to your resources.
locale: en-US
release: zurich
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource schedules

Understand the default schedules used in Resource Management and learn how to create your own custom schedules.

Resource management uses a default schedule named Resource Management Schedule. The Resource Management Schedule has the following characteristics:

-   Weekly on Weekdays
-   Monday through Friday 08:00-12:00
-   Monday through Friday 13:00-17:00

While planning a resource request for a resource plan, the user's schedule is considered to calculate planned and requested hours, if all users in that resource plan have the same schedule and that schedule is different from the resource management schedule.

## Default schedule

The schedule assigned to each user can be understood using the following information on the user profile.

-   Value provided in the **Schedule** field.
-   Schedules provided in the Schedules related list, with the **Context** field set to Resource Management.

    This related list can be seen in the Resource Manager view of the user profile.


If there are no entries in the Schedules related list, the value provided for the **Schedule** field is used to determine the resource schedule. If the Schedule field is empty too, then the schedule specified in the **Default Schedule Name \(com.snc.resource\_management.default\_schedule\)** property is applied as the resource schedule. To understand how to modify this property value, see [Specify the default resource management schedule](c_UsingResourceSchedules.md#).

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

## Custom schedules for resources

Check the default schedule associated to a resource and apply custom schedules to those resources who require it.

If custom schedules are necessary, work with your administrator to create them. An administrator can create a schedule as per your requirements and assign it to the user. This custom schedule can also be assigned to other users as appropriate.

The value specified for the **Schedule** field on a user profile overrides the schedule specified in the **Default Schedule Name** property.

**Note:** The **Time zone** field of a schedule is recommended to be set to **Floating**.

If necessary, the administrator can create a hierarchy of schedules. This is useful if you want users to have a primary schedule such as Monday-Friday 8:00-17:00 and a secondary schedule such as Saturday-Sunday 12:00-16:00. See [Custom schedule hierarchy](c_UsingResourceSchedules.md#section_hks_2lv_nsb).

### Custom schedule hierarchy

To create a schedule hierarchy for any user, use the Schedules related list. Create a schedule and within the new schedule, define the type, dates, and repeat schedule using the Schedule Entries related list.

For example, Alene's usual schedule is 8-5 weekdays, which is specified in the **Schedule** field of their user profile. On top of the usual work, Alene also has to attend a site check every Saturday. The schedule for this appointment can be created from the Schedules related list.

![Resource schedule hierarchy.](../image/resource-schedules.png "Custom schedule hierarchy example")

![Custom schedule entry.](../image/custom-schedule-entry.png "Schedule entry within a custom schedule")

## Specify the default resource management schedule

Choose the default schedule to be applied to your resources.

### Before you begin

Role required: it\_pps\_admin

### About this task

The base system uses Resource Management Schedule. You can change the default schedule at any time by using the **Default Schedule Name** property.

### Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Schedules** &gt; **Schedules**.

2.  Review the schedules and copy the Name of the schedule that you want to use.

3.  Navigate to **Project Administration** &gt; **Settings** &gt; **Properties - Resource**.

4.  In the **Default Schedule Name** property field, paste the name of the schedule that you identified in step 2.


