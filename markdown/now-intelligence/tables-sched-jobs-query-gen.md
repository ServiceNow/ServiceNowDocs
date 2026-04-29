---
title: Roles, tables, and scheduled jobs included with Query Generation
description: Several types of components are installed with Query Generation, including tables and scheduled jobs.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Roles, tables, and scheduled jobs included with Query Generation

Several types of components are installed with Query Generation, including tables and scheduled jobs.

## Roles included

<table id="table_zxs_4r3_1gc"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_query\_gen.user

</td><td>

Allows the person with the role to call the Query Generation service through the app they are using.

</td><td>

None, but applications that call Query Generation should contain this role in their own user roles.

</td></tr><tr><td>

sn\_query\_gen.admin

</td><td>

Allows the user to access the Query Generation tables like an admin user. Can configure sn\_query\_gen\_table\_config records and modify Entity and Dimension records as well as set up segments in the utterance bank.

</td><td>

-   sn\_nowassist\_admin.nsa.admin
-   ais\_admin
-   sn\_query\_gen.user

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_gsw_xm3_cgc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th><th>

Default frequency

</th></tr></thead><tbody><tr><td>

Generate Semantic Layer

</td><td>

Generates entities, dimensions, and segments. Cleans up unused segments and Entity and Source records. Segment generation works like the Sync Segments job.Runs when Query Generation is first installed and then on demand.

</td><td>

When first installed, then on demand

</td></tr><tr><td>

\[Query Generation\] Sync Segments Job

</td><td>

Generates segments from report sources, reports, indicator sources, modules, and filters. Synchronizes manual segments with segment table. Cleans up unused segments. Cleans up segments based on unused or otherwise ineligible reports, report sources, and indicator sources.

</td><td>

When first installed, then weekly, on Sundays

</td></tr><tr><td>

\[Query Generation\] Semantic Entity Auto-Scaling Job

</td><td>

Synchronizes entity activation states and helps with semantic entity scaling.

</td><td>

When first installed, then daily, at 20:23:00

</td></tr></tbody>
</table>## Tables installed

All tables require the admin role for access and are available under Query Generation in the Navigator.

<table id="table_isw_xm3_cgc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

 \[sn\_query\_gen\_entity\]

</td><td>

Representations of the tables that have semantic generation enabled for them \(explicitly or through their parent tables\) on the Semantic Table Configuration \[sn\_query\_gen\_table\_config\] table. Each Entity record corresponds to one supported table. Entity records are generated automatically, and this table is read-only.

</td></tr><tr><td>

Dimension

 \[sn\_query\_gen\_dimension\]

</td><td>

Representation of queryable columns for every table that an Entity record references. Each record corresponds to one column. Dimension records are generated automatically, and this table is read-only.

</td></tr><tr><td>

Segments\[sn\_query\_gen\_segment\]

</td><td>

Reusable definitions that provide non-obvious context, to assist the semantic layer or LLM to select the correct entity, dimension, and values. For example, in the utterance "How many open emergency change requests are there?", a segment identifies that "open" means "active=true" and "emergency" is a Type, not a Priority. Admins can add new segments, delete existing segments, or edit segment names and descriptions.

</td></tr><tr><td>

Manual Segment Configs\[sn\_query\_gen\_segment\_table\_config\]

</td><td>

Manually created segments. The \[Query Generation\] Sync Segments job syncs this table up to the Segments table.

</td></tr><tr><td>

Utterance bank\[sn\_query\_gen\_utterance\_bank\]

</td><td>

Predefined sentences and phrases mapped to database contexts and queries. User questions are compared to the utterance bank to see if a predefined mapping can apply. Admins can create, edit, and delete utterance banks.

</td></tr><tr><td>

AI Search Search Profile\[ais\_search\_profile\]

</td><td>

A container for all search experience configurations. A search profile is mapped to a specific experience you would like to expose in your app. Search Profile is  linked to a search box and can be used across applications. Admins can create, clone, and publish search profiles.

</td></tr><tr><td>

AI Search Indexed Sources\[ais\_datasource\]

</td><td>

Records on this table reflect what content users can search on. The content can be tables on the instance or external tables. You have the necessary indexed sources by default. The sn\_query\_gen.admin role or higher is necessary to edit this table. The most likely use case is if the system cannot find the correct table and not all the indexed queries are fully applied. For more information, see [Common AI Data Explorer issues and fixes](../../ai-data-explorer/concept/ai-data-explorer-troubleshooting.md).

</td></tr><tr><td>

Logs\[sn\_query\_gen\_log\]

</td><td>

A log of every call to Query Generation. For more information, see [Query Generation logs](../reference/query-generation-logs.md).

</td></tr><tr><td>

Semantic table configuration\[sn\_query\_gen\_table\_config\]

</td><td>

List of tables that Query Generation can search, whether semantic generation is enabled for that table, and whether child tables are included. Admins can create, edit, and delete these records. For more information, see [Add a table to the semantic data layer](../task/add-table-semantic-layer.md#).

</td></tr></tbody>
</table>**Parent Topic:**[Query Generation reference](query-generation-reference.md)

