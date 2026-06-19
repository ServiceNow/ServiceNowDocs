---
title: Exclude a field from being audited \(exclusion listing\)
description: Prevent the ServiceNow AI Platform from tracking a subset of fields in an audited table by excluding those fields from an audit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/t\_ExcludeAFieldFromBeingAudited.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Auditing]
---

# Exclude a field from being audited \(exclusion listing\)

Prevent the ServiceNow AI Platform from tracking a subset of fields in an audited table by excluding those fields from an audit.

## Before you begin

To exclude a field in a table from being audited, you must have first [enable auditing for that table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/t_EnableAuditingForATable.md).

Role required: admin

## About this task

Add a set of fields to an exclusion list when you want to audit most of the fields in an auditable table. If you want to audit only a few fields, follow the [inclusion listing procedure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/servicenow-ai-platform-security/security-whitelist-audit-field.md) instead.

**Note:** Disabling auditing on journal-based fields can impact the functionality of features, such as the Activity Formatter.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  If necessary, customize the list view to show the **Attributes** column.

3.  Navigate to the row corresponding to the table and field \(column\) you want to exclude from auditing.

4.  In the **Attributes** column for that row, enter `no_audit`.


