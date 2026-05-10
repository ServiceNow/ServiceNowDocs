---
title: Add a dynamic JavaScript filter
description: Add a dynamic JavaScript statement for evaluation as part of a report visualization's filter criteria.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 5
breadcrumb: [Filter data visualizations with the condition builder, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Add a dynamic JavaScript filter

Add a dynamic JavaScript statement for evaluation as part of a report visualization's filter criteria.

## Before you begin

Role required: itil, report\_user, report\_group, report\_global, report\_admin, or admin. To create a meaningful report, you must have the right to access the data you want to report on.

## About this task

JavaScript filters can be single-line statements, or longer scripts. For longer JavaScript statements, create a script include that returns the correct format and data type, conforms to the specific data that the report should filter for, and is client callable. For more information, see [Script includes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/scripts/c_ScriptIncludes.md).

This table lists the operators supported by each field type that supports JavaScript filters. Field types that are not in this table do not support JavaScript filters and the **Value** field in the condition builder for those field types does not have the option to paste your own statements.

<table id="table_qhw_2dn_1vb"><thead><tr><th>

Field type

</th><th>

Allowed operators

</th><th>

Expected return data type

</th></tr></thead><tbody><tr><td>

Sys ID \(GUID\)

</td><td>

"is", "is not", "is one of", "starts with", "ends with", "contains", "does not contain", "between", "greater than or is", "less than or is".

</td><td>

Textual representation of a complete or partial sys\_id value.For the "is one of" operator, the expected return type would be either a comma-delimited list of sys\_id values or an array containing each sys\_id that should be included in the results.

</td></tr><tr><td>

Free Text String

</td><td>

"is", "is not", "is one of", "starts with", "ends with", "contains", "does not contain", "between", "greater than or is", "less than or is"

</td><td>

One or more textual characters. For the "is one of" operator, the expected result would be either a comma-delimited list of string values or an array containing each of the values to include in the "is one of" search value field.

</td></tr><tr><td>

Reference

</td><td>

"starts with", "ends with", "contains", "does not contain"

</td><td>

One or more textual characters that may represent some value or portion of a value found in this field in the table or data source.

</td></tr><tr><td>

String \(referencing another table\)

</td><td>

"contains", "starts with", "ends with", "does not contain"

</td><td>

One or more textual characters that may represent some value or portion of a value found in this field in the table or data source.

</td></tr><tr><td>

User Input

</td><td>

"is", "is not"

</td><td>

Textual characters that could represent the full value of some record for this field in the table or data source.

</td></tr><tr><td>

Table Name

</td><td>

"is", "is not", "is one of", "starts with", "ends with", "contains", "does not contain", "between", "greater than or is", "less than or is"

</td><td>

Textual representation of a complete or partial Table Name in the system. For the "is one of" operator, the expected return type would be either a comma-delimited list of Table Name values or an array containing each Table Name that should be included in the results.

</td></tr><tr><td>

Template Value

</td><td>

"is", "is not"

</td><td>

Textual characters that will fulfill the value as per a Template found on the instance.

</td></tr><tr><td>

Domain ID

</td><td>

"starts with", "ends with", "contains", "does not contain"

</td><td>

One or more textual characters that may represent some value or portion of a value found in the domain field in the table or data source.

</td></tr><tr><td>

User Roles

</td><td>

"is", "is not"

</td><td>

Textual representation of a user role string value.

</td></tr><tr><td>

Domain Path

</td><td>

"starts with", "ends with", "contains", "does not contain", "is", "is not", "is one of", "less than or is", "greater than or is", "between"

</td><td>

One or more textual characters that may represent some value or portion of a value found in this field in the table or data source. For the "is one of" operator, either a comma-delimited list of textual values or an array object containing each value that should be included.

</td></tr><tr><td>

Translated Text

</td><td rowspan="2">

"is", "is not", "is one of", "starts with", "ends with", "contains", "does not contain", "between", "greater than or is", "less than or is"

</td><td rowspan="2">

Textual value.For the "is one of" operator, the expected return type would be either a comma-delimited list of textual values or an array of textual values.

</td></tr><tr><td>

Translated Field

</td></tr><tr><td>

HTML

</td><td rowspan="2">

"contains", "does not contain"

</td><td rowspan="2">

Textual value which might correspond to data in the selected field in this report criteria.

</td></tr><tr><td>

HTML Template

</td></tr><tr><td>

Email Script

</td><td>

"contains", "does not contain"

</td><td>

Textual value representing a value that should \(or should not\) be in the Email Script field.

</td></tr><tr><td>

Script \(Plain\)

</td><td rowspan="3">

"contains", "does not contain"

</td><td rowspan="3">

Textual value representing a value that should \(or should not\) be in the Script field.

</td></tr><tr><td>

Script \(server side\)

</td></tr><tr><td>

Script

</td></tr><tr><td>

Short Table Name

</td><td>

"is", "is not"

</td><td>

Textual value \(under 40 characters\).For the "is one of" operator, the expected return type is either a comma-delimited list of textual values or an array containing each textual character that would represent a short table name.

</td></tr><tr><td>

Field Name

</td><td>

"is", "is not", "is one of", "starts with", "ends with", "contains", "does not contain", "between", "greater than or is", "less than or is"

</td><td>

Textual representation of a complete or partial field name value.For the "is one of" operator, the expected return type would be either a comma-delimited list of field name values or an array containing each field name that should be included in the results.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.

2.  Open the data visualization that you want to add the dynamic filter to and select **Edit**.

3.  In the **Configuration** panel, select the data source you want to filter.

4.  In the Filters, section, construct your filter condition.

    These combinations of field types and operators allow you to specify a dynamic JavaScript statement.

    **Note:**

    -   The "between" operator provides two fields that can support the same or different JavaScript URLs.
    -   The "is" operator can return an array of data elements of the expected type. In this case the operator is treated as the "is one of" operator.
    -   List fields do not support dynamic JavaScript filters.
5.  Choose a field type and operator and enter a JavaScript statement.

    -   For a one-line JavaScript statement, use the format `javascript:<JavaScript_Statement>;`.
    -   For a JavaScript statement that calls a script include, use the format `javascript:new <Record_Name>().<Function_Name>();` in which `Record_Name` corresponds to the record name of the script include and `Function_Name` is the function in the script include that returns the value compared in the filter.
    **Note:** The Javascript URL can also include one or more parameters passed to the function which performs the calculation and returns a result. For example, a JavaScript function that passes two parameters to the script include record could be written as `javascript:new TextJSFilter().getGroupIDs("Professional Services","Sales");`.


## What to do next

After you add the necessary JavaScript statements and conditions and configure the remainder of the report, test the report to ensure it returns and displays the expected results.

**Parent Topic:**[Filter data visualizations with the condition builder](../../reporting/task/filter-dv-condition-builder.md)

