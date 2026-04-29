---
title: Resource Management properties
description: The Resource Management application provides several properties to control allocations, schedules, and other settings.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Resource Management reference, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Resource Management properties

The Resource Management application provides several properties to control allocations, schedules, and other settings.

You need the PPS admin role to access the Resource properties.

To manage resource properties, navigate to **Project Administration** &gt; **Settings** &gt; **Properties – Resource**.

<table id="table_xnq_t5p_ts"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Maximum number of daily resource allocation records that should be considered in synchronous mode for confirmation and allocation.\(**com.snc.resource\_management.plan.auto\_async\_threshold**\)

</td><td>

Determines the maximum number of daily resource allocation records that should be considered in synchronous mode during confirmation and allocation. The property improves the system performance when the number of daily allocation records is more than the value set in the property.

 The default value is 2600 which implies that the number of daily records considered for confirmation or allocation in synchronous mode is 2600. The value is equivalent to confirming or allocating 10 users on a group resource plan for 1-year duration \(260 working days\) or 5 users for 2-year duration, and so on. If the group resource plan contains 11 users for 1-year duration, the number of daily records are 2860. Thus the confirmation and allocation of the resource plan in this case is in asynchronous mode.

 If you always want to confirm and allocate the resource plan in synchronous mode, set the value of the property to a higher number based on your requirements.

**Note:** If the property **com.snc.resource\_management.run\_state\_changes\_async** is set to true, the confirmation and allocation of resource plans is always considered in asynchronous mode.

</td><td>

2600

</td></tr><tr><td>

Show Week/Month toggle on resource grid interface \(**com.snc.resource\_management.show\_week\_month\_toggle**\)

</td><td>

Shows the toggle button for switching between week and month in the resource grid.

</td><td>

Yes

</td></tr><tr><td>

Maximum time duration in Resource Finder in months\(**com.snc.resource\_management.max\_dur\_resource\_finder**\)

</td><td>

The maximum duration for which the resource details should be shown in the resource finder.

</td><td>

24

</td></tr><tr><td>

Use budget reference rates to calculate the Resource requested/allocated cost to derive hourly rate from Labor rate cards \(**com.snc.resource\_management.use\_budget\_reference\_rates**\)

</td><td>

-   When the property is set to Yes, the budget reference rates \[itfm\_fx\_rate\] are used to calculate the resource requested or allocated cost.
-   When the property is set to No, exchange rates \[fx\_rate\] are used to calculate the resource requested or allocated cost. For upgraded customers, the property is by default set to No.

</td><td>

Yes

</td></tr><tr><td>

Maximum number of days for which a resource plan can be created \(**com.snc.resource\_management.plan.max\_duration**\)

</td><td>

Restricts the maximum number of days for which a resource plan should be created.

</td><td>

3660

</td></tr><tr><td>

Default Schedule Name \(**com.snc.resource\_management.default\_schedule**\)

</td><td>

The schedule on the instance that the Resource Management application uses by default.

</td><td>

Resource Management Schedule

</td></tr><tr><td>

If resource\_management reporting for a resource/group has value of percentage\_allocation less than this value the color is shown as green. \(**com.snc.resource\_management.percentage\_allocation\_normal**\)

</td><td>

The value that determines when the availability of the resource is shown as green on the resource report. Green signifies that the resource is not being fully utilized and is probably available to have the work allocated.

</td><td>

50

</td></tr><tr><td>

If resource\_management reporting for a resource/group has value of percentage\_allocation less than this value and greater than the com.snc.resource\_management.percentage\_allocation\_normal, then color is shown as orange. \(**com.snc.resource\_management.percentage\_allocation\_warning**\)

</td><td>

The value that determines when the availability of the resource is shown as orange on the resource report. Orange signifies the resource does not have much availability.

</td><td>

90

</td></tr><tr><td>

Average Daily FTE Hours/Hours Per Person Day \(**com.snc.resource\_management.average\_daily\_fte**\)

</td><td>

The average daily full-time equivalent in hours or number of hours per person day. This value is used as the equivalent of a full-time day if no value is specified in the **Average Daily FTE Hours/Hours Per Person Day** field on the user or group resource record.

**Note:** Capacity is not derived from FTE, but from schedules. Both FTE and schedules must be in synchronization with each other.

</td><td>

8 \(hours\)

</td></tr><tr><td>

Calendar Event Duration \(Minutes\) \(**com.snc.resource\_management.allocation\_interval\_minutes**\)

</td><td>

The default duration for a calendar event.

 Resource allocations use this property to create allocations with a decimal value.

 For example, a user is available for three blocks of time: two 30-minute blocks and one 60-minute block.

-   If the value of this property is set to 30 minutes, and 1 hour needs to be allocated to the user, the allocation is divided into the two 30-minute blocks when the user is available.
-   If the value of this property is set to 60 minutes, the allocation is given to the 60-minute block.

**Note:** When you are changing the default value, enter a value which results a finite value when divided by 60. For example, 6, 12, 15, 30 and so on.

</td><td>

60 \(minutes\)

</td></tr><tr><td>

First Day of Week \(Monday = 1, Sunday = 7\) \(**com.snc.resource\_management.first\_day\_of\_week**\)

</td><td>

Determines which day of the week is the first day. The resource workbench uses this value to calculate the week number.

 For example, a resource is requested from October 14 \(Wednesday\) to October 21 \(Wednesday\).

 If the value of this property is set to 2 \(Tuesday\), the allocation is made and presented in the workbench in two blocks:

-   From Wednesday October 14 to Saturday October 15.
-   Tuesday October 20.

</td><td>

1 \(Monday\)

</td></tr><tr><td>

Perform Resource Confirmation/Allocation/Cancellation in asynchronous mode \(**com.snc.resource\_management.run\_state\_changes\_async**\)

</td><td>

Uses asynchronous mode when confirming, allocating, or canceling resource plans to improve application performance.

 Because resource confirmation and allocation create calendar events for each resource in a group, and also consider each resources schedule, the confirmation, and allocation process can take an excessively long time to complete.

 In asynchronous mode, the application uses an event manager to handle errors that might occur when processing the state of the resource plan. If the property is enabled:

 -   The state of the resource plan changes to Confirmation in Progress / Allocation in Progress / Cancellation in Progress.
-   If the confirmation, allocation, or cancellation does not work, the **Confirm**, **Allocate**, or **Cancel** UI actions appear so you can reprocess the action. If an allocation is only partially completed, you can click the **Allocate** UI action again to remove all previously created events for the plan and reprocesses the action.

 Enable this property if you encounter errors or longer processing times when handling confirmations, allocations, or cancellations. This might occur if there are more than 25 members in a group or if the duration of the resource plan exceeds 6 months.

</td><td>

No

</td></tr><tr><td>

Comma-separated list of resource event types which will be excluded from user's schedule to calculate available capacity and to avoid making resource allocations on the days having these events \(time\_off, meeting, and so on\) \(**com.snc.resource\_management.exclude\_events\_from\_schedule**\)

</td><td>

Specifies which events must be excluded for capacity calculations of the resources and when the system must not create events.

 The events to be entered must be from the **Category** field in the time card table.

</td><td>

time\_off

</td></tr><tr><td>

Show soft allocations in calendar for \(**com.snc.resource\_management.calendar\_show\_soft\_allocations**\)

</td><td>

Shows the following options:

-   Resource Managers: When selected, soft allocations can be seen in the calendar by the resource managers only.
-   Everyone: When selected, soft allocations can be seen in the calendar by all users who have the PPS Resource role.

</td><td>

Resource Managers

</td></tr><tr><td>

Number of records fetched at a time in Resource Grid\(**com.snc.resource\_management.number\_of\_records\_to\_fetch\_at\_a\_time**\)

</td><td>

The number of records that are fetched in resource grid in one server call.

 For example, if there are 100 projects in an allocation board, only 30 are fetched in the first call. When the user scrolls down, a call is made to fetch the next 30 projects. Similarly, when the user expands a project containing, say 100 resource plans, only 30 resource plans are fetched in the first call. Upon scrolling, the next 30 plans are fetched, and so on.

</td><td>

30

</td></tr><tr><td>

Do not allow resource plan dates to be outside the Project/Demand dates \(**com.snc.resource\_management.do\_not\_allow\_resource\_plan\_dates\_outside\_project\_demand\_dates**\)

</td><td>

Restricts the entry of resource plan dates that go beyond the project or demand dates to avoid discrepancies between project or demand dates and resource plan dates.

 If this property is enabled, the resource plan start and end dates must be within the project or demand dates when you create, extend, shift, move, or change the state of a resource plan from requested to confirm or allocate.

</td><td>

No

</td></tr><tr><td>

Limit the number of users retrieved for a group or role in Resource Finder search \(**com.snc.resource\_management.number\_of\_users\_to\_fetch\_in\_finder\_at\_once**\)

</td><td>

Sets the maximum number of users that must be displayed for a group or role while searching for users in Resource Finder

</td><td>

50

</td></tr><tr><td>

Allocate more than 24 hours of effort a day per resource \(**com.snc.resource\_management.allocate\_more\_than\_24hours\_per\_day**\)

</td><td>

Allocates more than 24 hours of efforts for a resource per a day.

</td><td>

No

</td></tr><tr><td>

Exclude resource assignments in specific states from capacity calculation \(**com.snc.resource\_management.exclude\_status\_from\_availability**\)

</td><td>

Excludes the resource assignments with defined statuses from calculating resource availability and aggregates.You can enter comma separated values such as Pending, Unapproved, and so on.

</td><td>

This field is left empty.

</td></tr></tbody>
</table>**Parent Topic:**[Resource Management reference](../task/rsrc-mgmt-reference.md)

