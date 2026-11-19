---
title: Create an indexed source
description: Define an indexed source to make content and metadata from ServiceNow AI Platform table records searchable using AI Search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/create-indexed-source-ais.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-23"
reading_time_minutes: 3
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Create an indexed source

Define an indexed source to make content and metadata from ServiceNow AI Platform® table records searchable using AI Search.

## Before you begin

Role required: ais\_admin

## About this task

When you create an indexed source, you specify a ServiceNow AI Platform table. AI Search indexes alphanumeric content and metadata from text and string fields found on records in the specified source table, making that content and metadata available for inclusion in search sources.

**Note:** AI Search doesn't index Unicode characters from the High Surrogate Area \(code units in the range U+D800 to U+DBFF\). Characters from this range are replaced with spaces during indexing.

By default, AI Search indexes alphanumeric content and metadata from all text and string fields found on records in the specified source table. You can limit which records are indexed by configuring a retention policy and filter conditions for the indexed source. For more information about retention policies and filter conditions, see [Indexed source retention policies and filter conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/retention-policies-conditions-ais.md).

**Note:** Retention policies are required for indexed sources that index records from the Task \[task\] table or tables that extend it. They are optional for other indexed sources.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Index** &gt; **Indexed Sources**.

2.  Select **New**.

3.  On the Indexed Source form, fill in the fields.

    For a description of the field values, see [Indexed Source form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/indexed-source-form-ais.md).

    **Note:** You can't create more than one indexed source for a single ServiceNow AI Platform table.

4.  Select **Submit**.

    The new indexed source appears in the AI Search Indexed Sources list with the **State** set to **New**. If the new indexed source requires manual indexing, an informational message and an alert triangle icon \[Omitted image "icon-alert-triangle.png"\] Alt text: appear.

5.  To configure indexing for child tables of the selected source table, open the new indexed source and create a related list record for each child table:

    1.  In the Child Tables related list, select **New**.

    2.  On the Child Table form, fill in the fields.

        For a description of the field values, see [Child Table form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/child-table-form-ais.md).

    3.  Select **Submit**.

        The new child table appears in the Child Tables related list.


## What to do next

To control how your new indexed source processes source records and fields during indexing, configure its indexed source attributes and field settings. For more information, see [Indexed source attributes for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/indexed-source-attributes-ais.md) and [Field settings for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/field-settings-ais.md).

To make content from source records searchable, perform a full table index for your new indexed source. For details on this procedure, see [Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/index-single-source-ais.md).

**Parent Topic:**[Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/indexed-sources-ais.md)

