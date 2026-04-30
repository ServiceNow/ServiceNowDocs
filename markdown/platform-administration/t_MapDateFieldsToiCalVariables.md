---
title: Map date fields to iCalendar variables
description: You can specify what fields provide the date information in calendar invitation notifications by changing the field mappings of the dtstart and dtend variables in the import export map for the iCalendar invitation.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Calendar integration, Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Map date fields to iCalendar variables

You can specify what fields provide the date information in calendar invitation notifications by changing the field mappings of the *dtstart* and *dtend* variables in the import export map for the iCalendar invitation.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, enter `sys_impex_map.list`.

2.  Open a map to edit.

3.  In the Field Maps related list, click either the **end\_date** or **start\_date** mapped field to change the mapping for *dtstart* or *dtend*, as needed.

4.  Change the **Database** field to the field you want to use to set the start date or end date.

5.  Select **Update**.


**Parent Topic:**[Calendar integration](../reference/r_CalendarIntegration.md)

