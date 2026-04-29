---
title: Tuning the semantic layer
description: The semantic layer maps natural language questions to ServiceNow AI Platform tables and fields. Tune the semantic layer to improve AI Data Explorer accuracy for your organization's terminology and data structure.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 2
keywords: [semantic layer, tuning, AI Data Explorer, query generation]
breadcrumb: [Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Tuning the semantic layer

The semantic layer maps natural language questions to ServiceNow AI Platform® tables and fields. Tune the semantic layer to improve AI Data Explorer accuracy for your organization's terminology and data structure.

The semantic layer identifies the best matching entities \(tables\), dimensions \(fields\), and segments \(filters\) when users ask questions in AI AI Data Explorer. Tuning improves these matches so users consistently get the right table, field, and filter.

## How the semantic layer works

When a user asks a question, the system identifies the best matching components and passes that context into query generation. The semantic layer has three building blocks:

-   **Entities**

    Represent tables such as Incident \[incident\], Change Request \[change\_request\], or CMDB Class Information \[cmdb\_class\_info\].

-   **Dimensions**

    Represent fields on those tables such as Priority, Assigned to, or State. Dimensions can follow reference fields across tables. For example, caller\_id.department traverses from an incident's caller to their department.

-   **Segments**

    Pre-defined filter conditions such as "Open incidents" = active=true.


## When to tune the semantic layer

Before you tune, verify that the issue is repeatable. The LLM occasionally makes incorrect decisions. Try the same question or a similar one multiple times first. Only tune if the problem is consistent.

Tune the semantic layer when:

-   The system selects the wrong table or cannot find one
-   A field is missing or the wrong field is selected
-   Your organization uses different terminology than the auto-generated labels
-   The right table or field is selected, but the query is constructed incorrectly
-   Special terminology of your organization is not translated accurately to filter conditions

## Validation and iteration process

1.  Capture the utterance and expected result.
2.  Classify the failure as entity, dimension, segment, or ACL.
3.  If results are wrong for only some users, verify read ACL access to the intended table and fields before retuning.
4.  Apply one targeted tuning change.
5.  Retest the same utterance.
6.  Check **Query Generation** &gt; **Logs** and confirm the improved match path.
7.  Repeat only if still incorrect.

-   **[Query Generation Health page](../../par-for-workspace/reference/querygen-health-page.md)**  
The health page shows the state of the Now LLM and AI Search, along with the states of Query Generation system properties, enabled products, and dependency plugins.
-   **[Semantic descriptions and labels](semantic-layer-descriptions-labels.md)**  
Semantic descriptions and labels are the primary fields that AI search uses to select the right table or field. Edit these fields when the system selects incorrect tables or fields.
-   **[Semantic usage instructions](semantic-usage-instructions.md)**  
Semantic usage instructions teach the system how to query data by defining matching strategies, expansion logic, and data conventions. Use these instructions when the right table or field is selected but the query is constructed incorrectly.
-   **[Database views for cross-table data](database-views-cross-table-data.md)**  
Database views combine fields from multiple tables into a single queryable entity. Add views to the semantic layer to answer cross-table questions in one query instead of requiring separate questions.
-   **[Segments in the Query Generation semantic layer](../../par-for-workspace/concept/querygen-segments.md#)**  
Segments are predefined filter conditions that map business terminology to specific query filters, helping the semantic layer translate natural language questions into accurate database queries.

**Parent Topic:**[Configuring Query Generation](../../par-for-workspace/concept/configuring-query-generation.md)

