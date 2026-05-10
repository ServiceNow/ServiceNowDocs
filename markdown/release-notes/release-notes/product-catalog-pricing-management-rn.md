---
title: Product Catalog Management and Pricing Management release notes
description: The ServiceNow Sales CRM applications include the ServiceNow Product Catalog Management and ServiceNow Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-21"
reading_time_minutes: 5
---

# Product Catalog Management and Pricing Management release notes

The ServiceNow® Sales CRM applications include the ServiceNow® Product Catalog Management and ServiceNow® Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Australia release.

## Product Catalog Management and Pricing Management highlights for the Australia release

-   In the Sales CRM Pricing API, support pricing requests using custom external IDs or codes for objects such as product offerings, price lists, and unit of measure instead of ServiceNow sys\_ids.
-   Support pricing calculations for renewals of products with price and quantity ramps.
-   Provide visibility into how the final price for a derived product is determined using adjustment records.
-   Set up pricing floor and ceiling controls for product offerings to keep pricing within acceptable ranges.
-   Use standard predefined formulas \(SUM, AVG, MIN, and MAX\) in derived pricing calculations to capture adjustments at each pricing step.
-   Enable agents and customers to view attribute-based pricing where the product offering price is based on a combination of attributes.

See [Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/product-catalog-managment.md) and [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-management.md) for more information.

**Important:** Product Catalog Management and Pricing Management are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Product Catalog Management and Pricing Management to Australia

Pricing Management v16.0.0 provides a default pricing plan that includes changes to support pricing strategies introduced in this release. If you have been using a custom pricing plan from an earlier release, after upgrading to Pricing Management v16.0.0, the default pricing plan is in a Retired state. Determine whether you want to publish the default pricing plan for use or customize it.

## New in the Australia release

-   **[Product families](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/product-catalog-managment.md)**

    Create product families to provide hierarchical classification similar to category trees. For example, you can use product families to roll up or aggregate measurable items, such as revenue forecasts for reporting or business insights.


-   **[Support manual pricing adjustments in the Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/sales-crm-pricing-api.md)**

    Pass manual pricing adjustments as part of a pricing request payload using the Pricing API. External systems can include adjustment values directly in a pricing run, rather than fetch manual adjustments from the pricing database when running pricing calculations.

-   **[Support external IDs in the Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/sales-crm-pricing-api.md)**

    Submit pricing requests that use custom external IDs or codes to reference objects from external systems, such as product offerings, price lists, and cost books. Set a request-level flag that indicates external IDs are to be used for these objects rather than sys\_ids. For additional information, see [External ID support in Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/external-ids-pricingapi.md).

-   **[Renewal pricing for products with price and quantity ramps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/defining-products-with-ramps.md)**

    Calculate renewal pricing for products with price and quantity ramps, using per year, per term, and price only uplift calculation methods.

-   **[Derived pricing support for sold products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**
    -   Use the `DerivedProductPriceExtensionPoint` extension to determine whether a source line for a quote or sold product and a target line are pairs.
    -   Use the `getAccountLevelDerivedPricedProductsLookupData(pricingEngineContext)` method to control the records scanned by the pricing engine to determine account-level derived prices for sold products.
    -   The pricing engine does the following:
        -   Displays a message indicating when a change to a source product affects the price of a derived product.
        -   Checks product offerings and excludes product offerings with child offerings from derived pricing.
-   **[Multi-attribute pricing rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-pricing-adjustment.md)**

    Display attribute-based pricing on transaction lines, where the offer price is determined by the combination of attributes, by setting up attribute-based pricing for product offerings based on multiple, combined attributes using the Attribute Adjustment matrix.

-   **[Blended pricing support for contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-management.md)**

    Enable sales agents to apply automatically calculated blended unit prices for renewals, based on the existing product price and the renewal uplift required. Blended pricing is used in upsell and down-sell scenarios and in contract line consolidation.


## Changed in this release

-   **[Product catalog interface enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-product-catalog.md)**

    Quickly identify products with derived pricing through product tiles that display a message stating that the product price varies. Pricing is calculated and updated automatically based on selections made.


-   **[Derived pricing enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**
    -   The Derived Pricing Matrix supports the following enhancements:
        -   Conditions defined on product offering fields for both source and target product offerings
        -   Predefined formulas for specifying prices for target product offerings and using floor and ceiling price controls to maintain acceptable price ranges
    -   Visibility into how the final price for derived products is determined.
    -   Support for account-level scope, which uses both cart items and sold products when calculating derived prices.
-   **[Price and quantity ramp enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/defining-products-with-ramps.md)**
    -   Enable sales agents to create custom ramp type segments for quotes. Agents can view the cumulative price of product offers across all ramp segments.
    -   View ramps inside the CPQ Configurator.
    -   Enable sales agents to create ramps for quotes with amendments, contract renewals, and cancellations.
-   **[Delta pricing enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/net-pricing-sp-contracts.md)**

    Show the delta pricing view in the CPQ Configurator during modify and amend flows.

-   **[Configurable pricing plan enhancement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-pricing-plan.md)**

    The Floor and Ceiling Calculation step in the default pricing plan applies the minimum and maximum prices for a product or service to help avoid pricing that isn't competitive or results in poor margins.


## Activation information

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrixes from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CPQ Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-servicenowcpq.md)**

    The CPQ Configurator interface streamlines the process of configuring and pricing customizable products in Sales Customer Relationship Management transactions such as quotes and orders.

-   **[Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-management.md)**

    The Quote Management application enables sales teams to create, configure, and manage customer quotes so that they accurately reflect products, pricing, and discounts throughout the sales cycle.

-   **[Sales Agreement Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-agreement-mgmt.md)**

    The Sales Agreement Management application captures the scope and conditions from a quote for future sales transactions over a specified period between a buyer and a seller.​


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

