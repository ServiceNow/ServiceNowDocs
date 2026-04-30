---
title: Define business calendar filtering options
description: Define date and time filtering options for a business calendar. These filtering options are in addition to the standard date and time filtering in the ServiceNow AI Platform. You can provide your users with additional filtering options when they use the business calendar with ServiceNow AI Platform packages and functional areas.
locale: en-US
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Creating business calendars, Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Define business calendar filtering options

Define date and time filtering options for a business calendar. These filtering options are in addition to the standard date and time filtering in the ServiceNow AI Platform. You can provide your users with additional filtering options when they use the business calendar with ServiceNow AI Platform packages and functional areas.

## Before you begin

Role required: admin

## About this task

To learn more about standard filtering options, see [Values for date/time fields](https://www.servicenow.com/docs/access?context=c_ValuesForDateTimeFields&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

**Note:** The easiest way to create business calendar filtering options and associate them with a business calendar is to use the Business Calendar Filter Options related list in the Business Calendar form. To learn more about creating a business calendar, see [Create a business calendar](create-business-calendar.md).

## Procedure

1.  Navigate to **All** &gt; **Business Calendar** &gt; **Business Calendar Filter Options**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_k35_43z_vhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Period

</td><td>

Number of periods that should be traversed forward, backward, or both, for the business calendar. For example, if the business calendar reflects a week:-   Provide a filter option for the current week by entering `0` for the base period.
-   Provide a filter option for a previous period by entering a negative number that represents the number of periods that should be traversed from the base period. For example, enter `-1` for the last period, or enter `-2` for two periods ago.
-   Provide a filter option for a future period by entering a positive number. For example, enter `1` for the next period, or enter `2` for the next two weeks.
 If the business calendar reflects a week:

-   Provide a filter option for the current week by entering `0` for the base period.
-   Provide a filter option for a previous period by entering a negative number that represents the number of periods that should be traversed from the base period. For example, enter `-1` for the last period, or enter `-2` for two periods ago.
-   Provide a filter option for a future period by entering a positive number. For example, enter `1` for next period, or enter `2` for the next two weeks.
 If the business calendar reflects a fiscal year with 13 periods:

-   Provide a filter option for the current fiscal year by entering `0` for the base period.
-   Provide a filter option for a previous fiscal year by entering a negative number that represents the number of periods that should be traversed from the base period. For example, enter `-2` for two fiscal periods ago, or enter `-13` for the last fiscal year.
-   Provide a filter option for a future fiscal year by entering a positive number. For example, enter `13` for the next fiscal year.
 If the business calendar reflects a fiscal year with four fiscal quarters:

-   Provide a filter option for the current fiscal quarter by entering `0` for the base period.
-   Provide a filter option for a previous fiscal quarter by entering a negative number that represents the number of periods that should be traversed from the base period. For example, enter `-1` for the last fiscal quarter, or enter `-2` for the last two fiscal quarters.
-   Provide a filter option for a future fiscal quarter by entering a positive number. For example, enter `1` for the next fiscal quarter, or enter `2` for the next two fiscal quarters.


</td></tr><tr><td>

Calendar

</td><td>

Name of the business calendar that you want the filter options to belong to. To select a business calendar, or create a new one:

1.  Search for an existing business calendar by clicking ![Search button](../../search-administration/image/SearchIcon.png).
2.  If no business calendar exists, or if you want to create a new business calendar, click **New**.


</td></tr><tr><td>

Application

</td><td>

Application that is associated with this business calendar. If you are working on an application or are creating a business calendar from an application record, the field defaults to that application. Otherwise, the field defaults to **Global**. Any records that are created from the table record, such as modules and security rules, are assigned to this application by default. To learn more about application scoping, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

</td></tr></tbody>
</table>    **Note:** Within a calendar filtering option record, you can only associate a business calendar with a single filter option. To create multiple filtering options, you have to create multiple filtering option records, each with its own period entry.

4.  Click **Submit**.


## Result

Records are created in the Business Calendar Filter Option \(business\_calendar\_filter\_option\) table. If you create business calendar filtering options in the Business Calendar Filter Options related list in the Business Calendar form, these records are also associated with the specific business calendar.

**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

