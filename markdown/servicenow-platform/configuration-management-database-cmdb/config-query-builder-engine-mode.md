---
title: Set execution mode for running a query
description: Configure the execution mode to use when running a query. The execution mode setting determines whether the query runs using a performance-enhancing engine \(V2\) or the legacy engine \(V1\).
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-09-03"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set execution mode for running a query

Configure the execution mode to use when running a query. The execution mode setting determines whether the query runs using a performance-enhancing engine \(V2\) or the legacy engine \(V1\).

## Before you begin

Role required: cmdb\_query\_builder

## About this task

A query can run in either of the following execution modes:

-   V1: Runs the query using the legacy query execution engine.
-   V2: Runs the query using an enhanced query execution engine which is designed for improved performance and scalability.

**Note:** When running queries that contain 'OR' nodes, the format of the returned results is different between the two modes.

The system uses query-level settings and system-wide properties, and also checks the query structure, to determine which mode to use. The query-level setting described in this procedure has precedence over system property settings in the decision flow of which engine to use to run a query.

For more information, see [CMDB Query Builder engine execution modes](../concept/query-builder-engine-execution-mode.md).

## Procedure

1.  Navigate to **All** and then, in the navigation filter, enter `qb_saved_query.list` to open the Saved Queries table.

2.  In the Saved Queries list view, select the query for which you want to set execution mode.

3.  On the query's form, set **Query Execution Mode** to '**v1**' or '**v2**'.

4.  Select **Update**.


