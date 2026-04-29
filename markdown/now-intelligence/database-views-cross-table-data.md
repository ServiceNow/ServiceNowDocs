---
title: Database views for cross-table data
description: Database views combine fields from multiple tables into a single queryable entity. Add views to the semantic layer to answer cross-table questions in one query instead of requiring separate questions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 1
keywords: [database views, cross-table data, semantic layer, table configuration]
breadcrumb: [Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Database views for cross-table data

Database views combine fields from multiple tables into a single queryable entity. Add views to the semantic layer to answer cross-table questions in one query instead of requiring separate questions.

Database views in the semantic layer enable you to answer questions that join data across tables in a single query instead of requiring separate questions or complex queries.

## When to use database views

Use database views when:

-   Users ask questions that join data across tables, such as incidents and changes.
-   A cross-table report already exists as a database view.
-   The same fields from different tables keep appearing together in user questions.

## Implementation requirements

When working with database views:

-   You must be in the same application scope as the database view.
-   Add database views to Semantic Table Configuration the same way as regular tables. You need the sn\_query\_gen.admin role or higher.
-   Dimension names include a source-table prefix, such as inc\_number or chg\_priority.
-   Entity descriptions are auto-generated from the source tables and update automatically.
-   The Include child hierarchy setting has no effect for database views.

**Parent Topic:**[Tuning the semantic layer](semantic-layer-tuning-overview.md)

**Related topics**  


[Add a table to the semantic data layer](../../par-for-workspace/task/add-table-semantic-layer.md#)

