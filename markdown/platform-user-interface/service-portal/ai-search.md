---
title: AI Search in Service Portal
description: Configure the ServiceNow AI Search application for Service Portal so that portal users can take advantage of intelligent query features and quickly find the answers they need.
locale: en-US
release: zurich
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# AI Search in Service Portal

Configure the ServiceNow AI Search application for Service Portal so that portal users can take advantage of intelligent query features and quickly find the answers they need.

## AI Search features

-   **Powerful and flexible search**

    Unlike the legacy Zing search that was used in previous releases, AI Search is faster and more assistive. Portal users can find answers more quickly and easily with features like auto-complete search queries, natural language support, and typo handling.

    ![Search suggestions example](../image/ais-search-suggestions.png "Search suggestions")

    ![Typo handling example](../image/ais-typo-handling.png "Typo handling")

-   **Relevant and actionable search results**

    With AI Search enabled in Service Portal, the portal search engine captures information about the user — such as their role, location, department, assets, and search history — and returns search results that are relevant and personalized.

    AI Search also includes genius results that enable users to take action directly from the search results list.

    ![Genius result example](../image/ais-genius-result.png "Genius result")

-   **Intelligent search refinement**

    Portal users can refine their search results using dynamic and static filters. For example, if a user searches `Mac`, they can use facets to filter search results by hardware or user profiles.

    ![Search facets example](../image/ais-facets.png "Search facets")

    ![Tab filters example](../image/ais-tab-filters.png "Tab filters")

    For more information on using facets and tabs, see [Faceted Search widget](faceted-search.md).


For more information on AI Search features, see [Exploring AI Search](https://www.servicenow.com/docs/access?context=explore-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Activation information

AI Search is a ServiceNow AI Platform feature that is active by default.

AI Search is enabled in Service Portal for all new and zBoot customers by default.

If you are upgrading to Zurich as an existing customer, AI Search is disabled in Service Portal by default. You can enable it by updating the portal record. For more information, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

**Note:** Search widgets that you cloned or customized before a system upgrade may not be compatible with AI Search. You can resolve this issue by running a fix script that reclassifies search widget instances. For more information, see [Reclassify cloned or customized search widgets](../task/reclassify-search-widgets.md).

## Configuring AI Search for Service Portal

Configure AI Search in Service Portal by defining the following:

-   **Search application configuration**

    Defines search experience settings, such as the search engine, search results limit, and suggestions limit. For more information on defining a search application configuration, see [Defining search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **Search results configuration**

    Defines how search results are displayed. For more information on defining a search results configuration, see [Define a composite dataset](https://www.servicenow.com/docs/access?context=define-composite-dataset&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


You can change the search application configuration or search results configuration that your portal uses by updating the portal record. For more information, see [Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md).

To use a different search application or search results configuration for a specific search widget, update the widget instance options. AI Search is used in the following widgets:

-   [Homepage Search widget](home-page-search-widget.md)
-   [Typeahead Search widget](typeahead-search-widget.md)
-   [Faceted Search widget](faceted-search.md)
-   [Catalog Homepage Search widget](cat-homepage-search-widget.md)
-   [Knowledge Breadcrumbs widget](knowledge-breadcrumbs.md)

To configure the search results payload to navigate to and display the appropriate portal page for a selected data source, define an AI Search results action. For more information, see [Define an AI Search Results Action](../task/ais-results-action.md).

You can configure the action buttons in genius results by defining an Entity View Action Mapping \(EVAM\) action. For more information, see [Define an EVAM action](https://www.servicenow.com/docs/access?context=define-evam-action&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

You can customize the look and feel of the AI Search experience in Service Portal by updating the relevant CSS variables. For more information on these variables, see [Theming for AI Search in Service Portal](../reference/ais-sp-css-vars.md).

## Browser support

With AI Search enabled in Service Portal, users must log in with a modern browser such as Google Chrome, Mozilla Firefox, Microsoft Edge \(Chromium\), or Apple Safari.

-   **[Enable and configure AI Search in Service Portal](../task/enable-ais-sp.md)**  
Enable and define the AI Search experience in your portal.
-   **[Define an AI Search Results Action](../task/ais-results-action.md)**  
Configure which portal page opens when a result is selected from the list of search results.
-   **[Create a CSS include to override theming for AI Search in Service Portal](../task/css-override-ais-theming-sp.md)**  
Override theming for AI Search in Service Portal to match your company branding.

**Parent Topic:**[Configuring search in a portal](search-service-portal.md)

