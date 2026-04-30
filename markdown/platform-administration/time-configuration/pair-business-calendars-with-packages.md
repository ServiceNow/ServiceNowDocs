---
title: Pair business calendars with packages
description: Pair a business calendar that you created with a package, or functional area, in the ServiceNow AI Platform. When you associate a business calendar with a package, it enables the use of the calendar in that specific functional area. Until you pair a business calendar definition with at least one package, it remains a definition record only.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating business calendars, Using time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Pair business calendars with packages

Pair a business calendar that you created with a package, or functional area, in the ServiceNow AI Platform. When you associate a business calendar with a package, it enables the use of the calendar in that specific functional area. Until you pair a business calendar definition with at least one package, it remains a definition record only.

## Before you begin

Role required: admin

## About this task

A package is an application, or generic set of functions, such as HR Service Delivery or Finance Close Automation, in the ServiceNow AI Platform. For example, if you created a fiscal calendar, you can associate it with the Finance Close Automation package.

**Note:** Within a single calendar package record, you can only associate a business calendar with a single package. To associate business calendars with multiple packages, you have to create multiple calendar package records. For example, if you created a fiscal calendar and want to associate it with the HR and Fixed Assets packages:

-   In the first record you create, in the **Calendar** field, select the fiscal year, and in the **Package** field, select **HR**.
-   In the second record you create, you again select the same fiscal calendar, and then select **Fixed Asset** in the **Package** field.

## Procedure

1.  Navigate to **All** &gt; **Business Calendar** &gt; **Calendars for Package**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Calendar|Name of the business calendar that you want to associate with a ServiceNow AI Platform package. Click ![Search button](../../search-administration/image/SearchIcon.png) to access Business Calendars where you can search for an existing business calendar. If there is no existing calendar, you can create a new one.|
    |Package|Name of the ServiceNow AI Platform package that you want to associate with the selected business calendar. Click ![Search button](../../search-administration/image/SearchIcon.png) to access Packages where you can search for an existing package. If there is no existing package, you can create a new one.|

4.  Click **Submit**.


## Result

A record is created in the Calendars for Package \(calendars\_for\_package\) table that associates the selected business calendar with a ServiceNow AI Platform package.

**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

