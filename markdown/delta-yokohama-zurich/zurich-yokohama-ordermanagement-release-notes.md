---
title: Combined Order Management release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Order Management from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-ordermanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Order Management release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Order Management from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Order Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Order Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Order Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Business Portal for order case management](https://servicenow-staging.fluidtopics.net/access?context=order-mgt-business-portal&family=yokohama&ft:locale=en-US)**

Enable your customers to create cases for common order-related issues such as delivery delays, quantity disputes, and other routine inquiries directly using the Business Portal, ensuring faster issue resolution and improved customer satisfaction. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **Hierarchical view of order line items**

Enable order agents and order managers to use the hierarchical list view to view parent and child relationships within order lines.

-   **[Price adjustment details for order lines](https://servicenow-staging.fluidtopics.net/access?context=view-price-adjustment-details-order-lines&family=yokohama&ft:locale=en-US)**

Provides order agents and order managers the visibility into the price adjustments applied at each step of the pricing plan, including a detailed breakdown of all adjustments applied to the unit base price and unit list price to see how the unit net price is derived.

-   **[Multi-instance product offering configurations](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Create multiple instances of a child product offering in orders to generate a custom configuration for each product offering instance. When a child product offering has a quantity greater than 1, agents can clone or split a child product offering to create multiple product offering instances so that each quantity has its own configuration.

-   **[Transient products](https://servicenow-staging.fluidtopics.net/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Add transient products, which are defined as one-time-use products or services, to new orders. Sold product and product inventory records are created but not maintained for transient products. Move, Add, Change and Disconnect \(MACD\) actions are not supported for transient products.

-   **[Business Portal for Order Management](https://servicenow-staging.fluidtopics.net/access?context=order-mgt-create-an-order-using-customer-portal&family=yokohama&ft:locale=en-US)**

Use the Business Portal to view product catalogs, select product options, and place orders. Customers can also view their order status using the Business Portal.

-   **[Cases for multiple invoices](https://servicenow-staging.fluidtopics.net/access?context=csm-invoice-operations&family=yokohama&ft:locale=en-US)**

Create cases for multiple invoices or for specific invoice lines. Agents can reference multiple invoices or invoice lines as case line items on an invoice case record. By using case line items, agents can track multiple issues for the same invoice case and resolve the issues in each case line item independently before resolving and closing the order case. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **[Add subscription pricing to an order](https://servicenow-staging.fluidtopics.net/access?context=add-subscription-pricing-to-an-order&family=yokohama&ft:locale=en-US)**

Enable order agents and order managers to access and view key calculated metrics such as monthly recurring price and annual recurring price. The subscription pricing fields are automatically calculated based on contract start date and contract end date. These metrics enhance revenue reporting and help you to better understand recurring revenue dynamics.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Move order](https://servicenow-staging.fluidtopics.net/access?context=move-order&family=zurich&ft:locale=en-US)**

The move order helps agents to perform move journey that requires location change, the location and change of attribute values, the location change and add or delete the product.


-   **[Pricing Adjustments for order line items](https://servicenow-staging.fluidtopics.net/access?context=add-pricing-adjustment-to-an-order-line-item&family=zurich&ft:locale=en-US)**

Enables order agents to quickly view, add, and edit manual price adjustments for order line items directly from the list view, reducing clicks and streamlining the process. This new experience makes it easier for order agents to enter manual price adjustments and provides a holistic view of both automatic and manual adjustments.

-   **[Summarization for Order Management](https://servicenow-staging.fluidtopics.net/access?context=now-assist-order-mgmt-summarize-order&family=zurich&ft:locale=en-US)**

Summarizes complex orders across products, services, and fulfillment tasks. This helps agents quickly understand status, take the right actions, and avoid navigating fragmented views. This results in easier next steps and improved productivity. For more information, see the [Now Assist for Order Management release notes](https://servicenow-staging.fluidtopics.net/access?context=now-assist-order-management-rn&family=zurich&ft:locale=en-US).


-   **[Support for complex characteristics for orders](https://servicenow-staging.fluidtopics.net/access?context=som-using&family=zurich&ft:locale=en-US)**

Take advantage of the following complex characteristics for orders:

    -   Define complex characteristics for product offerings and specifications using object structures, data arrays, and other data input types such as String, Integer, Date, DateTime, and Decimal. For more information, see [Defining characteristics and options](https://servicenow-staging.fluidtopics.net/access?context=defining-prod-characteristics&family=zurich&ft:locale=en-US).
    -   Define compatibility, decomposition, and attribute propagation rules based on conditions that use characteristics at any level of a complex attribute hierarchy. For more information, see [Create a compatibility rule](https://servicenow-staging.fluidtopics.net/access?context=create-compatibility-rules&family=zurich&ft:locale=en-US), [Decomposition rules](https://servicenow-staging.fluidtopics.net/access?context=order-mgt-create-decomposition-rules&family=zurich&ft:locale=en-US), and [Domain order](https://servicenow-staging.fluidtopics.net/access?context=define-domain-order-attributes&family=zurich&ft:locale=en-US).
-   **[Order header discount](https://servicenow-staging.fluidtopics.net/access?context=add-header-discount-to-an-order&family=zurich&ft:locale=en-US)**

Provide order agents with the ability to apply discounts across multiple order lines with a single action through an order header discount feature. This feature streamlines discounting workflows, improves pricing consistency, and helps speed up order processing for large complex deals.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Order Management features.

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

-   **[Changes to OM integration with SPM](https://servicenow-staging.fluidtopics.net/access?context=configure-site-project-product-offering&family=zurich&ft:locale=en-US)**

Use OM integration with SPM to create program, reuse program, create site project and reuse site project in the SPM.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Order Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Order Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   The Subscription start and end dates have been deprecated starting with the Q2 2025 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.
-   The fields listed for the following tables are no longer supported.

    |Table name|Fields|
    |----------|------|
    |Order \(sn\_ind\_tmt\_orm\_order\)|Total monthly recurring price, Total annual recurring price|
    |Order line item \(sn\_ind\_tmt\_orm\_order\_line\_item\)|Cumulative monthly recurring price, Cumulative annual recurring price, Subscription start date, Subscription end date|
    |Order line item \(sn\_csm\_om\_order\_line\_item\)|Total recurring price|


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Order Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Order Management by requesting it from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Order Management by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Order Management, such as specific requirements or compliance levels.

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

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Order Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Enable order agents to view price adjustment details while processing orders.
-   Enable customers to view the product catalog, add products to a shopping cart, and create orders by using the Business Portal.
-   Create cases for multiple orders or for specific order lines using the Business Portal.
-   Create cases for multiple invoices or for specific invoice lines.
-   Provide metrics that help sales agents and sales managers track and analyze the revenue impact of subscriptions.

 See [Order Management](https://servicenow-staging.fluidtopics.net/access?context=order-mgt-exploring&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Handle move orders support.
-   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) to enable projects for site and maintain program project and sub-project hierarchy.
-   Enables agents to change the location for product inventory at the order line level.
-   Support for nested objects, arrays, and custom attributes to model complex products.​
-   Support for order header discounts​.

 See [Order management](https://servicenow-staging.fluidtopics.net/access?context=explore-order-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

