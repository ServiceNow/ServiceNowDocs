---
title: Archive table schemas
description: Archive tables use the ar\_ prefix. Integer and reference fields become VARCHAR display values, dates are preserved, and journal fields are serialized.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/archive-table-schemas.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [archive table, schema, incident, problem, field types]
breadcrumb: [Reference, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Archive table schemas

Archive tables use the ar\_ prefix. Integer and reference fields become VARCHAR display values, dates are preserved, and journal fields are serialized.

## incident and ar\_incident

The `incident` table is typically one of the widest and most frequently archived tables on a ServiceNow instance. The following table shows how key fields differ between the live and archive tables.

|Field|`incident` \(live\)|`ar_incident` \(archive\)|
|-----|-------------------|-------------------------|
|`sys_id`|VARCHAR\(32\). Unique record identifier.|VARCHAR\(32\). Preserved on archive.|
|`number`|VARCHAR\(40\). For example, `INC0012345`.|VARCHAR\(40\). Same.|
|`state`|INTEGER. Choice list code. For example, `6` = Resolved.|VARCHAR. Display label. For example, `Resolved`.|
|`priority`|INTEGER. 1 \(Critical\) through 5 \(Planning\).|VARCHAR. Display label. For example, `1 - Critical`.|
|`assigned_to`|VARCHAR\(32\). `sys_id` of `sys_user` record.|VARCHAR. Display name. For example, `John Baker`.|
|`assignment_group`|VARCHAR\(32\). `sys_id` of `sys_user_group` record.|VARCHAR. Group name. For example, `Service Desk`.|
|`category`|VARCHAR. Choice field value. For example, `network`.|VARCHAR. Display label. For example, `Network`.|
|`cmdb_ci`|VARCHAR\(32\). `sys_id` of `cmdb_ci` record.|VARCHAR. CI name. For example, `PROD-ROUTER-01`.|
|`opened_by`|VARCHAR\(32\). `sys_id` of `sys_user` record.|VARCHAR. Display name.|
|`work_notes`|Not stored on the incident table. Stored as child records in `sys_journal_field`.|Serialized text stored directly in the archive row|
|`comments`|Not stored on the incident table — stored as child records in `sys_journal_field`|Serialized text stored directly in the archive row|
|`resolved_at`|DATETIME|DATETIME. Same.|
|`closed_at`|DATETIME|DATETIME. Same.|
|`resolve_time`|INTEGER. Minutes to resolve.|INTEGER. Same.|

## problem and ar\_problem

If a problem archive rule has run on the instance, the resulting archive table `ar_problem` follows the same structural conventions as `ar_incident`. The following table focuses on fields where the difference is most consequential for queries.

|Field|`problem` \(live\)|`ar_problem` \(archive\)|
|-----|------------------|------------------------|
|`state`|INTEGER. Choice code. For example, `4` = Resolved.|VARCHAR. Display label. For example, `Resolved`.|
|`priority`|INTEGER. 1 through 4.|VARCHAR. Display label. For example, `2 - High`.|
|`assigned_to`|VARCHAR\(32\). `sys_id` reference.|VARCHAR. Display name.|
|`assignment_group`|VARCHAR\(32\). `sys_id` reference.|VARCHAR. Group name.|
|`cause_notes`|CLOB. Stored on the problem record.|CLOB. Preserved in archive row.|
|`fix_notes`|CLOB — stored on the problem record|CLOB — preserved in archive row|
|`known_error`|BOOLEAN. True or false.|VARCHAR. `true` or `false`.|
|`related_incidents`|Relationship. Not stored as a column on the problem record.|Not present in archive. Relationship data is not preserved.|
|`workaround`|CLOB — stored on the problem record|CLOB — preserved in archive row|
|`opened_at`|DATETIME|DATETIME — same|
|`resolved_at`|DATETIME|DATETIME — same|
|`closed_at`|DATETIME|DATETIME — same|

**Note:** The `related_incidents` relationship is not preserved in the archive. Incident-to-problem relationships are maintained through the `problem_id` field on the incident record in the live table. In the archive this link is severed. If incident-to-problem linkage is required in a historical query, join `ar_incident.problem_id` to `ar_problem.sys_id` while both records are within the same archiving window.

## Verify archive table structure

Inspect the structure of any archive table before writing queries. Navigate to `sys_dictionary.list`, filter by **Name** equal to the archive table name such as `ar_incident`, and review the column definitions.

Through Live Connect, the following query returns all column names and types visible to the current service account for a specific archive table.

```
SELECT column_name, data_type
FROM information_schema.columns
WHERE table_name = 'ar_incident'
ORDER BY ordinal_position;
```

