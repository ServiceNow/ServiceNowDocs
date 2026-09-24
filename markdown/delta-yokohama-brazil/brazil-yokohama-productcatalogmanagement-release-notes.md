---
title: Combined Product Catalog Management release notes for upgrades from Yokohama to Brazil
description: Consolidated page of all release notes for Product Catalog Management from Yokohama to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-brazil/brazil-yokohama-productcatalogmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Product Catalog Management release notes for upgrades from Yokohama to Brazil

Consolidated page of all release notes for Product Catalog Management from Yokohama to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Product Catalog Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Product Catalog Management to Brazil

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

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Product Catalog Management.

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

-   **[Extended product life cycle states for product offerings and specifications](https://www.servicenow.com/docs/access?context=extended-product-lifecycle-states&family=brazil&ft:locale=en-US)**

Validate product offerings and specifications before publication by moving them through the In Test and Staged life cycle states. Build and test catalog hierarchies without publishing unfinished records, helping reduce unnecessary revisions and prevent incomplete catalog content from becoming available to users.

-   **[Channel-specific availability for product offerings](https://www.servicenow.com/docs/access?context=channel-specific-availability&family=brazil&ft:locale=en-US)**

Coordinate phased product launches by releasing a published product offering to different distribution channels on different dates. Use channel overrides to align product availability with channel readiness, training, partner enablement, or regional rollout plans without delaying channels that are ready to launch. The offering stays hidden from a channel, in both catalog search and AI Search, until that channel's release date arrives.

A new table, Product Offering Channel Override \[sn\_prd\_pm\_product\_offering\_channel\_override\], has been introduced to support this feature.

-   **[Localized product catalog experiences](https://www.servicenow.com/docs/access?context=enable-multi-locale-catalogs&family=brazil&ft:locale=en-US)**

Generate language-specific versions of product catalogs and product offerings when they are published so sales agents can view product names, descriptions, and characteristics in their preferred language across configurator screens, carts, and quotes. If translated content isn't available for a language, the default-language version is displayed automatically.

The following new tables have been introduced to support this feature:

    -   Product Offering Translation \[sn\_prd\_pm\_product\_offering\_translation\]
    -   Product Offering Catalog Translation \[sn\_prd\_pm\_product\_offering\_catalog\_translation\]
-   **[Customize the display order of product offerings](https://www.servicenow.com/docs/access?context=som-managing-product-catalogs&family=brazil&ft:locale=en-US)**

Help sales agents find relevant product offerings faster by defining how offerings appear in the Catalog UI, both on the CRM Workspace and Business Portal. Sales agents can sort product offerings by Display Order, making it easier to surface prioritized offerings while creating quotes and orders instead of sorting alphabetically. A catalog or category without a configured order continues to sort alphabetically.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Product Catalog Management features.

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

-   **[Minor updates to published product offerings and specifications](https://www.servicenow.com/docs/access?context=minor-updates-published-offerings-specs&family=brazil&ft:locale=en-US)**

Simplify updates to published product offerings by adding optional characteristics and optional child offerings without creating a new offering version. Set a future effective date for the child-offering relationship to control when the child becomes available for new purchases or order changes. Previously, these updates required a new version of the parent offering and replication of its related configuration.

Previously, turning on the transient setting for a published product offering required creating a new version. Now, turning it on doesn't require a new version. Turning it off still requires one.

-   **[Product catalog sort options](https://www.servicenow.com/docs/access?context=using-product-catalog&family=brazil&ft:locale=en-US)**

Previously, the sort drop-down menu in the product catalog was hidden unless AI Search was turned on. Now it is always available, and includes a new Display Order option that sorts by your configured display order. The Relevancy option still appears only when AI Search is on.

-   **Product Catalog Management data model changes**

New columns have been added to the Product Catalog Management tables to enable new life cycle states, channel-specific launch dates, and control the display sequence of offerings in the catalog.

    -   Value column has been added to the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. It canonically maps the channel name resolved from the context variable or the Sales CRM entity header to the sys\_id \(Name\) in the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.
    -   State column on the Product Offering \[sn\_prd\_pm\_product\_offering\] table now includes In Test and Staged values, sequenced between Draft and Published. A new Approval state column has been added, with values Not yet requested \(default\), In Review, Approved, Rejected, and Recalled. A new Active channels column has also been added. It's a read-only, comma-separated list of distribution channel references that stores the channels the offering is currently available on, so catalog search can filter on availability without a table join.
    -   State column on the Specification \[sn\_prd\_pm\_specification\] table now includes In Test and Staged values, sequenced between Draft and Published.
    -   Effective from column has been added to the Product Offering Relationship \[sn\_prd\_pm\_product\_offering\_relationship\] and Specification Relationship \[sn\_prd\_pm\_specification\_relationship\] tables.
    -   Order column has been added to the Catalog Category \[sn\_prd\_pm\_catalog\_category\_relationship\] and Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] tables.
    -   Display Order column has been added to the Product Offering \[sn\_prd\_pm\_product\_offering\] table

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Product Catalog Management features or functionality were removed.

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

Between your current release family and Brazil, some Product Catalog Management features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Product Catalog Management.

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

Activate Product Catalog Management Core \(sn\_prd\_pm\) from the plugin activation page. A System Administrator role is required. Activation includes demo data and installs any related applications and plugins that aren't already active on your instance.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Product Catalog Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Product Catalog Management we have noted them here.

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

Review details on accessibility information for Product Catalog Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Product Catalog Management we have noted them here.

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

-   **Localization information**

Certain Product Catalog Management fields, such as product offering name and description, support multilingual text. Admins can display these fields in multiple languages in the product catalog interface when the corresponding ServiceNow base system language plugin is active.


</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Product Catalog Management we have noted them here.

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

-   Accelerate product launches by creating, publishing, and managing commercial and technical offerings from a centralized catalog foundation.
-   Simplify complex product sales with support for configurable products, bundles, and service-based offerings.
-   Connect sales and fulfillment processes through a unified catalog that powers the lead-to-cash life cycle.
-   Manage catalog changes with confidence using controlled versioning and scheduled product updates.
-   Help sellers find and sell the right products faster with organized catalogs, eligibility controls, and intuitive navigation.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-yokohama-brazil/rn-combined-intro.md)

