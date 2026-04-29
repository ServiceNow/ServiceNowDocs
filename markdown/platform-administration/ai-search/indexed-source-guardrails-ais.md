---
title: Indexed source guardrails
description: Reduce index size and increase search performance with guardrails that limit the number of task and alert source records indexed from indexed sources.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed source guardrails

Reduce index size and increase search performance with guardrails that limit the number of task and alert source records indexed from indexed sources.

## Guardrails overview

The Task \[task\] and Alert \[em\_alert\] tables and their child tables contain large numbers of records. Indexing the full set of records from these tables for search increases the size of the AI Search index and can impact indexing and search performance.

To reduce index size and preserve search performance, AI Search applies guardrails when indexing records from these tables. These guardrails limit the maximum number of records that can be indexed from the Task and Alert tables.

Guardrails are enabled in the base system for the Task and Alert tables and their child tables. By default, AI Search indexes a maximum of 10 million records for each of these tables.

## How guardrails work

When guardrails are enabled, AI Search first checks the Guard Rail Limit for Indexed Data Sources \[`ais_guard_rail_limit_data_source`\] table to see whether a record exists for the indexed source \(defining the maximum number of records to index for that indexed source\). If no table entry exists, AI Search checks the `glide.ais.ingestion.guard_rails_enabled_datasources` system property value to see whether a limit is defined there for the indexed source. If no limit is found in either place, AI Search does not apply guardrail limits to the indexed source.

Guardrail limits on the number of records indexed are applied after the set of source records is limited by the indexed source's filter conditions and retention policy. For details on indexed source filter conditions and retention policies, see [Indexed source retention policies and filter conditions](retention-policies-conditions-ais.md).

AI Search always indexes the most recently-modified records from the indexed source table. If indexing causes the record count for the table to exceed the guardrail limit, AI Search discards older records from the index to make room for the newer records.

## Modifying guardrail settings

A ServiceNow® employee can modify guardrail settings for your instance as follows:

-   Override the base system record-count limits for the Task and Alert table guardrails
-   Create custom guardrails to limit the maximum number of records indexed from other source tables
-   Disable guardrails

**Note:** Changes to your instance's guardrail settings may take up to 24 hours to be reflected in AI Search's indexing behavior.

**Parent Topic:**[Indexed sources in AI Search](indexed-sources-ais.md)

