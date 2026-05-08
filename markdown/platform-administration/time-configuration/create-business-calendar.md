---
title: Create a business calendar
description: Create a definition record for an individual parent or child business calendar. You create this record so that you can easily identify a business calendar when you use it in a ServiceNow AI Platform package or functional area. A business calendar can represent any length of time, such as a week, a month, a year, or a fiscal period.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating business calendars, Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a business calendar

Create a definition record for an individual parent or child business calendar. You create this record so that you can easily identify a business calendar when you use it in a ServiceNow AI Platform package or functional area. A business calendar can represent any length of time, such as a week, a month, a year, or a fiscal period.

## Before you begin

Role required: business\_calendar\_admin

## About this task

When you create a business calendar, you specify a reference name, labeling, parent business calendar, if any, and a time zone for it.

You first create a business calendar record and then create business calendar entries for it in the Business Calendar Entries related list. To learn more about how business calendar entries work, see [Define business calendar entries](define-business-calendar-entries.md#) and [Create business calendar entry names](define-business-calendar-entries.md#). You can also create records from the Business Calendar Entries table itself.

Using the Business Calendar Filter Options related list, you can also define the date and time filtering options for the business calendar that you’re creating.

You can also create a business calendar span using a Script includes titled, **BusinessCalendarGeneratorUtil**. For more information, see [Create a business calendar span using a Script includes](create-a-business-calendar-span-using-a-script-includes.md).

**Note:** Fiscal calendars or schedules you may have created in the **Fiscal Calendar** or **System Scheduler** &gt; **Schedules** menu also appear on the lists on the **Business Calendar** menu. If you select a fiscal calendar or schedule, it appears in the legacy function that you originally used to create it. You can't view or update legacy fiscal calendars or schedules using this form.

## Procedure

1.  Navigate to **All** &gt; **Business Calendar** &gt; **Business Calendars**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ffs_l3w_bp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique reference name and identifier for the business calendar record. The name should be unique per domain.

</td></tr><tr><td>

Label

</td><td>

Unique singular label for identifying the business calendar when you perform filtering. For example, you can assign a week-long work calendar with a label of `Workweek`.

</td></tr><tr><td>

Plural Labels

</td><td>

Unique plural label for identifying the business calendar. For example, you can assign a week-long work calendar with a label of `Workweeks`. Use plural labels when you do filtering that is based on more than one unit in the past or future. For example, Last 2 Fiscal Quarters.

</td></tr><tr><td>

Parent

</td><td>

Parent business calendar to the current business calendar that you’re creating. To search for an existing business calendar, select the **Lookup using list** icon \(![](../../ai-search/image/icon-search.png)\).

 For example, you created a business calendar for 2020, and an individual child calendar for each month within the year, each with its own business calendar entries. As you create a business calendar for each month, you would select 2020 as the parent calendar for each.

 These entries create the relationship between a parent and its child business calendars. Leave this field empty if you’re creating a parent business calendar.

</td></tr><tr><td>

Application

</td><td>

Application that is associated with this business calendar. If you are working on an application or are creating a business calendar from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default. To learn more about application scoping, see Application scope

</td></tr><tr><td>

Time zone

</td><td>

Time zone to use for the business calendar when you specify the starting and ending times for each associated business calendar entry. Select a time zone entry:

-   **-None-**: Use the time zone specified in the logged in user's profile.
-   **Use System Time Zone**: Use the default system time zone specified for the instance.
-   **– Floating --**: Time zone is relative to whatever is accessing the business calendar entry at any given time. For example, if an administrator in Amsterdam creates a floating business calendar for 08:00 a.m. to 5:00 p.m., a person in San Jose, California, sees it as 08:00 a.m. to 5:00 p.m. When you define a business calendar in a specific time zone, users in different time zones see the business calendar in their own time zone.
-   Actual time zone. For example, Europe/London, US/Pacific, US/Central.


</td></tr><tr><td>

Description

</td><td>

Description of the business calendar.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  In the Business Calendars list, select the business calendar that you created.

6.  In the Business Calendar Entries related list, create entries that define each span of time within the business calendar.

    Create, at minimum, one business calendar entry for the selected calendar.

    **Note:** To learn more about creating business calendar entries, see [Define business calendar entries](define-business-calendar-entries.md#) and [Creating business calendars](../concept/business-calendars.md).

7.  In the Business Calendar Filter Options related list, select **New** to create filtering options for the business calendar.

    You can define the date and time filtering options for the business calendar that you’re creating. These filtering options are in addition to the standard date and time filtering in the ServiceNow AI Platform.

    **Note:** To learn more about creating business calendar filtering options, see [Define business calendar filtering options](define-business-calendar-filtering-options.md).

8.  Select **Submit**.


## Result

A business calendar record is saved in the Business Calendar \[business\_calendar\] table.

If you create business calendar entries in the Business Calendar Entries related list, records are created in the Business Calendar Entry \(business\_calendar\_span\) table. The records are associated with the business calendar.

If you created business calendar filter options in the Business Calendar Filter Options related list, a record is saved in the Business Calendar Filter Option \(business\_calendar\_filter\_option\) table. The record is associated with the business calendar.

**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

