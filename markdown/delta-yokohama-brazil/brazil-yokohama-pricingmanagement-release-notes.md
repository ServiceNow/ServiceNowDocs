---
title: Combined Pricing Management release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Pricing Management from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-pricingmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-11-19"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Pricing Management release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Pricing Management from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Pricing Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **Upgrade information**

If you were using a custom pricing plan before upgrading to the v16.0.1 release, review the new default pricing plan, which is in a Retired state after the upgrade. Decide whether to publish the default plan as is or continue customizing your own plan.


</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Pricing Management.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **[Consumer context variable](https://www.servicenow.com/docs/access?context=som-create-context-variable&family=brazil&ft:locale=en-US)**

Define pricing and eligibility rules for individual consumers with the new system-defined Consumer context variable for transaction lines. The variable references the Consumer \[csm\_consumer\] table.

-   **[Deselected lines in the pricing response](https://www.servicenow.com/docs/access?context=sales_crm_pricing-POST-compute-price&family=brazil&ft:locale=en-US)**

Keep a complete view of the transaction in pricing responses by returning deselected lines. When the **price\_all\_lines** request setting is true, lines sent with **selected** set to false are included in the response. Deselected lines don't contribute to derived prices.


 -   **[Cache for derived price rule results](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=brazil&ft:locale=en-US)**

Accelerate derived pricing with cached rule matrix results, reducing repeated rule matrix evaluations for source and target product offering pairs. The improvement is especially significant for accounts with many sold products. Caching is enabled by default, and results expire after 72 hours.

-   **[Buyer organization and channel partner context variables](https://www.servicenow.com/docs/access?context=som-create-context-variable&family=brazil&ft:locale=en-US)**

Tailor pricing and eligibility rules to the buyer organization or channel partner using the new Buyer Organization and Channel Partner context variables for transaction lines. Both system-defined variables reference the Customer Service Organization \[sn\_customer\_service\_organization\] table.

-   **[Extension point for line lookup in derived pricing](https://www.servicenow.com/docs/access?context=extension-points-som-pricing&family=brazil&ft:locale=en-US)**

Customize transaction line lookup for derived pricing by implementing the getLinesFromEntityTableEncodedQuery method of the DerivedProductPriceExtensionPoint extension point. The method returns an encoded query for the lines associated with the current header entity, such as a quote.


 -   **[Automatic addition of derived product lines](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=brazil&ft:locale=en-US)**

Accelerate quoting for derived pricing by automating the creation and alignment of derived product lines. Sellers add the source products and the derived product to the transaction. The pricing engine then generates the required derived lines, aligns their dates to the source lines that fund them, and keeps them synchronized as the sources change. The engine automatically splits derived lines when a source is ramped or amended, ensuring date ranges remain aligned across all related lines.

Previously, sellers manually calculated and aligned dates for derived lines. If a derived line's dates did not align with its sources, the line was excluded from the price calculation.

System-generated lines are marked with the System generated \[**system\_generated**\] field set to true, which distinguishes them from seller-added lines.

-   **[Configurable rounding precision for non-currency pricing fields](https://www.servicenow.com/docs/access?context=pricing-management-properties&family=brazil&ft:locale=en-US)**

Configure the rounding precision applied to non-currency pricing fields, such as margin percentage, to match your organization's rounding requirements. The default precision is 4 decimal digits. To use a different precision, set the **sn\_csm\_pricing.rounding.non\_currency\_max\_precision\_digits** property in the system properties. Viewing or setting this property requires the Price List Administrator \(sn\_csm\_pricing.pricelist\_administrator\) role.

-   **[Floor and ceiling price in the pricing response](https://www.servicenow.com/docs/access?context=sales_crm_pricing-POST-compute-price&family=brazil&ft:locale=en-US)**

Access floor and ceiling pricing values directly in pricing responses and persist them on custom quote or order line fields for downstream business processes and validations. To include these values in the response, the include\_floor\_ceiling pricing request setting must be set to true. When the setting is absent or false, floor and ceiling price are omitted from the response. If pricing\_elements setting isn't specified in the request, the PRICE element is included by default.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Pricing Management features.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **[Derived product lines in upsell and renewal quotes](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=brazil&ft:locale=en-US)**

Improve derived product line generation and placement in upsell and renewal quotes.

    -   Renewal quotes
        -   Newly generated split lines for derived products now have the Renew line type and Add action. Previously, these lines had the New line type and Add action.
        -   Split lines for derived products now inherit the applicable sold product fields from the contract line. Previously, these fields could be missing.
        -   Derived product lines in renewal quotes now show the correct term. Previously, the term was incorrect and required you to reprice the quote
    -   Upsell quotes
        -   When a source product is swapped, the derived product now gets the required Amend and Add lines.
        -   Derived product split lines are now added within their wrapper line. Previously, a split line could be added outside the wrapper.
    -   Early renewals
        -   For early renewals that cover multiple contracts, source lines, target lines, and sold products are now limited to the contract being renewed. Previously, a no-change line could be selected from a different contract.
        -   No-change lines are now skipped when the parent line is also renewed. Previously, these lines could be inserted under the renewal wrapper.
-   **[Pricing requests and responses](https://www.servicenow.com/docs/access?context=sales_crm_pricing-POST-compute-price&family=brazil&ft:locale=en-US)**

Get complete and consistent pricing responses for your integrations.

    -   Pricing continues when a setting in the request isn't defined, instead of stopping.
    -   Extra spaces in a **pricing\_elements** value are trimmed, so the list price step is no longer skipped.
    -   When **use\_external\_code** is true, **product\_offering** returns the external ID code rather than the sys\_id.
    -   In upsell, renewal, and new business quotes, values that aren't numbers, such as support type, are returned as empty strings instead of null.
-   **Pricing for product instance changes**

Price changes to product instances against the characteristics the sold product already has.

    -   Characteristic-based adjustments for modify, add, change, and disconnect requests on a product instance now use the product model characteristics of the sold product, which pricing previously left out.

 -   **[Derived pricing in renewals and amendments](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&family=brazil&ft:locale=en-US)**

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
-   **[Validation of pricing plan conditions before publishing](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=brazil&ft:locale=en-US)**

Prevent pricing plans with invalid conditions from reaching transactions. You can no longer publish a pricing plan with a step condition that can't be evaluated. Publishing is blocked until each step condition is valid.

-   **Context variables and rule matrices**

Keep rule matrix evaluation accurate.

    -   A context variable and a decision table column that differ only by the u\_ prefix such as u\_age\_new or age\_new are now matched, so the rule matrix no longer falls back to its default row.
    -   The result columns of the Derived Pricing Matrix v2 decision table are loaded whenever the Pricing Matrix plugin is active, not only when demo data is installed.

 -   **[Extended product life cycle support in Price Management](https://www.servicenow.com/docs/access?context=extended-product-lifecycle-states&family=brazil&ft:locale=en-US)**

Validate pricing setup against catalog changes earlier in their life cycle by extending product offering life cycle visibility into Price Management.

    -   Previously, price list lines, cost book lines, and attribute adjustments could reference only Published product offerings. Now, when extended product life cycle states are enabled, they can also reference offerings in the In Test and Staged states. This enables the pricing admin to create price lists and define rules in pricing matrices for offerings that are in the In Test and Staged states.
    -   Previously, context variable rules and pricing matrix rules could filter on Published product offerings only. Now, they can also filter on offerings in the In Test and Staged states.
-   **[Delta price calculation for consolidated renewal lines](https://www.servicenow.com/docs/access?context=renewal-pricing-ramped-products&family=brazil&ft:locale=en-US)**

Calculate delta price more accurately for renewal lines that consolidate multiple contract line items affected by upsells or downsells. The calculation now uses the prior contract value over the subscription's full previous term, together with the new renewal price including uplift, to determine the delta price amount.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Pricing Management features or functionality were removed.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Pricing Management features or functionality were deprecated.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **Parallel execution properties for the pricing engine**

The sn\_csm\_pricing.enable\_pricing\_engine\_parallel\_execution and sn\_csm\_pricing.pricing\_engine\_parallelism\_lines\_threshold Pricing Engine Parallel Execution properties have been removed. These properties previously controlled parallel execution of pricing plan steps in the pricing engine. The pricing engine now processes pricing requests sequentially. This change helps ensure that rollup calculations and auto-added derived pricing are applied correctly. No replacement properties are available.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Pricing Management.

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

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Install the Pricing Management application \(sn\_csm\_pricing\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://www.servicenow.com/docs/access?context=install-price-management&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Pricing Management we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Pricing Management we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Pricing Management, such as specific requirements or compliance levels.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Pricing Management we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Pricing Management we have noted them here.

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

</td></tr><tr><td>

Brazil

</td><td>

-   Deliver accurate and competitive pricing across opportunities, quotes, and orders by centrally managing prices for products and services.
-   Tailor pricing to each selling context by applying adjustments based on product attributes, customer accounts, markets, sales channels, quantities, and bundles.

-   Protect profit margins by giving sellers cost and margin visibility and applying pricing controls that limit excessive discounting
-   Support complex pricing models for one-time and recurring charges, configurable products, bundles, renewals, amendments, and products with price and quantity ramps
-   Increase pricing transparency by providing a clear record of the adjustments used to calculate the final selling price.

 See [Product pricing](https://www.servicenow.com/docs/access?context=pricing-management&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

