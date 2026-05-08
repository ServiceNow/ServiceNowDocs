---
title: Indexed Source form
description: The Indexed Source form contains information about indexed sources defined for AI Search. Use this form when creating or modifying an indexed source.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed Source form

The Indexed Source form contains information about indexed sources defined for AI Search. Use this form when creating or modifying an indexed source.

For details on creating or modifying an indexed source, see [Create an indexed source](../task/create-indexed-source-ais.md).

<table id="ais-indexed-sources-table"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the indexed source.

</td></tr><tr><td>

Source

</td><td>

The ServiceNow AI Platform® table to index. AI Search excludes some ServiceNow AI Platform tables from indexing. You can't define indexed sources for these excluded tables or their derived tables. For a list of excluded tables, see [ServiceNow AI Platform tables excluded from AI Search indexing](excluded-tables-ais.md).

 To index content from a remote table, create an external indexed source. For more details on configuring indexed sources for external content, see [Indexing and searching external content in AI Search](../concept/external-content-ais.md).

 Plugins and applications can define multiple indexed sources for the same ServiceNow AI Platform table, but only one of them can be active at a time. For more details, see **Active**.

</td></tr><tr><td>

Active

</td><td>

Option to activate the indexed source. AI Search only indexes content and metadata from active indexed sources.**Note:** Only one indexed source can be active at a time for a given ServiceNow AI Platform table. The system makes duplicate indexed sources for a table inactive by default. Before you can make one of these duplicate sources active, you must edit the currently active source and make it inactive. AI Search only indexes content and metadata from active indexed sources.

</td></tr><tr><td>

Application

</td><td>

Application scope for the indexed source. This field is automatically set.

</td></tr><tr><td>

Retention Policy

</td><td>

Policy specifying a retention time limit for records from the source table. AI Search only indexes source records that were last updated within the specified time period, and purges records from the index when their time since last update exceeds the limit. If this field is empty, AI Search indexes source records regardless of their last updated date and retains them in the index indefinitely.

**Note:** This field is required when **Source** is set to the Task \[task\] table or any table that extends it.

</td></tr><tr><td>

Force Late Binding

</td><td>

Option to make AI Search use late binding security for all search results from the indexed source. This field isn't shown in the default Indexed Source form view. For instructions on configuring the form layout to show the field, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#).

 For an explanation of late binding security and its effects on search, see [Content security in AI Search](../concept/content-security-ais.md).

</td></tr><tr><td class="sub-head" colspan="2">

Condition

</td></tr><tr><td>

Filter

</td><td>

Optional filter conditions limiting the set of records to index from the source table. AI Search only indexes records that satisfy all defined filter conditions, and purges records from the index if they no longer satisfy these conditions.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

