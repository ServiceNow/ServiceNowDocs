---
title: Combined Product Catalog Management and Pricing Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Product Catalog Management and Pricing Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-productcatalogmanagementandpricingmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Product Catalog Management and Pricing Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Product Catalog Management and Pricing Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Product Catalog Management and Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Product Catalog Management and Pricing Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Upgrade information**

Pricing Management provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you've been using a custom pricing plan from an earlier release, after upgrading to a new version of Pricing Management, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

If you've been using AI Search for product catalog in a previous release, after upgrading to Product Catalog Management Core v.19.0.0 or higher, republish the stop word dictionary, search profiles, and index tables used by AI Search. To republish, run the **Scheduled job to publish stop words dictionary, search profiles and index tables**. Republishing includes the changes for multilingual support of product catalog entities introduced in the v.19.0.0 release.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Eligible catalog-category hierarchy API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US)**

Enable external integrations and in-platform applications to retrieve the eligible catalog-category tree hierarchy by using a REST endpoint.


 -   **[Product Catalog Search API](https://www.servicenow.com/docs/access?context=product-catalog-search-api&family=australia&ft:locale=en-US)**

Enable external integrations to query the product catalog by calling the `POST /api/sn_prd_pm/v1/catalog/search` endpoint. This REST API accepts a JSON request body and returns product offering and service specification results, including a semantic similarity score when AI Search is enabled. Users with the sn\_prd\_pm.product\_catalog\_viewer or sn\_prd\_pm.external\_product\_viewer role can access the endpoint.


 -   **[Multilingual support for product catalog entities](https://www.servicenow.com/docs/access?context=product-catalog-multilingual-support&family=australia&ft:locale=en-US)**

Certain key fields in Product Catalog Management tables, such as product offering name and description, have been changed in the Data Dictionary from type string to translated\_text. Admins can now set these product catalog fields to display in multiple languages in the product catalog interface.


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

 -   **[Product families](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=australia&ft:locale=en-US)**

Create product families to provide hierarchical classification similar to category trees. For example, you can use product families to roll up or aggregate measurable items, such as revenue forecasts for reporting or business insights.


 -   **[Multi-attribute pricing rules](https://www.servicenow.com/docs/access?context=som-create-pricing-adjustment&family=australia&ft:locale=en-US)**

Display attribute-based pricing on transaction lines, where the offer price is determined by the combination of attributes, by setting up attribute-based pricing for product offerings based on multiple, combined attributes using the Attribute Adjustment matrix.

-   **[Blended pricing support for contract renewals](https://www.servicenow.com/docs/access?context=pricing-management&family=australia&ft:locale=en-US)**

Enable sales agents to apply automatically calculated blended unit prices for renewals, based on the existing product price and the renewal uplift required. Blended pricing is used in upsell and down-sell scenarios and in contract line consolidation.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Product Catalog Management and Pricing Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Domain separation support](https://www.servicenow.com/docs/access?context=domain-separation-overview&family=australia&ft:locale=en-US)**

Starting with Product Catalog Management Core v19.1.0, all product catalog tables support the basic level of domain separation.


 -   **[Custom context variable enhancement](https://www.servicenow.com/docs/access?context=som-create-context-variable&family=australia&ft:locale=en-US)**

Use the **Applicable to** field in the Context Variable form to indicate that a custom context variable is to be used for pricing. The pricing engine uses this indicator to resolve pricing in the correct transaction scope, to help prevent mispricing of product bundles.


 -   **[Product catalog interface enhancement](https://www.servicenow.com/docs/access?context=using-product-catalog&family=australia&ft:locale=en-US)**

Quickly identify products with derived pricing through product tiles that display a message stating that the product price varies. Pricing is calculated and updated automatically based on selections made.


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


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Product Catalog Management and Pricing Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Product Catalog Management and Pricing Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

The pricing engine parallel execution properties, `sn_csm_pricing.enable_pricing_engine_parallel_execution` and `sn_csm_pricing.pricing_engine_parallelism_lines_threshold,`have been removed from Pricing Management to support automatic addition of derived pricing lines and calculation of pricing rollups.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrixes from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


**Important:** Product Catalog Management and Pricing Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

