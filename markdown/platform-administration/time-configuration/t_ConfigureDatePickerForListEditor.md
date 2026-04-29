---
title: Configure the date picker for the list editor
description: A system property enables you to choose between two date picker configurations for the list editor.
locale: en-US
release: australia
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Date and Date/Time fields, Explore, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the date picker for the list editor

A system property enables you to choose between two date picker configurations for the list editor.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Search for the property **glide.ui.list\_edit.show\_calendar\_only**.

3.  Set the property **Value** to either of the following options.

    |Value|Description|
    |-----|-----------|
    |false|Calendar as well as a field appears for a date picker for manual date entry.|
    |true|Calendar only appears for a date picker, which is the default behavior in Core UI.|


**Parent Topic:**[Date and Date/Time fields](../reference/r_UseDateAndTimeFields.md)

**Related topics**  


[List editor administration](../../list-administration/reference/r_AdministeringTheListEditor.md)

