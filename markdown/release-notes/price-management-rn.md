---
title: Pricing Management release notes
description: The ServiceNow Pricing Management application enables your organization to create, manage, and optimize pricing and discounting strategies, so your sales team can generate opportunities, quotes, and orders with accurate, competitive pricing. See the following sections for release notes by version.Define pricing rules for individual consumers with a new context variable and return deselected lines in pricing responses. This release also improves derived product line generation in upsell and renewal quotes, prices product instance changes against existing characteristics, and makes pricing responses more consistent for integrations.Speed up derived pricing with cached rule matrix results and tailor pricing rules using new buyer organization and channel partner context variables. This release also validates pricing plan conditions before publishing and improves derived price accuracy in renewals, amendments, and bundle rollups.Automate derived product line creation, configure rounding precision for non-currency fields, and access floor and ceiling pricing values in API responses. This release also extends product life cycle support to In Test and Staged states and improves delta price calculation for consolidated renewal lines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/price-management-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 9
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

See [Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-management.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install the Pricing Management application \(sn\_csm\_pricing\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-price-management.md).

-   **Upgrade information**

    If you were using a custom pricing plan before upgrading to the v16.0.1 release, review the new default pricing plan, which is in a Retired state after the upgrade. Decide whether to publish the default plan as is or continue customizing your own plan.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/sales-order-management-rn-landing.md)

## November 2026

Define pricing rules for individual consumers with a new context variable and return deselected lines in pricing responses. This release also improves derived product line generation in upsell and renewal quotes, prices product instance changes against existing characteristics, and makes pricing responses more consistent for integrations.

### What's new

-   **[Consumer context variable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-context-variable.md)**

    Define pricing and eligibility rules for individual consumers with the new system-defined Consumer context variable for transaction lines. The variable references the Consumer \[csm\_consumer\] table.

-   **Deselected lines in the pricing response**

    Keep a complete view of the transaction in pricing responses by returning deselected lines. When the **price\_all\_lines** request setting is true, lines sent with **selected** set to false are included in the response. Deselected lines don't contribute to derived prices.


### What's changed

-   **[Derived product lines in upsell and renewal quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**

    Improve derived product line generation and placement in upsell and renewal quotes.

    -   Renewal quotes
        -   Newly generated split lines for derived products now have the Renew line type and Add action. Previously, these lines had the New line type and Add action.
        -   Split lines for derived products now inherit the applicable sold product fields from the contract line. Previously, these fields could be missing.
        -   Derived product lines in renewal quotes now show the correct term. Previously, the term was incorrect and required you to reprice the quote
    -   Upsell quotes
        -   When a source product is swapped, the derived product now gets the required Amend and Add lines.
        -   Derived product split lines are now added within their wrapper line. Previously, a split line could be added outside the wrapper.
-   **Pricing requests and responses**

    Get complete and consistent pricing responses for your integrations.

    -   Pricing continues when a setting in the request isn't defined, instead of stopping.
    -   Extra spaces in a **pricing\_elements** value are trimmed, so the list price step is no longer skipped.
    -   In upsell, renewal, and new business quotes, values that aren't numbers, such as support type, are returned as empty strings instead of null.
-   **Pricing for product instance changes**

    Price changes to product instances against the characteristics the sold product already has.

    -   Characteristic-based adjustments for modify, add, change, and disconnect requests on a product instance now use the product model characteristics of the sold product, which pricing previously left out.

## October 2026

Speed up derived pricing with cached rule matrix results and tailor pricing rules using new buyer organization and channel partner context variables. This release also validates pricing plan conditions before publishing and improves derived price accuracy in renewals, amendments, and bundle rollups.

### What's new

-   **[Cache for derived price rule results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**

    Accelerate derived pricing with cached rule matrix results, reducing repeated rule matrix evaluations for source and target product offering pairs. The improvement is especially significant for accounts with many sold products. Caching is enabled by default, and results expire after 72 hours.

-   **[Buyer organization and channel partner context variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-create-context-variable.md)**

    Tailor pricing and eligibility rules to the buyer organization or channel partner using the new Buyer Organization and Channel Partner context variables for transaction lines. Both system-defined variables reference the Customer Service Organization \[sn\_customer\_service\_organization\] table.

-   **[Extension point for line lookup in derived pricing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/extension-points-som-pricing.md)**

    Customize transaction line lookup for derived pricing by implementing the getLinesFromEntityTableEncodedQuery method of the DerivedProductPriceExtensionPoint extension point. The method returns an encoded query for the lines associated with the current header entity, such as a quote.


### What's changed

-   **[Derived pricing in renewals and amendments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**

    Calculate derived prices that reflect the current state of their source lines.

    -   When a contributing product is amended, pricing now carries the auto-renew value from the sold product to generated sold product lines, derived product lines, and other generated lines. Previously, generated lines didn't retain the auto-renew setting, causing lines such as derived product lines to have auto-renew set to false.
    -   Previously, when a source line was fully terminated \(canceled and disconnected, or canceled and added\), the markdown on the derived product line was zero. Now, the markdown is calculated from the source line's price before cancellation, so the derived line reflects the removed contribution.
    -   Only sold products whose price list currency matches the transaction currency now contribute to a derived price. Previously, sold products in other currencies could contribute when an account had sold products in multiple currencies.
    -   During early renewal, derived pricing now skips lines already covered by a consolidated contract line and excludes canceled lines from derived adjustments on renewal lines. Previously, covered lines could be added again when derived lines were generated, and canceled lines with a zero price could affect derived adjustments.
    -   In early renewal quotes, a terminated source line no longer contributes to its derived product line.
    -   Improved performance for derived price calculation for accounts with a high number of sold products.
    -   When all the source lines of a derived product line are terminated, the derived product line is now terminated as well.
-   **Bundle rollups and margin**

    Show accurate bundle totals and margins on quote lines.

    -   Bundle rollups no longer include child lines deleted from the bundle. The cumulative price uses only the remaining lines.
    -   When the cumulative net price is zero, the cumulative margin percentage is saved as zero instead of an invalid value.
-   **[Validation of pricing plan conditions before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-pricing-plan.md)**

    Prevent pricing plans with invalid conditions from reaching transactions. You can no longer publish a pricing plan with a step condition that can't be evaluated. Publishing is blocked until each step condition is valid.

-   **Context variables and rule matrices**

    Keep rule matrix evaluation accurate.

    -   A context variable and a decision table column that differ only by the u\_ prefix such as u\_age\_new or age\_new are now matched, so the rule matrix no longer falls back to its default row.
    -   The result columns of the Derived Pricing Matrix v2 decision table are loaded whenever the Pricing Matrix plugin is active, not only when demo data is installed.

## Brazil Early Availability \(September 2026\)

Automate derived product line creation, configure rounding precision for non-currency fields, and access floor and ceiling pricing values in API responses. This release also extends product life cycle support to In Test and Staged states and improves delta price calculation for consolidated renewal lines.

### What's new

-   **[Automatic addition of derived product lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-related-product-pricing.md)**

    Accelerate quoting for derived pricing by automating the creation and alignment of derived product lines. Sellers add the source products and the derived product to the transaction. The pricing engine then generates the required derived lines, aligns their dates to the source lines that fund them, and keeps them synchronized as the sources change. The engine automatically splits derived lines when a source is ramped or amended, ensuring date ranges remain aligned across all related lines.

    Previously, sellers manually calculated and aligned dates for derived lines. If a derived line's dates did not align with its sources, the line was excluded from the price calculation.

    System-generated lines are marked with the System generated \[**system\_generated**\] field set to true, which distinguishes them from seller-added lines.

-   **Configurable rounding precision for non-currency pricing fields**

    Configure the rounding precision applied to non-currency pricing fields, such as margin percentage, to match your organization's rounding requirements. The default precision is 4 decimal digits. To use a different precision, set the **sn\_csm\_pricing.rounding.non\_currency\_max\_precision\_digits** property in the system properties. Viewing or setting this property requires the Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\) role.

-   **Floor and ceiling price in the pricing response**

    Access floor and ceiling pricing values directly in pricing responses and persist them on custom quote or order line fields for downstream business processes and validations. To include these values in the response, the include\_floor\_ceiling pricing request setting must be set to true. When the setting is absent or false, floor and ceiling price are omitted from the response. If pricing\_elements setting isn't specified in the request, the PRICE element is included by default.


### What's changed

-   **Extended product life cycle support in Price Management**

    Validate pricing setup against catalog changes earlier in their life cycle by extending product offering life cycle visibility into Price Management.

    -   Previously, price list lines, cost book lines, and attribute adjustments could reference only Published product offerings. Now, when extended product life cycle states are enabled, they can also reference offerings in the In Test and Staged states. This enables the pricing admin to create price lists and define rules in pricing matrices for offerings that are in the In Test and Staged states.
    -   Previously, context variable rules and pricing matrix rules could filter on Published product offerings only. Now, they can also filter on offerings in the In Test and Staged states.
-   **[Delta price calculation for consolidated renewal lines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/renewal-pricing-ramped-products.md)**

    Calculate delta price more accurately for renewal lines that consolidate multiple contract line items affected by upsells or downsells. The calculation now uses the prior contract value over the subscription's full previous term, together with the new renewal price including uplift, to determine the delta price amount.


### What's deprecated or removed

-   **Parallel execution properties for the pricing engine**

    The sn\_csm\_pricing.enable\_pricing\_engine\_parallel\_execution and sn\_csm\_pricing.pricing\_engine\_parallelism\_lines\_threshold Pricing Engine Parallel Execution properties have been removed. These properties previously controlled parallel execution of pricing plan steps in the pricing engine. The pricing engine now processes pricing requests sequentially. This change helps ensure that rollup calculations and auto-added derived pricing are applied correctly. No replacement properties are available.


