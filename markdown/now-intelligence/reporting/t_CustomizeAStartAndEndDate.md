---
title: Customize start and end dates
description: You can configure calendar reports to support the spanning of multi-day events across calendar cells.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize calendar reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Customize start and end dates

You can configure calendar reports to support the spanning of multi-day events across calendar cells.

## Before you begin

Role required: dictionary admin or admin.

## About this task

A change request with a **Work Start** date on Monday and a **Work End** date on Tuesday is displayed on both days when viewed in a **Calendar** field. However, when two custom fields named **First Date** and **Last Date** are used, the same behavior doesn’t occur.

The code looks for an ending field with the same name as the start date field, except using the word end instead of start. If the custom fields are **My Start Date** and **My End Date**, the system correctly interprets the meaning of these fields because their names are the same except for the words start and end.

## Procedure

1.  Follow the steps in [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

2.  Enter the following values in the form to create the start date span field.

    |Field|Value|
    |-----|-----|
    |**Name**|`Calendar start date span`|
    |**Database column name**|`u_first_date → u_my_start_date`|
    |**Type**|Date|

3.  Add another field using the following values for the end date span field.

    |Field|Value|
    |-----|-----|
    |**Name**|`Calendar end date span`|
    |**Database column name**|`u_last_date → u_my_end_date`|
    |**Type**|Date|


**Parent Topic:**[Customize calendar reports](../concept/c_CustomizeCalendarReports.md)

**Related topics**  


[Configure how calendar entries look](t_ConfigureACalendarAttribute.md)

[Modifying and adding calendar report system properties](modify-add-calendar-sys-props.md#)

[Change highlighting of calendar report events](t_HighlightACalendarEntry.md)

