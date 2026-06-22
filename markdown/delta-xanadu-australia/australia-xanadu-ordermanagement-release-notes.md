---
title: Combined Order Management release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Order Management from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-ordermanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Order Management release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Order Management from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Order Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Order Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Features introduced in the Xanadu release aren't supported in earlier releases of Order Management.

 If you’re upgrading from Order Management for Telecommunications and Media version 6.0 or earlier:

-   Starting with the  Washington DC release, the  Monthly Recurring Charges  \(MRC\) and the  Non-Recurring Charges  \(NRC\) for product offerings and product attribute characteristics are no longer stored in the product offering data model. Instead, the MRC and NRC are stored in the Pricing data model in price lists and price list lines. If you want to upgrade your pricing information to use price lists after upgrading to  Washington DC, see the  [Price Management Plugin \(com.sn\_csm\_pricing\) uptake for Telecommunications, Media, and Technology customers upgrading to Washington \[KB1585863\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585863) article in the Now Support Knowledge Base.
-   After upgrading to the  Xanadu release, a fix script runs automatically to deactivate certain telecommunications list records that are no longer needed to resume the capture of an unfinished order. For more information on these records and using the former order capture process, see the  [Deprecating Telco List for Order Capture \[KB1586538\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1586538) article in the Now Support Knowledge Base.

 If you’re an upgrade customer who uses the **contract start date** and **contract end date** fields and has records, you can migrate those records to the latest data model by running the **Migrate data from deprecated contract fields to new fields on Order and Order Lines** scheduled job. This scheduled job must be manually executed by navigating to **System Definitions** &gt; **Scheduled Jobs**. For more information on scheduled jobs, see [Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&family=xanadu&ft:locale=en-US).

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

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Order Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Add sales agreements to orders](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&family=xanadu&ft:locale=en-US)**

When an agent creates an order, the sales agreement associated with the account is automatically applied and the catalog is filtered with the agreement products and prices.

-   **[Add business hours to Jeopardy Management tasks](https://www.servicenow.com/docs/access?context=configuring-jeopardy-management&family=xanadu&ft:locale=en-US)**

Admins can set planned task due dates, which are calculated based on business hours during weekdays in Jeopardy Management.

-   **[Update specification versions](https://www.servicenow.com/docs/access?context=som-specification-version-update&family=xanadu&ft:locale=en-US)**

Admins can perform a batch version update to a product inventory’s specification version.

-   **[Add covered products to an order](https://www.servicenow.com/docs/access?context=som-update-covered-products&family=xanadu&ft:locale=en-US)**

Agents can create covered products and modifications as part of an order capture to establish coverage relationships. They can also create change orders that remove sold products or install base items as covered products from entitlements and contracts.

-   **Order to Cash Operations**
    -   [Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&family=xanadu&ft:locale=en-US): Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.
    -   [Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&family=xanadu&ft:locale=en-US): Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Business Portal for order case management](https://www.servicenow.com/docs/access?context=order-mgt-business-portal&family=yokohama&ft:locale=en-US)**

Enable your customers to create cases for common order-related issues such as delivery delays, quantity disputes, and other routine inquiries directly using the Business Portal, ensuring faster issue resolution and improved customer satisfaction. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **Hierarchical view of order line items**

Enable order agents and order managers to use the hierarchical list view to view parent and child relationships within order lines.

-   **[Price adjustment details for order lines](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-order-lines&family=yokohama&ft:locale=en-US)**

Provides order agents and order managers the visibility into the price adjustments applied at each step of the pricing plan, including a detailed breakdown of all adjustments applied to the unit base price and unit list price to see how the unit net price is derived.

-   **[Multi-instance product offering configurations](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Create multiple instances of a child product offering in orders to generate a custom configuration for each product offering instance. When a child product offering has a quantity greater than 1, agents can clone or split a child product offering to create multiple product offering instances so that each quantity has its own configuration.

-   **[Transient products](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Add transient products, which are defined as one-time-use products or services, to new orders. Sold product and product inventory records are created but not maintained for transient products. Move, Add, Change and Disconnect \(MACD\) actions are not supported for transient products.

-   **[Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&family=yokohama&ft:locale=en-US)**

Use the Business Portal to view product catalogs, select product options, and place orders. Customers can also view their order status using the Business Portal.

-   **[Cases for multiple invoices](https://www.servicenow.com/docs/access?context=csm-invoice-operations&family=yokohama&ft:locale=en-US)**

Create cases for multiple invoices or for specific invoice lines. Agents can reference multiple invoices or invoice lines as case line items on an invoice case record. By using case line items, agents can track multiple issues for the same invoice case and resolve the issues in each case line item independently before resolving and closing the order case. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **[Add subscription pricing to an order](https://www.servicenow.com/docs/access?context=add-subscription-pricing-to-an-order&family=yokohama&ft:locale=en-US)**

Enable order agents and order managers to access and view key calculated metrics such as monthly recurring price and annual recurring price. The subscription pricing fields are automatically calculated based on contract start date and contract end date. These metrics enhance revenue reporting and help you to better understand recurring revenue dynamics.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Move order](https://www.servicenow.com/docs/access?context=move-order&family=zurich&ft:locale=en-US)**

The move order helps agents to perform move journey that requires location change, the location and change of attribute values, the location change and add or delete the product.


-   **[Pricing Adjustments for order line items](https://www.servicenow.com/docs/access?context=add-pricing-adjustment-to-an-order-line-item&family=zurich&ft:locale=en-US)**

Enables order agents to quickly view, add, and edit manual price adjustments for order line items directly from the list view, reducing clicks and streamlining the process. This new experience makes it easier for order agents to enter manual price adjustments and provides a holistic view of both automatic and manual adjustments.

-   **[Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&family=zurich&ft:locale=en-US)**

Summarizes complex orders across products, services, and fulfillment tasks. This helps agents quickly understand status, take the right actions, and avoid navigating fragmented views. This results in easier next steps and improved productivity. For more information, see the [Now Assist for Order Management release notes](https://www.servicenow.com/docs/access?context=now-assist-order-management-rn&family=zurich&ft:locale=en-US).


-   **[Support for complex characteristics for orders](https://www.servicenow.com/docs/access?context=som-using&family=zurich&ft:locale=en-US)**

Take advantage of the following complex characteristics for orders:

    -   Define complex characteristics for product offerings and specifications using object structures, data arrays, and other data input types such as String, Integer, Date, DateTime, and Decimal. For more information, see [Defining characteristics and options](https://www.servicenow.com/docs/access?context=defining-prod-characteristics&family=zurich&ft:locale=en-US).
    -   Define compatibility, decomposition, and attribute propagation rules based on conditions that use characteristics at any level of a complex attribute hierarchy. For more information, see [Create a compatibility rule](https://www.servicenow.com/docs/access?context=create-compatibility-rules&family=zurich&ft:locale=en-US), [Decomposition rules](https://www.servicenow.com/docs/access?context=order-mgt-create-decomposition-rules&family=zurich&ft:locale=en-US), and [Domain order](https://www.servicenow.com/docs/access?context=define-domain-order-attributes&family=zurich&ft:locale=en-US).
-   **[Order header discount](https://www.servicenow.com/docs/access?context=add-header-discount-to-an-order&family=zurich&ft:locale=en-US)**

Provide order agents with the ability to apply discounts across multiple order lines with a single action through an order header discount feature. This feature streamlines discounting workflows, improves pricing consistency, and helps speed up order processing for large complex deals.


</td></tr><tr><td>

Australia

</td><td>

-   **[Delta pricing on orders](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&family=australia&ft:locale=en-US)**

Calculate pricing and quantity changes during MACD activities and renewals by deriving deltas from existing products, contracts, or purchases. This improves accuracy when processing order modifications.

    -   Defaults contract type and contract line type when empty, based on the order and line actions being performed.
    -   Adds delta pricing–related header and line fields, along with pricing adjustment rule identifiers and conditions, and supports mapping these fields across order, product instance, and order copy flows.
-   **[Price and quantity ramps on order line items](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&family=australia&ft:locale=en-US)**

View price and quantity ramps directly on order line items to model planned changes over time within a single order, providing visibility into pricing changes without managing multiple orders. For more information, see the [Product Catalog Management and Pricing Management release notes](https://www.servicenow.com/docs/access?context=product-catalog-pricing-management-rn&family=australia&ft:locale=en-US)

-   **[Manage order updates with Now Assist](https://www.servicenow.com/docs/access?context=bulk-update-order-lines-with-now-assist&family=australia&ft:locale=en-US)**

Use a conversational AI assistant to improve order triage and resolution. The assistant understands order context and supports guided actions such as updating shipping addresses and quantities across order line items.

-   **[Customer entities on Order](https://www.servicenow.com/docs/access?context=som-create-product-order&family=australia&ft:locale=en-US)**

Capture Deal Type \(Direct or Indirect\) and Route to Market on every order to ensure the right parties are assigned, and deal structure is consistent from quote through to order.


-   **[Order header tasks](https://www.servicenow.com/docs/access?context=order-header-tasks&family=australia&ft:locale=en-US)**

Create and track tasks at the order and top order line level, independent of order line items, across all stages of the order lifecycle from pre-decomposition through post-fulfillment to support operational tasks such as customer onboarding, compliance review, approval tracking, customer notifications, and post-activation follow-up.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Order Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Add a sales agreement](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&family=xanadu&ft:locale=en-US)**

When an agent creates an order, the latest sales agreement associated with the account is automatically applied and the catalog is filtered to display the agreement's products and prices.

-   **[Update product locations at the order line level](https://www.servicenow.com/docs/access?context=order-mgt-copy-order-line-location&family=xanadu&ft:locale=en-US)**

Agents can create orders by location, which enables them to tailor orders for a customer location and streamline the ordering process by managing orders that have multiple locations.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Changes to OM integration with SPM](https://www.servicenow.com/docs/access?context=configure-site-project-product-offering&family=zurich&ft:locale=en-US)**

Use OM integration with SPM to create program, reuse program, create site project and reuse site project in the SPM.


</td></tr><tr><td>

Australia

</td><td>

-   **[Managing inflight order for site projects](https://www.servicenow.com/docs/access?context=inflight-offering-somt&family=australia&ft:locale=en-US)**

Use the OM integration with SPM for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Order Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Order Management features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

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

Xanadu

</td><td>

Install Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Order Management by requesting it from the ServiceNow Store.

 Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Order Management by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Order Management, such as specific requirements or compliance levels.

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

-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Order Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Order Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Sales agreements associated with the account are automatically applied and the catalog is filtered to display the agreement's products and prices.
-   Admins can set planned task due dates in Jeopardy Management, which are calculated based on business hours during weekdays.
-   Order agents can associate product specifications to a product offer at any level of a product offer hierarchy.
-   Admins can update product inventory records in a batch when there are changes to product specifications.
-   Order agents create orders tailored to each customer location from the product catalog.
-   Agents can use the Order Operations Case Management application to create cases for customer orders, unifying order tracking and resolution solutions.

 See [Order management](https://www.servicenow.com/docs/access?context=reviewing-approving-fulfilling-orders&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enable order agents to view price adjustment details while processing orders.
-   Enable customers to view the product catalog, add products to a shopping cart, and create orders by using the Business Portal.
-   Create cases for multiple orders or for specific order lines using the Business Portal.
-   Create cases for multiple invoices or for specific invoice lines.
-   Provide metrics that help sales agents and sales managers track and analyze the revenue impact of subscriptions.

 See [Order Management](https://www.servicenow.com/docs/access?context=order-mgt-exploring&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Handle move orders support.
-   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) to enable projects for site and maintain program project and sub-project hierarchy.
-   Enables agents to change the location for product inventory at the order line level.
-   Support for nested objects, arrays, and custom attributes to model complex products.​
-   Support for order header discounts​.

 See [Order management](https://www.servicenow.com/docs/access?context=explore-order-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Enable agents and customers to make faster, more confident decisions on orders by instantly seeing the impact of price and quantity changes, ensuring clarity on what's owed for every update.
-   Improve order approval accuracy by validating contract start and end dates and terms for recurring and entitlement orders, while preventing contract dates from being set on one-time orders. This helps orders process correctly the first and contract obligations to be properly tracked.
-   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.
-   Enable visibility into all entities involved in a deal by viewing billing, shipping, entitlement, and partner details on the customer order.
-   Enable order agents to create, track, and complete order-level tasks at the order header and top order line item level, with support for dependent task chains that automatically sequence work across submission, post-approval, and post-fulfillment stages.

 See [Order management](https://www.servicenow.com/docs/access?context=explore-order-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

