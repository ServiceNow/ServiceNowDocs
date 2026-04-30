---
title: Using product catalogs
description: The product catalog provides a visual display of the available product offerings that can be added to a Sales Customer Relationship Management transaction, such as an opportunity, quote, or order. Use the catalog interface to add simple products and complex products that can be further customized.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-15"
reading_time_minutes: 3
breadcrumb: [Lead-to-cash foundation apps, Use, Sales Customer Relationship Management]
---

# Using product catalogs

The product catalog provides a visual display of the available product offerings that can be added to a Sales Customer Relationship Management transaction, such as an opportunity, quote, or order. Use the catalog interface to add simple products and complex products that can be further customized.

Agents use the Catalog tab \(related list\) for a transaction in the CSM Configurable Workspace to open the product catalog. Customers engaged in self-service transactions such as placing orders, use the product catalog in the Business Portal.

**Note:** When you start a lead, the Catalog tab displays only simple products that can be added and don't require further customization.

Starting with the Product Catalog Management Core v17.0.0 release, the product catalog interface supports semantic search queries powered by AI Search, in addition to keyword searches.

## Product catalog interface with simple search

The product catalog interface enables agents and customers to find product offerings by navigating product catalogs and categories. Or, they can use the search bar to match by product name, code, or description.

![Product catalog interface that shows the product catalog hierarchy, product tiles with product images, and search option.](../image/som-catalog-ui.png "Product catalog interface with simple search")

The catalog view has the following features for selecting products:

-   **Catalog navigation tree**: Catalog and a list of its categories used to organize product offerings. Selecting a category filters the display and shows only the product tiles for that category.
-   **Search bar**: Option for finding product offerings using simple searches by product name, code, or description. The search feature displays the product tiles that match the product name, code, or search string \(description\).
-   **Product tiles**: Cards that depict each product, which has a brief description, optional image, and an option to add or customize the product offer. The **Add** option displays when the product is a simple \(fixed\) product offering. The **Customize** option displays for configurable product offerings that have different options and attributes that can be selected. Selecting **Customize** opens the product configurator for configuring the product offering.

## Product catalog interface with AI Search

AI Search in the product catalog interface enables agents and customers to find relevant product offerings by using semantic search queries, in addition to keyword searches.

Entering a query term or phrase in the search bar finds all catalog items that contain sedan as a characteristic, any parent products containing child products with this characteristic, and related products that have semantic similarity. In AI Search, semantic similarity means that the context of the query, such as the user, the catalog selected, and the terms entered, are evaluated to return the most useful catalog items first.

AI Search provides other features to enhance the search process:

-   **Search query language options**: Use Boolean operators, wildcards, and multi-term and quoted phrases in queries to broaden or narrow search results.
-   **Auto-complete suggestions:** When you start entering text in the search bar, AI Search displays auto-complete suggestions to help you get directly to the results you need. Suggestions may include recent search queries, recently viewed search results, or search queries or results that match the terms you're typing into the search bar.
-   **Auto-corrections of misspelled or incomplete words**: If your queries contain misspelled words or are incomplete, AI Search automatically replaces those search query terms with correct spellings, based on the search sources \(product offerings and service specifications\). Typo corrections are shown above search results.
-   Sort by filter: Organize how search results are returned, for example, by relevancy or product description. Control the order, descending or ascending, in which the results are displayed.

![AI Search features in product catalog interface: Sort by filter options, sort order, and search bar. Another example shows search bar with auto-complete suggestions.](../image/ai-search-bar-catalog.png "Product catalog interface with AI Search")

For more information on search queries and the search query language that you can use to find catalog items, see [Use AI Search in product catalogs](../task/use-ai-search-catalog.md).

**Note:** Check your entitlements to determine if you have access to this feature.

-   **[Use AI Search in product catalogs](../task/use-ai-search-catalog.md)**  
As an agent or customer, use AI Search queries in the product catalog to find relevant product offerings or service specifications. For example, you can search by product offering characteristics or other attributes, when adding products in Sales Customer Relationship Management transactions.

**Parent Topic:**[Using lead-to-cash foundation applications](using-lead-cash-foundation.md)

