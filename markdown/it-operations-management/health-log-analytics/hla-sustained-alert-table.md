---
title: Sustained alert table schema
description: Reference documentation for the sn\_occ\_sustained\_alerts table that stores sustained alert feedback configurations per metric.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/health-log-analytics/hla-sustained-alert-table.html
release: brazil
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [sustained alert table, schema, sn\_occ\_sustained\_alerts, Health Log Analytics]
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Sustained alert table schema

Reference documentation for the sn\_occ\_sustained\_alerts table that stores sustained alert feedback configurations per metric.

## Table overview

The `sn_occ_sustained_alerts` table stores per-metric sustained alert feedback configurations. Each record represents a sustained alert setting applied to a specific metric. The table supports multi-tenant deployments through domain separation and provides audit trail support through standard system fields.

## Table access and permissions

Access to the sustained alert table is controlled by role-based access control \(RBAC\) lists. Standard read, write, create, and delete operations are supported. Users with alert feedback permissions can create and modify sustained alert entries for metrics they have access to.

|Field name|Type|Description|
|----------|----|-----------|
|`metric_id`|String \(indexed\)|Full metric identifier and foreign key reference to the metric being configured. Required field. Indexed for fast lookup during detection evaluation.|
|`required_duration_minutes`|Integer|Minimum sustained duration threshold in minutes. Valid range: 1–120 minutes. The system requires anomalies to persist continuously for this duration before emitting a detection. Updates without creating a new record when feedback is reapplied.|
|`duration_mode`|Choice \(enum\)|Feedback mode indicator. Values: `adaptive` \(system-calculated duration based on signal characteristics\) or `manual` \(operator-selected duration\). Default: `adaptive`.|
|`sustain_count`|Integer|Counter tracking how many times sustained alert feedback has been applied to this metric. Auto-increments on each reapplication. Allows the system to learn from repeated operator feedback patterns.|
|`applied_by`|User reference|User who initially applied the sustained alert feedback. Captured for audit trail purposes.|
|`applied_at`|Timestamp|Date and time when the sustained alert feedback was first applied. Captured for audit trail purposes.|
|`expires_at`|Datetime \(nullable\)|Optional expiration timestamp. When set, the feedback automatically becomes inactive after this date. Default: null \(feedback does not expire\).|
|`active`|Boolean|Active status flag. Values: `true` \(feedback is evaluated\) or `false` \(feedback is deactivated\). Default: `true`. The system skips inactive entries during detection evaluation.|
|`sys_domain`|Domain reference|Multi-tenancy support field. Indicates which domain \(partition\) the record belongs to. Enforces domain isolation for all operations and queries.|
|`sys_created_by`|User reference|System-generated field capturing the user who created the record. Set automatically on record creation.|
|`sys_updated_by`|User reference|System-generated field capturing the user who last modified the record. Updated automatically on any change.|
|`sys_created_on`|Timestamp|System-generated field capturing the creation timestamp. Set automatically on record creation.|
|`sys_updated_on`|Timestamp|System-generated field capturing the last modification timestamp. Updated automatically on any change.|

## Constraints and validation

The sustained alert table enforces these constraints:

-   Metric uniqueness per domain: Each metric can have only one active sustained alert entry per domain. Reapplying feedback updates the existing record rather than creating a duplicate.
-   Duration range validation: `required_duration_minutes` must be between 1 and 120 minutes. Invalid values are rejected.
-   Domain isolation: All queries and operations are scoped to the active domain. Cross-domain access is blocked by ACL enforcement.
-   Expiration enforcement: Records with `expires_at` dates in the past are treated as inactive during detection evaluation, even if `active` is `true`.

## Performance characteristics

The sustained alert table is optimized for detection-time lookups:

-   Lookup performance: P95 query latency ≤ 50 milliseconds per metric lookup, enabled by indexing on `metric_id`.
-   Caching: The system caches sustained alert entries in memory with automatic invalidation when table records change, reducing database query load.
-   Feedback application: Single-alert feedback application responds in P95 ≤ 500 milliseconds; bulk feedback \(up to 50 alerts\) in P95 ≤ 2 seconds.

## Audit trail and history

All changes to sustained alert records are logged in the audit table. The following changes are tracked:

-   Record creation \(user, timestamp, initial configuration\)
-   Duration threshold modifications \(`required_duration_minutes` changes\)
-   Mode changes \(switches between adaptive and manual\)
-   Deactivation or removal \(record deletion or `active` flag changes\)
-   Expiration date updates

The `sys_created_by`, `sys_updated_by`, `sys_created_on`, and `sys_updated_on` fields provide basic audit information. For detailed change history, query the audit table using the sustained alert record's `sys_id`.

**Parent Topic:**[Health Log Analytics reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/health-log-analytics/hla-reference.md)

