---
title: Combined Product Catalog Management and Pricing Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Product Catalog Management and Pricing Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-productcatalogmanagementandpricingmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Product Catalog Management and Pricing Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Product Catalog Management and Pricing Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Product Catalog Management and Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Product Catalog Management and Pricing Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

After upgrading to the May 2025 release of Sales and Order Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

 The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

</td></tr><tr><td>

Zurich

</td><td>

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

 If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

 If you want to use AI Search for product catalog searches, before upgrading install Now Assist for Sales Force Automation \(SFA\), which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Product offering recommendations](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Provide sales agents with offer recommendations for upselling or cross-selling additional products in quotes. Product catalog admins create the offer recommendations for sellable products. Sales agents can view the recommendations when adding products to quotes from the product catalog or when reviewing the lines items for a quote.

-   **[Product catalog and product configurator in the Business Portal for Order Management](https://servicenow-staging.fluidtopics.net/access?context=order-mgt-create-an-order-using-customer-portal&family=yokohama&ft:locale=en-US)**

Enable customers to view the product catalog and order products using the product configurator in the Business Portal for Order Management.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create configurable product offerings and associated blueprints](https://servicenow-staging.fluidtopics.net/access?context=som-create-configurable-prod-offerings&family=zurich&ft:locale=en-US)**

Enable product catalog admins to generate blueprints for configurable products using the CPQ Configurator. A blueprint contains the product attributes, product relationships, product and pricing rules, and child products that control the structure of a configurable product offering. It also contains configuration rules, such as inclusion, exclusion, and determination. Blueprints drive the agent and customer experience when configurable products are added using the configurator. Catalog admins can review and update an offering blueprint in the CPQ Configurator, then publish the product offering to the product catalog.

-   **[AI Search queries in the product catalog interface](https://servicenow-staging.fluidtopics.net/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US)**

Enable semantic search features that agents and customers can use in the product catalog to find relevant product offerings. Users can search by product offer attributes, characteristics, and child offerings, and also view auto-complete suggestions. AI Search supports queries with synonyms, multi-languages, Boolean operators, and auto-correction \(typo handling\). Product catalog admins can configure stop words, synonyms, and rules that control the search results displayed.

-   **[Complex characteristics](https://servicenow-staging.fluidtopics.net/access?context=som-product-config-add-characteristics&family=zurich&ft:locale=en-US)**

Starting with Product Catalog Management Core v13.0, enable product catalog admins to define product and specification characteristics using an object-based structure that supports the following data types: integer, decimal, date and date time, and data arrays. For example, product catalog admins can use these new data types to define characteristics for communication products, such as routing characteristics, that have nested levels of characteristics and characteristic options. These complex characteristics can then be used to define conditions for setting decomposition, attribute propagation, and compatibility rules.

    -   Agents can view and select the complex characteristics available for configurable product offerings when creating opportunities, quotes, and orders. Complex attributes are displayed as separate nodes in the product hierarchy tree of the legacy product configurator interface.
    -   Fulfillment agents can perform fulfillment tasks that capture complex characteristic data for new or MACD orders.
    -   Customers can view and select complex characteristics when using the Business Portal to order configurable products.
**Note:**  Complex characteristics aren’t supported in the CPQ Configurator.


-   **[Derived product pricing](https://servicenow-staging.fluidtopics.net/access?context=configuring-related-product-pricing&family=zurich&ft:locale=en-US)**

Define dynamic product pricing relationships between products, where the price for a product is derived from the price of another product or transaction-level values, such as the total quote value or annual contract value \(ACV\). When sales or order agents add the product to a quote or order, they can see how the product price is derived in real time.

-   **[Price and quantity ramps](https://servicenow-staging.fluidtopics.net/access?context=defining-products-with-ramps&family=zurich&ft:locale=en-US)**

Enable product catalog admins to identify configurable product offerings for which pricing ramps can be created. These product offerings must also have the recurring pricing method. Sales agents create price ramps for quote lines that define and schedule pricing and quantity changes as product deals evolve over a given time period.

-   **[Product pricing changes related to MACD activities](https://servicenow-staging.fluidtopics.net/access?context=net-pricing-sp-contracts&family=zurich&ft:locale=en-US)**

Support different price bases, such as original prices, fresh prices, or zero prices, used to calculate pricing for products during MACD activities.

-   **[Cost-based attribute adjustments](https://servicenow-staging.fluidtopics.net/access?context=create-cost-attribute-adjustment&family=zurich&ft:locale=en-US)**

Enable pricing admins or managers to set different product costs based on product attributes, such as model or size, by using cost book-specific or product offering-based adjustments for cost book lines. Previously, only a single cost amount was captured for a product offering, even if the product had different attributes that affected the product cost. These adjustments determine the base product cost used to calculate profit margins for sales agents when they create quotes for customers.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Product Catalog Management and Pricing Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Multiple configurations](https://servicenow-staging.fluidtopics.net/access?context=multiple-child-offering-configurations&family=yokohama&ft:locale=en-US)**

Define child product offerings that can have multiple configurations in configurable opportunities, quotes, and orders. Agents can clone or split a child product offering to create multiple product offering instances. Each quantity for an offering instance can then have its own unique configuration.

-   **[Transient product offerings](https://servicenow-staging.fluidtopics.net/access?context=configuring-transient-products&family=yokohama&ft:locale=en-US)**

Define single-use product offerings, such as installation services or consulting services, as transient products that are fulfilled in ServiceNow Order Management. After orders for transient products are fulfilled, sold product or product inventory records are created but have an Inactive status. Move, Add, Change, Delete \(MACD\) actions aren't supported for the sold product or product inventory records of transient products.


-   **[Configurable pricing plan enhancements](https://servicenow-staging.fluidtopics.net/access?context=configuring-pricing-plan&family=yokohama&ft:locale=en-US)**
    -   Apply Renewal Adjustment step: This new step determines whether a contract renewal adjustment, either a markup or markdown amount or percentage, is to be calculated and applied. For example, as a pricing admin, you might want to apply a pricing uplift of a fixed amount at contract renewal. This renewal adjustment step is enabled by default, but you can change or remove it in a custom configurable pricing plan.
    -   Extension point updates: The ListPriceExtensionPoint, which gathers the data needed to make required adjustments, now includes the adjustment data for contract renewals.
-   **[Volume-based pricing](https://servicenow-staging.fluidtopics.net/access?context=configure-volume-pricing&family=yokohama&ft:locale=en-US)**

Set volume discounts for product offerings based on the product quantity.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Support minor changes to published product offerings and specifications](https://servicenow-staging.fluidtopics.net/access?context=minor-updates-published-offerings-specs&family=zurich&ft:locale=en-US)**

Make minor changes to published versions of a product offering or specification, without creating a version. Minor updates include changes such as modifying the product offering display name, description, or product image.

-   **[Configurable product offerings](https://servicenow-staging.fluidtopics.net/access?context=som-create-product-offering&family=zurich&ft:locale=en-US)**

The Create Product Offering form, used when creating product offerings, has two new options. The **Configurable** option indicates that the product offering is configurable and that it can be customized by agents and customers using the CPQ Configurator. The **Enable ramps** option indicates that price ramps can be defined for a configurable product.

-   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://servicenow-staging.fluidtopics.net/access?context=export-import-product-catalog-entities&family=zurich&ft:locale=en-US)**

Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://servicenow-staging.fluidtopics.net/access?context=export-product-catalog-entities&family=zurich&ft:locale=en-US).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://servicenow-staging.fluidtopics.net/access?context=import-product-catalog-entities&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Product Catalog Management and Pricing Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Product Catalog Management and Pricing Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the product configurator feature from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

The Product Catalog Management and Pricing Management features are included with Sales and Order Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the CPQ Integration application for the CPQ Configurator from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Product Catalog Management and Pricing Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Enable agents to create multiple configurations of child product offerings in configurable products and customize the options and characteristics for each child product instance.
-   Identify single-use product offerings, such as installation services, with a transient flag to differentiate them from products that are maintained as active sold products or product inventory.
-   Provide the options to choose a drop-down or radio control to display characteristics of type choice in the product configurator UI.
-   Give sales agents a list of recommended product offerings that can be added to complement or supplement products in quotes.
-   Enable pricing admins to set pricing adjustments based on the quantity of product offerings in a quote or order.

 See [Product Catalog Management](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US) and [Pricing Management](https://servicenow-staging.fluidtopics.net/access?context=pricing-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Support AI-powered semantic search queries to find relevant product offerings and service specifications in the product catalog interface.
-   Generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.
-   Enable sales agents to create price and quantity ramps, a pricing strategy for increasing product pricing and quantity amounts over specified time periods.
-   Define pricing on product offers based on the price of other product offers or transaction context variables.
-   Use product characteristics to adjust product costs, which are then used in margin calculations for sales quotes.

 See [Product Catalog Management](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-managment&family=zurich&ft:locale=en-US) and [Pricing Management](https://servicenow-staging.fluidtopics.net/access?context=pricing-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

