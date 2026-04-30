---
title: Generate a fiscal calendar
description: You can generate a fiscal calendar for a specified time period.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Defining fiscal calendars, Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Generate a fiscal calendar

You can generate a fiscal calendar for a specified time period.

## Before you begin

Role required: fiscal\_calendar\_admin

## About this task

**Important:** Once you start working with a set of financial data with a fiscal calendar type, you cannot change to another type of fiscal calendar. Verify that your fiscal calendar can be used with your financial data.

**Note:** Instead of generating fiscal calendars, can also use the Business Calendar functions to create fiscal calendars. To learn more about creating business calendars and schedules, see [Creating business calendars](../../../administer/time/concept/business-calendars.md).

## Procedure

1.  Navigate to **All** &gt; **Fiscal Calendar** &gt; **Generate**

2.  In the **Fiscal Calendar Types** section, select the type of fiscal year calendar.

    ![The Fiscal Calendar form](../image/fiscal_calendar.png)

3.  In the **Fiscal Calendar Configuration** section, fill in the fields.

<table id="table_pry_j5k_g5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Fiscal Unit

</td><td>

Base unit for the calendar.-   **Month**: Generate fiscal calendar with monthly periods.
-   **Quarter**: Generate fiscal calendar with quarterly periods.


</td></tr><tr><td>

Start Month

</td><td>

Month that is the beginning of your fiscal year.

</td></tr><tr><td>

Start Year

</td><td>

Starting year for the calendar.

</td></tr><tr><td>

Prefix for Year

</td><td>

Prefix that the application uses in the name of the records that represent the fiscal year.

</td></tr><tr><td>

Prefix for Quarter/Period

</td><td>

Prefix that the application uses in the name of the records that represent the fiscal quarter or period.

</td></tr><tr><td>

Start Day

</td><td>

Day that represents the beginning of each month.

</td></tr><tr><td>

End Year

</td><td>

Ending year for the calendar.

</td></tr><tr><td>

Prefix for Month/Period

</td><td>

Prefix that the application uses in the name of the records that represent the month or period.

</td></tr></tbody>
</table>4.  Click **Generate Calendar**.

5.  Navigate to **System Definition** &gt; **Fiscal Periods** and verify that the monthly, quarterly, and annual fiscal period records exist.


**Parent Topic:**[Defining fiscal calendars](../concept/c_FiscalCalendar.md)

