---
title: Delete a function field
description: A user with the admin role can delete a function field from its table. Deleting a function field is useful if you want to create a function field with the same name as one that exists on that table.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Report on function fields, Advanced Core UI reporting topics, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Delete a function field

A user with the admin role can delete a function field from its table. Deleting a function field is useful if you want to create a function field with the same name as one that exists on that table.

## Before you begin

Role required: admin

Function fields are stored as columns on the table that you create them on. To delete a function field, you delete the associated column.

**Important:** &gt;No check is made on a where a function field is used when you delete. In addition, deleting a function field is not reversible.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select the table with the function field that you want to delete.

3.  Select the column to open its form.

4.  Select **Delete Column**.

    You can only delete the column if the **Column name** begins with `u_` or `x_`. If the **Column name** begins with something else, it was created by ServiceNow support. Contact support to delete it.


## Result

The function field is deleted and can no longer be used in data visualizations.

**Parent Topic:**[Report on function fields](../concept/function-fields-reporting.md)

