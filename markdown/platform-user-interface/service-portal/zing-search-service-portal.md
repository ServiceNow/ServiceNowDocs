---
title: Zing search in Service Portal
description: Service Portal search supports the ServiceNow Zing text indexing and search engine. Zing allows you to index and search record data by table and is created entirely with ServiceNow code and implemented within the relational model.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Configuring search in a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Zing search in Service Portal

Service Portal search supports the ServiceNow Zing text indexing and search engine. Zing allows you to index and search record data by table and is created entirely with ServiceNow code and implemented within the relational model.

To make data searchable from Service Portal, you create search sources that fetch data from a single table within your ServiceNow instance, from multiple ServiceNow tables, or from an external site.

## Search sources

A search source is a record that describes the behavior and source of searchable data. A search source defines:

-   Where to retrieve search data from.
-   Whether search suggestions can populate the search field based on user input.
-   How a search entry displays in the search result page.

Search sources have simple and advanced configurations.

-   **Simple**

    Define a table within your ServiceNow instance as a source of searchable data. To learn more, see [Define a search source](../task/add-table-search-source.md).

    When you create a simple search source, Service Portal uses the search engine settings configured on your instance. To learn more, see [Zing text indexing and search engine](https://www.servicenow.com/docs/access?context=c_ZingTextSearch&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Advanced**

    Define a data fetch script to return data. A data fetch script executes on the server and returns a result array to the search widget. This method is more complex, but offers complete power over how a search executes. You are not limited to querying single tables within ServiceNow and can define a script that fetches data from multiple tables, or from anywhere on the web. To learn more, review the [Tutorial: set up an external knowledge base search source](../task/search-sp-advanced-ext-kb.md).

    **Note:** Search facets may not behave as expected if integrated into an advanced search source that queries data from a non- ServiceNow site.


## Text index groups

A text index group defines how users see search results. For example, combine search results from several sources, or set the weight of certain fields. Text index groups are a ServiceNow AI Platform feature. To learn more, see [Configure multiple tables for indexing and searching](https://www.servicenow.com/docs/access?context=index-multiple-tables&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Associate a portal with a text index group to create common search rules and to combine search results from all search sources in the group. If you have a custom search source or portal, consider whether you want to use the base system **portal\_index\_group** text index group, or create your own text index group. The base system text index group includes the Catalog items and Knowledge tables. When a user searches for an item in Service Portal, they see combined results from these tables. To add an index group to a portal, see [Add a text index group to a portal](../task/create-text-index-group.md).

**Note:** Text index groups do not support external search sources.

## Search suggestions and typeahead search

Search suggestions replaces typeahead search in Service Portal. Update the **glide.service\_portal.search\_as\_you\_type\_behavior** system property to change this behavior. For more information, see [Enable and disable search suggestions](https://www.servicenow.com/docs/access?context=enable-search-suggestions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). Service Portal search widgets automatically use whichever feature you enable.

## Search facets

Enable your end users to filter search results for a more meaningful result set. Facets can return results based on:

-   Fields in a table such as **Active** or **Author**.
-   Query conditions such as **\[Updated\]\[After\]\[Last week\]**.

**Note:** Only set search facets for indexed fields. Fields that are not indexed may take longer to return results and are not optimized for a fast search experience. Learn more: [Configure a table for indexing and searching](https://www.servicenow.com/docs/access?context=configure-single-table-for-indexing&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Search facets render in the Faceted Search widget on the sp\_search page. In new instances, search facets are enabled by default. If upgrading from a previous release, enable search facets by activating a record in the Page Route Maps \[sp\_page\_route\_map\] table. See [Enable search facets](../task/enable-facets.md).

-   **Simple**

    Enable end users to refine search results for a simple search source. You can create facets for a table search source that return results based on field values or query conditions. See [Add facets to a simple search source](../task/create-search-filter.md).

-   **Advanced**

    Define facets for advanced search sources using the **Facet generation script** on the search source record. Use facet APIs to create facets and assign ServiceNow facet items or mapped queries to the facet.

    |API|Use|
    |---|---|
    |[SPScriptedFacetService - Scoped](https://www.servicenow.com/docs/access?context=SPScriptedFacetServiceScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|Creates a single or multi choice facet.|
    |[SPScriptedFacet - Scoped](https://www.servicenow.com/docs/access?context=SPScriptedFacetScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)|Defines facet items, filters, or mapped queries for the facet.|


-   **[Define a search source](../task/add-table-search-source.md)**  
Configure a basic search source to query data from an instance table, or configure an advanced data fetch script to query data across multiple tables and data sources, or to pull data from anywhere on the web.
-   **[Enable search facets](../task/enable-facets.md)**  
In new instances, search facets are enabled by default. If upgrading from a previous release, enable search facets by activating a record in the Page Route Maps \[sp\_page\_route\_map\] table.
-   **[Add facets to a simple search source](../task/create-search-filter.md)**  
Enable end users to refine search results for a simple search source. You can create facets for a table search source that return results based on field values or query conditions.
-   **[Disable facets for a search source](../task/disable-search-facets.md)**  
Disable facets for one or more search sources by adding a system property. Once disabled, the search source does not display search facets in the Faceted Search widget on the sp\_search page. You can disable facets for simple or advanced search sources.
-   **[Populate search suggestions in Service Portal](../task/populate-search-suggestions-sp.md)**  
If you are upgrading from a previous release, run a script to populate search suggestions with data from a platform search table to provide search suggestions to your users. Alternatively, you can wait until users search for keywords instead of running this script.
-   **[Add a text index group to a portal](../task/create-text-index-group.md)**  
Define how users see search results. For example, combine search results from several sources, or set the weight of certain fields.
-   **[Set the default portal search source](../task/default-search-sources.md)**  
Use the **glide.service\_portal.default\_search\_sources** system property to define default search sources.
-   **[Configure Search Sources available on a page](configure-contextual-search.md)**  
Use contextual search to limit search results for an instance of the type-ahead search widget.

**Parent Topic:**[Configuring search in a portal](search-service-portal.md)

