---
title: Invoke the Schedule page and view a calendar
description: You can use the URL from arguments module, a field decoration \(dictionary attribute ref\_contributions\), or a UI Action linking to show\_schedule.do to invoke the Schedule page.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using schedules and calendars, Schedules, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Invoke the Schedule page and view a calendar

You can use the URL from arguments module, a field decoration \(dictionary attribute `ref_contributions`\), or a UI Action linking to `show_schedule.do` to invoke the Schedule page.

For example, the On-call calendar module generates the calendar from the following URL:

```
$ocf.do?sysparm_start_date=2016-03-01&sysparm_current_view=monthly&sysparm_include_view=monthly,daily
```

This URL takes the user to the monthly calendar view dated March 1, 2016.

-   The URL component `sysparm_current_view = monthly || weekly || daily` determines the current calendar view. If `sysparm_current_view` is given an invalid or empty value, it defaults to monthly view and rewrite the URL to that view. Valid values are monthly or weekly or daily.
-   The URL component `sysparm_include_view = monthly,weekly,daily` determines which calendar views are available. If`sysparm_include_view` is given invalid or empty values, only the valid views appear. If all values are invalid, the default three views appears and rewrites the URL to those views. Valid values are `monthly`, `weekly`, and `daily`.

    **Note:** The `sysparm_include_view` is only available for the new on-call calendar view.

-   The URL component `sysparm_group_id=group_sys_id` determines the specified group to filter on. If `sysparm_group_id` is specified, it filters by the specified group. Valid value is a group sysId.
-   The URL component `sysparm_start_date=2016-03-02` determines the date based on which every view appears. If `sysparm_start_date` is specified, it opens the calendar contesting that particular date in which every view is selected. The format is YYYY-MM-DD. If an invalid format or date is specified, it uses the current date and rewrites the URL to that date.

**Note:** The `sysparm_zoom` URL component has been replaced with `sysparm_current_view` in OnCallRotation only.

**Parent Topic:**[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

**Related topics**  


[Schedule calendar](schedule-calendar.md)

