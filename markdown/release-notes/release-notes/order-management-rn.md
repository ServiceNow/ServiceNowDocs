---
title: Order Management release notes
description: The ServiceNow Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-28"
reading_time_minutes: 5
---

# Order Management release notes

The ServiceNow® Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Xanadu release.

## Order Management highlights for the Xanadu release

-   Sales agreements associated with the account are automatically applied and the catalog is filtered to display the agreement's products and prices.
-   Admins can set planned task due dates in Jeopardy Management, which are calculated based on business hours during weekdays.
-   Order agents can associate product specifications to a product offer at any level of a product offer hierarchy.
-   Admins can update product inventory records in a batch when there are changes to product specifications.
-   Order agents create orders tailored to each customer location from the product catalog.
-   Agents can use the Order Operations Case Management application to create cases for customer orders, unifying order tracking and resolution solutions.

See [Order management](https://www.servicenow.com/docs/access?context=reviewing-approving-fulfilling-orders&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US) for more information.

## Important information for upgrading Order Management to Xanadu

Features introduced in the Xanadu release aren't supported in earlier releases of Order Management.

If you’re upgrading from Order Management for Telecommunications and Media version 6.0 or earlier:

-   Starting with the  Washington DC release, the  Monthly Recurring Charges  \(MRC\) and the  Non-Recurring Charges  \(NRC\) for product offerings and product attribute characteristics are no longer stored in the product offering data model. Instead, the MRC and NRC are stored in the Pricing data model in price lists and price list lines. If you want to upgrade your pricing information to use price lists after upgrading to  Washington DC, see the  [Price Management Plugin \(com.sn\_csm\_pricing\) uptake for Telecommunications, Media, and Technology customers upgrading to Washington \[KB1585863\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1585863) article in the Now Support Knowledge Base.
-   After upgrading to the  Xanadu release, a fix script runs automatically to deactivate certain telecommunications list records that are no longer needed to resume the capture of an unfinished order. For more information on these records and using the former order capture process, see the  [Deprecating Telco List for Order Capture \[KB1586538\] ](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1586538) article in the Now Support Knowledge Base.

If you’re an upgrade customer who uses the **contract start date** and **contract end date** fields and has records, you can migrate those records to the latest data model by running the **Migrate data from deprecated contract fields to new fields on Order and Order Lines** scheduled job. This scheduled job must be manually executed by navigating to **System Definitions** &gt; **Scheduled Jobs**. For more information on scheduled jobs, see [Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## New in the Xanadu release

-   **[Add sales agreements to orders](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    When an agent creates an order, the sales agreement associated with the account is automatically applied and the catalog is filtered with the agreement products and prices.

-   **[Add business hours to Jeopardy Management tasks](https://www.servicenow.com/docs/access?context=configuring-jeopardy-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Admins can set planned task due dates, which are calculated based on business hours during weekdays in Jeopardy Management.

-   **[Update specification versions](https://www.servicenow.com/docs/access?context=som-specification-version-update&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Admins can perform a batch version update to a product inventory’s specification version.

-   **[Add covered products to an order](https://www.servicenow.com/docs/access?context=som-update-covered-products&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Agents can create covered products and modifications as part of an order capture to establish coverage relationships. They can also create change orders that remove sold products or install base items as covered products from entitlements and contracts.

-   **Order to Cash Operations**
    -   [Order Operations Case Management](https://www.servicenow.com/docs/access?context=csm-case-mgmt-order-ops&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US): Use the Order Operations Case Management application \(com.sn\_order\_case\) to create order cases that reference multiple line items, including orders and order lines. Agents can use these cases to process order-related services such as order changes, inquiries, and disputes.
    -   [Case lines and workflows](https://www.servicenow.com/docs/access?context=csm-case-mgmt-case-lines&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US): Use the Case lines and workflows application \(com.sn\_case\_line\) to reference multiple line items on a case record, including orders or order lines, invoices or invoices lines, contracts, and sold products.

## Changed in this release

-   **[Add a sales agreement](https://www.servicenow.com/docs/access?context=som-add-sales-agreement-to-order&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    When an agent creates an order, the latest sales agreement associated with the account is automatically applied and the catalog is filtered to display the agreement's products and prices.

-   **[Update product locations at the order line level](https://www.servicenow.com/docs/access?context=order-mgt-copy-order-line-location&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    Agents can create orders by location, which enables them to tailor orders for a customer location and streamline the ordering process by managing orders that have multiple locations.


## Activation information

Install Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The Configuration Management Database \(CMDB\) application creates required configuration items and activates base items for the services and resources that are delivered to customers. It helps to assure that service begins when an order has been fulfilled.

-   **[CSM Inventory Data Model](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The Customer Service Management application uses the account, consumer, and product inventory data model. Customer service agents have full visibility into products and services that have been delivered to customers using Order Management

-   **[CSM Catalog Administrators](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The Product Catalog Management application enables your catalog administrators to create products catalogs that agents use to find and add products and services to orders.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Pricing Management application enables your pricing administrators to set prices for products and services that are used in orders. Pricing administrators also set the controls that enable your sales agents to adjust product pricing in orders.

-   **[Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=xanadu&pubname=xanadu-order-management&ft:locale=en-US)**

    The Quote Management application enables your sales agents and account executives to generate and manage sales quotes for your customers. You can convert sales quotes to orders when the customer is ready.

-   **[Flow Designer Actions](https://www.servicenow.com/docs/access?context=csm-flow-designer-actions&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    Workflow Studio components enable you to invoke flows or subflows that are designed as part of a workflow, such as an orchestration workflow. The components also enable you to find the output or execution status of the flows or subflows.

-   **[Configure Field Service Management](https://www.servicenow.com/docs/access?context=configure-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    The Customer Service with Field Service Management plugin \(com.snc.csm\_fsm\_integration\) integrates the Customer Service Management and Field Service Management applications to enable you to view account and contact information on work orders and work order tasks in the application.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

