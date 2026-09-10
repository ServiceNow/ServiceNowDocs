---
title: Combined Product Catalog Management and Pricing Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Product Catalog Management and Pricing Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-productcatalogmanagementandpricingmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 14
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

-   **Upgrade information**

After upgrading to the May 2025 release of Sales Customer Relationship Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.


</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

If you want to use AI Search for product catalog searches, before upgrading install ServiceNow Otto for Sales Automation, which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

Pricing Management provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you've been using a custom pricing plan from an earlier release, after upgrading to a new version of Pricing Management, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

If you've been using AI Search for product catalog in a previous release, after upgrading to Product Catalog Management Core v.19.0.0 or higher, republish the stop word dictionary, search profiles, and index tables used by AI Search. To republish, run the **Scheduled job to publish stop words dictionary, search profiles and index tables**. Republishing includes the changes for multilingual support of product catalog entities introduced in the v.19.0.0 release.


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

-   **[Complex characteristics](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&family=zurich&ft:locale=en-US)**

Starting with Product Catalog Management Core v13.0, enable product catalog admins to define product and specification characteristics using an object-based structure that supports the following data types: integer, decimal, date and date time, and data arrays. For example, product catalog admins can use these new data types to define characteristics for communication products, such as routing characteristics, that have nested levels of characteristics and characteristic options. These complex characteristics can then be used to define conditions for setting decomposition, attribute propagation, and compatibility rules.

    -   Agents can view and select the complex characteristics available for configurable product offerings when creating opportunities, quotes, and orders. Complex attributes are displayed as separate nodes in the product hierarchy tree of the legacy product configurator interface.
    -   Fulfillment agents can perform fulfillment tasks that capture complex characteristic data for new or MACD orders.
    -   Customers can view and select complex characteristics when using the Business Portal to order configurable products.
**Note:**  Complex characteristics aren’t supported in the CPQ Configurator.


 -   **[Cost-based attribute adjustments](https://www.servicenow.com/docs/access?context=create-cost-attribute-adjustment&family=zurich&ft:locale=en-US)**

Enable pricing admins or managers to set different product costs based on product attributes, such as model or size, by using cost book-specific or product offering-based adjustments for cost book lines. Previously, only a single cost amount was captured for a product offering, even if the product had different attributes that affected the product cost. These adjustments determine the base product cost used to calculate profit margins for sales agents when they create quotes for customers.


</td></tr><tr><td>

Australia

</td><td>

-   **[Support manual pricing adjustments in the Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&family=australia&ft:locale=en-US)**

Pass manual pricing adjustments as part of a pricing request payload using the Pricing API. External systems can include adjustment values directly in a pricing run, rather than fetch manual adjustments from the pricing database when running pricing calculations.

-   **[Support external IDs in the Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=sales-crm-pricing-api&family=australia&ft:locale=en-US)**

Submit pricing requests that use custom external IDs or codes to reference objects from external systems, such as product offerings, price lists, and cost books. Set a request-level flag that indicates external IDs are to be used for these objects rather than sys\_ids. For additional information, see [External ID support in Sales CRM Pricing API](https://www.servicenow.com/docs/access?context=external-ids-pricingapi&family=australia&ft:locale=en-US).


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

-   **[Needs analysis in CRM Workspace](https://www.servicenow.com/docs/access?context=configuring-needs-analysis&family=yokohama&ft:locale=en-US)**

Starting with the Yokohama release, the options for configuring a needs analysis are available in the List view of the CRM Workspace and can be found by navigating to **Needs**.


 -   **[Volume-based pricing](https://www.servicenow.com/docs/access?context=configure-volume-pricing&family=yokohama&ft:locale=en-US)**

Set volume discounts for product offerings based on the product quantity.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


 -   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://www.servicenow.com/docs/access?context=export-import-product-catalog-entities&family=zurich&ft:locale=en-US)**

Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://www.servicenow.com/docs/access?context=export-product-catalog-entities&family=zurich&ft:locale=en-US).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://www.servicenow.com/docs/access?context=import-product-catalog-entities&family=zurich&ft:locale=en-US).

 -   **[Configurable pricing plan enhancements](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=zurich&ft:locale=en-US)**
    -   Pricing plan changes in Pricing Management v15.0.0
        -   Input Price Point column: Identifies the input for a pricing step.
        -   Output Price Point column: Identifies the output resulting from the pricing step.
        -   Analyze line changes step: This step uses the Delta Price Treatment Matrix to define how adjustments to sold products or contracts are handled by the pricing engine.
        -   Annual Price Increase Adjustments for Ramps: This step applies the percentage Annual Price Increase to the list price of products that have pricing ramps enabled. Sales agents specify the percentage increase when they create price ramps.
        -   Net Price Calculation step: This step calculates the net price using any automatic and manual adjustments made in quotes or orders.
        -   Line Rollup step: This step uses the net price to calculate the cumulative pricing fields in quote and order lines that are rolled up to the parent line of bundled products.
        -   Header Rollup step: This step calculates total pricing values, such as total annual or total monthly amounts, displayed at the header level.
        -   Derived Price Calculation step: This step calculates the line prices using the Derived Pricing Matrix that defines the pricing source and the unit base list price for the price list line.
        -   Calculate Delta Prices step: This step calculates product pricing during MACD activities using different price point bases, as configured by the pricing admin.
    -   Pricing plan changes in Pricing Management v13.0.0
        -   Apply Attribute-based Cost Adjustment step: This new step applies an attribute-based cost adjustment, either a percentage or markup or markdown of the cost book line cost. The pricing engine uses the cost adjustment to determine product costs when calculating margins for quote lines.
        -   The Fetch Cost and Fetch Price List Price steps have been renamed Fetch Base Cost and Fetch Base Price List Price.

</td></tr><tr><td>

Australia

</td><td>

-   **[Custom context variable enhancement](https://www.servicenow.com/docs/access?context=som-create-context-variable&family=australia&ft:locale=en-US)**

Use the **Applicable to** field in the Context Variable form to indicate that a custom context variable is to be used for pricing. The pricing engine uses this indicator to resolve pricing in the correct transaction scope, to help prevent mispricing of product bundles.


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

The pricing engine parallel execution properties, `sn_csm_pricing.enable_pricing_engine_parallel_execution` and `sn_csm_pricing.pricing_engine_parallelism_lines_threshold,`have been removed from Pricing Management to support automatic addition of derived pricing lines and calculation of pricing rollups.

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

-   **Activation information**

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the product configurator feature from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the CPQ Integration application for the CPQ Configurator from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


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

-   In derived pricing, enable the automatic creation of target product lines based on source products and their contract start and end dates.
-   Use the Product Catalog Search API to enable external integrations to query the product catalog.
-   In the Sales CRM Pricing API, support pricing requests using custom external IDs or codes for objects such as product offerings, price lists, and unit of measure instead of ServiceNow sys\_ids.
-   Support pricing calculations for renewals of products with price and quantity ramps.
-   Provide visibility into how the final price for a derived product is determined using adjustment records.
-   Set up pricing floor and ceiling controls for product offerings to keep pricing within acceptable ranges.
-   Use standard predefined formulas \(SUM, AVG, MIN, and MAX\) in derived pricing calculations to capture adjustments at each pricing step.
-   Enable agents and customers to view attribute-based pricing where the product offering price is based on a combination of attributes.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=australia&ft:locale=en-US) and [Product pricing](https://www.servicenow.com/docs/access?context=pricing-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

