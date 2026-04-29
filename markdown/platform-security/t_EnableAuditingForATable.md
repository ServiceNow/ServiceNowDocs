---
title: Configuring auditing for a table
description: You can enable table auditing to track changes to all or some of the table's fields.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Auditing]
---

# Configuring auditing for a table

You can enable table auditing to track changes to all or some of the table's fields.

## Before you begin

Role required: admin.

**Note:** Encrypted fields aren’t audited by design. This behavior isn’t configurable.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

    The system displays the list of dictionary entries. The list includes a row for each table as well as a row for each column \(field\) in the table.

2.  In the list of dictionary entries, find the row corresponding to the table you want to audit, for example `cmdb_ci_computer`.

    You can distinguish the row for the table itself – versus a row for a column in the table – by finding the row with the correct table name, an empty entry for the **Column** name, and a **Type** of **Collection**.

3.  Select the dictionary entry for the table.

    The system displays the dictionary entry form.

4.  Check the **Audit** check box.

5.  Select **Update**.


## What to do next

If you want to audit only a few fields in the table [Enable inclusion list auditing for a table](enable-whitelist-for-table.md). If you want to audit most – but exclude some – fields, see [Exclude a field from being audited \(exclusion listing\)](t_ExcludeAFieldFromBeingAudited.md).

