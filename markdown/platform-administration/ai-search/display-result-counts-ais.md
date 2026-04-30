---
title: Show search result counts for facets on the results page for a search application
description: Display search result counts for facets on the results page for AI Search applications that use Seismic components. Search result counts for facets show the number of matching search results for each source facet bucket.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-03"
reading_time_minutes: 3
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Show search result counts for facets on the results page for a search application

Display search result counts for facets on the results page for AI Search applications that use Seismic components. Search result counts for facets show the number of matching search results for each source facet bucket.

## Before you begin

The search application configuration must not have hybrid search enabled. When hybrid search is activated in a search application configuration, search result counts for facets aren't displayed in that search application configuration. For more information on hybrid search, see [Hybrid search in AI Search](../concept/hybrid-search-ais.md).

Role required: search\_application\_admin

## About this task

Search administrators can enable display of search result counts for facets in AI Search applications that use Seismic components. With this option enabled, the results page for the search application shows the number of matching search results for each search source displayed as a source facet bucket.

Because the late binding security implementation may have removed some search results that aren't accessible, search result counts are shown as a minimum value. As an example, a count of `6+` on a source facet bucket means that there are at least six search results from the specified source, but that there may be more.

**Note:** Source facet buckets with 1,000 or more matching search results display **1000+** as their result count. When search result counts for facets are enabled, source facet buckets with 0 matching search results aren't shown on the search results page.

To learn more about content security in AI Search and how the late binding security implementation can affect search result counts, see [Content security in AI Search](../concept/content-security-ais.md).



**Note:** Search result counts for facets indicate the number of results that matched the user's search. Late binding security can remove results after they’re counted, causing the actual number of displayed results to be lower than the count. For more information on late binding security, see [Content security in AI Search](../concept/content-security-ais.md).

Search result counts for facets are supported in search applications that use Seismic components. You can display search result counts for facets in these search applications:

-   Service Portal
-   Employee Service Center \(ESC\)
-   AI Search for Next Experience global and workspace search
-   Custom UI Builder applications that use Seismic UI components

Other search applications, such as Virtual Agent and Now Mobile, don't use Seismic components and so don’t support display of search result counts for facets. For best results, don't enable search result counts for facets in these search applications.

Search result counts for facets are enabled by default for new search application configuration records. You only need to perform this procedure to enable search result counts for facets in existing search application configuration records after upgrading from a previous release.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Select the record for the AI Search application that you want to display result counts for.

3.  Select the **Show counts for facets** option.

4.  Select **Update**.


## Result

AI Search displays source facet bucket result counts on the results page for the selected search application.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

