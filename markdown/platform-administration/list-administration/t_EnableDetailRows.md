---
title: Enable detail rows in lists
description: Show additional information about each record in a list by turning on detail rows and adding them to specific tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/list-administration/t\_EnableDetailRows.html
release: brazil
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Administer, List administration, Forms, fields, and lists, Configure core features, ServiceNow AI Platform]
---

# Enable detail rows in lists

Show additional information about each record in a list by turning on detail rows and adding them to specific tables.

## Before you begin

Role required: admin

## About this task

To display detail rows, an administrator must enable them globally and add them to lists.

## Procedure

1.  To enable detail rows, [add a new system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md) with the following field values.

    |Field|Value|
    |-----|-----|
    |Name|glide.ui.list.detail\_row|
    |Type|true \| false|
    |Value|true|

2.  To add detail rows to a list, complete the following steps.

    1.  Add the **detail\_row** [dictionary attribute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md) to the table.

        Specify the name of the field to display in the following format: `detail_row=short_description`

    2.  Use the **all\_tables** element descriptor with the **detail\_row** attribute to display detail rows for all child tables that contain the designated field.

        For example, **all\_tables.detail\_row=short\_description** is on the Task \[task\] table by default, so the short description detail row appears in lists for Incident \[incident\], Problem \[problem\], and other child tables unless you set **detail\_row** to a different field for each one.


**Related topics**  


[Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/c_UseLists.md)

[Altering tables and fields using dictionary attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/table-administration-and-data-management/c_DictionaryAttributes.md)

