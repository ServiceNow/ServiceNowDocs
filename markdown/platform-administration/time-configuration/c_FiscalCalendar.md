---
title: Defining fiscal calendars
description: Create fiscal calendars with defined fiscal periods, for use with Financial Management applications, such as Finance Close Automation. You can define fiscal periods, such as one month long, four weeks long, Q1 2015, or July 2015.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Defining fiscal calendars

Create fiscal calendars with defined fiscal periods, for use with Financial Management applications, such as Finance Close Automation. You can define fiscal periods, such as one month long, four weeks long, Q1 2015, or July 2015.

To create a fiscal calendar, activate the Fiscal Calendar \[com.snc.fiscal\_calendar\] plugin. You can then use the legacy functions on the **Fiscal Calendar** menu to generate and validate fiscal calendars and their associated fiscal periods. You can create one of these types:

<table id="table_xh1_rsn_lz"><thead><tr><th>

Calendar type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Regular

</td><td>

A calendar with 12 periods, each of which is one month long.

</td></tr><tr><td>

13 Period

</td><td>

A calendar with 13 periods, each of which is four weeks long.**Note:** This calendar is the only type that doesn’t use quarters.

</td></tr><tr><td>

445

</td><td>

A calendar that divides a year into subsequent 4-week, 4-week, 5-week periods. The first and second periods have four weeks, and the last has five weeks. The application creates these periods for the calendar duration.

</td></tr><tr><td>

454

</td><td>

A calendar that divides a year into subsequent 4-week, 5-week, 4-week periods. The first period has four weeks, the second has five weeks, and the third has four weeks. The application creates these periods for the calendar duration.

</td></tr><tr><td>

544

</td><td>

A calendar that divides a year into subsequent 5-week, 4-week, 4-week periods. The first period has five weeks, and the second and third have four weeks.

</td></tr></tbody>
</table>**Important:** After you start working with a set of financial data with a fiscal calendar type, you can’t change to another type of fiscal calendar. Verify that your fiscal calendar can be used with your financial data. If you import records into the Fiscal period \[fiscal\_period\] table, you should validate that they’re correct and don’t contain any gaps.

After the fiscal calendar has been generated, don’t change either **Start date time** or **End date time** fields of fiscal period records to avoid validation issues.

**Note:**

-   The legacy functions that you may have used, on the **System Scheduler** &gt; **Schedules** and Fiscal Calendar menus, to define schedules and fiscal calendars, continue to be supported. However, you should use the Business Calendar menu in their places to define calendars and schedules and then associate them with specific ServiceNow AI Platform packages. To learn more about defining and using business calendars, see [Creating business calendars](../../../administer/time/concept/business-calendars.md).
-   For Strategic Portfolio Management \(SPM\) applications, you must define Fiscal Calendars using the [Generate a fiscal calendar](../task/t_GenerateFiscalCalendar.md) feature.

-   **[Activate Fiscal Calendar plugin](../task/activate-fiscal-calendar.md)**  
If you have the admin role, you can activate the Fiscal Calendar plugin \(com.snc.fiscal\_calendar\). This plugin includes demo data and activates related plugins if they are not already active.
-   **[Generate a fiscal calendar](../task/t_GenerateFiscalCalendar.md)**  
You can generate a fiscal calendar for a specified time period.
-   **[View, modify, and validate fiscal periods](../task/t_ViewFiscalPeriods.md)**  
After you generate a fiscal calendar, you can view fiscal period records, modify the start and end date, deactivate a fiscal period if necessary, and validate.

**Parent Topic:**[Using time configuration](../../../administer/time/using-time-configuration.md)

