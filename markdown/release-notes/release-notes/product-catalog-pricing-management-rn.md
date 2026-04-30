---
title: Product Catalog Management and Pricing Management release notes
description: The ServiceNow Sales Customer Relationship Management applications include the ServiceNow Product Catalog Management and ServiceNow Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
---

# Product Catalog Management and Pricing Management release notes

The ServiceNow® Sales Customer Relationship Management applications include the ServiceNow® Product Catalog Management and ServiceNow® Pricing Management features, which enable you to create and manage the product offerings, catalogs, pricing, and discounting strategies used in your organization. These foundational features were enhanced and updated in the Zurich release.

## Product Catalog Management and Pricing Management highlights for the Zurich release

-   Support AI-powered semantic search queries to find relevant product offerings and service specifications in the product catalog interface.
-   Generate and update product offering blueprints that guide the accurate configuration of customizable products by agents and customers.
-   Enable sales agents to create price and quantity ramps, a pricing strategy for increasing product pricing and quantity amounts over specified time periods.
-   Define pricing on product offers based on the price of other product offers or transaction context variables.
-   Use product characteristics to adjust product costs, which are then used in margin calculations for sales quotes.

See [Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=zurich&pubname=zurich-order-management&ft:locale=en-US) and [Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Product Catalog Management and Pricing Management are available in the ServiceNow Store. The blueprint feature introduced in this release is provided with the CPQ Integration application available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Product Catalog Management and Pricing Management to Zurich

Pricing Management v15.0.0 provides a default pricing plan that includes new steps to support pricing strategies introduced in this release. If you're using a custom pricing plan from an earlier release, review the default pricing plan, which is in a Retired state after you upgrade. Determine whether you want to publish the default plan or customize the default pricing plan for your needs. The default plan contains new steps for calculating net pricing and roll-up values for configurable products in quotes and orders: Net Price Calculation, Line Rollup, and Header Rollup steps. This pricing functionality existed in previous releases for quotes and orders but wasn’t included in the default pricing plan. To retain this previous functionality for quotes and orders, you must add the Net Price Calculation, Line Rollup, and Header Rollup steps in your custom pricing plan before you publish it for use.

If you used the legacy product configurator previously and want to use the CPQ Configurator, after upgrading set the **sn\_prd\_pm.enable\_advanced\_configuration** system property to true. When set to true, this property enables the CPQ Configurator.

If you want to use AI Search for product catalog searches, before upgrading install Now Assist for Sales Force Automation \(SFA\), which includes the plugins needed for AI Search functionality. After upgrading, complete various steps to implement AI Search. These steps include running a scheduled job to set up AI Search and enabling AI Search in the product catalog interface by setting the **enable\_ai\_search\_in\_catalog** system property to true. For details on these configuration steps, see [Configuring AI Search for product catalog search](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

## New in the Zurich release

-   **[Create configurable product offerings and associated blueprints](https://www.servicenow.com/docs/access?context=som-create-configurable-prod-offerings&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable product catalog admins to generate blueprints for configurable products using the CPQ Configurator. A blueprint contains the product attributes, product relationships, product and pricing rules, and child products that control the structure of a configurable product offering. It also contains configuration rules, such as inclusion, exclusion, and determination. Blueprints drive the agent and customer experience when configurable products are added using the configurator. Catalog admins can review and update an offering blueprint in the CPQ Configurator, then publish the product offering to the product catalog.

-   **[AI Search queries in the product catalog interface](https://www.servicenow.com/docs/access?context=configure-ai-search-prod-catalog&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable semantic search features that agents and customers can use in the product catalog to find relevant product offerings. Users can search by product offer attributes, characteristics, and child offerings, and also view auto-complete suggestions. AI Search supports queries with synonyms, multi-languages, Boolean operators, and auto-correction \(typo handling\). Product catalog admins can configure stop words, synonyms, and rules that control the search results displayed.

-   **[Complex characteristics](https://www.servicenow.com/docs/access?context=som-product-config-add-characteristics&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Starting with Product Catalog Management Core v13.0, enable product catalog admins to define product and specification characteristics using an object-based structure that supports the following data types: integer, decimal, date and date time, and data arrays. For example, product catalog admins can use these new data types to define characteristics for communication products, such as routing characteristics, that have nested levels of characteristics and characteristic options. These complex characteristics can then be used to define conditions for setting decomposition, attribute propagation, and compatibility rules.

    -   Agents can view and select the complex characteristics available for configurable product offerings when creating opportunities, quotes, and orders. Complex attributes are displayed as separate nodes in the product hierarchy tree of the legacy product configurator interface.
    -   Fulfillment agents can perform fulfillment tasks that capture complex characteristic data for new or MACD orders.
    -   Customers can view and select complex characteristics when using the Business Portal to order configurable products.
    **Note:**  Complex characteristics aren’t supported in the CPQ Configurator.


-   **[Derived product pricing](https://www.servicenow.com/docs/access?context=configuring-related-product-pricing&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Define dynamic product pricing relationships between products, where the price for a product is derived from the price of another product or transaction-level values, such as the total quote value or annual contract value \(ACV\). When sales or order agents add the product to a quote or order, they can see how the product price is derived in real time.

-   **[Price and quantity ramps](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable product catalog admins to identify configurable product offerings for which pricing ramps can be created. These product offerings must also have the recurring pricing method. Sales agents create price ramps for quote lines that define and schedule pricing and quantity changes as product deals evolve over a given time period.

-   **[Product pricing changes related to MACD activities](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Support different price bases, such as original prices, fresh prices, or zero prices, used to calculate pricing for products during MACD activities.

-   **[Cost-based attribute adjustments](https://www.servicenow.com/docs/access?context=create-cost-attribute-adjustment&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable pricing admins or managers to set different product costs based on product attributes, such as model or size, by using cost book-specific or product offering-based adjustments for cost book lines. Previously, only a single cost amount was captured for a product offering, even if the product had different attributes that affected the product cost. These adjustments determine the base product cost used to calculate profit margins for sales agents when they create quotes for customers.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Support minor changes to published product offerings and specifications](https://www.servicenow.com/docs/access?context=minor-updates-published-offerings-specs&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Make minor changes to published versions of a product offering or specification, without creating a version. Minor updates include changes such as modifying the product offering display name, description, or product image.

-   **[Configurable product offerings](https://www.servicenow.com/docs/access?context=som-create-product-offering&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    The Create Product Offering form, used when creating product offerings, has two new options. The **Configurable** option indicates that the product offering is configurable and that it can be customized by agents and customers using the CPQ Configurator. The **Enable ramps** option indicates that price ramps can be defined for a configurable product.

-   **[Enhancements for exporting and importing product catalog entities between ServiceNow instances](https://www.servicenow.com/docs/access?context=export-import-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Support the export and import of product catalog-related entities:

    -   Product Catalog Management Core V15.0.0: During import, the system checks for minor updates to product offerings and specifications in the target version and imports them accordingly.
    -   Product Catalog Management Core v13.0.0
        -   Export catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as fetching referenced specifications during export. For details, see [Export catalog entities](https://www.servicenow.com/docs/access?context=export-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US).
        -   Import catalog entities, such as complex characteristic hierarchies, default values for characteristics including complex characteristics for product offerings and specifications, catalog entity versions in any order, and more, such as suppressing validation of business rule errors in logs. For details, see [Import product catalog entities](https://www.servicenow.com/docs/access?context=import-product-catalog-entities&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

-   **[CSM Pricing API](https://www.servicenow.com/docs/access?context=csm-pricing-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Use the Pricing REST API to enable integration of Pricing Management features with external applications. The CPQ Configurator is integrated with the Pricing REST API, to display pricing information for configurable products.

-   **[Published pricing and product eligibility matrices](https://www.servicenow.com/docs/access?context=edit-published-matrices&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Starting with Context Rules Management v9.1.0, published pricing and product eligibility matrices can’t be edited. To change a published matrix, pricing or product catalog admins must generate a new version of the matrix. If needed, admins can use the **allow\_edit\_on\_published\_matrices** system property to enable editing of pricing and product eligibility matrices.

-   **[Configurable pricing plan enhancements](https://www.servicenow.com/docs/access?context=configuring-pricing-plan&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**
    -   Pricing plan changes in Pricing Management v15.0.0
        -   Input Price Point column: Identifies the input for a pricing step.
        -   Output Price Point column: Identifies the output resulting from the pricing step.
        -   Analyze line changes step: This step uses the Delta Price Treatment Matrix to define how adjustments to sold products or contracts are handled by the pricing engine.
        -   Annual Price Increase Adjustments for Ramps: This step applies the percentage Annual Price Increase to the list price of products that have pricing ramps enabled. Sales agents specify the percentage increase when they create price ramps.
        -   Net Price Calculation step: This step calculates the net price using any automatic and manual adjustments made in quotes or orders.
        -   Line Rollup step: This step uses the net price to calculate the cumulative pricing fields in quote and order lines that are rolled up to the parent line of bundled products.
        -   Header Rollup step: This step calculates total pricing values, such as total annual or total monthly amounts, displayed at the header level.
        -   Derived Price Calculation step: This step calculates the line prices using the Derived Pricing Matrix that defines the pricing source and the unit base list price for the price list line.
        -   Calculate Delta Prices step: This step calculates product pricing during MACD activities using different price point bases, as configured by the pricing admin.
    -   Pricing plan changes in Pricing Management v13.0.0
        -   Apply Attribute-based Cost Adjustment step: This new step applies an attribute-based cost adjustment, either a percentage or markup or markdown of the cost book line cost. The pricing engine uses the cost adjustment to determine product costs when calculating margins for quote lines.
        -   The Fetch Cost and Fetch Price List Price steps have been renamed Fetch Base Cost and Fetch Base Price List Price.

## Activation information

The Product Catalog Management and Pricing Management features are included with Sales Customer Relationship Management store applications and don’t need activation. Depending on your entitlements, you can install the Product and Pricing Rules application for pricing and product eligibility matrices and the CPQ Integration application for the CPQ Configurator from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

