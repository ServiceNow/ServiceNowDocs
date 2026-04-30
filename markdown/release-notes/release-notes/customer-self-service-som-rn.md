---
title: Customer self-service for Sales Customer Relationship Management release notes
description: The ServiceNow Business Portal is a self-service web portal that supports your business-to-business \(B2B\) customers by providing integrated access to knowledge articles, community forums, service catalogs, and chatbots. Business Portal was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-12"
reading_time_minutes: 3
---

# Customer self-service for Sales Customer Relationship Management release notes

The ServiceNow® Business Portal is a self-service web portal that supports your business-to-business \(B2B\) customers by providing integrated access to knowledge articles, community forums, service catalogs, and chatbots. Business Portal was enhanced and updated in the Zurich release.

## Business Portal highlights for the Zurich release

-   Enable B2B customers to request for quotes \(RFQ\) from the Business Portal, improving customer autonomy and reducing sales cycle time.
-   Provide a persistent shopping cart experience to your B2B customers.
-   Enable your customers to download and share their cart summary with other stakeholders.
-   Provide seamless order checkout and an easy order creation process to your customers.

See [Self-Service for Sales and Order Management](https://www.servicenow.com/docs/access?context=som-self-service-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Sales Cart plugin \(sn\_sales\_cart\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Business Portal to Zurich

The new order checkout experience and improved cart capabilities are delivered through a new Sales Cart plugin \(sn\_sales\_cart\). As an admin, you must perform the [Post-upgrade order migration for the Business Portal](https://www.servicenow.com/docs/access?context=post-upgrade-task-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US) to continue providing a seamless experience for your customers. Failing to perform the upgrade steps can result in your customers losing products added to their carts.

## New in the Zurich release

-   **[Customer-initiated RFQs](https://www.servicenow.com/docs/access?context=create-rfq-business-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Request quotes for products and services without relying on manual outreach. The RFQ feature in the Business Portal streamlines the quoting process by enabling customers to:

    -   Submit quote requests from within their portal experience
    -   Specify the overall budget and cumulative target price for each top-level product
    -   Track RFQ status and quotes in real time
    -   Accelerate sales response time with seamless quote-to-order conversion
-   **[Generate quotes from RFQs](https://www.servicenow.com/docs/access?context=convert-rfq-quote-workspace&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    View all RFQs submitted through the Business Portal in the CSM/FSM Configurable Workspace, eliminating the need for managing and tracking them offline. Convert RFQs into quotes with a single action, accelerating the quote-to-order process, improving turnaround times, and enabling scalable quote management.

-   **[Create orders from the Business Portal](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Deploying the Sales Cart plugin provides the following advantages to your B2B customers when they order products using the Business Portal:

    -   Preserve products and configurations added to the cart across sessions and devices so customers can review or update their selections without placing an order. They don't have to start their shopping process all over again if they get interrupted, leave the site, or decide to come back later.
    -   Enable better collaboration and decision making by downloading a cart summary in PDF format and reviewing products to be purchased and terms and conditions with business stakeholders.
    -   Sign the acknowledgment section and share the cart summary PDF with the seller to place an offline order.
    -   Provide the flexibility to select or modify billing and shipping addresses during the checkout process.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install the following applications by requesting them from the ServiceNow Store:

-   Customer Request for Quote plugin \(sn\_cust\_rfq\)
-   Sales Cart plugin \(sn\_sales\_cart\)

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

