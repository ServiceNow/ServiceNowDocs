---
title: Enable inclusion list auditing for a table
description: Enable a table to audit only those fields you explicitly designate. This is useful when you want to audit only a small number of fields in an audited table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring auditing for a table, Auditing]
---

# Enable inclusion list auditing for a table

Enable a table to audit only those fields you explicitly designate. This is useful when you want to audit only a small number of fields in an audited table.

## Before you begin

Role required: admin

The table must be [enabled for auditing](t_EnableAuditingForATable.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

    The system displays the list of dictionary entries. The list includes a row for each table as well as a row for each column \(field\) in the table.

2.  If necessary, customize the list view to show the **Attributes** column.

3.  In the list of dictionary entries, find the row corresponding to the table you want to audit, for example `cmdb_ci_computer`.

    You can distinguish the row for the table itself – versus a row for a column in the table – by finding the row with the correct table name, an empty entry for Column name, and a type of **collection**.

4.  In the **Attributes** field for that row, enter **audit\_type=whitelist**.


## What to do next

[Designate which fields you want to audit in this table.](security-whitelist-audit-field.md)

