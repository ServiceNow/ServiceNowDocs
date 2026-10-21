---
title: Live tables and archive tables
description: When Live Archive moves records out of a live table, it stores them in a corresponding archive table with a different schema and storage format. Understanding these differences is essential for writing effective queries and interpreting results correctly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/live-tables-and-archive-tables.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [live tables, archive tables, columnar storage, flattened schema, immutability]
breadcrumb: [Live Archive, Explore, RaptorDB Professional, Extend ServiceNow AI Platform capabilities]
---

# Live tables and archive tables

When Live Archive moves records out of a live table, it stores them in a corresponding archive table with a different schema and storage format. Understanding these differences is essential for writing effective queries and interpreting results correctly.

## Structural differences

Live tables and archive tables differ fundamentally in how data is stored and structured. The following table summarizes the key differences.

|Live table|Archive table|
|----------|-------------|
|Row-oriented: all columns for a record are stored together|Columnar: all values for each column are stored together|
|Reference fields store `sys_id`|Reference fields store the display value by default, or `sys_id` when **Retain References** is enabled on the archive rule|
|Choice fields store integer codes|Choice fields store display labels|
|Journal fields stored as child records in `sys_journal_field`|Journal fields serialized directly into the archive row|
|Records are mutable|Records are immutable; restore to the live table to modify|
|Full relational structure intact|Flattened, self-contained schema|

## Flattened schema

When a record moves from a live table to an archive table, its relational structure is flattened. In a live table, a reference field such as `assigned_to` stores a `sys_id` pointer to a record in `sys_user`. Retrieving the assigned user's name requires a join.

In an archive table, the behavior of reference fields depends on the archive rule configuration. By default, when **Retain References** is not selected on the archive rule, reference fields are denormalized: the display value of the referenced record is stored directly in the archive row at the time of archiving. When **Retain References** is enabled, the `sys_id` is preserved, and joins to reference tables remain possible if the referenced records still exist on the instance.

Choice fields store their display labels rather than integer codes. Journal fields such as work notes and comments are serialized and stored as structured text within the archive record, rather than as separate child records in `sys_journal_field`.

The practical consequence is that archive tables are self-contained. A query against `ar_incident` does not require joins to resolve reference fields, the resolved values are already in the row. However, archive data reflects the state of referenced records at the time of archiving. If an assigned user's name changed after archiving, the archive record retains the original name.

## Type differences when combining live and archive data

Live and archive tables store the same field with different data types. Queries that combine both must normalize the values so that the columns align.

For the full list of type differences, see the table in [Structural differences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/live-tables-and-archive-tables.md). In a query, the difference is concrete: a live `state` value of `6` corresponds to an archive value of `Resolved`, and `assigned_to` holds a `sys_id` in the live table but a display name in the archive table.

Use the `DV()` function on the live side of a query to return the display value instead of the stored code or `sys_id`. For example, `DV(assignment_group)` returns the group name, which matches the value already stored in the archive table.

Fields that store the same type in both tables, such as `opened_at`, `closed_at`, and `resolve_time`, require no conversion.

**Note:** Without normalization, a `UNION ALL` across a live table and its archive counterpart returns mismatched values in the same column, integer codes from the live table and display labels from the archive table. Grouping and filtering on those columns produce incorrect results.

## Columnar storage format

Archive tables use a columnar storage format rather than the row-based format used by live tables. In a row-based store, all columns for a given record are stored together on disk. In a columnar store, all values for a given column are stored together, which means every `closed_at` timestamp, `priority` value, and `category` string are all adjacent to each other on disk.

A query that reads `priority`, `closed_at`, and `category` across millions of archived records does not need to read any other column data. On a wide table such as `incident`, which can have hundreds of fields, this reduces I/O significantly compared to an equivalent query on a live row-based table.

Columnar storage also compresses more effectively than row-based storage, typically achieving approximately 50% compression on archive data.

## Immutability

Records in archive tables are immutable. A record in `ar_incident` can't be updated or deleted while it resides in archive storage. To modify an archived record, restore it to the live table first. This constraint verifies the integrity of historical data for audit and conformance purposes.

## Query patterns suited to archive tables

Because of the columnar storage format and the flattened schema, archive tables perform well for specific query patterns and less well for others.

Archive tables perform well for:

-   **Column-selective aggregations.** Queries that aggregate a small number of columns across many rows. `COUNT`, `AVG`, `SUM`, `MIN`, `MAX` are fast because the database reads only the columns involved in the calculation.
-   **Filtered scans on date range or low-cardinality columns.** `WHERE` clauses on `opened_at`, `closed_at`, `state`, `priority`, or `category` allow the columnar engine to skip large portions of data.
-   **Trend and time-series analysis.** Queries that group by date parts and aggregate metrics over long time horizons read only the date column and metric column.
-   **Reporting on resolved dimensions.** Because reference fields are already resolved to display values, queries don't need joins to look up names, groups, or categories.

Archive tables perform less well for:

-   **Full record retrieval.** Queries that select all columns \(`SELECT *`\) or a large proportion of columns on a small number of rows are less efficient in columnar storage. For single-record lookups, use the platform's standard record view.
-   **Joins to live tables on sys\_id.** Reference fields in archive tables hold display values, not `sys_id` values. Joining on `sys_id` requires the `DV()` function or careful handling.

