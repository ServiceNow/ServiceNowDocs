---
title: Indexed sources in AI Search
description: Indexed sources designate ServiceNow AI Platform tables and external document sets with alphanumeric text and string field content that you want to make searchable. AI Search ingests text and string fields from table records or external documents and stores their searchable alphanumeric content in its search index.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-10-23"
reading_time_minutes: 6
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed sources in AI Search

Indexed sources designate ServiceNow AI Platform® tables and external document sets with alphanumeric text and string field content that you want to make searchable. AI Search ingests text and string fields from table records or external documents and stores their searchable alphanumeric content in its search index.

For instructions on creating an indexed source, see [Create an indexed source](../task/create-indexed-source-ais.md).

## Indexed source types

AI Search supports the following indexed source types.

-   **Internal indexed source**

    An internal indexed source retrieves alphanumeric content and metadata from text and string fields on ServiceNow AI Platform records. It includes a unique name and a reference to a ServiceNow AI Platform table with records that you want to make searchable. AI Search extracts and indexes searchable alphanumeric content and metadata from text and string fields on records in this table and in any of its child tables that you configure for indexing.

    AI Search excludes some ServiceNow AI Platform tables from indexing. You can't define indexed sources for these excluded tables or their derived tables. For a list of excluded tables, see [ServiceNow AI Platform tables excluded from AI Search indexing](../reference/excluded-tables-ais.md).

    You can't index [remote tables](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) with internal indexed sources. To index content from a remote table, create an external indexed source.

-   **External indexed source**

    An external indexed source retrieves alphanumeric content and metadata from text and string fields of documents in an external repository or a [remote table](https://www.servicenow.com/docs/access?context=remote-tables&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). It includes a unique name and a reference to an external content schema table instead of a ServiceNow AI Platform table. For more details on configuring indexed sources for external content, see [Indexing and searching external content in AI Search](external-content-ais.md).


**Note:** AI Search doesn't index Unicode characters from the High Surrogate Area \(code units in the range U+D800 to U+DBFF\). Characters from this range are replaced with spaces during indexing.

## Indexed source retention policies and filter conditions

Indexing large source tables, such as the Task \[task\] table and tables that extend it, can add large numbers of records to the AI Search index. To limit the set of records indexed from a source table, you can configure retention policies and filter conditions for your indexed sources. AI Search also uses these settings to automatically purge stale records from the index. For more information on retention policies and filter conditions, see [Indexed source retention policies and filter conditions](retention-policies-conditions-ais.md).

**Note:** Retention policies are required for indexed sources that index records from the Task \[task\] table or tables that extend it. They are optional for other indexed sources.

## Indexed source attributes and field settings

You can configure attributes and field settings for an indexed source to control indexing behavior for source records. Attributes control the indexed source's behavior at the record level, while field settings define its behavior for individual fields on indexed records. For more information, including lists of available attributes and field settings, see [Indexed source attributes for AI Search](indexed-source-attributes-ais.md#) and [Field settings for AI Search](field-settings-ais.md#).

## Indexing content from an indexed source

Once you define an indexed source, AI Search begins automatically indexing to reflect changes to records in the selected source table and its specified child tables. The results of all record create, update, and delete operations in these tables are reflected in the search index. AI Search doesn't index content from unmodified records in these tables until you perform a full table index. For more information on indexing behavior, including steps for full table indexing, see [Indexing content from AI Search indexed sources](indexing-content-ais.md).

**Note:** The pre-configured indexed sources included with AI Search only index content from text and string fields on source records. When searching records from these indexed sources, you can use numeric fields to facet or filter your search results, but you can't find records using their numeric field values. To search on a record's numeric field values, copy them into a text or string field so they can be indexed.

## Indexing content from knowledge articles

When indexing content from records in the Knowledge \[kb\_knowledge\] table, AI Search defaults to including content defined in knowledge blocks. Administrators can override this default behavior and configure AI Search to exclude content from knowledge blocks when indexing knowledge articles. For details on making this change, see [Exclude knowledge block content from the AI Search index](../task/exclude-know-blocks-ais-index.md).

## Multiple indexed sources for the same ServiceNow AI Platform table

You can't create more than one indexed source for a single ServiceNow AI Platform table. However, plugins and applications may define duplicate indexed sources for a ServiceNow AI Platform table. For example, the base system includes an indexed source defined for the User \[sys\_user\] table, but a plugin or application might define a second indexed source for this table under a different name.

**Note:** Only one indexed source can be active at a time for a given ServiceNow AI Platform table. The system makes duplicate indexed sources for a table inactive by default. Before you can make one of these duplicate sources active, you must edit the currently active source and make it inactive. AI Search only indexes content and metadata from active indexed sources.

-   **[Create an indexed source](../task/create-indexed-source-ais.md)**  
Define an indexed source to make content and metadata from ServiceNow AI Platform® table records searchable using AI Search.
-   **[Indexed source retention policies and filter conditions](retention-policies-conditions-ais.md)**  
AI Search uses settings to automatically purge stale records from the index and optimize search performance. To limit the set of records indexed from source tables, you can configure retention policies and filter conditions for your indexed sources.
-   **[Indexed source guardrails](indexed-source-guardrails-ais.md)**  
Reduce index size and increase search performance with guardrails that limit the number of task and alert source records indexed from indexed sources.
-   **[Semantic index configuration for indexed sources](semantic-index-cfg-ais.md)**  
The AI Search generalized RAG \(Retrieval-Augmented Generation\) framework offers a streamlined way to configure semantic indexing settings for records indexed from ServiceNow AI Platform® tables.
-   **[Exclude knowledge block content from the AI Search index](../task/exclude-know-blocks-ais-index.md)**  
Prevent AI Search from indexing content found in your knowledge blocks.
-   **[Activate indexing of catalog variable content on Catalog Item records](../task/activate-catalog-variable-indexing.md)**  
Activate indexing of searchable content from variables on Catalog Item records. Configure the set of Catalog Items eligible for catalog variable indexing and the set of variables to index.
-   **[Indexed source attributes for AI Search](indexed-source-attributes-ais.md#)**  
An indexed source attribute defines indexing behavior for all records from an indexed source.
-   **[Field settings for AI Search](field-settings-ais.md#)**  
A field setting controls indexing behavior for a specified field \(column\) on all records from an indexed source.
-   **[Indexing content from AI Search indexed sources](indexing-content-ais.md)**  
AI Search indexes records on indexed source tables to make their content searchable.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

