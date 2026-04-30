---
title: Configuring AI Search for the product catalog
description: Configure and manage the implementation of AI Search in the product catalog for Sales Customer Relationship Management.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-01"
reading_time_minutes: 5
breadcrumb: [Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Configuring AI Search for the product catalog

Configure and manage the implementation of AI Search in the product catalog for Sales Customer Relationship Management.

## How AI Search works in the catalog interface

AI Search in the product catalog for Sales Customer Relationship Management transactions enables agents and customers to use semantic queries combined with keyword queries to find relevant product offerings and service specifications.

AI Search looks across all product offerings and service specifications, including product characteristics, bundled product offerings, and child offerings, to return results in the product catalog interface.

For example, entering the term `sedan` finds any products that contain this characteristic, parent products containing child products with this characteristic, and related products that have semantic similarity to this search term or results. Semantic similarity considers the context behind user queries, such as the user intent, to determine relevant results even if the exact terms or phrases aren’t provided​.

To enhance the accuracy of semantic results, AI Search uses the AI Search Retrieval Augmented Generation \(RAG\) application, which matches user queries with indexed records based on both keyword and semantic similarity.

The main elements of AI Search for product catalog include the following:

-   **Indexed source**

    Defines the table records to be indexed for product catalog search:

    -   The Product Offering Indexed source uses the Product Offering \[sn\_prd\_pm\_product\_offering\] table as the source. The Configuration JSON field in the Product Offering table provides the characteristic options and attributes for products, which are used by AI Search to find catalog items by characteristics and options.
    -   The Service Specification indexed source uses the Service Specification \[sn\_prd\_pm\_service\_specification\] table as the source.
    -   Semantic Index Configuration settings define the embedding model, chunking configuration, and the semantic index fields used to control semantic indexing in AI Search. To learn more about semantic indexing, see [Semantic index configuration for indexed sources](https://www.servicenow.com/docs/access?context=semantic-index-cfg-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
    For more information on indexed sources, see [Indexed sources in AI Search](https://www.servicenow.com/docs/access?context=indexed-sources-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **Search source**

    A search source defines the searchable set of indexed records to be used and the conditions for items that can be searched. For example, the Product Offering Search source has two conditions that a product offering must meet so that it's returned as a search result:

    -   \[State\] \[is\] \[published\]
    -   \[Sellable\] \[is\] \[true\]
    The Service Specification Search source has one condition, \[State\] \[is\] \[published\], that a specification must meet so that it's returned as a search result.

    For more information on search sources, see [Search sources in AI Search](https://www.servicenow.com/docs/access?context=search-sources-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **Search profiles**

    Search profiles \(Product Offering Search Profile and Service Specification Search Profile\) manage the search experience offered to users and the data to be searched. You can fine-tune the synonyms, stop words, typo handling rules used in auto-correction, and result improvement rules that control the product catalog search experience. To learn more about the features that can be changed in a search file, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **Search application configurations**

    Search application configurations define the search engine used, the search profile used, and also auto-complete suggestions. For details about these configurations, see [Search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


Product catalog admins inherit the ais\_admin role, which enables them to create, read, update, and delete content indexing and search settings for AI Search.

## Implementing AI Search for product catalog

Users with the admin role perform the following steps to implement AI Search for the product catalog.

1.  [Install AI Search for Next Experience](https://www.servicenow.com/docs/access?context=install-ais-next-experience-app&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) only if you upgraded from Tokyo or a previous release.

    Skip this step if you're a new customer using the Zurich release or if your instance was zBooted in the Zurich release. AI Search for Next Experience is automatically installed.

2.  [Configure Now Assist for Sales Force Automation \(SFA\)](../../now-assist-som/task/configure-now-assist-som.md).

    Depending on your entitlements, the Now Assist for Sales Force Automation \(SFA\) plugin might be automatically installed. If it is not automatically installed but you have the appropriate entitlements, install the Now Assist for Sales Force Automation \(SFA\) plugin \(sn\_som\_gen\_ai\). This plugin installs the AI Search RAG plugin \(sn\_ais\_rag\) and the AI Search Semantic Controller plugin \(com.glide.ais.semantic\_search\) for the AI Search Retrieval Augmented Generation \(RAG\) application used by AI Search for product catalog.

    **Note:** If you don’t install Now Assist for Sales Force Automation \(SFA\) plugin \(sn\_som\_gen\_ai\), the product catalog interface provides simple keyword search, also known as Zing search.

3.  [Run scheduled job to populate product offering categories](../task/run-scheduled-job-prod-offer-categories.md) only if you upgraded to the Zurich.

    This step adds the product offering categories field to the Product Offering table. Skip this step if you're a new customer using the Zurich release or if your instance was zBooted in the Zurich release.

4.  [Run scheduled job to publish stop words dictionary, search profiles, and index tables](../task/run-sched-job-index-stopwords-profile.md).

    This scheduled job sets up the indexes and publishes the stop word dictionary and search profiles used in AI Search for product catalogs.

5.  [Enable AI Search in product catalog](../task/enable-ai-search-catalog.md).

    Set the **enable\_ai\_search\_in\_catalog** property to true, which enables AI Search for the product catalog interface and verifies that the necessary files are configured to run AI Search.


After AI Search has been implemented, product catalog admins can manage and customize various AI Search features if needed. Product catalog admins inherit the ais\_admin role, which enables them to create, read, update, and delete content indexing and search settings for AI Search.

**Related topics**  


[Using product catalogs](using-product-catalog.md)

[Use AI Search in product catalogs](../task/use-ai-search-catalog.md)

