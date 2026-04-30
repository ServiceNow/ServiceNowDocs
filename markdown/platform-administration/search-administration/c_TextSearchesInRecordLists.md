---
title: List search finds records from the current table
description: Search records from a table list view.
locale: en-US
release: yokohama
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List search finds records from the current table

Search records from a table list view.

Indexed tables display the for text option in the list title bar, which searches all records for matching field values.

![Sample global text search from a list for the query "Oracle OR SAP".](../image/sample-list-search-results.png "List search")

The list search field accepts [Boolean operators](c_BooleanOperators.md) \(AND, OR, and NOT\) in search queries. When a user adds a Boolean operator to a search query, the system only returns records that match all search conditions of the query.

The system also converts any search query into an equivalent keyword condition in the list breadcrumbs and filter. For example, searching for the text "Oracle OR SAP" produces the condition **\[Keywords\] \[are\] \[Oracle OR SAP\]**. The standard list controls can modify or remove these breadcrumbs and conditions.

**Parent Topic:**[Available search options](c_IntroductionToSearching.md)

**Related topics**  


[Boolean operators allow conditional search results](c_BooleanOperators.md)

[Quotation marks allow exact phrase searches](c_PhraseSearches.md)

[Wildcard characters allow searching for patterns and variations](c_Wildcards.md)

[Enable or disable the Zing junk filter](../task/t_DisableTheJunkFilter.md)

[Debug Zing](../task/t_DebugZing.md)

