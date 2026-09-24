---
title: Combined Pricing Management release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Pricing Management from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-pricingmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Pricing Management release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Pricing Management from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Pricing Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

