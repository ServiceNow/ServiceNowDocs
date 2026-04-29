---
title: Create a business calendar group
description: For Performance Analytics and Reporting to use business calendars, organize several calendars into a business calendar group. An application might also contain a business calendar group.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating business calendars, Use, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a business calendar group

For Performance Analytics and Reporting to use business calendars, organize several calendars into a business calendar group. An application might also contain a business calendar group.

## Before you begin

Role required: business\_calendar\_admin

## About this task

You can base a Performance Analytics indicator or a report on business calendars instead of the standard calendar. The business calendars themselves are too granular in scale, and have to be grouped. The report or indicator then uses that group. Work with your Performance Analytics team to design the business calendar groups.

**Note:** Fiscal calendars are also supported. When you generate a fiscal calendar, a corresponding business calendar group is also generated automatically.

## Procedure

1.  Navigate to **All** &gt; **Business calendars** &gt; **Business calendar group**.

2.  Select **New**.

3.  Name the group and save it.

    The **Business calendars** related list appears.

4.  In the **Business calendars** related list, select **Edit**.

5.  Choose from existing business calendars to add to the group.

    You can also create a new business calendar from this list.

    **Important:** Do not select business calendars that cover a period shorter than a 24-hour day for use with Performance Analytics indicators. Performance Analytics does not store times, only dates. If only reports will use the group, you can select a shorter period.

6.  Select **Update** when finished.


## Gregorian calendar group

The Gregorian Calendar group comes with the base system. It includes the Week, Month, Quarter, and Year business calendars, which also come with the base system.

Each business calendar record \(Week, Month, Quarter, and Year\) also shows which groups it belongs to.

**Parent Topic:**[Creating business calendars](../concept/business-calendars.md)

**Related topics**  


["Indicators with business calendars" in Create an automated indicator](https://www.servicenow.com/docs/access?context=t_CreateAnAutomatedIndicator&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)

