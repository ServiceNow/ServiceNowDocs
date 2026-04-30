---
title: Administer detail rows
description: Detail rows provide additional information about records in a list.
locale: en-US
release: xanadu
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [List administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Administer detail rows

Detail rows provide additional information about records in a list.

## Before you begin

Role required: admin

## About this task

To display detail rows, an administrator must enable them globally and add them to lists.

**Note:** Detail rows are not supported in List v3.

## Procedure

1.  To enable detail rows, [add a new system property](../../reference-pages/reference/r_AvailableSystemProperties.md#) with the following field values.

<table id="table_esm_jyw_j1b"><tbody><tr><td>

Name

</td><td>

glide.ui.list.detail\_row

</td></tr><tr><td>

Type

</td><td>

true \| false

</td></tr><tr><td>

Value

</td><td>

true

</td></tr></tbody>
</table>2.  To add detail rows to a list, complete the following steps.

    1.  Add the **detail\_row** [dictionary attribute](../../reference-pages/concept/c_DictionaryAttributes.md) to the table.

        Specify the name of the field to display in the following format: `detail_row=short_description`

    2.  Use the **all\_tables** element descriptor with the **detail\_row** attribute to display detail rows for all child tables that contain the designated field.

        For example, **all\_tables.detail\_row=short\_description** is on the Task \[task\] table by default, so the short description detail row appears in lists for Incident \[incident\], Problem \[problem\], and other child tables unless you set **detail\_row** to a different field for each one.


**Parent Topic:**[List administration](../../core-configuration/concept/p_ListAdministration.md)

**Related topics**  


[Lists](https://www.servicenow.com/docs/access?context=c_UseLists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

[Altering tables and fields using dictionary attributes](../../reference-pages/concept/c_DictionaryAttributes.md)

