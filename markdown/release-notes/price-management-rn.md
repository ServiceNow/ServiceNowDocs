---
title: Pricing Management release notes
description: The ServiceNow Pricing Management application enables your organization to create, manage, and optimize pricing and discounting strategies, so your sales team can generate opportunities, quotes, and orders with accurate, competitive pricing. See the following sections for release notes by version.Price Management version 18.0.3 adds floor and ceiling pricing values in API responses, configurable rounding precision for non-currency fields, and automatic generation of derived product lines. This release also extends product life cycle support and improves delta price calculation for consolidated renewals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/price-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Pricing Management release notes

The ServiceNow® Pricing Management application enables your organization to create, manage, and optimize pricing and discounting strategies, so your sales team can generate opportunities, quotes, and orders with accurate, competitive pricing. See the following sections for release notes by version.

## About Pricing Management

-   Deliver accurate and competitive pricing across opportunities, quotes, and orders by centrally managing prices for products and services.
-   Tailor pricing to each selling context by applying adjustments based on product attributes, customer accounts, markets, sales channels, quantities, and bundles.

-   Protect profit margins by giving sellers cost and margin visibility and applying pricing controls that limit excessive discounting
-   Support complex pricing models for one-time and recurring charges, configurable products, bundles, renewals, amendments, and products with price and quantity ramps
-   Increase pricing transparency by providing a clear record of the adjustments used to calculate the final selling price.

See [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-management.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install the Pricing Management application \(sn\_csm\_pricing\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/install-price-management.md).

-   **Upgrade information**

    If you were using a custom pricing plan before upgrading to the v16.0.1 release, review the new default pricing plan, which is in a Retired state after the upgrade. Decide whether to publish the default plan as is or continue customizing your own plan.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Version 18.0.3

Price Management version 18.0.3 adds floor and ceiling pricing values in API responses, configurable rounding precision for non-currency fields, and automatic generation of derived product lines. This release also extends product life cycle support and improves delta price calculation for consolidated renewals.

### What's new

-   **[Automatic addition of derived product lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/configuring-related-product-pricing.md)**

    Accelerate quoting for derived pricing by automating the creation and alignment of derived product lines. Sellers add the source products and the derived product to the transaction. The pricing engine then generates the required derived lines, aligns their dates to the source lines that fund them, and keeps them synchronized as the sources change. The engine automatically splits derived lines when a source is ramped or amended, ensuring date ranges remain aligned across all related lines.

    Previously, sellers manually calculated and aligned dates for derived lines. If a derived line's dates did not align with its sources, the line was excluded from the price calculation.

    System-generated lines are marked with the System generated \[**system\_generated**\] field set to true, which distinguishes them from seller-added lines.

-   **[Configurable rounding precision for non-currency pricing fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/pricing-management-properties.md)**

    Configure the rounding precision applied to non-currency pricing fields, such as margin percentage, to match your organization's rounding requirements. The default precision is 4 decimal digits. To use a different precision, set the **sn\_csm\_pricing.rounding.non\_currency\_max\_precision\_digits** property in the system properties. Viewing or setting this property requires the Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\) role.

-   **[Floor and ceiling price in the pricing response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/sales_crm_pricing-POST-compute-price.md)**

    Access floor and ceiling pricing values directly in pricing responses and persist them on custom quote or order line fields for downstream business processes and validations. To include these values in the response, the include\_floor\_ceiling pricing request setting must be set to true. When the setting is absent or false, floor and ceiling price are omitted from the response. If pricing\_elements setting isn't specified in the request, the PRICE element is included by default.


### What's changed

-   **[Extended product life cycle support in Price Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)**

    Validate pricing setup against catalog changes earlier in their life cycle by extending product offering life cycle visibility into Price Management.

    -   Previously, price list lines, cost book lines, and attribute adjustments could reference only Published product offerings. Now, when extended product life cycle states are enabled, they can also reference offerings in the In Test and Staged states. This enables the pricing admin to create price lists and define rules in pricing matrices for offerings that are in the In Test and Staged states.
    -   Previously, context variable rules and pricing matrix rules could filter on Published product offerings only. Now, they can also filter on offerings in the In Test and Staged states.
-   **[Delta price calculation for consolidated renewal lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/renewal-pricing-ramped-products.md)**

    Calculate delta price more accurately for renewal lines that consolidate multiple contract line items affected by upsells or downsells. The calculation now uses the prior contract value over the subscription's full previous term, together with the new renewal price including uplift, to determine the delta price amount.


### What's deprecated or removed

-   **Parallel execution properties for the pricing engine**

    The sn\_csm\_pricing.enable\_pricing\_engine\_parallel\_execution and sn\_csm\_pricing.pricing\_engine\_parallelism\_lines\_threshold Pricing Engine Parallel Execution properties have been removed. These properties previously controlled parallel execution of pricing plan steps in the pricing engine. The pricing engine now processes pricing requests sequentially. This change helps ensure that rollup calculations and auto-added derived pricing are applied correctly. No replacement properties are available.


