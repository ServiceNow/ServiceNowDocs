---
title: Create or modify a request filter
description: Create or modify a request filter for the requests page in the Employee Center.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Employee requests page, Setup task management and integration features, Configure, Employee Center, Employee Service Management]
---

# Create or modify a request filter

Create or modify a request filter for the requests page in the Employee Center.

## Before you begin

Role required: sn\_hr\_sp.esc\_admin

Each request filter is associated with a table that is an extension of the Task \[task\] table. You can use a condition builder to specify the conditions that a request must meet for it to appear on the user's requests page. You can also associate the request filter with a ticket page.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **My Request Filter**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_knk_r2j_qfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short Description

</td><td>

Description of the request filter.

</td></tr><tr><td>

Table Name

</td><td>

Name of the table that the request filter is associated with.**Note:** The table must be an extension of the Task \[task\] table.

</td></tr><tr><td>

Active

</td><td>

Check box to activate the request filter for use.

</td></tr><tr><td>

Applies to

</td><td>

Select one of the following:-   Desktop
-   Service Portal
-   Desktop/Service Portal
-   Mobile


</td></tr><tr><td>

Filter

</td><td>

Conditions that a request must meet to appear on the requests page in the Employee Center.When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

 **Note:** The conditions available to use are dependent on the table you select.

</td></tr><tr><td>

Portal page

</td><td>

Ticket page that the request filter is associated with.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


