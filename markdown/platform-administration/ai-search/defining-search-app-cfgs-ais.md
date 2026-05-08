---
title: Search application configurations
description: A search application configuration specifies the search engine and settings to use for search in a ServiceNow AI Platform application. When you choose AI Search as an application's search engine, you can select a search profile for the application and configure its search result display and refinement settings.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search application configurations

A search application configuration specifies the search engine and settings to use for search in a ServiceNow AI Platform® application. When you choose AI Search as an application's search engine, you can select a search profile for the application and configure its search result display and refinement settings.

A search application configuration contains a reference to a search profile, along with settings that affect how search results are displayed to users of the application. The search profile specifies settings that determine how AI Search generates search results for a given search. To learn more about search profile configuration settings, see [Search profiles in AI Search](defining-search-profiles-ais.md).

Some ServiceNow AI Platform applications install their own AI Search application configurations when you activate them. For example, activating the Customer Service Management \(CSM\) application installs AI Search application configurations for the Customer Service Portal and Consumer Service Portal.

AI Search includes search application configurations for use in the following ServiceNow AI Platform applications:

-   Employee Center
-   Virtual Agent
-   Service Portal

You can modify existing search application configurations, or create and configure your own search application configurations with AI Search specified as the search engine.

For details on enabling AI Search and specifying search application configurations in supported applications, see [Enabling and configuring AI Search in ServiceNow AI Platform applications](enable-configure-apps-ais.md).

**Note:** When you view or edit search application configuration records, the system may display a warning message telling you to reindex one or more indexed sources. This reindexing process \(a one-time process for each indexed source listed\) is required to correctly populate search-based auto-complete suggestions. For more details on auto-complete suggestions, see [Auto-complete suggestions in AI Search applications](auto-complete-ais.md#).

-   **[Create a search application configuration for AI Search](../task/create-search-app-config-ais.md)**  
Create a search application configuration to specify AI Search as the search engine for a ServiceNow AI Platform® application. Select a search profile for the application to use. Configure the application's settings for refinement and display of search results.
-   **[Grouping attachment search results with their parent search results](grouping-attachment-srch-results-ais.md)**  
Search application administrators can control whether attachment search results appear grouped with their parent search results or whether they display on their own. By default, AI Search displays attachments grouped with their parent search results.
-   **[Create a facet in an AI Search application configuration](../task/create-facet-ais.md)**  
Define facets to refine your searches using categories dynamically generated from the current search results.
-   **[Show search result counts for facets on the results page for a search application](../task/display-result-counts-ais.md)**  
Display search result counts for facets on the results page for AI Search applications that use Seismic components. Search result counts for facets show the number of matching search results for each source facet bucket.
-   **[Clear facet filters when selecting a new source facet bucket](../task/persist-facets-nav-tabs-ais.md)**  
Specify whether AI Search applications should preserve existing facet filters when you select a new source facet bucket.
-   **[Configure source facet buckets in an AI Search application configuration](../task/config-nav-tabs-ais.md)**  
Define settings for source facet buckets in a search application configuration. Users of the application can select source facet buckets to refine their search query results by search source.
-   **[Auto-complete suggestions in AI Search applications](auto-complete-ais.md#)**  
Automatically display intelligent suggestions in your search application's input field, helping users formulate their searches or jump directly to relevant results. Suggestions can include relevant search results, popular queries, recent queries from the user's personal history, and popular search results.
-   **[Using search scripted post-processors in AI Search application configurations](script-post-process-ais.md#)**  
Use scripted post-processors to modify search result records for display in a search application.
-   **[Search result sort options in AI Search application configurations](sort-options-srch-app-cfg-ais.md#)**  
A search result sort option enables users to display search results in an order determined by their field values. Applying a search result sort option overrides the default AI Search relevancy-based result order. You can define custom search result sort options for your AI Search applications.

**Parent Topic:**[Configuring AI Search](configuring-ais.md)

