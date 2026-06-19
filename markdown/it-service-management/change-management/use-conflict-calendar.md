---
title: Manage your change schedules and resolve conflicts
description: Prevent schedule conflicts by using the conflict calendar to manage your change schedule details, customize views, and resolve conflicts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/use-conflict-calendar.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conflict calendar, Conflict detection, Configure, Change Management, IT Service Management]
---

# Manage your change schedules and resolve conflicts

Prevent schedule conflicts by using the conflict calendar to manage your change schedule details, customize views, and resolve conflicts.

## Before you begin

Role required: admin

**Note:** Users with the admin role must activate the Change Request Calendar \(com.snc.change\_request\_calendar\) plugin for the **Conflict Calendar** button to appear.

## About this task

When there is a conflict, you can use **Scheduling Assistant** link in the change form to find the next available slot.

When there are no available slots for the next 90 days, then an actionable message is displayed with the reason the assistant was not able to find a slot.

Alternatively, you can resolve conflicts by moving the change request to be within a maintenance window in the conflict calendar. The **Conflict Calendar** button appears in the header of the change form once the **Planned start date**, **Planned end date**, and the **Configuration items** fields are added and the record is saved.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open**.

2.  Open your required change request.

3.  Select **Conflict Calendar**.

4.  Select **Scheduling Assistant**.

    The scheduling assistant dialog box displays the next available times to choose to resolve the conflict. The number of days factored after the planned start and end dates and the number of suggestions calculated for the next available time are configured under **Conflict properties**. For more information, see [Configure conflict analysis properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/configure-conflict-properties.md) form.

5.  Select the time from the available time slots.

6.  Select **Select Available Time**.

    The planned start date and end date are updated with the new time, and the conflict is resolved.

7.  To select another day from the calendar, select the calendar icon \(\[Omitted image "view-calendar-icon.png"\] Alt text: Calendar icon\) and select the date.


## Result

The conflicts are reviewed and resolved.

**Parent Topic:**[Conflict calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-conflict-calendar.md)

