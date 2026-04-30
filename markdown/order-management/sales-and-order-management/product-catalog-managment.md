---
title: Product Catalog Management
description: Product Catalog Management enables your organization to manage your product offerings by grouping them into catalogs and categories, which streamlines the ordering process and helps manage leads, opportunities, quotes, and orders in Sales Customer Relationship Management.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Product Catalog Management

Product Catalog Management enables your organization to manage your product offerings by grouping them into catalogs and categories, which streamlines the ordering process and helps manage leads, opportunities, quotes, and orders in Sales Customer Relationship Management.

Product Catalog Management provides various features to implement product catalogs and categories in your organization.

-   Product catalog user interface: Launch from anywhere in opportunity, quote, and order capture workflows, enabling agents to browse and find products quickly with a full catalog search function.
-   Catalog category hierarchy: Use hierarchical structures of catalogs and categories to organize products and services logically.
-   Version control: Track changes made to product information over time, helping with transparency and auditability.
-   Product offer eligibility: Filter your product catalogs, product offering categories, and product offerings so that agents sell customers only the products for which they’re eligible.

**Note:** Check your entitlements to determine if you have access to these features. Also, starting with the Yokohama release, customers can use the Business Portal with Order Management to create orders using the product catalog and product configurator. For more information on this self-service portal, see [Using the Business Portal.](order-mgt-business-portal.md)

To learn more about setting up product offering catalogs, see [Configuring product offerings and catalogs](som-managing-product-catalogs.md).

## Product catalog UI

The product offering catalog enables agents to do the following:

-   Browse and search product offerings by using keywords, descriptions, and industry codes​.
-   Review product offers that are organized by catalog category hierarchy, which streamlines catalog navigation.

![Product catalog interface that shows the product catalog hierarchy, product tiles with images, and search option.](../image/som-catalog-ui.png "Product catalog user interface")

## Product offering catalogs and categories

Product offering catalogs and categories offer a way to organize product offerings so that agents can easily find products to create orders.

-   Product Offering Catalog: Hierarchical product offering structures of categories and product offerings.
-   Product Offering Categories: Categories are a logical grouping of product offerings.
-   Product Offerings: Physical goods or non-tangible services that are configurable.
-   Characteristic and Characteristic options: Product options that are created based on customer preferences.​

![Infographic shows how catalogs, categories, product offerings, product characteristics, and characteristic options are configured in Sales Customer Relationship Management](../image/l2c-product-catalog-hierarchy-2.png "Example catalog hierarchy with categories and product offerings")

## Product offer bundling

You can create product offer bundles with an offer hierarchy using product offer relationships and relationship groups. These bundle offers can have references to a product specification or specification hierarchy at any level in the bundle. For more information, see [Product offer bundling with product specifications](../task/som-offer-bundles-with-specs.md).

## Product offer eligibility

As a product catalog admin or manager, you can use business rules to filter the product catalog, product offering categories, and product offerings dynamically, displaying only the appropriate catalog, categories, and offerings for which a customer is eligible. These rules enable your sales agents to sell the correct products to customers based on context, such as specific customer accounts, customer location, sales contracts, and more. You define these rules using product eligibility matrices. To learn more about using the product eligibility matrices, see [Configuring product offer eligibility](configuring-sales-eligibility.md).

## Product recommendations

In Sales Customer Relationship Management, different types of product recommendations are available to your sales agents. Your agents can get product recommendations as they're generating or updating leads and opportunities, or updating quotes.

-   Product recommendations using needs analysis - When your sales agents are generating leads and opportunities, they can use product selection guides to help determine relevant products for their customers. For information on setting up needs analysis, including the product selection guides, see [Configuring needs analysis](configuring-needs-analysis.md). For details on how your agents can get product recommendations for leads and opportunities, see [Get product recommendations for leads using needs analysis](../task/lead-management-use-needs-analysis.md) and [Get product recommendations for opportunities using needs analysis](../task/opp-mgmt-use-needs-analysis.md).
-   Product offering recommendations for quotes - When your sales agents are updating quotes, they can get product recommendations for upselling or cross-selling additional products for existing quote line items. For information on setting up these recommendations, see [Configuring product offering recommendations](configuring-offer-recommendations.md). For details on how product offering recommendations work in quotes, see [Using product offering recommendations in quotes](using-prod-recommendations-quote.md).

