---
title: Product Catalog Management and Pricing Management release notes
description: The ServiceNow Sales Customer Relationship Management applications include the ServiceNow Product Catalog Management and ServiceNow Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-01"
reading_time_minutes: 4
---

# Product Catalog Management and Pricing Management release notes

The ServiceNow® Sales Customer Relationship Management applications include the ServiceNow® Product Catalog Management and ServiceNow® Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Yokohama release.

## Product Catalog Management and Pricing Management highlights for the Yokohama release

-   Enable agents to create multiple configurations of child product offerings in configurable products and customize the options and characteristics for each child product instance.
-   Identify single-use product offerings, such as installation services, with a transient flag to differentiate them from products that are maintained as active sold products or product inventory.
-   Provide the options to choose a drop-down or radio control to display characteristics of type choice in the product configurator UI.
-   Give sales agents a list of recommended product offerings that can be added to complement or supplement products in quotes.
-   Enable pricing admins to set pricing adjustments based on the quantity of product offerings in a quote or order.

See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

## Important information for upgrading to Yokohama

After upgrading to the May 2025 release of Sales Customer Relationship Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

## New in the Yokohama release

-   **[Product offering recommendations](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Provide sales agents with offer recommendations for upselling or cross-selling additional products in quotes. Product catalog admins create the offer recommendations for sellable products. Sales agents can view the recommendations when adding products to quotes from the product catalog or when reviewing the lines items for a quote.

-   **[Product catalog and product configurator in the Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Enable customers to view the product catalog and order products using the product configurator in the Business Portal for Order Management.


## UI changes

-   **[Needs analysis in CSM Configurable Workspace](https://www.servicenow.com/docs/access?context=configuring-needs-analysis&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Starting with the Yokohama release, the options for configuring a needs analysis are available in the List view of the CSM Configurable Workspace and can be found by navigating to **Needs**.


## Changed in this release

-   **[Multiple configurations](https://www.servicenow.com/docs/access?context=multiple-child-offering-configurations&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Define child product offerings that can have multiple configurations in configurable opportunities, quotes, and orders. Agents can clone or split a child product offering to create multiple product offering instances. Each quantity for an offering instance can then have its own unique configuration.

-   **[Transient product offerings](https://www.servicenow.com/docs/access?context=configuring-transient-products&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Define single-use product offerings, such as installation services or consulting services, as transient products that are fulfilled in ServiceNow Order Management. After orders for transient products are fulfilled, sold product or product inventory records are created but have an Inactive status. Move, Add, Change, Delete \(MACD\) actions aren't supported for the sold product or product inventory records of transient products.


-   **[Configurable pricing plan enhancements](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**
    -   Apply Renewal Adjustment step: This new step determines whether a contract renewal adjustment, either a markup or markdown amount or percentage, is to be calculated and applied. For example, as a pricing admin, you might want to apply a pricing uplift of a fixed amount at contract renewal. This renewal adjustment step is enabled by default, but you can change or remove it in a custom configurable pricing plan.
    -   Extension point updates: The ListPriceExtensionPoint, which gathers the data needed to make required adjustments, now includes the adjustment data for contract renewals.
-   **[Volume-based pricing](https://www.servicenow.com/docs/access?context=configure-volume-pricing&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Set volume discounts for product offerings based on the product quantity.


## Activation information

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the product configurator feature from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

