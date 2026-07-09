---
title: Configure the date picker for the list editor
description: A system property enables you to choose between two date picker configurations for the list editor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/time-configuration/t\_ConfigureDatePickerForListEditor.html
release: yokohama
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Date and Date/Time fields, Exploring time configuration, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the date picker for the list editor

A system property enables you to choose between two date picker configurations for the list editor.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Search for the property named **glide.ui.list\_edit.show\_calendar\_only**.

3.  Set the property **Value** to either of the following options.

<table id="simpletable_kld_1xs_zs"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

false

</td><td>

Calendar as well as a field appears for a date picker for manual date entry.\[Omitted image "DatePickerFieldAndCalendar.png"\] Alt text: Date picker with field and calendar

</td></tr><tr><td>

true

</td><td>

Calendar only appears for a date picker, which is the default behavior in Core UI and UI15.\[Omitted image "DatePickerCalendarOnly.png"\] Alt text: Date picker with calendar only

</td></tr></tbody>
</table>
**Parent Topic:**[Date and Date/Time fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/time-configuration/r_UseDateAndTimeFields.md)

**Related topics**  


[List editor administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/list-administration/r_AdministeringTheListEditor.md)

