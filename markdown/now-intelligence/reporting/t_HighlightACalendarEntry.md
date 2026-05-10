---
title: Change highlighting of calendar report events
description: Field styles control the highlighting of events in calendar reports. Manage field styles to change how highlighting works.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize calendar reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Change highlighting of calendar report events

Field styles control the highlighting of events in calendar reports. Manage field styles to change how highlighting works.

## Before you begin

Role required: admin.

## About this task

You can apply field styles for the table that a calendar is based on or field styles for the Task \[task\] table to a calendar. The field styles that are applied for calendar highlighting depend on the **glide.ui.report.extend\_calendar\_choices** system property.

You can change only the background color of calendar events. All other CSS is ignored. Events without a defined field style display a white background when highlighting is applied to a calendar report.

**Note:**

[Define field styles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DefineFieldStyles.md) for the appropriate table.

-   To define field styles for all calendar reports, define the style on the Task \[task\] table.
-   To define field styles that apply only to calendars that are a based on a specific table or report source, define the field styles on that table.

If calendar reports are configured to use field styles from their tables or report sources, these field styles override the Task \[task\] table styles.

## Procedure

1.  Navigate to **System UI** &gt; **Field Styles**.

2.  Filter the list to show the tables you want to address and then group the result by field name.

    ![Field styles table with filter button highlighted](../image/filter-field-styles-table.gif)

3.  Select the name of the table next to the field and value that you want to highlight.

    ![A section of the field styles list with the task table highlighted](../image/field-style-list-selection.png)

4.  Change the background-color value as desired.

    Color names and RGB values are both valid.

5.  Select **Update**.


**Parent Topic:**[Customize calendar reports](../concept/c_CustomizeCalendarReports.md)

**Related topics**  


[Configure how calendar entries look](t_ConfigureACalendarAttribute.md)

[Modifying and adding calendar report system properties](modify-add-calendar-sys-props.md#)

[Customize start and end dates](t_CustomizeAStartAndEndDate.md)

