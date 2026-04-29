---
title: Configuring search in a portal
description: Service Portal displays search results data within a widget on the search page. To make data searchable from Service Portal, you can fetch data from a single table within your ServiceNow instance, from multiple ServiceNow tables, or from an external site.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Configuring search in a portal

Service Portal displays search results data within a widget on the search page. To make data searchable from Service Portal, you can fetch data from a single table within your ServiceNow instance, from multiple ServiceNow tables, or from an external site.

## Search engines

-   **AI Search**

    AI Search provides a modern consumer-grade search engine that is faster and more assistive than the legacy Zing search engine. Portal users can find answers more quickly and easily with features like auto-complete search queries, natural language support, and typo handling. AI Search is only supported in Service Portal, Employee Center \(ESC\), Consumer Service Portal, and Customer Service Portal. Custom portals must be built off a baseline of one of these portals to have the AI Search capability.

-   **Zing**

    Zing is the legacy text indexing and search engine originally used by Service Portal. Some portals still use this search engine by default.


## Search analytics and suggestions

Generate relevant search suggestions for your users and monitor search analytics to understand what your users are searching for and whether they're finding what they need. Search Suggestions is a ServiceNow AI Platform feature. For more information, see [Search Suggestions](https://www.servicenow.com/docs/access?context=search-suggestions-overview&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

-   **Generate suggestions from custom widgets**

    By default, the Search Events \[sys\_search\_event\] and Search Source Events \[sys\_search\_source\_event\] tables collect search data from base system search widgets. To generate search analytics from custom Service Portal search widgets, use the GlideSPSearchAnalytics API. For more information, see [GlideSPSearchAnalytics](https://www.servicenow.com/docs/access?context=GlideSPSearchAnalyticsAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).


## Performance recommendations

To avoid performance degradation and to ensure a fast search experience for end users, follow these recommendations.

-   Limit search sources when possible to perform only the necessary query. For example, if a search only needs to return active incidents, add a condition to the search source set to **\[Active\]** **\[is\]** **\[true\]**. A search that queries only active incidents is faster than a search that queries all records in the incident table.
-   Create facet items and mapped queries with no more than 30 filter items. To verify, test each search source with a variety of keywords as a user with low permissions.

**Note:** Service Portal search results display as text only. HTML tags, images, and formatting do not display in search results.

-   **[AI Search in Service Portal](ai-search.md)**  
Configure the ServiceNow AI Search application for Service Portal so that portal users can take advantage of intelligent query features and quickly find the answers they need.
-   **[Zing search in Service Portal](zing-search-service-portal.md)**  
Service Portal search supports the ServiceNow Zing text indexing and search engine. Zing allows you to index and search record data by table and is created entirely with ServiceNow code and implemented within the relational model.

**Parent Topic:**[Configuring Service Portal](configuring-service-portal.md)

