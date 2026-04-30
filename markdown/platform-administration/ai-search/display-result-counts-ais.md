---
title: Display search result counts on the results page for a search application
description: Display search result counts on the results page for AI Search applications that use Seismic components. Counts show the total number of matching search results and the number of matching results for each navigation tab.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-16"
reading_time_minutes: 2
breadcrumb: [Search application configurations, Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display search result counts on the results page for a search application

Display search result counts on the results page for AI Search applications that use Seismic components. Counts show the total number of matching search results and the number of matching results for each navigation tab.

## Before you begin

Role required: search\_application\_admin

## About this task

Search administrators can enable display of search result counts in AI Search applications that use Seismic components. With this option enabled, the results page for the search application displays matching search result counts in two locations:

-   The total number of results that matched the user's search
-   The number of matching search results for each search source displayed as a navigation tab

    **Note:** Navigation tabs with 1,000 or more matching search results display **1000+** as their result count.


![Service Portal results page showing result counts before result list and in navigation tabs.](../image/service-portal-result-counts-ais.png "Sample results page with results counts")

**Note:** Result counts indicate the number of results that matched the user's search. Late binding security can remove results after they’re counted, causing the actual number of displayed results to be lower than the count. For more information on late binding security, see [Content security in AI Search](../concept/content-security-ais.md).

Result counts are supported in search applications that use Seismic components. You can display search result counts in the following search applications:

-   Service Portal
-   Employee Service Center \(ESC\)
-   AI Search for Next Experience global and workspace search
-   Custom UI Builder applications that use Seismic UI components

Other search applications, such as Virtual Agent and Now Mobile, don't use Seismic components and so don’t support display of search result counts. For best results, don't enable search result counts for these search applications.

Search result counts are enabled by default for new search application configuration records. You only need to perform this procedure to enable search result counts for existing search application configuration records after upgrading from a previous release.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

2.  Select the record for the AI Search application that you want to display result counts for.

3.  Select the **Show Search Results Count** option.

4.  Select **Update**.


## Result

AI Search displays the total result count and navigation tab result counts on the results page for the selected search application.

**Parent Topic:**[Search application configurations](../concept/defining-search-app-cfgs-ais.md)

