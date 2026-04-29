---
title: Configuring location-based product transactions
description: In Sales and Order Management, agents can create opportunities, quotes, and orders tailored to customer location. These transactions are called location-based product transactions.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring agent tools in SOM, Configure, Sales and Order Management]
---

# Configuring location-based product transactions

In Sales and Order Management, agents can create opportunities, quotes, and orders tailored to customer location. These transactions are called location-based product transactions.

When the product offerings and services available to customers vary based on location, your agents can use a location filter in the product catalog UI to select a service location and view only the products and services appropriate for that location. Agents can then add the appropriate products to an opportunity, quote, or order. Agents can also copy products and services from one location to another within the same transaction, which eliminates the need to create another opportunity, quote, or order for each location.

![Quote product catalog interface with location filter and quote line item view with Service location field](../image/location-interface.png "Location filter in the product catalog UI and service location in the line item view for quotes")

## How location-based transactions work

-   **Admin and product catalog admin configuration**

    Admins activate location-based transactions by enabling the **sn\_sales\_common.enable\_location\_based\_transactions** system property.

    Product catalog admins use the product eligibility rule entity filters to identify eligible and ineligible product entities \(catalogs, categories, and product offerings\). They also set up decision rules in product eligibility matrices, to specify the context variables, such as billing state or the service location variables \(introduced in the November 2024 release\), for controlling the display of eligible catalogs, categories, or product offerings.

    ![List views of the rule entity filters and product eligibility matrices](../image/eligibility-rules-matrices.png "Rule entity filters and product eligibility rule matrices")

    In the following example of the Product Offering Catalog Eligibility matrix, a rule entity filter for ineligible catalogs and the context variable, service state, are used to filter the product catalog displayed.

    ![Product offering catalog eligibility matrix that shows the context variables available and the decision rule applied, including the rule entity filters used and eligibility results](../image/matrix-condition-service-location.png "Example product offering catalog eligibility matrix")

-   **Agent experience for location-based transactions**

    When agents specify a service location, the product catalog UI displays the eligible catalog, categories, or offerings for that location, depending on the product eligibility entities configured. When they select a simple or fixed product, the line item is created automatically for the specified location. If they select a configurable product, they use the product configurator to customize the product options. A line item is created automatically when they save the product configuration.

    Your agents can then copy line items to another location in the same transaction \(opportunity, quote, or order\). They can indicate that only eligible line items be copied to the specified location.

    ![Copy line items dialog box to copy order line item to another location](../image/copy-line-item-location.png "Example order line item copy")

    For details on how agents add products to an opportunity, quote, or order by location, see the following:

    -   [Use location filter to add opportunity line items](../task/use_location_filter_to_add_line_items.md).
    -   [Copy opportunity line items to a location](../task/copy_opportunity_line_items_to_a_location.md).
    -   [Filter catalogs by location in a quote](../task/quote-using-product-location.md).
    -   [Copy locations for quote line items](../task/quote-mgt-copy-quote-item-location.md).
    -   [Filter product catalog by location](../task/order-mgt-filter-catalog-by-location.md).

## Setting up location-based transactions

Admins and product catalog admins complete the following configuration tasks to set up location-based transactions.

|Step|Description|Role|
|----|-----------|----|
|[Activate location-based transactions](../task/som-activate-location-filter.md)|Enable the **sn\_sales\_common.enable\_location\_based\_transactions** system property.|Admin|
|[Create rule entity filters](../task/som-create-rule-entity-filter.md)|Define the rule entity filters that make catalogs, categories, and product offerings either eligible or ineligible for display.|Product catalog admin|
|[Define product eligibility rules](../task/som-define-eligibility-rules.md)|Set the product eligibility rules by selecting the context variables, such as the service location context variables, that control the display of product catalog, category, or offerings.|Product catalog admin|

-   **[Activate location-based transactions](../task/som-activate-location-filter.md)**  
Turn on location-based transactions for opportunities, quotes, and orders by using the **sn\_sales\_common.enable\_location\_based\_transactions** system property.

**Parent Topic:**[Configuring agent tools in Sales and Order Management](som-agent-tools.md)

