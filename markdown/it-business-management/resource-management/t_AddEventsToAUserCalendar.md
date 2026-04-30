---
title: Add events to a user calendar
description: Resource managers can add events to user calendars.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [My Calendar, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Add events to a user calendar

Resource managers can add events to user calendars.

## Before you begin

Role required: resource\_manager

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resources** &gt; **Users**.

2.  Do one of the following.

<table id="choicetable_g3t_jz2_zs"><tbody><tr><td id="d113542e80">

**From the User list**

</td><td>

Right-click a user name in the Users list and select **View Calendar**.

</td></tr><tr><td id="d113542e92">

**From the User form**

</td><td>

Select a User record to open the User form, and then select the **View Calendar** related link.

</td></tr></tbody>
</table>    The calendar for that user opens in a new window or tab.

3.  Open the **Add Event** form by selecting an empty white cell on the calendar.

4.  On the form, fill the fields.

    For description of the field names, see [Add events to your calendar](t_AddEventsToYourCalendar.md).


## Result

-   When you add a calender event, the resource aggregate daily, weekly, and monthly tables are updated. The resource aggregate daily table isn’t enabled by default. To generate daily aggregates and store them in this table, create the **com.snc.resource\_management.generate\_daily\_aggregates** property and set the value to true.
-   All the non-project events created for a user from the calender appear as Operational Work for the user in [Resource Finder](create-resource-plan-with-finder.md).

**Parent Topic:**[My Calendar](../concept/c_MyCalendar.md)

**Related topics**  


[Add events to your calendar](t_AddEventsToYourCalendar.md)

[Create repeatable events](t_CreateRepeatableEvents.md)

[View a user calendar](t_ViewAUserCalendar.md)

[Delete events](t_DeleteEvents.md)

