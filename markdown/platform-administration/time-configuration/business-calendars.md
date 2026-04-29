---
title: Creating business calendars
description: Create business calendars in the ServiceNow AI Platform so that you can schedule events for your users and track their time across applications. You define schedules and calendars of all types, including fiscal calendars, in the Business Calendar menu.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Creating business calendars

Create business calendars in the ServiceNow AI Platform so that you can schedule events for your users and track their time across applications. You define schedules and calendars of all types, including fiscal calendars, in the Business Calendar menu.

## Business calendar components

Use the following forms when you define calendars and schedules in the Business Calendar menu:

-   **Business calendar definition record**

    Identifies an individual business calendar where you can specify a reference name, labeling, parent business calendar \(if any\), and a time zone. A business calendar can represent any time period, and its definition record is saved in the Business Calendar \[business\_calendar\] table.

    To learn more about creating a business calendar definition, see [Create a business calendar](../task/create-business-calendar.md).

-   **Business calendar entries**

    Defines the individual entries that make up a business calendar, and saves them in the Business Calendar Entry \[business\_calendar\_span\] and Business Calendar Entry Name \(business\_calendar\_span\_name\) tables. In contrast to legacy schedule entries, which have repeating and excluding time spans, you must create individual business calendar entries for all time spans in the calendar. You can also create business calendar spans across both global and scoped applications using the Script Includes **BusinessCalendarGeneratorUtil**. To learn more see [Create a business calendar span using a Script includes](../task/create-a-business-calendar-span-using-a-script-includes.md).

    To learn more about creating entries for a business calendar, see [Define business calendar entries](../task/define-business-calendar-entries.md#) and [Create business calendar entry names](../task/define-business-calendar-entries.md#).


-   **Business calendar filter options**

    Defines the date and time filtering options for the business calendar that you’re creating. These filtering options are in addition to the standard date and time filtering in the ServiceNow AI Platform.

    To learn more about creating filtering options for a business calendar, see [Create a business calendar](../task/create-business-calendar.md).

-   **Calendars for package**

    Pairs a business calendar with a ServiceNow AI Platform package so that you can enable the calendar for use in that functional area. A package is a collection of scopes and applications that make up a functional area, such as HR Service Delivery.

    To learn more about associating a business calendar with a package, see [Pair business calendars with packages](../task/pair-business-calendars-with-packages.md).


**Warning:** If you’re using Performance Analytics, use caution when changing time spans. Any change you make to the time span on a business or fiscal calendar can invalidate the Performance Analytics data. Consult with a Performance Analytics administrator before making such changes.

## Fiscal calendar example

In this example, you create a fiscal calendar with 4 quarters and 12 fiscal periods. ![Business calendar example](../image/fiscal-calendar-ex_updated.png)

-   When you navigate to **Business Calendar** &gt; **Business Calendars**, you create:

    -   A business calendar with a title of Fiscal Year.
    -   A calendar for quarters that belong to the fiscal year.
    -   A calendar for periods with a parent of Fiscal Year or Fiscal Quarter.
    When you create the Fiscal Year Quarter child calendar, you designate that the Fiscal Year is its parent calendar. For the child Fiscal Year Period calendar, you designate a Fiscal Year Quarter as its immediate parent.

-   When you create each calendar, use the Business Calendar Entries related list, or navigate to **Business Calendar** &gt; **Business Calendar Entries** to create business calendar entries for it. For each business calendar entry, create a reference name \(for example, Fiscal Period 1\) and designate start and end dates for each time span within the calendar.
    -   For example, the parent Fiscal Year calendar has a business calendar entry for the time span of October 1, 20nn 12:00 through September 30, 20nn 23:59:59.
    -   The child Fiscal Year Quarter calendar consists of four business calendar entries, each with the start and end dates of each quarter that makes up the fiscal year.

        **Note:** You can also create 13 period, 445, 454 and 544 types of fiscal calendars. To learn more about these types of fiscal calendars, see [Defining fiscal calendars](../../../product/it-finance/concept/c_FiscalCalendar.md).

    -   The child Fiscal Year Quarters calendar consists of multiple business calendar entries, with the start and end date times for each period in the fiscal year.
-   Use **Business Calendar** &gt; **Calendars for Package** to pair the parent Fiscal Year 20nn calendar with ServiceNow AI Platform packages, such as HR Service Delivery or Finance Close Automation.

## Business calendar schedule example

In this example, you create a work schedule for the month of December.

-   The work schedule consists of a parent calendar, a child calendar for the working weeks in December, and another child calendar for the working days in December.
-   The December Workdays calendar consists of business calendar entries for each working day. You don’t include non-work days such as Saturdays, Sundays, and company holidays.

![Business calendar schedule example](../image/business-calendar-schedule-ex_updated.png)

-   Use **Business Calendar** &gt; **Business Calendars** to create a parent business calendar with a title of December Work Schedule, and a child business calendar for December work weeks. When you create the child calendar, you designate that the December Work Schedule is its parent calendar.

    **Note:** You can make the December Work Schedule even more granular by creating a subordinate child calendar for December workdays. In this case, its immediate parent is the December Work Weeks calendar.

-   When you create each calendar, use the Business Calendar Entries related list, or navigate to **Business Calendar** &gt; **Business Calendar Entries** to create, at minimum, one business calendar entry for it. For each business calendar entry, you give it a reference name, and designate the start and end date times for each time span within the calendar.
    -   For example, the parent December Work Schedule calendar is for a time span of December 1, 20nn 12:00 through December 31, 20nn 23:59:59.
    -   The child December Work Week calendar consists of five business calendar entries. Each entry is for the start and end dates of each calendar week in December.
    -   The child December Workdays calendar consists of multiple business calendar entries. Each entry is for the start and end date times for each working day in December. You don’t create business calendar entries for company holidays such as New Year's Eve or New Year's Day.
-   Use **Business Calendar** &gt; **Calendars for Package** to pair the parent business calendar December Work Schedule with the appropriate ServiceNow AI Platform packages, such as Customer Service Management.

## Using business calendars in place of legacy calendar and schedule definitions

The legacy functions that you may have used, on the **System Scheduler** &gt; **Schedules** and Fiscal Calendar menus, to define schedules and fiscal calendars, continue to be supported. However, you should use the Business Calendar menu in their places to define calendars and schedules and then associate them with specific ServiceNow AI Platform packages.

**Note:** For Strategic Portfolio Management \(SPM\) applications, you must define Fiscal Calendars using the [Generate a fiscal calendar](../../../product/it-finance/task/t_GenerateFiscalCalendar.md) feature.

-   If you use the legacy functions to create fiscal calendars and schedules, the resulting definition records are internally flagged as belonging to the legacy \[cmn\_schedule\] table hierarchy. These records appear on the lists on the Business Calendar menu, as well as on the lists on the respective menus for the legacy functions used. For example, if you defined fiscal calendars using legacy fiscal calendar functions, the resulting records appear on lists on the Business Calendar Fiscal Calendar menus.
-   If you select a legacy fiscal calendar or schedule from these lists, you can only modify it using the legacy function that you originally used to create it. For example, if you select a legacy fiscal calendar, you can only modify it by using the functions on the Fiscal Calendar menu. You can't modify it with the Business Calendar menu functions.

-   **[Create a business calendar](../task/create-business-calendar.md)**  
Create a definition record for an individual parent or child business calendar. You create this record so that you can easily identify a business calendar when you use it in a ServiceNow AI Platform package or functional area. A business calendar can represent any length of time, such as a week, a month, a year, or a fiscal period.
-   **[Create a business calendar group](../task/create-business-calendar-group.md)**  
For Performance Analytics and Reporting to use business calendars, organize several calendars into a business calendar group. An application might also contain a business calendar group.
-   **[Create a business calendar span using a Script includes](../task/create-a-business-calendar-span-using-a-script-includes.md)**  
You can generate business calendar spans and their names using the **Script includes** titled **BusinessCalendarGeneratorUtil**. The calendars you create are accessible across both global and scoped applications.
-   **[Define business calendar entries](../task/define-business-calendar-entries.md#)**  
Create business calendar entry records that define the individual time periods that make up a business calendar. You create a business calendar entry for every individual time span in the calendar.
-   **[Define business calendar filtering options](../task/define-business-calendar-filtering-options.md)**  
Define date and time filtering options for a business calendar. These filtering options are in addition to the standard date and time filtering in the ServiceNow AI Platform. You can provide your users with additional filtering options when they use the business calendar with ServiceNow AI Platform packages and functional areas.
-   **[Pair business calendars with packages](../task/pair-business-calendars-with-packages.md)**  
Pair a business calendar that you created with a package, or functional area, in the ServiceNow AI Platform. When you associate a business calendar with a package, it enables the use of the calendar in that specific functional area. Until you pair a business calendar definition with at least one package, it remains a definition record only.

**Parent Topic:**[Using time configuration](../using-time-configuration.md)

**Related topics**  


[Using schedules and calendars](../reference/r_CreateCalendarsWithSchedulePages.md)

