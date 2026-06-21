---
title: Combined Product Catalog Management and Pricing Management release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Product Catalog Management and Pricing Management from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-productcatalogmanagementandpricingmanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Product Catalog Management and Pricing Management release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Product Catalog Management and Pricing Management from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Product Catalog Management and Pricing Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Product Catalog Management and Pricing Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

If you’re using the extension point **sn\_csm\_pricing.PricingAdjustmentsExtensionPoint** for pricing adjustments, change the default pricing plan \(introduced in the November 2024 release\) after upgrading. The pricing plan steps for the Configuration Component Price Adjustment and Standard Price Adjustment matrices are not applicable. As pricing admin or manager, remove the steps for these matrices from the default pricing plan.

1.  Navigate to **All** &gt; **Pricing** &gt; **Pricing Plans**.
2.  Select the published Default Pricing Plan.
3.  Select **Copy**.
4.  In the pricing plan copy, go to the Pricing Plan steps related list.
5.  Select the rows for the Apply configuration component adjustments step \(Sequence 50\) and the Apply contextual adjustments step \(Sequence 60\) and select **Delete** in the Actions on selected rows menu.
6.  Select **Update**.
7.  Publish the pricing plan copy.

</td></tr><tr><td>

Yokohama

</td><td>

After upgrading to the May 2025 release of Sales and Order Management applications, you must run a scheduled job that automatically enables the **Allow multiple configurations** option when your catalog admin creates product offerings with an associated product specification. This job is called **Scheduled job with an upgrade script to set 'allow\_multiple\_configurations' to true on an Offering**. When multiple product offering configurations are allowed in configurable opportunities, quotes, or orders, agents can create multiple instances of a child product offering and define custom configurations for each offering instance.

**Note:** The **Allow multiple configurations** option is always enabled \(set to true\) for all product offerings that have an associated product specification. However, if the product specification has a child hierarchy, this option is honored only for orders placed through the TMF APIs. For specifications without a hierarchy, the flag is honored across all ordering channels.

 The May 2025 release provides a default pricing plan that includes a new step, Apply Renewal Adjustment. If you've been using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after upgrading to the May 2025 release. Determine whether you want to publish the default plan or customize the default pricing plan for your needs and then publish the custom plan to be used.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Location-based transactions](https://www.servicenow.com/docs/access?context=config-location-transaction&family=xanadu&ft:locale=en-US)**

Enable agents to specify a service location in the product catalog UI and display only the eligible products for that location when they’re adding products to opportunities, quotes, and orders. Agents can create line items for the specified location, as well as copy line items to multiple service or installation locations in the same opportunity, quote, or order. Set up eligibility rules to filter the product catalog, catalog categories, or product offerings by service location.

-   **[Control cascading quantity values in child product offerings](https://www.servicenow.com/docs/access?context=som-activate-cascade-quantity&family=xanadu&ft:locale=en-US)**

Control how quantity values on top-level product offerings are cascaded to child lines.

-   **[Product offer eligibility](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=xanadu&ft:locale=en-US)**

Use business rules to filter the product catalog, product categories, and product offerings dynamically, displaying only eligible product offerings for a customer in the product catalog. Define the business rules using product eligibility matrices. If you're using sales agreements, the product catalog displays only the eligible product offers set in the sales agreement.

The November 2024 release provides the following:

    -   Version 2 of product eligibility matrices: Supports eligibility rules based on transaction line attributes along with document header attributes.
    -   System-defined context variables for service locations: Service City, Service State, Service Country, and Service Zip context variables are available to specify service locations in the product eligibility and pricing matrices.
-   **[Product offer bundling with product specifications](https://www.servicenow.com/docs/access?context=som-offer-bundles-with-specs&family=xanadu&ft:locale=en-US)**

Support bundling of offers that have an associated product specification or specification hierarchy. For example, you can create a product offer that has an associated product specification and indicate whether to inherit the characteristics from the child specifications in addition to the parent specification.


-   **[Configurable pricing plan](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=xanadu&ft:locale=en-US)**

Define the sequence of steps in which pricing rules and calculations are applied. The November 2024 release provides a default pricing plan. You can customize the default plan by copying it and then adding new steps, modifying existing steps, changing the sequence of steps, and adding conditions for running an existing step.

-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&family=xanadu&ft:locale=en-US)**

View system-calculated recurring revenue amounts for product and service subscriptions in opportunities and quotes. These amounts help sales agents and sales managers assess the financial value of monthly and annual subscriptions.

-   **[Sales Agreement price lists](https://www.servicenow.com/docs/access?context=pricing-management&family=xanadu&ft:locale=en-US)**

If you're using the Sales Agreement feature, a published sales agreement price list is generated automatically when a sales agent creates a sales agreement from a completed quote. The sales agreement price list reflects the final unit price for each product captured in the sales agreement and is valid for the start and end dates specified for the agreement. To learn more about sales agreements, see [Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&family=xanadu&ft:locale=en-US).

The November 2024 release supports hierarchical price lists and multiple price lists for a sales agreement. Hierarchical price lists enable agents to negotiate different pricing for an offer depending on whether it is sold in the context of a bundle or parent offer or as a standalone product. If multiple price lists exist for a sales agreement, the default price list used is based on currency and the sales agreement. Agents can select from different options, products, and characteristics within a configurable bundle or product, which determines what is available as part of the sales agreement and resulting order.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Product offering recommendations](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US)**

Provide sales agents with offer recommendations for upselling or cross-selling additional products in quotes. Product catalog admins create the offer recommendations for sellable products. Sales agents can view the recommendations when adding products to quotes from the product catalog or when reviewing the lines items for a quote.

-   **[Product catalog and product configurator in the Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&family=yokohama&ft:locale=en-US)**

Enable customers to view the product catalog and order products using the product configurator in the Business Portal for Order Management.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Product Catalog Management and Pricing Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Product catalog hierarchy visualization](https://www.servicenow.com/docs/access?context=som-catalog-hierarchy&family=xanadu&ft:locale=en-US)**

Toggle the view to show the specification hierarchy along with the offer hierarchy or show just the offer hierarchy using the Catalog Hierarchy tab for a product offering.

-   **Configuration UI changes**
    -   Sorting of product entities: Product catalog categories and categories are now displayed in alphabetic order. Characteristic options and child offers in the configuration UI are also displayed in alphabetical order, unless product catalog admins set a different display order when defining the associated product offerings.
    -   [Configurable products for sales agreements](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&family=xanadu&ft:locale=en-US): Agents can select from the different options for products and characteristics within a configurable bundle or product. These selections determine what product offerings are available as part of the sales agreement when creating orders from sales agreements.
    -   Improved the display and aggregation of alerts, error, and information messages in the Configuration UI to provide more context. Added visual indicators that indicate when a configuration is incomplete.
-   **[Configuration State Model API Framework enhancements](https://www.servicenow.com/docs/access?context=som-open-state-management-model&family=xanadu&ft:locale=en-US)**

Use the configuration state model to control various features in the product configurator. For example, you can define different default product configurations displayed to your agents, based on context, such as role or sales channel. You can also control the quantity values that agents can enter on a configuration node or optionally define info messages that are triggered for specific conditions that you set.


-   **Changing a published price list**

Starting with the Xanadu release, you can change only the **Description** and price list **End date** fields in a published price list. You can continue to add price list lines.

-   **[Copy a price list](https://www.servicenow.com/docs/access?context=copy-price-list&family=xanadu&ft:locale=en-US)**

Duplicate a published price list, its price list lines, and any related attribute adjustments and decision tables, without having to re-create the price list and its price list lines. For example, you can copy a published price list and its price list lines and use the price list copy for another account or location.

-   **[Cost book enhancements](https://www.servicenow.com/docs/access?context=pricing-management&family=xanadu&ft:locale=en-US)**

Create multiple cost books for a given currency and set a default cost book for a given currency. You can also do the following:

    -   [Copy a cost book](https://www.servicenow.com/docs/access?context=copy-cost-book&family=xanadu&ft:locale=en-US).
    -   Manage the default cost books used and set cost book validation rules by using the [Cost Book Defaulting Matrix](https://www.servicenow.com/docs/access?context=som-control-default-costbook&family=xanadu&ft:locale=en-US).
    -   Customize the default cost book logic called by other SOM applications by using the [DefaultCostBookExtensionPoint extension point](https://www.servicenow.com/docs/access?context=extension-points-som-pricing&family=xanadu&ft:locale=en-US).
-   **[Matrix rule validations](https://www.servicenow.com/docs/access?context=configuring-rule-validations&family=xanadu&ft:locale=en-US)**

Use predefined validation rules or create your own rules to validate the context variables, such as mandatory inputs, in pricing and product eligibility rule matrices. Each validation definition has a script that identifies the context variables to be validated and the corresponding error or warning messages that are displayed in the matrix decision table, depending on the validation results.

-   **Name change for Pricing Matrix Management application**

Starting with the Xanadu release, the Pricing Matrix Management application is renamed as the Product and Pricing Rules application \(sn\_csm\_price\_mtrx plugin\). The application includes the product catalog eligibility matrices introduced in this release as well as the pricing matrices.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Multiple configurations](https://www.servicenow.com/docs/access?context=multiple-child-offering-configurations&family=yokohama&ft:locale=en-US)**

Define child product offerings that can have multiple configurations in configurable opportunities, quotes, and orders. Agents can clone or split a child product offering to create multiple product offering instances. Each quantity for an offering instance can then have its own unique configuration.

-   **[Transient product offerings](https://www.servicenow.com/docs/access?context=configuring-transient-products&family=yokohama&ft:locale=en-US)**

Define single-use product offerings, such as installation services or consulting services, as transient products that are fulfilled in ServiceNow Order Management. After orders for transient products are fulfilled, sold product or product inventory records are created but have an Inactive status. Move, Add, Change, Delete \(MACD\) actions aren't supported for the sold product or product inventory records of transient products.


-   **[Configurable pricing plan enhancements](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&family=yokohama&ft:locale=en-US)**
    -   Apply Renewal Adjustment step: This new step determines whether a contract renewal adjustment, either a markup or markdown amount or percentage, is to be calculated and applied. For example, as a pricing admin, you might want to apply a pricing uplift of a fixed amount at contract renewal. This renewal adjustment step is enabled by default, but you can change or remove it in a custom configurable pricing plan.
    -   Extension point updates: The ListPriceExtensionPoint, which gathers the data needed to make required adjustments, now includes the adjustment data for contract renewals.
-   **[Volume-based pricing](https://www.servicenow.com/docs/access?context=configure-volume-pricing&family=yokohama&ft:locale=en-US)**

Set volume discounts for product offerings based on the product quantity.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Product Catalog Management and Pricing Management features or functionality were removed.

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

Between your current release family and Yokohama, some Product Catalog Management and Pricing Management features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Product Catalog Management and Pricing Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the Product Configurator feature from the ServiceNow Store.

</td></tr><tr><td>

Yokohama

</td><td>

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the product configurator feature from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Product Catalog Management and Pricing Management we have noted them here.

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

If any specific browser requirements were introduced or changed for Product Catalog Management and Pricing Management we have noted them here.

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

Review details on accessibility information for Product Catalog Management and Pricing Management, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Product Catalog Management and Pricing Management we have noted them here.

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

If there are specific highlight considerations for Product Catalog Management and Pricing Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Enable sales agents and managers to create opportunities, quotes, and orders for service or installation locations.
-   Use a configurable pricing plan that defines the sequence in which pricing rules and calculations, such as list price and various adjustments are applied.
-   Enable sales agents to create sales agreements with configurable product offerings.
-   Sell the right products and reduce the risk of order errors by setting rules that enable only eligible products from the product catalog to be added to quotes and orders.
-   Fulfill complex orders for bundled product offers that reference product specifications or product specification hierarchies.
-   Streamline the quote and order process for your agents by setting the default product configurations displayed in the product configurator.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=xanadu&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Enable agents to create multiple configurations of child product offerings in configurable products and customize the options and characteristics for each child product instance.
-   Identify single-use product offerings, such as installation services, with a transient flag to differentiate them from products that are maintained as active sold products or product inventory.
-   Provide the options to choose a drop-down or radio control to display characteristics of type choice in the product configurator UI.
-   Give sales agents a list of recommended product offerings that can be added to complement or supplement products in quotes.
-   Enable pricing admins to set pricing adjustments based on the quantity of product offerings in a quote or order.

 See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&family=yokohama&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

