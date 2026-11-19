---
title: Time zones in Dispatcher Workspace
description: There are a few ways that dispatchers can choose to control the time zones that show on the calendar in Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/field-service-scheduling/time-zones-dispatcher.html
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Using Dispatcher Workspace, Assigning WOTs from Dispatcher Workspace, Scheduling and dispatching, Use, Field Service Management]
---

# Time zones in Dispatcher Workspace

There are a few ways that dispatchers can choose to control the time zones that show on the calendar in Dispatcher Workspace.

## Using a single time zone on the calendar

Dispatchers can use the calendar in Dispatcher Workspace with a single time zone. This can be helpful if you, and all of your agents are in one place. In this configuration there is one time zone shown on the calendar, and no time zones are available in the time zone drop-down menu.

To use this you must have **Show multiple time zone rows** disabled, and no entries in the **Select time zones for calendar** field.

\[Omitted image "one-time-zone.png"\] Alt text: single time zone in dispatcher workspace

## Using a single time zone with multiple selection options

Dispatcher Workspace can also be configured to show a single time zone on the calendar, with the ability to switch between time zones. This can be helpful for dispatchers who manage agents across different time zones. For example, if you’re a dispatcher in California, but manage agents across the United States. Dispatchers can quickly switch between time zones and minimize mental calculations needed to understand what agent’s schedule is like in their local time.

To use this, you must have **Show multiple time zone rows** disabled with multiple time zones entries in the **Select time zones for calendar** field.

For more information, see [Change the time zone in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-scheduling/change-timezone-calendar.md).

\[Omitted image "select-one-time-zone.png"\] Alt text: change single selection in dispatcher workspace

## Using multiple time zones on the calendar

Dispatchers can choose to show multiple time zones on the calendar, with several time zone options to select from. This can be helpful if you regularly manage agents across multiple time zones and want to continuously see the time zones where your agents are located. You can configure up to three time zones to display on the calendar at once, and you can also switch between these time zones as needed.

To use this you must have **Show multiple time zone rows** enabled, and multiple entries in the **Select time zones for calendar** field.

For more information, see [Show multiple time zones at once in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/field-service-scheduling/use-stacked-time-zones.md).

\[Omitted image "stacked-time-zone.png"\] Alt text: stacked time zones in dispatcher workspace

