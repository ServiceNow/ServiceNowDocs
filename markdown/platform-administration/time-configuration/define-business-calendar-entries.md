---
title: Define business calendar entries
description: Create business calendar entry records that define the individual time periods that make up a business calendar. You create a business calendar entry for every individual time span in the calendar.Create a name for an individual business calendar entry. You create this record so you can easily identify a specific business calendar entry when you use it in a business calendar.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Creating business calendars, Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define business calendar entries

Create business calendar entry records that define the individual time periods that make up a business calendar. You create a business calendar entry for every individual time span in the calendar.

## Before you begin

Role required: business\_calendar\_admin

## About this task

In contrast to legacy schedule entries that have repeating and excluding time spans, you have to create individual business calendar entries for every business calendar time span. For example, if you are creating a Fiscal Year 2020 business calendar with 13 fiscal periods, you have to create individual business calendar entries for each fiscal period. For each fiscal period, you specify start and end date times. The year is appended to the beginning of the display name, according to the information entered in the `long name` field. This helps in avoiding confusion between similarly named entries.

**Note:** Fiscal calendars or schedules you may have created in the **Fiscal Calendar** or **System Scheduler** &gt; **Schedules** menu also appear on the lists on the **Business Calendar** menu. If you select a fiscal calendar or schedule, it appears in the legacy function that you originally used to create it. You can't view or update legacy fiscal calendars or schedules using this form.

To create business calendar entries and associate them with a business calendar, use the Business Calendar Entries related list in the Business Calendar form. To learn more about creating a business calendar, see [Create a business calendar](create-business-calendar.md).

## Procedure

1.  Navigate to **All** &gt; **Business Calendar** &gt; **Business Calendar Entries**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_lbb_zys_m3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique reference name for the business calendar entry. To select a business calendar name or to create one: 1.  To search for an existing business calendar entry name, select ![Search button](../../search-administration/image/SearchIcon.png).
2.  If no business calendar entry name exists and you want to create a business calendar entry name, select **New**. The Business Calendar Entry Name form appears.

**Note:** To learn how to create business calendar entry names, see [Create business calendar entry names](define-business-calendar-entries.md#).

</td></tr><tr><td>

Start

</td><td>

Start date and time for the business calendar period. It uses the time zone that you specified in the business calendar record that you associate with it. For example, if you’re defining a fiscal period for the month of January, the starting date time is January 31, 2020 12:00

</td></tr><tr><td>

End

</td><td>

End date and time for the business calendar period. It uses the time zone that you specified in the business calendar record that you associate with it. For example, if you’re defining a fiscal period for the month of January, the ending date time is January 31, 2020 23:59

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select the business calendar entry that you created from the list that populates.

6.  Verify that the info in the fields for the `Short name`, `Long name`, `Label`, `Calendar`, and `Application` is correct.

7.  Select **Update** to save any changes and return to the list.


**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

## Create business calendar entry names

Create a name for an individual business calendar entry. You create this record so you can easily identify a specific business calendar entry when you use it in a business calendar.

### Before you begin

Role required: business\_calendar\_admin

### Procedure

1.  Navigate to **All** &gt; **Business Calendar** &gt; **Business Calendar Entry Names**.

    **Note:** Alternately, you can create a business calendar entry name at the time you create the associated business calendar entry. To learn more about creating a business calendar entry, see [Define business calendar entries](define-business-calendar-entries.md#).

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ffs_l3w_bp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Abbreviated name for the business calendar entry. For example, January.

</td></tr><tr><td>

Long name

</td><td>

Longer name for the business calendar entry. For example, January fiscal period. It is from this field that the year is pulled and appended to the display name.

</td></tr><tr><td>

Label

</td><td>

Unique label for identification of the business calendar entry when you perform filtering.

</td></tr><tr><td>

Calendar

</td><td>

Name of the business calendar that you want the business calendar entry to belong to. This entry creates the relationship between a business calendar and the business calendar entries that define each individual time span with it. For example, if you’re creating a business calendar entry for the January fiscal period, you select FY20 to associate it with Fiscal Year 2020. To select an existing business calendar:

1.  Select the **Lookup using list** icon \(![](../../ai-search/image/icon-search.png)\) or
2.  Select inside the **Calendar** field to view and select from a listing of recent business calendars that are created in **Business Calendar** &gt; **Business Calendars**.
**Note:** If you attempt to use the **Lookup using list** icon \(![](../../ai-search/image/icon-search.png)\) and see a dialog box with **Cancel** and **Leave** options, select **Cancel** and then select inside the **Calendar** field to select from a listing of recent business calendars.

</td></tr><tr><td>

Calendar type

</td><td>

Select the type of calendar. By default, no option is selected. The base system options are, **Business calendar** and **Fiscal calendar**. You can add other choices for the calendar type by extending the table and adding the choices you prefer. For scoped applications, you should extend the table with in the scope, create a choice list, then add choices from the choice set.

</td></tr><tr><td>

Application

</td><td>

Application that is associated with this business calendar. If you are working on an application or are creating a business calendar from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default. To learn more about application scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td></tr></tbody>
</table>4.  Select **Submit**.


### Result

Records are created in the Business Calendar Entry \(business\_calendar\_span\) and the Business Calendar Entry Name \(business\_calendar\_span\_name\) tables. If you create business calendar entries in the Business Calendar Entries related list in the Business Calendar form, these records are also associated with the specific business calendar.

