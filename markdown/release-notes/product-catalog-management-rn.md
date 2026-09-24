---
title: Product Catalog Management release notes
description: The ServiceNow Product Catalog Management application helps your organization manage product offerings by grouping them into catalogs and categories, which streamlines the ordering process for leads, opportunities, quotes, and orders. See the following sections for release notes by version.Validate catalog changes before publishing, control when a published offering becomes available on each sales channel. Add optional characteristics and child offerings to published records without creating new versions. Generate multilingual catalog configurations automatically and set a custom display order for catalogs and categories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/product-catalog-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Product Catalog Management release notes

The ServiceNow® Product Catalog Management application helps your organization manage product offerings by grouping them into catalogs and categories, which streamlines the ordering process for leads, opportunities, quotes, and orders. See the following sections for release notes by version.

## About Product Catalog Management

-   Accelerate product launches by creating, publishing, and managing commercial and technical offerings from a centralized catalog foundation.
-   Simplify complex product sales with support for configurable products, bundles, and service-based offerings.
-   Connect sales and fulfillment processes through a unified catalog that powers the lead-to-cash life cycle.
-   Manage catalog changes with confidence using controlled versioning and scheduled product updates.
-   Help sellers find and sell the right products faster with organized catalogs, eligibility controls, and intuitive navigation.

See [Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md) for more information.

## Activation and other requirements

-   **Activation information**

    Activate Product Catalog Management Core \(sn\_prd\_pm\) from the plugin activation page. A System Administrator role is required. Activation includes demo data and installs any related applications and plugins that aren't already active on your instance.


## Accessibility and localization

-   **Localization information**

    Certain Product Catalog Management fields, such as product offering name and description, support multilingual text. Admins can display these fields in multiple languages in the product catalog interface when the corresponding ServiceNow base system language plugin is active.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Brazil Early Availability

Validate catalog changes before publishing, control when a published offering becomes available on each sales channel. Add optional characteristics and child offerings to published records without creating new versions. Generate multilingual catalog configurations automatically and set a custom display order for catalogs and categories.

### What's new

-   **[Extended product life cycle states for product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)**

    Validate product offerings and specifications before publication by moving them through the In Test and Staged life cycle states. Build and test catalog hierarchies without publishing unfinished records, helping reduce unnecessary revisions and prevent incomplete catalog content from becoming available to users.

-   **[Channel-specific availability for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/channel-specific-availability.md)**

    Coordinate phased product launches by releasing a published product offering to different distribution channels on different dates. Use channel overrides to align product availability with channel readiness, training, partner enablement, or regional rollout plans without delaying channels that are ready to launch. The offering stays hidden from a channel, in both catalog search and AI Search, until that channel's release date arrives.

    A new table, Product Offering Channel Override \[sn\_prd\_pm\_product\_offering\_channel\_override\], has been introduced to support this feature.

-   **[Localized product catalog experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-multi-locale-catalogs.md)**

    Generate language-specific versions of product catalogs and product offerings when they are published so sales agents can view product names, descriptions, and characteristics in their preferred language across configurator screens, carts, and quotes. If translated content isn't available for a language, the default-language version is displayed automatically.

    The following new tables have been introduced to support this feature:

    -   Product Offering Translation \[sn\_prd\_pm\_product\_offering\_translation\]
    -   Product Offering Catalog Translation \[sn\_prd\_pm\_product\_offering\_catalog\_translation\]
-   **[Customize the display order of product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-managing-product-catalogs.md)**

    Help sales agents find relevant product offerings faster by defining how offerings appear in the Catalog UI, both on the CRM Workspace and Business Portal. Sales agents can sort product offerings by Display Order, making it easier to surface prioritized offerings while creating quotes and orders instead of sorting alphabetically. A catalog or category without a configured order continues to sort alphabetically.


### What's changed

-   **[Minor updates to published product offerings and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/minor-updates-published-offerings-specs.md)**

    Simplify updates to published product offerings by adding optional characteristics and optional child offerings without creating a new offering version. Set a future effective date for the child-offering relationship to control when the child becomes available for new purchases or order changes. Previously, these updates required a new version of the parent offering and replication of its related configuration.

    Previously, turning on the transient setting for a published product offering required creating a new version. Now, turning it on doesn't require a new version. Turning it off still requires one.

-   **[Product catalog sort options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)**

    Previously, the sort drop-down menu in the product catalog was hidden unless AI Search was turned on. Now it is always available, and includes a new Display Order option that sorts by your configured display order. The Relevancy option still appears only when AI Search is on.

-   **Product Catalog Management data model changes**

    New columns have been added to the Product Catalog Management tables to enable new life cycle states, channel-specific launch dates, and control the display sequence of offerings in the catalog.

    -   Value column has been added to the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table. It canonically maps the channel name resolved from the context variable or the Sales CRM entity header to the sys\_id \(Name\) in the Distribution Channel \[sn\_prd\_pm\_distribution\_channel\] table.
    -   State column on the Product Offering \[sn\_prd\_pm\_product\_offering\] table now includes In Test and Staged values, sequenced between Draft and Published. A new Approval state column has been added, with values Not yet requested \(default\), In Review, Approved, Rejected, and Recalled. A new Active channels column has also been added. It's a read-only, comma-separated list of distribution channel references that stores the channels the offering is currently available on, so catalog search can filter on availability without a table join.
    -   State column on the Specification \[sn\_prd\_pm\_specification\] table now includes In Test and Staged values, sequenced between Draft and Published.
    -   Effective from column has been added to the Product Offering Relationship \[sn\_prd\_pm\_product\_offering\_relationship\] and Specification Relationship \[sn\_prd\_pm\_specification\_relationship\] tables.
    -   Order column has been added to the Catalog Category \[sn\_prd\_pm\_catalog\_category\_relationship\] and Product Offering Catalog \[sn\_prd\_pm\_product\_offering\_catalog\] tables.
    -   Display Order column has been added to the Product Offering \[sn\_prd\_pm\_product\_offering\] table

