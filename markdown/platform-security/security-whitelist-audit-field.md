---
title: Include a table field in auditing \(inclusion listing\)
description: Track a subset of fields in an audited table by add those fields to an inclusion listing.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring auditing for a table, Auditing]
---

# Include a table field in auditing \(inclusion listing\)

Track a subset of fields in an audited table by add those fields to an inclusion listing.

## Before you begin

Role required: admin

To add fields in a table to an inclusion list, you must have first [enabled auditing for that table](t_EnableAuditingForATable.md) and [enabled inclusion list auditing for that table](enable-whitelist-for-table.md).

## About this task

Add a set of fields to an inclusion list when you want to audit only a small number of an audited table's fields. If you need to audit most fields, and exclude only a few, follow the [exclusion list procedure](t_ExcludeAFieldFromBeingAudited.md) instead.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  If necessary, customize the list view to include showing the **Attributes** column.

3.  Navigate to the table and field \(column\) you want to the inclusion list.

4.  In the **Attributes** field, enter **audit=true**.


