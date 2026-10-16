---
title: Combined ServiceNow Quote Experience release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for ServiceNow Quote Experience from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-servicenowquoteexperience-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Quote Experience release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for ServiceNow Quote Experience from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Quote Experience release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Quote Experience to Brazil

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

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for ServiceNow Quote Experience.

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

-   **[Quote Experience configuration for subscriptions](https://www.servicenow.com/docs/access?context=sm-configuring-subscription-quote-experience&family=brazil&ft:locale=en-US)**

Import the system-provided blueprint to define the fields and rules for populating, representing, and validating quote data. The blueprint includes transaction header-level fields, transaction line-level fields, line type and line action fields, business rules, and guardrails that enable ServiceNow Quote Experience to process subscription amendments and renewals.

-   **[Transaction header-level system fields for subscriptions](https://www.servicenow.com/docs/access?context=sm-quote-tm-system-fields&family=brazil&ft:locale=en-US)**

Reference the transaction header-level fields that ServiceNow Quote Experience uses to process subscription amendments and renewals.

-   **[Transaction line-level system fields for subscriptions](https://www.servicenow.com/docs/access?context=sm-quote-tm-system-line-fields&family=brazil&ft:locale=en-US)**

Reference the transaction line-level fields that ServiceNow Quote Experience uses to process subscription amendments and renewals.

-   **[Line type and line action fields for subscriptions](https://www.servicenow.com/docs/access?context=sm-quote-tm-line-type-action-fields&family=brazil&ft:locale=en-US)**

Reference the line type and line action fields that ServiceNow Quote Experience uses to process subscription amendments and renewals. These values add context to transaction fields and identify the type of change and action required for upsells, downsells, end date changes, product swaps, and standard and early renewals.

-   **[Header-level and line-level business rules for subscriptions](https://www.servicenow.com/docs/access?context=sm-quote-tm-header-level-business-rules&family=brazil&ft:locale=en-US)**

Reference the business rules that ServiceNow Quote Experience uses to process data from subscription workflows. Business rules work with transaction fields, line type, and line action to support accurate quote processing and downstream workflows.

-   **[Guardrail rules for subscriptions](https://www.servicenow.com/docs/access?context=sm-tm-subscription-guardrails-quote&family=brazil&ft:locale=en-US)**

Reference the guardrails that ServiceNow Quote Experience uses to help prevent invalid changes during amendment and renewal processing. Guardrails work with transaction fields, line type, line action, and business rules to maintain quote validity.


 -   **ServiceNow Quote Experience Experience integration with Contracts**

Amend simple and configurable products that originate from a contract, directly within a quote. Amend the products from a contract to complete upsell, downsell, and end-date changes, including early termination and extension. You can also renew the products from a contract using standard renewal, early renewal, or automatic renewal operations.

-   **ServiceNow Quote Experience Integration with Subscription Management**

Subscription Management integrates with ServiceNow Quote Experience, CPQ Configurator, and the Pricing Management to provide a unified experience throughout the Subscription Management lifecycle.

-   **[Pricing in the ServiceNow Quote Experience](https://www.servicenow.com/docs/access?context=pricing-in-quote-experience&family=brazil&ft:locale=en-US)**

Calculate and adjust transaction pricing directly from a quote.

    -   Enable Pricing setup without manual field mappings. Set the pricing integration type to **productized**, and the application loads context-variable mappings from blueprint metadata and connects to the pricing service automatically when the blueprint is deployed.
    -   Reprice on demand or automatically. Recalculate transaction pricing with the Reprice action, or let it recalculate when a configuration is added to a quote. Administrators can turn off the default triggers for each event.
    -   Set automatic pricing behavior by stage. For example, enable automatic reprice in **Draft** stage, but disable for **Order Submitted** stage.
    -   Adjust prices manually. Apply a fixed-amount or percentage discount or uplift to a line or the header total. Each adjustment is preserved as a distinct input and tracked for audit.
    -   Apply automatic price adjustments. Use rules such as volume tiers, promotions, and contracted discounts during a pricing call. A manual adjustment always takes precedence over an automatic one on the same line or header.
-   **Configure ServiceNow Quote Experience through Guided Setup**

Set up ServiceNow Quote Experience directly from the Guided Setup for CPQ Integration. Configure it alongside the rest of your CPQ integration in a single guided flow, instead of configuring components separately.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing ServiceNow Quote Experience features.

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
</table>## Removed

Between your current release family and Brazil, some ServiceNow Quote Experience features or functionality were removed.

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

Between your current release family and Brazil, some ServiceNow Quote Experience features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate ServiceNow Quote Experience.

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

Install the Pricing Management application \(`sn_csm_pricing`\) from the ServiceNow Store. For more information, see [Install Pricing Management](https://www.servicenow.com/docs/access?context=install-price-management&family=brazil&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Quote Experience we have noted them here.

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

If any specific browser requirements were introduced or changed for ServiceNow Quote Experience we have noted them here.

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

Review details on accessibility information for ServiceNow Quote Experience, such as specific requirements or compliance levels.

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

-   **Accessibility information**

Color contrast in ServiceNow Quote Experience was updated to display all interface elements clearly in dark-themed environments. This update helps users view and interact with all interface elements clearly in a dark-themed environment.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Quote Experience we have noted them here.

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

-   **Localization information**

Enhanced localization in CPQ: Translation and localization support is enhanced to include product offering labels, definitions, and field text in CPQ. Content is translated at compile time, enabling multilingual configuration workflows and a more consistent localized experience.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Quote Experience we have noted them here.

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

The ServiceNow Quote Experience is enhanced to integrate with Subscription Management and supports the complete lifecycle of Subscription Management workflows. Using ServiceNow Quote Experience, you can:

-   Amend a contract by adding or removing products mid-term, including upsells and downsells. The Pricing Service automatically calculates deltas and adjusts pricing changes accordingly.
-   Swap one product offering with another. Initiate a full or partial swap, while maintaining contract continuity.
-   Create an auto-renewal automatically, enabling a renewal pipeline before expiration.
-   Initiate an early or late renewal and add or remove products during the renewal process, providing greater flexibility to accommodate changing needs.

 See [Subscription Management in Quote Experience](https://www.servicenow.com/docs/access?context=sm-quote-integration&family=brazil&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

