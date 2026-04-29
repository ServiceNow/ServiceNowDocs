---
title: Create a function field to perform a database function
description: Create a function field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Displaying function results, Work with database views, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a function field to perform a database function

Create a function field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.

## Before you begin

Role required: admin

You can either select a function field from a physical table or create a function field directly on the database view.

If you create a function field directly on the database view, you must use the variable prefixes from the database view in the function definition to identify the columns. Before you create the function field, take note of the variable prefixes in your database view.

For example, if the variable prefix for the Incidents table is `inc2` and you want to return the length of the description field, the function definition would be `glidefunction:length(inc2_description)`. If the variable prefix for the Metric Instance table is `mi` and you want to concatenate the Definition and Value fields, the function definition would be `glidefunction:concat(mi_definition.name,' ',mi_value)`.

For information on supported functions, see [Report on function fields](https://www.servicenow.com/docs/access?context=function-fields-reporting&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Select **New**.

3.  Select **Function field**.

4.  On the form, fill in the fields.

<table id="table_lbr_qbf_xtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table or database view to which the function field is added.If you select a database view, you must include the database view's variable prefixes in the **Function definition** field.

</td></tr><tr><td>

Type

</td><td>

The type of field: string, number, date, and so on.

</td></tr><tr><td>

Column label

</td><td>

The label for the column.

</td></tr><tr><td>

Column name

</td><td>

The name of the column. This field is automatically set to the value of the **Column label** field.

</td></tr><tr><td>

Max length

</td><td>

The maximum length of the return value.

</td></tr><tr><td>

Function field

</td><td>

If selected, creates a field that displays the results of a database function, such as a mathematical operation, field length computation, or day of the week calculation.Once the new function record is saved, you cannot clear the check box to make the field a regular field.

</td></tr><tr><td>

Function definition

</td><td>

The function that the field performs.The format for functions starts with `glidefunction:`, followed by the operation to be performed \(for example, `concat`\), followed by function parameters. Constants must be enclosed in single quotes.

 **Important:** If you create the function field on a database view and not a physical table, you must include the database view's variable prefixes in the **Function definition** field.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Create a Function field on the Incident Metric database view

In this example, a new Function field, CallerDesc, is added to the Incident Metric database view. The field concatenates the caller name, a hyphen, and the short description.

![Function field on the Incident Metric database view](../../../administer/table-administration/image/FunctionFieldDatabaseView.png)

The variable prefix `inc` is included because the function field is defined on the Incident Metric database view and not on a physical table. The prefix is necessary to distinguish which short\_description and caller\_id columns to use from the tables that are part of the database view.

## What to do next

[Display function results in a database view](display-function-results-in-a-database-view.md)

**Parent Topic:**[Displaying function results in a database view](displaying-function-results-in-a-database-view.md)

