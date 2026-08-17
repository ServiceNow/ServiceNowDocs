---
title: Indexed source guardrails
description: Reduce index size and increase search performance with guardrails that limit the number of task and alert source records indexed from indexed sources.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/indexed-source-guardrails-ais.html
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-07-02"
reading_time_minutes: 4
breadcrumb: [Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed source guardrails

Reduce index size and increase search performance with guardrails that limit the number of task and alert source records indexed from indexed sources.

## Guardrails overview

The Task \[task\] and Alert \[em\_alert\] tables and their child tables contain large numbers of records. Indexing the full set of records from these tables for search increases the size of the AI Search index and can impact performance for indexing and search.

To reduce index size and preserve indexing and search performance, AI Search applies guardrails when indexing records from these tables. These guardrails limit the maximum number of records that can be indexed from the Task and Alert tables.

Guardrails are enabled in the base system for the Task and Alert tables and their child tables. By default, AI Search indexes a maximum of 10 million records for each of these tables.

## How guardrails work

When guardrails are enabled, AI Search first checks the Guard Rail Limit for Indexed Data Sources \[`ais_guard_rail_limit_data_source`\] table to see whether a record exists for the indexed source \(defining the maximum number of records to index for that indexed source\). If no table entry exists, AI Search checks the `glide.ais.ingestion.guard_rails_enabled_datasources` system property value to see whether a limit is defined there for the indexed source. If no limit is found in either place, AI Search does not apply guardrail limits to the indexed source.

Guardrail limits on the number of records indexed are applied after the set of source records is limited by the indexed source's filter conditions and retention policy. For details on indexed source filter conditions and retention policies, see [Indexed source retention policies and filter conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/retention-policies-conditions-ais.md).

AI Search always indexes the most recently modified records from the indexed source table. If indexing causes the record count for the table to exceed the guardrail limit, AI Search discards older records from the index to make room for the newer records.

## Modifying guardrail settings

A ServiceNow® employee can modify guardrail settings for your instance as follows:

-   Override the base system record-count limits for the Task and Alert table guardrails
-   Create custom guardrails to limit the maximum number of records indexed from other source tables
-   Disable guardrails

**Note:** Changes to your instance's guardrail settings may take up to 24 hours to be reflected in AI Search's indexing behavior.

## Search performance considerations for indexing

Search performance for AI Search is affected by several customer-controlled factors related to content indexing. Changes to these factors can impact search performance as follows.

-   **Index size**

    Indexing more content produces a larger index, which takes more time to search. Avoid indexing content that isn't needed for search.

    Indexing large source tables, such as the Task \[task\] table and tables that extend it, can add significant numbers of records to the AI Search index.

-   **Number of indexed sources**

    An index with more indexed sources takes longer to search than one with fewer indexed sources. This is true even if the two indexes are the same size.

-   **Number of indexed fields**

    Increasing the number of fields you index across your indexed sources makes the system take longer to find search results. This effect is independent of index size and number of indexed sources.

-   **Indexing frequency**

    The more often your indexed content is synchronized and updated, the more often search will compete with indexing for compute resources, increasing search response time. This is especially pertinent for indexed sources with frequently modified fields.


## Indexed source retention policies and filter conditions

To limit the size of your index and the frequency of index updates, you can define retention policies and filter conditions for your indexed sources.

As an example, you can define a retention policy for an indexed source to exclude records that are more than two years old. This policy keeps your search results more current and reduces the size of your index. Changes made to the excluded records don't trigger index updates, so this policy also reduces indexing frequency.

Similarly, you can define a filter condition for an indexed source that excludes source table records with a specific status, such as Open. This filter condition reduces the number of records indexed from the source table, which in turn reduces the total amount of data you index. Excluding open records that have frequent updates also reduces indexing frequency.

AI Search also uses your retention policy and filter condition settings to automatically purge stale records from the index, reducing its size.

To learn more about creating retention policies and filter conditions for your indexed sources, see [Indexed source retention policies and filter conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/retention-policies-conditions-ais.md).

**Note:** Retention policies are required for indexed sources that index records from the Task \[task\] table or tables that extend it. They are optional for other indexed sources.

**Parent Topic:**[Indexed sources in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/indexed-sources-ais.md)

