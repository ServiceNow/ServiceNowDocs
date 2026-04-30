---
title: Product Catalog Management and Pricing Management release notes
description: The Sales Customer Relationship Management applications include Product Catalog Management and Pricing Management features for creating and managing the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-23"
reading_time_minutes: 7
---

# Product Catalog Management and Pricing Management release notes

The Sales Customer Relationship Management applications include Product Catalog Management and Pricing Management features for creating and managing the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Xanadu release.

## Product Catalog Management and Pricing Management highlights for the Xanadu release

-   Enable sales agents and managers to create opportunities, quotes, and orders for service or installation locations.
-   Use a configurable pricing plan that defines the sequence in which pricing rules and calculations, such as list price and various adjustments are applied.
-   Enable sales agents to create sales agreements with configurable product offerings.
-   Sell the right products and reduce the risk of order errors by setting rules that enable only eligible products from the product catalog to be added to quotes and orders.
-   Fulfill complex orders for bundled product offers that reference product specifications or product specification hierarchies.
-   Streamline the quote and order process for your agents by setting the default product configurations displayed in the product configurator.

See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US) for more information.

## Important information for upgrading Product Catalog Management and Pricing Management to Xanadu

If you’re using the extension point **sn\_csm\_pricing.PricingAdjustmentsExtensionPoint** for pricing adjustments, change the default pricing plan \(introduced in the November 2024 release\) after upgrading. The pricing plan steps for the Configuration Component Price Adjustment and Standard Price Adjustment matrices are not applicable. As pricing admin or manager, remove the steps for these matrices from the default pricing plan.

1.  Navigate to **All** &gt; **Pricing** &gt; **Pricing Plans**.
2.  Select the published Default Pricing Plan.
3.  Select **Copy**.
4.  In the pricing plan copy, go to the Pricing Plan steps related list.
5.  Select the rows for the Apply configuration component adjustments step \(Sequence 50\) and the Apply contextual adjustments step \(Sequence 60\) and select **Delete** in the Actions on selected rows menu.
6.  Select **Update**.
7.  Publish the pricing plan copy.

## New in the Xanadu release

-   **[Location-based transactions](https://www.servicenow.com/docs/access?context=config-location-transaction&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Enable agents to specify a service location in the product catalog UI and display only the eligible products for that location when they’re adding products to opportunities, quotes, and orders. Agents can create line items for the specified location, as well as copy line items to multiple service or installation locations in the same opportunity, quote, or order. Set up eligibility rules to filter the product catalog, catalog categories, or product offerings by service location.

-   **[Control cascading quantity values in child product offerings](https://www.servicenow.com/docs/access?context=som-activate-cascade-quantity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Control how quantity values on top-level product offerings are cascaded to child lines.

-   **[Product offer eligibility](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Use business rules to filter the product catalog, product categories, and product offerings dynamically, displaying only eligible product offerings for a customer in the product catalog. Define the business rules using product eligibility matrices. If you're using sales agreements, the product catalog displays only the eligible product offers set in the sales agreement.

    The November 2024 release provides the following:

    -   Version 2 of product eligibility matrices: Supports eligibility rules based on transaction line attributes along with document header attributes.
    -   System-defined context variables for service locations: Service City, Service State, Service Country, and Service Zip context variables are available to specify service locations in the product eligibility and pricing matrices.
-   **[Product offer bundling with product specifications](https://www.servicenow.com/docs/access?context=som-offer-bundles-with-specs&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Support bundling of offers that have an associated product specification or specification hierarchy. For example, you can create a product offer that has an associated product specification and indicate whether to inherit the characteristics from the child specifications in addition to the parent specification.


-   **[Configurable pricing plan](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Define the sequence of steps in which pricing rules and calculations are applied. The November 2024 release provides a default pricing plan. You can customize the default plan by copying it and then adding new steps, modifying existing steps, changing the sequence of steps, and adding conditions for running an existing step.

-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    View system-calculated recurring revenue amounts for product and service subscriptions in opportunities and quotes. These amounts help sales agents and sales managers assess the financial value of monthly and annual subscriptions.

-   **[Sales Agreement price lists](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    If you're using the Sales Agreement feature, a published sales agreement price list is generated automatically when a sales agent creates a sales agreement from a completed quote. The sales agreement price list reflects the final unit price for each product captured in the sales agreement and is valid for the start and end dates specified for the agreement. To learn more about sales agreements, see [Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).

    The November 2024 release supports hierarchical price lists and multiple price lists for a sales agreement. Hierarchical price lists enable agents to negotiate different pricing for an offer depending on whether it is sold in the context of a bundle or parent offer or as a standalone product. If multiple price lists exist for a sales agreement, the default price list used is based on currency and the sales agreement. Agents can select from different options, products, and characteristics within a configurable bundle or product, which determines what is available as part of the sales agreement and resulting order.


## UI changes

-   **[Context Rule Management navigation changes](https://www.servicenow.com/docs/access?context=configuring-sales-eligibility&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    In the CSM Configurable Workspace, you can access the product eligibility matrices from the List view and navigate to **Rules** &gt; **Eligibility Rules** or **Context Rule Management** &gt; **Rule Matrices** to select the appropriate matrix for controlling product eligibility.


## Changed in this release

-   **[Product catalog hierarchy visualization](https://www.servicenow.com/docs/access?context=som-catalog-hierarchy&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Toggle the view to show the specification hierarchy along with the offer hierarchy or show just the offer hierarchy using the Catalog Hierarchy tab for a product offering.

-   **Configuration UI changes**
    -   Sorting of product entities: Product catalog categories and categories are now displayed in alphabetic order. Characteristic options and child offers in the configuration UI are also displayed in alphabetical order, unless product catalog admins set a different display order when defining the associated product offerings.
    -   [Configurable products for sales agreements](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US): Agents can select from the different options for products and characteristics within a configurable bundle or product. These selections determine what product offerings are available as part of the sales agreement when creating orders from sales agreements.
    -   Improved the display and aggregation of alerts, error, and information messages in the Configuration UI to provide more context. Added visual indicators that indicate when a configuration is incomplete.
-   **[Configuration State Model API Framework enhancements](https://www.servicenow.com/docs/access?context=som-open-state-management-model&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Use the configuration state model to control various features in the product configurator. For example, you can define different default product configurations displayed to your agents, based on context, such as role or sales channel. You can also control the quantity values that agents can enter on a configuration node or optionally define info messages that are triggered for specific conditions that you set.


-   **Changing a published price list**

    Starting with the Xanadu release, you can change only the **Description** and price list **End date** fields in a published price list. You can continue to add price list lines.

-   **[Copy a price list](https://www.servicenow.com/docs/access?context=copy-price-list&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Duplicate a published price list, its price list lines, and any related attribute adjustments and decision tables, without having to re-create the price list and its price list lines. For example, you can copy a published price list and its price list lines and use the price list copy for another account or location.

-   **[Cost book enhancements](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Create multiple cost books for a given currency and set a default cost book for a given currency. You can also do the following:

    -   [Copy a cost book](https://www.servicenow.com/docs/access?context=copy-cost-book&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
    -   Manage the default cost books used and set cost book validation rules by using the [Cost Book Defaulting Matrix](https://www.servicenow.com/docs/access?context=som-control-default-costbook&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
    -   Customize the default cost book logic called by other SOM applications by using the [DefaultCostBookExtensionPoint extension point](https://www.servicenow.com/docs/access?context=extension-points-som-pricing&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US).
-   **[Matrix rule validations](https://www.servicenow.com/docs/access?context=configuring-rule-validations&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Use predefined validation rules or create your own rules to validate the context variables, such as mandatory inputs, in pricing and product eligibility rule matrices. Each validation definition has a script that identifies the context variables to be validated and the corresponding error or warning messages that are displayed in the matrix decision table, depending on the validation results.

-   **Name change for Pricing Matrix Management application**

    Starting with the Xanadu release, the Pricing Matrix Management application is renamed as the Product and Pricing Rules application \(sn\_csm\_price\_mtrx plugin\). The application includes the product catalog eligibility matrices introduced in this release as well as the pricing matrices.


## Activation information

The Product Catalog Management and Pricing Management features are included with each store application and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the Product Configurator feature from the ServiceNow Store.

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

