---
title: Combined Quote Management release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Quote Management from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-quotemanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Quote Management release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Quote Management from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Quote Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Quote Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Quote Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Sales agreement in quotes include product bundles](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&family=xanadu&ft:locale=en-US)**

Add a sales agreement to a quote that contains configurable product bundles with the ability to choose from available child offers and optional characteristics.

-   **[Location function filters products and creates line items](https://www.servicenow.com/docs/access?context=quote-using-product-location&family=xanadu&ft:locale=en-US)**

Location-based quoting is a new feature where line items can be created for different service or installation locations and agents can copy line items from one location to another. Agents can also filter products in the catalog by location.

-   **[Add covered products to a quote](https://www.servicenow.com/docs/access?context=som-quote-add-covered-products&family=xanadu&ft:locale=en-US)**

As an agent, add covered products to quote line items. Covered products include entitlements, service agreements, and warranties. Adding a covered product to a quote enables you to add start and end dates for the agreements.


-   **[Synchronize a quote with an opportunity](https://www.servicenow.com/docs/access?context=som-sync-quote-with-opportunity&family=xanadu&ft:locale=en-US)**

As an agent, synchronize quote information to an opportunity. As quote information changes, use this function to update the opportunity with information from the quote to keep records accurate.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Apply a sales agreement to a quote in Quote Management](https://www.servicenow.com/docs/access?context=quote-add-sales-agreement-quotes&family=yokohama&ft:locale=en-US)**

Create a new sales agreement or apply an existing sales agreements to a quote. When a sales agreement is enabled in a quote, the products and services added to the quote are also added to a sales agreement. When an existing sales agreement is added to a new quote, the catalog is filtered to show the products and options from the sales agreement, the price list is set to the agreement price list, and the sales agreement line is referenced on quote line.

-   **[View price adjustment details for a quote line item](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-for-quote-lines&family=yokohama&ft:locale=en-US)**

Agents gain visibility into the price adjustments that were applied to the base and list price of the product ordered. This provides sales agent the visibility of how the net price is determined.


-   **[Quote PDF documents generation](https://www.servicenow.com/docs/access?context=quote-create-pdf-document&family=yokohama&ft:locale=en-US)**

Generate a quote PDF document. Quote PDF documents can have designated signers and be emailed to customers for signatures through Docusign. Customers can also create PDF templates that reflect customer branding and logos.


-   **[Hierarchical quote line list view](https://www.servicenow.com/docs/access?context=quote-management-view-hierarchical-line-items&family=yokohama&ft:locale=en-US)**

View quote lines as a hierarchical list. Agents can then view parent and child relationships for quote line items.


-   **[Product offer recommendations for quotes](https://www.servicenow.com/docs/access?context=quote-get-product-offer&family=yokohama&ft:locale=en-US)**

Enable your agents to get product offer recommendations that complement or supplement existing products within a quote.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Quote Management features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Quote Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Quote Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The following table columns are deprecated from Quote Management.

|Table name|Column name|
|----------|-----------|
|sn\_quote\_mgmt\_core\_quote\_line\_item|cumulative\_monthly\_recurring\_price, cumulative\_annual\_recurring\_price|
|sn\_quote\_mgmt\_core\_quote|total\_monthly\_recurring\_price, total\_annual\_recurring\_price, total\_recurring\_price|

</td></tr><tr><td>

Yokohama

</td><td>

The Subscription start date and Subscription end date have been deprecated starting with the Q2 2024 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Quote Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Install Quote Management by requesting it from the ServiceNow Store.

</td></tr><tr><td>

Yokohama

</td><td>

Install Quote Management by requesting it from the ServiceNow Store.

 To add Docusign plugin to the Quote Management PDF document function, use the Docusign eSignature Spoke plugin \(sn\_docusign\_spoke\).

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Quote Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Quote Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Quote Management, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Quote Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Quote Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Add covered products to a quote.
-   Synchronize quote information with an opportunity to help ensure that the information is accurate and complete.
-   Create sales agreements that contain configurable and bundled products and services.
-   Add location-based product eligibility, which enables products to be filtered in the catalog based on location.

 See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enable agents to manage sales agreements in quotes.
-   Enable agents to view the price adjustments that are applied to the base and list price of a product in a quote.
-   Enable agents to create PDF documents from a quote using the ServiceNow PDF generator.
-   Use the hierarchical list view to view parent and child relationships within quote lines.
-   Provide agents with offer recommendations to upsell or cross-sell products that complement products in quotes.

 See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

