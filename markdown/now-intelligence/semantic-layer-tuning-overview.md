---
title: Tuning the semantic layer
description: The semantic layer maps natural language questions to ServiceNow AI Platform tables and fields. Tune the semantic layer to improve AI Data Explorer accuracy for your organization's terminology and data structure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/semantic-layer-tuning-overview.html
release: brazil
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 3
keywords: [semantic layer, tuning, AI Data Explorer, query generation]
breadcrumb: [Configure, Query Generation, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Tuning the semantic layer

The semantic layer maps natural language questions to ServiceNow AI Platform® tables and fields. Tune the semantic layer to improve AI Data Explorer accuracy for your organization's terminology and data structure.

The [semantic layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md) identifies the best matching [entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md) \(tables\), [dimensions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md) \(fields\), and [segments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md) \(filters\) when users ask questions in AI Data Explorer. Tuning improves these matches so users consistently get the right table, field, and filter.

## How the semantic layer works

When a user asks a question, the system identifies the best matching components and passes that context into query generation. The semantic layer has three building blocks:

-   **Entities**

    Represent tables such as Incident \[incident\], Change Request \[change\_request\], or CMDB Class Information \[cmdb\_class\_info\].

-   **Dimensions**

    Represent fields on those tables such as Priority, Assigned to, or State. Dimensions can follow reference fields across tables. For example, caller\_id.department traverses from an incident's caller to their department.

-   **Segments**

    Pre-defined filter conditions such as "Open incidents" = active=true.


## When to tune the semantic layer

Before you tune, verify that the issue is repeatable. The [LLM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md) occasionally makes incorrect decisions. Try the same question or a similar one multiple times first. Only tune if the problem is consistent.

Tune the semantic layer when:

-   The system selects the wrong table or cannot find one. For example, the system could be processing queries on reference fields, and the referenced tables are missing from the semantic layer. For another example, the query could span more than one table, but not all the tables are included in the semantic layer.
-   A field is missing or the wrong field is selected.
-   Your organization uses different terminology than the auto-generated labels.
-   The right table or field is selected, but the query is constructed incorrectly.
-   Special terminology of your organization is not translated accurately to filter conditions.

## Validation and iteration process

1.  Through communication with the user who is reporting an issue, find out what their query \([utterance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/now-assist-platform-analytics-glossary.md)\) is, what sort of response they expected, and how the actual response differed from their expectations.
2.  Open **Query Generation** &gt; **Logs** and find the log that matches the user name, utterance, and date submitted. Capture the response and any error message. See [Query Generation logs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/query-generation-logs.md).
3.  If results are wrong for only some users, verify read ACL access to the intended table and fields before retuning. Also see [Enabling access to protected scope applications for AI Data Explorer and Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/enable-aide-secure-scope-apps.md).
4.  Classify the failure as entity, dimension, segment, or ACL.
5.  Apply one targeted tuning change.
6.  Retest the same utterance.
7.  Check **Query Generation** &gt; **Logs** and confirm the improved match path.
8.  Repeat only if still incorrect.

-   **[Query Generation Health page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/querygen-health-page.md)**  
The health page shows the state of the Now LLM and AI Search, along with the states of Query Generation system properties, enabled products, and dependency plugins.
-   **[Customizing semantic metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/customize-semantic-metadata.md)**  
Semantic metadata — descriptions, labels, and usage instructions — control how Query Generation interprets natural language questions. Customize these metadata to improve accuracy for your organization's terminology and data.
-   **[Database views for cross-table data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/database-views-cross-table-data.md)**  
Database views combine fields from multiple tables into a single queryable entity. Add views to the semantic layer to answer cross-table questions in one query instead of requiring separate questions.
-   **[Segments in the Query Generation semantic layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/querygen-segments.md)**  
Segments are predefined filter conditions that map business terminology to specific query filters, helping the semantic layer translate natural language questions into accurate database queries.

**Parent Topic:**[Configuring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/configuring-query-generation.md)

