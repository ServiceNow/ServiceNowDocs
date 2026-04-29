---
title: Indexed source retention policies and filter conditions
description: AI Search uses settings to automatically purge stale records from the index and optimize search performance. To limit the set of records indexed from source tables, you can configure retention policies and filter conditions for your indexed sources.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Indexed sources, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Indexed source retention policies and filter conditions

AI Search uses settings to automatically purge stale records from the index and optimize search performance. To limit the set of records indexed from source tables, you can configure retention policies and filter conditions for your indexed sources.

## Indexed source retention policies

Indexing large source tables, such as the Task \[task\] table and tables that extend it, can add significant numbers of records to the AI Search index. To limit the set of source table records indexed based on the time since they were last updated, select a retention policy for your indexed source. AI Search only indexes source records updated within the time period defined for the retention policy. For example, if you select a two-year retention policy, AI Search excludes source records that were last updated more than two years ago.

When the time since a source record's last update exceeds the limit from the indexed source's retention policy, AI Search marks the corresponding indexed record as stale.

**Note:** Retention policies are required for indexed sources that index records from the Task \[task\] table or tables that extend it. They are optional for other indexed sources.

## Indexed source filter conditions

To limit the set of records indexed from a source table, define filter conditions for your indexed source. AI Search only indexes records that match all defined filter conditions.

When a source record no longer satisfies the indexed source's filter conditions, AI Search marks the corresponding indexed record as stale.

## Purging stale records

AI Search automatically purges stale records from the index daily. Users with the admin role can manually purge stale records. For details on this procedure, see [Purge stale records from the AI Search index](../task/purge-stale-records-ais-index.md).

-   **[Purge stale records from the AI Search index](../task/purge-stale-records-ais-index.md)**  
Execute a scheduled job to delete stale records from the AI Search index.

**Parent Topic:**[Indexed sources in AI Search](indexed-sources-ais.md)

