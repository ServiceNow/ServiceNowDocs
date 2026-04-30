---
title: Order Management release notes
description: The ServiceNow Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-25"
reading_time_minutes: 4
---

# Order Management release notes

The ServiceNow® Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Yokohama release.

## Order Management highlights for the Yokohama release

-   Enable order agents to view price adjustment details while processing orders.
-   Enable customers to view the product catalog, add products to a shopping cart, and create orders by using the Business Portal.
-   Create cases for multiple orders or for specific order lines using the Business Portal.
-   Create cases for multiple invoices or for specific invoice lines.
-   Provide metrics that help sales agents and sales managers track and analyze the revenue impact of subscriptions.

See [Order Management](https://www.servicenow.com/docs/access?context=order-mgt-exploring&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US) for more information.

**Important:** Order Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Business Portal for order case management](https://www.servicenow.com/docs/access?context=order-mgt-business-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Enable your customers to create cases for common order-related issues such as delivery delays, quantity disputes, and other routine inquiries directly using the Business Portal, ensuring faster issue resolution and improved customer satisfaction. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **Hierarchical view of order line items**

    Enable order agents and order managers to use the hierarchical list view to view parent and child relationships within order lines.

-   **[Price adjustment details for order lines](https://www.servicenow.com/docs/access?context=view-price-adjustment-details-order-lines&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Provides order agents and order managers the visibility into the price adjustments applied at each step of the pricing plan, including a detailed breakdown of all adjustments applied to the unit base price and unit list price to see how the unit net price is derived.

-   **[Multi-instance product offering configurations](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Create multiple instances of a child product offering in orders to generate a custom configuration for each product offering instance. When a child product offering has a quantity greater than 1, agents can clone or split a child product offering to create multiple product offering instances so that each quantity has its own configuration.

-   **[Transient products](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Add transient products, which are defined as one-time-use products or services, to new orders. Sold product and product inventory records are created but not maintained for transient products. Move, Add, Change and Disconnect \(MACD\) actions are not supported for transient products.

-   **[Business Portal for Order Management](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Use the Business Portal to view product catalogs, select product options, and place orders. Customers can also view their order status using the Business Portal.

-   **[Cases for multiple invoices](https://www.servicenow.com/docs/access?context=csm-invoice-operations&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Create cases for multiple invoices or for specific invoice lines. Agents can reference multiple invoices or invoice lines as case line items on an invoice case record. By using case line items, agents can track multiple issues for the same invoice case and resolve the issues in each case line item independently before resolving and closing the order case. This application is a feature of Customer Service Management and the Order to Cash Operations functionality for Order Management.

-   **[Add subscription pricing to an order](https://www.servicenow.com/docs/access?context=add-subscription-pricing-to-an-order&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Enable order agents and order managers to access and view key calculated metrics such as monthly recurring price and annual recurring price. The subscription pricing fields are automatically calculated based on contract start date and contract end date. These metrics enhance revenue reporting and help you to better understand recurring revenue dynamics.


## Deprecations

-   The Subscription start and end dates have been deprecated starting with the Q2 2025 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.
-   The fields listed for the following tables are no longer supported.

    |Table name|Fields|
    |----------|------|
    |Order \(sn\_ind\_tmt\_orm\_order\)|Total monthly recurring price, Total annual recurring price|
    |Order line item \(sn\_ind\_tmt\_orm\_order\_line\_item\)|Cumulative monthly recurring price, Cumulative annual recurring price, Subscription start date, Subscription end date|
    |Order line item \(sn\_csm\_om\_order\_line\_item\)|Total recurring price|


## Activation information

Install Order Management by requesting it from the ServiceNow Store.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The Order Management application uses the Customer Service Management account, consumer, and product inventory data model.

-   **[Opportunity Management](https://www.servicenow.com/docs/access?context=opportunity-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Opportunity Management application provides your sales agents and account executives with product recommendations for customers based on a needs analysis. You can seamlessly convert sales opportunities to quotes when the customer is ready.

-   **[Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Product Catalog Management feature in Sales Customer Relationship Management enables your catalog administrators to create product catalogs with pricing that enable agents to find and add products and services to orders.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Pricing Management feature in Sales Customer Relationship Management enables your pricing administrators to set pricing for products and services in orders. Pricing administrators also set the controls that enable your agents to adjust pricing for orders that have complex product offers.

-   **[Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The Quote Management application enables your sales agents to generate and manage sales quotes for your customers.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

