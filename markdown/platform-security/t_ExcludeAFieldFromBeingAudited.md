---
title: Excluding a field from being audited \(exclusion listing\)
description: Prevent the ServiceNow AI Platform from tracking a subset of fields in an audited table by excluding those fields from an audit.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring auditing for a table, Auditing]
---

# Excluding a field from being audited \(exclusion listing\)

Prevent the ServiceNow AI Platform from tracking a subset of fields in an audited table by excluding those fields from an audit.

## Before you begin

Role required: admin

To exclude a field in a table from being audited, you must have first [enable auditing for that table](t_EnableAuditingForATable.md).

## About this task

Add a set of fields to an exclusion list when you want to audit most of the fields in an auditable table. If you want to audit only a few fields, follow the [inclusion listing procedure](security-whitelist-audit-field.md) instead.

**Note:** Disabling auditing on journal-based fields can impact the functionality of features, such as the Activity Formatter. For more information, see [KB0743142](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0743142%26sysparm_stack%3D%26sysparm_view%3D).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  If necessary, customize the list view to show the **Attributes** column.

3.  Navigate to the row corresponding to the table and field \(column\) you want to exclude from auditing.

4.  In the **Attributes** column for that row, enter `no_audit`.


