---
title: Quote Management release notes
description: The ServiceNow Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Quote Management release notes

The ServiceNow® Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Xanadu release.

## Quote Management highlights for the Xanadu release

-   Add covered products to a quote.
-   Synchronize quote information with an opportunity to help ensure that the information is accurate and complete.
-   Create sales agreements that contain configurable and bundled products and services.
-   Add location-based product eligibility, which enables products to be filtered in the catalog based on location.

See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US) for more information.

**Important:** Quote Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Sales agreement in quotes include product bundles](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Add a sales agreement to a quote that contains configurable product bundles with the ability to choose from available child offers and optional characteristics.

-   **[Location function filters products and creates line items](https://www.servicenow.com/docs/access?context=quote-using-product-location&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Location-based quoting is a new feature where line items can be created for different service or installation locations and agents can copy line items from one location to another. Agents can also filter products in the catalog by location.

-   **[Add covered products to a quote](https://www.servicenow.com/docs/access?context=som-quote-add-covered-products&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    As an agent, add covered products to quote line items. Covered products include entitlements, service agreements, and warranties. Adding a covered product to a quote enables you to add start and end dates for the agreements.


-   **[Synchronize a quote with an opportunity](https://www.servicenow.com/docs/access?context=som-sync-quote-with-opportunity&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    As an agent, synchronize quote information to an opportunity. As quote information changes, use this function to update the opportunity with information from the quote to keep records accurate.


## Deprecations

The following table columns are deprecated from Quote Management.

|Table name|Column name|
|----------|-----------|
|sn\_quote\_mgmt\_core\_quote\_line\_item|cumulative\_monthly\_recurring\_price, cumulative\_annual\_recurring\_price|
|sn\_quote\_mgmt\_core\_quote|total\_monthly\_recurring\_price, total\_annual\_recurring\_price, total\_recurring\_price|

## Activation information

Install Quote Management by requesting it from the ServiceNow Store.

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=exploring-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The Quote Management application uses the ServiceNow® Customer Service Management account, consumer, and product inventory data model. Customer service agents have full visibility into the quotes created using Quote Management.

-   **[Opportunity Management](https://www.servicenow.com/docs/access?context=opportunity-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The ServiceNow® Opportunity Management application gives your sales agents and account executives with product recommendations for customers based on a needs analysis. You can seamlessly convert sales opportunities to quotes when the customer is ready.

-   **[Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Product Catalog Management feature in the Sales Customer Relationship Management application enables your catalog administrators to create product catalogs with pricing that enables agents to find and add products and services to sales quotes.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Pricing Management feature in Sales Customer Relationship Management enables your pricing administrators to set the pricing for products and services that are used in quotes. Pricing administrators also set the controls that enable your sales agents to adjust the pricing for complex product offers in quotes.

-   **[Order Management](https://www.servicenow.com/docs/access?context=order-mgt-exploring&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Order and fulfillment agents can use ServiceNow® Order Management to fulfill customer orders created from the Quote Management application.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

