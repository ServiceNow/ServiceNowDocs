---
title: Integrating AI Search into other ServiceNow AI Platform applications
description: AI Search integrates with other ServiceNow AI Platform applications. Populate your UI Builder pages with search components and customize display of search results and Genius Results with EVAM definitions. Improve incident deflection in Service Portal by configuring AI Search Assist for record producers.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 2
breadcrumb: [AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Integrating AI Search into other ServiceNow AI Platform applications

AI Search integrates with other ServiceNow AI Platform applications. Populate your UI Builder pages with search components and customize display of search results and Genius Results with EVAM definitions. Improve incident deflection in Service Portal by configuring AI Search Assist for record producers.

## UI Builder search components

AI Search provides components for search input, search results, search facets, and source facet bucket filters. You can add these components to your pages in UI Builder.

The AI Search components are described in detail on the [ServiceNow® Developer Site](https://developer.servicenow.com/):

-   [Search facets](https://developer.servicenow.com/dev.do#!/reference/now-experience/vancouver/shared-components/sn-search-facets/overview)
-   [Search input](https://developer.servicenow.com/dev.do#!/reference/now-experience/vancouver/shared-components/sn-search-combobox/overview)
-   [Search results](https://developer.servicenow.com/dev.do#!/reference/now-experience/vancouver/shared-components/sn-search-results-container/overview)
-   [Tab filter](https://developer.servicenow.com/dev.do#!/reference/now-experience/vancouver/shared-components/sn-tab-filter/overview)

For details on adding components to your pages in UI Builder, see [Add and configure components](https://www.servicenow.com/docs/access?context=add-components&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Entity View Action Mapping \(EVAM\) definitions

Entity View Action Mapping \(EVAM\) is a ServiceNow AI Platform application that standardizes how different data sources display records in cards and lists.

AI Search provides EVAM configurations that you can use to customize display of search results and Genius Results in Service Portal and your UI Builder pages.

You can customize EVAM settings to display AI Search results as a card grid view or as a list view. Users can page through large data sets of search results and see different views based on filtering.

For details on EVAM definitions, configurations, templates, and configuration bundles, see [Entity View Action Mapping \(EVAM\)](https://www.servicenow.com/docs/access?context=exploring-entity-view-action-mapper&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Service Portal record producer integration

AI Search Assist is a Service Portal widget that uses AI Search to improve incident deflection by displaying the most relevant set of related search results within a record producer. You can use AI Search Assist instead of Contextual Search.

For more details on the AI Search Assist widget, see [AI Search Assist record producer integration for Service Portal](ai-search-assist.md).

-   **[AI Search Assist record producer integration for Service Portal](ai-search-assist.md)**  
AI Search Assist is a Service Portal widget that uses AI Search to improve incident deflection by displaying the most relevant set of related Catalog Item and knowledge article search results within a record producer. You can use AI Search Assist instead of Contextual Search.

**Parent Topic:**[AI Search](overview-ais.md)

