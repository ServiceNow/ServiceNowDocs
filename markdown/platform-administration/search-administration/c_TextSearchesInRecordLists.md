---
title: List search finds records from the current table
description: Search records from a table list view.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/c\_TextSearchesInRecordLists.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Available search options, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# List search finds records from the current table

Search records from a table list view.

Indexed tables display the for text option in the list title bar, which searches all records for matching field values.

\[Omitted image "sample-list-search-results.png"\] Alt text: Sample global text search from a list for the query "Oracle OR SAP".

The list search field accepts [Boolean operators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_BooleanOperators.md) \(AND, OR, and NOT\) in search queries. When a user adds a Boolean operator to a search query, the system only returns records that match all search conditions of the query.

The system also converts any search query into an equivalent keyword condition in the list breadcrumbs and filter. For example, searching for the text "Oracle OR SAP" produces the condition **\[Keywords\] \[are\] \[Oracle OR SAP\]**. The standard list controls can modify or remove these breadcrumbs and conditions.

**Parent Topic:**[Available search options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/c_IntroductionToSearching.md)

**Related topics**  


[Boolean operators allow conditional search results]()

[Quotation marks allow exact phrase searches]()

[Wildcard characters allow searching for patterns and variations]()

[Enable or disable the Zing junk filter]()

[Debug Zing]()

