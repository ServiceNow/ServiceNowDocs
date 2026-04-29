---
title: Automatic search query resubmission
description: When a search query returns too few results, AI Search automatically modifies and resubmits it with the goal of returning at least the desired number of results.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Automatic search query resubmission

When a search query returns too few results, AI Search automatically modifies and resubmits it with the goal of returning at least the desired number of results.

Search administrators configure the minimum number of desired results per search query using the **Search Results Limit** field in search application configurations. For more details, see [Create a search application configuration for AI Search](../task/create-search-app-config-ais.md).

## AND-to-OR search query resubmission

When a search query with conjunctive terms or phrases returns insufficient results, AI Search resubmits it with the default Boolean operator changed from AND to OR and displays results for the modified query.

For example, if a query for `hotel "conference room" suite` matches no results, AI Search resubmits it as `hotel OR "conference room" OR suite`. This less-restrictive query may match more results than the original query.

**Note:** If you set the **Boolean search operator to use when a search query includes multiple terms** \(**glide.ais.query.search\_operator**\) system property to **OR query**, AI Search doesn't resubmit search queries in this way because the initial search already treats all query terms and phrases as though separated by the `OR` operator.

When automatically resubmitting a search query in this way, AI Search adds a minimum match count restriction to the OR expression. The modified query only returns results that match at least half \(rounded up\) of the terms separated by OR operators. This restriction improves query performance and provides more relevant results.

For example, suppose a search query for `laptop can't access wi-fi network` returns no results. AI Search automatically resubmits the query as `laptop OR can't OR access OR wi-fi OR network`. Only records that match at least three of the five query terms appear as results for the resubmitted search.

## Conditions for automatic search query resubmission

Automatic search query resubmission ignores search queries that meet any of the following conditions.

-   The original search query only includes a single term.
-   The original search query includes 8 or more terms and returns at least one search result.

**Parent Topic:**[Searching in AI Search](use-ais.md)

