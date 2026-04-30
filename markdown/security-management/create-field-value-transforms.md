---
title: Create Security Operations field value transforms
description: Field Value Transforms defines one transformation between provided source data, and the replacement value to use.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Operations field value transforms, Security Operations common functionality, Security Operations]
---

# Create Security Operations field value transforms

**Field Value Transforms** defines one transformation between provided source data, and the replacement value to use.

## Before you begin

Role required: sn\_sec\_cmn.basic or sn\_si.basic

## About this task

Define each transformation entry to apply either when there is a match to the search value, or when the search value is contained within the provided source data, or when no matches are found. Set a default value for when no match is found. If no default value is set, and no matches are found, the original source data is used.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Utilities** &gt; **Field Value Transforms**.

2.  Click **New**.

3.  Fill in the fields on the form, as appropriate.

<table id="table_fml_2hy_4y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the field value transform.

</td></tr><tr><td>

Description

</td><td>

Description for the field map.

</td></tr><tr><td>

Field Value Transform Entries

</td><td>

The table list of entries.1.  Under **Replace data**, double-click 'Insert a new row.'
2.  Choose one of the following:
    -   When the date for this field matches
    -   When the data for this field contains
    -   When no other transform entry matches the data \(default\)
3.  Click the green check mark.
4.  Double-click under **Search value**, add your search value.
5.  Click the green check mark.
6.  Double-click under **Replacement value** add the ServiceNow corresponding value.
7.  Repeat if necessary.


</td></tr><tr><td>

Active

</td><td>

Select this check box to activate the transform.

</td></tr><tr><td>

Application

</td><td>

Scope of the application.

</td></tr></tbody>
</table>4.  Click **Submit.**


**Parent Topic:**[Security Operations field value transforms](../concept/field-value-transforms.md)

