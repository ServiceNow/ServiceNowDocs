---
title: Configure search and navigation
description: You can use service catalog properties to configure search and navigation within the service catalog homepage.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Service catalog home page configuration, Service Catalog customization, Types of catalog items, Exploring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure search and navigation

You can use service catalog properties to configure search and navigation within the service catalog homepage.

Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **Properties** to view service catalog properties.

## Restrict search access

Each catalog homepage provides a search bar to help locate items not displayed on the homepage. By default, any user who can access the catalog homepage can search using this search bar.

To restrict access to this search function by role, use the **List of roles \(comma-separated\) that can search the service catalog** property \(**glide.sc.can\_search**\).

For example, to only allow logged-in users to access search, set this field to blank. To remove the search function for all users, set this field to **None**.

**Note:** Search results only show items that the logged-in user can access.

## Hide search results from inactive categories

By default, search results are returned from all categories, including inactive categories.

To avoid returning results from inactive categories, set the **Service catalog searches return items in inactive categories** property \(**glide.sc.search.disabled\_cats**\) to **No**. For example, when designing a new category, you can avoid users seeing search results from this category until you are ready to make it active.

**Note:** Security constraints can also make a category or catalog item inaccessible.

## Restrict search by item type

By default, a search field does not appear when viewing order guides, record producers, and wizard launchers.

To define which catalog item types do not show the search field, list these types in the **List of class names for catalog items that do not have the search field displayed** \(**glide.sc.item.cannot\_show\_search**\) property.

For example, to enable searching when viewing record producers, remove `sc_cat_item_producer` from this list.

![Service catalog search bar removed](../image/ServiceCatalogSearchBarRemoved.png "Service catalog search bar removed")

![Service catalog search bar enabled](../image/ServiceCatalogSearchBarEnabled.png "Service catalog search bar enabled")

## Enable breadcrumb links

By default, breadcrumbs appear without links when using content management pages as service catalog homepages.

To display these breadcrumbs with links, set the **Use links for breadcrumbs rendered in Service Catalog pages accessed via a CMS site** property \(**glide.sc.use\_breadcrumb\_links.cms**\) to **Yes**. This setting provides greater navigational control for end users.

## Disable search suggestions

By default, service catalog searches display "Did you mean?" suggestions if a search does not return any results and an alternate spelling or similar recent search does.

To disable these suggestions, set the **Specify whether search suggestions should be enabled** property \(**glide.sc.search.suggestions**\) to **No**.

-   **[Refine search results](../task/t_UsePropertiesToRefineSrchResult.md)**  
Use properties to refine search results in Service Catalog.
-   **[Configure keyword search for catalog items](../task/search-catalog-item.md)**  
When you search for a catalog item by a keyword in Service Catalog, the search results are displayed by considering a few fields of the catalog table.
-   **[Configure AI-based catalog search experience](../task/config-ai-search-cat.md)**  
Improve employee engagement with an AI-based catalog search experience in Service Portal and Now Mobile. Intelligent query features enable users to quickly and easily find the answers they need.

**Parent Topic:**[Service catalog home page configuration](c_ManagingTheHomepageForACatalog.md)

