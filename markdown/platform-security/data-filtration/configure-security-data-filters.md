---
title: Create a security data filter
description: Learn how to create security data filter rules to grant your users' access to records are tables.
locale: en-US
release: zurich
product: Data Filtration
classification: data-filtration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security data filters, Access Management]
---

# Create a security data filter

Learn how to create security data filter rules to grant your users' access to records are tables.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Security Data Filters**.

2.  Click **New** in the **Security Data Filters** list.

3.  In the form, fill in the fields as needed.

<table id="table_l4z_lc1_w4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table name

</td><td>

The table that the security data filter applies to.

</td></tr><tr><td>

Description

</td><td>

Description of the security data filter rule.

</td></tr><tr><td>

Active

</td><td>

Sets the security data filter rule as active.**Note:** Keep security data filter rules inactive until you are ready to test to avoid unintentionally locking users out of records.

</td></tr><tr><td>

Show in UI

</td><td>

Determines whether a notification will be displayed in the UI if the security data filter applies to a query

</td></tr><tr><td>

Application

</td><td>

The application scope of the security data filter.

</td></tr><tr><td>

Mode

</td><td>

The mode of the data filter.

</td></tr><tr><td>

Filter

</td><td>

The filter condition that determines which records the data filter applies to

</td></tr><tr><td>

Security Attributes

</td><td>

The security attributes that control if the data filter will apply or not

</td></tr></tbody>
</table>4.  Select **Save** from the form menu.


## Result

After you have saved your security data filter rule, this rule automatically applies to all records on the selected table, unless specified otherwise by the data condition.

