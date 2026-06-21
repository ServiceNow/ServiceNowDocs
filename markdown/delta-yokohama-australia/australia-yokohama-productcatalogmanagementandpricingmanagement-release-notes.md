---
title: Combined Product Catalog Management and Pricing Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Product Catalog Management and Pricing Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-productcatalogmanagementandpricingmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Product Catalog Management and Pricing Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Product Catalog Management and Pricing Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Product Catalog Management and Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Product Catalog Management and Pricing Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

After upgrading to the May 2025 release of Sales Customer Relationship Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

 The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

</td></tr><tr><td>

Zurich

</td><td>

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

 If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

 If you want to use AI Search for product catalog searches, before upgrading install Now Assist for Sales Force Automation \(SFA\), which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Pricing Management v16.0.0 provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you've been using a custom pricing plan from an earlier release, after upgrading to Pricing Management v16.0.0, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Product offering recommendations](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Provide sales agents with offer recommendations for upselling or cross-selling additional products in quotes. Product catalog admins create the offer recommendations for sellable products. Sales agents can view the recommendations when adding products to quotes from the product catalog or when reviewing the lines items for a quote.

-   **[Product catalog and product configurator in the Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&family=yokohama&ft:locale=en-US)**

Enable customers to view the product catalog and order products using the product configurator in the Business Portal for Order Management.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Create configurable offerings and blueprints](https://www.servicenow.com/docs/access?context=som-create-configurable-prod-offerings&family=zurich&ft:locale=en-US)**

Enable product catalog admins to generate blueprints for configurable products using the CPQ Configurator. A blueprint contains the product attributes, product relationships, product and pricing rules, and child products that control the structure of a configurable product offering. It also contains configuration rules, such as inclusion, exclusion, and determination. Blueprints drive the agent and customer experience when configurable products are added using the configurator. Catalog admins can review and update an offering blueprint in the CPQ Configurator, then publish the product offering to the product catalog.

-   **[AI Search queries in the product catalog interface](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US)**

Enable semantic search features that agents and customers can use in the product catalog to find relevant product offerings. Users can search by product offer attributes, characteristics, and child offerings, and also view auto-complete suggestions. AI Search supports queries with synonyms, multi-languages, Boolean operators, and auto-correction \(typo handling\). Product catalog admins can configure stop words, synonyms, and rules that control the search results displayed.

-   **[Complex characteristics](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&family=zurich&ft:locale=en-US)**

Starting with Product Catalog Management Core v13.0, enable product catalog admins to define product and specification characteristics using an object-based structure that supports the following data types: integer, decimal, date and date time, and data arrays. For example, product catalog admins can use these new data types to define characteristics for communication products, such as routing characteristics, that have nested levels of characteristics and characteristic options. These complex characteristics can then be used to define conditions for setting decomposition, attribute propagation, and compatibility rules.

    -   Agents can view and select the complex characteristics available for configurable product offerings when creating opportunities, quotes, and orders. Complex attributes are displayed as separate nodes in the product hierarchy tree of the legacy product configurator interface.
    -   Fulfillment agents can perform fulfillment tasks that capture complex characteristic data for new or MACD orders.
    -   Customers can view and select complex characteristics when using the Business Portal to order configurable products.
**Note:**  Complex characteristics aren’t supported in the CPQ Configurator.


-   **[Derived product pricing](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=zurich&ft:locale=en-US)**

Define dynamic product pricing relationships between products, where the price for a product is derived from the price of another product or transaction-level values, such as the total quote value or annual contract value \(ACV\). When sales or order agents add the product to a quote or order, they can see how the product price is derived in real time.

-   **[Price and quantity ramps](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&family=zurich&ft:locale=en-US)**

Enable product catalog admins to identify configurable product offerings for which pricing ramps can be created. These product offerings must also have the recurring pricing method. Sales agents create price ramps for quote lines that define and schedule pricing and quantity changes as product deals evolve over a given time period.

-   **[Product pricing changes related to MACD activities](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&family=zurich&ft:locale=en-US)**

Support different price bases, such as original prices, fresh prices, or zero prices, used to calculate pricing for products during MACD activities.

-   **[Cost-based attribute adjustments](https://www.servicenow.com/docs/access?context=create-cost-attribute-adjustment&family=zurich&ft:locale=en-US)**

Enable pricing admins or managers to set different product costs based on product attributes, such as model or size, by using cost book-specific or product offering-based adjustments for cost book lines. Previously, only a single cost amount was captured for a product offering, even if the product had different attributes that affected the product cost. These adjustments determine the base product cost used to calculate profit margins for sales agents when they create quotes for customers.


</td></tr><tr><td>

Australia

</td><td>

-   **[Multilingual support for product catalog entities](https://www.servicenow.com/docs/access?context=product-catalog-multilingual-support&family=australia&ft:locale=en-US)**

Certain key fields in Product Catalog Management tables, such as product offering name and description, have been changed in the Data Dictionary from type string to translated\_text. Admins can now set these product catalog fields to display in multiple languages in the product catalog interface.

-   **[Product families](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=australia&ft:locale=en-US)**

Create product families to provide hierarchical classification similar to category trees. For example, you can use product families to roll up or aggregate measurable items, such as revenue forecasts for reporting or business insights.


-   **[Support manual pricing adjustments in the Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&family=australia&ft:locale=en-US)**

Pass manual pricing adjustments as part of a pricing request payload using the Pricing API. External systems can include adjustment values directly in a pricing run, rather than fetch manual adjustments from the pricing database when running pricing calculations.

-   **[Support external IDs in the Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&family=australia&ft:locale=en-US)**

Submit pricing requests that use custom external IDs or codes to reference objects from external systems, such as product offerings, price lists, and cost books. Set a request-level flag that indicates external IDs are to be used for these objects rather than sys\_ids. For additional information, see [External ID support in Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=external-ids-pricingapi&family=australia&ft:locale=en-US).

-   **[Renewal pricing for products with price and quantity ramps](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&family=australia&ft:locale=en-US)**

Calculate renewal pricing for products with price and quantity ramps, using per year, per term, and price only uplift calculation methods.

-   **[Derived pricing support for sold products](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=australia&ft:locale=en-US)**
    -   Use the `DerivedProductPriceExtensionPoint` extension to determine whether a source line for a quote or sold product and a target line are pairs.
    -   Use the `getAccountLevelDerivedPricedProductsLookupData(pricingEngineContext)` method to control the records scanned by the pricing engine to determine account-level derived prices for sold products.
    -   The pricing engine does the following:
        -   Displays a message indicating when a change to a source product affects the price of a derived product.
        -   Checks product offerings and excludes product offerings with child offerings from derived pricing.
-   **[Multi-attribute pricing rules](https://www.servicenow.com/docs/access?context=som-create-pricing-adjustment&family=australia&ft:locale=en-US)**

Display attribute-based pricing on transaction lines, where the offer price is determined by the combination of attributes, by setting up attribute-based pricing for product offerings based on multiple, combined attributes using the Attribute Adjustment matrix.

-   **[Blended pricing support for contract renewals](https://www.servicenow.com/docs/access?context=pricing-management&family=australia&ft:locale=en-US)**

Enable sales agents to apply automatically calculated blended unit prices for renewals, based on the existing product price and the renewal uplift required. Blended pricing is used in upsell and down-sell scenarios and in contract line consolidation.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Product Catalog Management and Pricing Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Multiple configurations](https://www.servicenow.com/docs/access?context=multiple-child-offering-configurations&family=yokohama&ft:locale=en-US)**

Define child product offerings that can have multiple configurations in configurable opportunities, quotes, and orders. Agents can clone or split a child product offering to create multiple product offering instances. Each quantity for an offering instance can then have its own unique configuration.

-   **[Transient product offerings](https://www.servicenow.com/docs/access?context=configuring-transient-products&family=yokohama&ft:locale=en-US)**

Define single-use product offerings, such as installation services or consulting services, as transient products that are fulfilled in ServiceNow Order Management. After orders for transient products are fulfilled, sold product or product inventory records are created but have an Inactive status. Move, Add, Change, Delete \(MACD\) actions aren't supported for the sold product or product inventory records of transient products.


-   **[Configurable pricing plan enhancements](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=yokohama&ft:locale=en-US)**
    -   Apply Renewal Adjustment step: This new step determines whether a contract renewal adjustment, either a markup or markdown amount or percentage, is to be calculated and applied. For example, as a pricing admin, you might want to apply a pricing uplift of a fixed amount at contract renewal. This renewal adjustment step is enabled by default, but you can change or remove it in a custom configurable pricing plan.
    -   Extension point updates: The ListPriceExtensionPoint, which gathers the data needed to make required adjustments, now includes the adjustment data for contract renewals.
-   **[Volume-based pricing](https://www.servicenow.com/docs/access?context=configure-volume-pricing&family=yokohama&ft:locale=en-US)**

Set volume discounts for product offerings based on the product quantity.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Support minor changes to published product offerings and specifications](https://www.servicenow.com/docs/access?context=minor-updates-published-offerings-specs&family=zurich&ft:locale=en-US)**

Make minor changes to published versions of a product offering or specification, without creating a version. Minor updates include changes such as modifying the product offering display name, description, or product image.

-   **[Configurable product offerings](https://www.servicenow.com/docs/access?context=som-create-product-offering&family=zurich&ft:locale=en-US)**

The Create Product Offering form, used when creating product offerings, has two new options. The **Configurable** option indicates that the product offering is configurable and that it can be customized by agents and customers using the CPQ Configurator. The **Enable ramps** option indicates that price ramps can be defined for a configurable product.

-   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://www.servicenow.com/docs/access?context=export-import-product-catalog-entities&family=zurich&ft:locale=en-US)**

Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://www.servicenow.com/docs/access?context=export-product-catalog-entities&family=zurich&ft:locale=en-US).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://www.servicenow.com/docs/access?context=import-product-catalog-entities&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

-   **[Product catalog interface enhancement](https://www.servicenow.com/docs/access?context=using-product-catalog&family=australia&ft:locale=en-US)**

Quickly identify products with derived pricing through product tiles that display a message stating that the product price varies. Pricing is calculated and updated automatically based on selections made.


-   **[Custom context variable enhancement](https://www.servicenow.com/docs/access?context=som-create-context-variable&family=australia&ft:locale=en-US)**

Use the **Applicable to** field in the Context Variable form to indicate that a custom context variable is to be used for pricing. The pricing engine uses this indicator to resolve pricing in the correct transaction scope, to help prevent mispricing of product bundles.

-   **[Derived pricing enhancements](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=australia&ft:locale=en-US)**
    -   The Derived Pricing Matrix supports the following enhancements:
        -   Conditions defined on product offering fields for both source and target product offerings
        -   Predefined formulas for specifying prices for target product offerings and using floor and ceiling price controls to maintain acceptable price ranges
    -   Visibility into how the final price for derived products is determined.
    -   Support for account-level scope, which uses both cart items and sold products when calculating derived prices.
-   **[Price and quantity ramp enhancements](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&family=australia&ft:locale=en-US)**
    -   Enable sales agents to create custom ramp type segments for quotes. Agents can view the cumulative price of product offers across all ramp segments.
    -   View ramps inside the CPQ Configurator.
    -   Enable sales agents to create ramps for quotes with amendments, contract renewals, and cancellations.
-   **[Delta pricing enhancement](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&family=australia&ft:locale=en-US)**

Show the delta pricing view in the CPQ Configurator during modify and amend flows.

-   **[Configurable pricing plan enhancement](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=australia&ft:locale=en-US)**

The Floor and Ceiling Calculation step in the default pricing plan applies the minimum and maximum prices for a product or service to help avoid pricing that isn't competitive or results in poor margins.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Product Catalog Management and Pricing Management features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Product Catalog Management and Pricing Management features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

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

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the product configurator feature from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the CPQ Integration application for the CPQ Configurator from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrixes from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

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

</td></tr><tr><td>

Australia

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

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Support AI-powered semantic search queries to find relevant product offerings and service specifications in the product catalog interface.
-   Generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.
-   Enable sales agents to create price and quantity ramps, a pricing strategy for increasing product pricing and quantity amounts over specified time periods.
-   Define pricing on product offers based on the price of other product offers or transaction context variables.
-   Use product characteristics to adjust product costs, which are then used in margin calculations for sales quotes.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=zurich&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   In the Sales CRM Pricing API, support pricing requests using custom external IDs or codes for objects such as product offerings, price lists, and unit of measure instead of ServiceNow sys\_ids.
-   Support pricing calculations for renewals of products with price and quantity ramps.
-   Provide visibility into how the final price for a derived product is determined using adjustment records.
-   Set up pricing floor and ceiling controls for product offerings to keep pricing within acceptable ranges.
-   Use standard predefined formulas \(SUM, AVG, MIN, and MAX\) in derived pricing calculations to capture adjustments at each pricing step.
-   Enable agents and customers to view attribute-based pricing where the product offering price is based on a combination of attributes.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=australia&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

