---
title: Customer self-service for Sales Customer Relationship Management release notes
description: The ServiceNow Business Portal is a self-service web portal that supports your B2B customers by providing integrated access to knowledge articles, community forums, service catalogs, and chatbots. Business Portal was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-12"
reading_time_minutes: 5
---

# Customer self-service for Sales Customer Relationship Management release notes

The ServiceNow® Business Portal is a self-service web portal that supports your B2B customers by providing integrated access to knowledge articles, community forums, service catalogs, and chatbots. Business Portal was enhanced and updated in the Zurich release.

## Business Portal highlights for the Zurich release

-   Enable business-to-business \(B2B\) customers to request quantity changes and shipping location updates for their existing orders, in addition to expedited delivery, through AI-powered chat and voice assistants.
-   Provide customers with an automatically generated quote when a quantity-change request exceeds the configured price threshold.
-   Provide customers an option to upload a delivery note during invoice case creation so that the invoice dispute intake assistant AI agent can instantly validate quantity disputes.

-   Enable customers to request for quotes \(RFQ\) from the Business Portal, improving customer autonomy and reducing sales cycle time.
-   Provide a persistent shopping cart experience to your B2B customers.
-   Enable your customers to download and share their cart summary with other stakeholders.
-   Provide seamless order checkout and an easy order creation process to your customers.

See [Self-Service for Sales and Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/som-self-service-business-portal.md) for more information.

**Important:** Sales Cart plugin \(sn\_sales\_cart\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Business Portal to Zurich

The new order checkout experience and improved cart capabilities are delivered through a new Sales Cart plugin \(sn\_sales\_cart\). As an admin, you must perform the [Post-upgrade order migration for the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/post-upgrade-task-business-portal.md) to continue providing a seamless experience for your customers. Failing to perform the upgrade steps can result in your customers losing products added to their carts.

## New in the Zurich release

-   **[Delivery note upload for quantity dispute validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/dispute-invoice-issues-now-assist.md)**

    Provide customers an option to upload a delivery note during invoice case creation so that the invoice dispute intake assistant AI agent can instantly validate quantity disputes and resolve the issue without human intervention.

-   **[Automated email notifications for order cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/order-case-email-notifications.md)**

    Keep your customers informed by sending automated emails when the manage order operations AI agent opens an order case from a Business Portal chat conversation and when the case is closed with a successful resolution. The closure email includes the resolution details, and the quote details when a quote was generated for the case. Order cases that are created through the voice channel don't trigger email notifications.

-   **[Customer-initiated RFQs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/create-rfq-business-portal.md)**

    Request quotes for products and services without relying on manual outreach. The RFQ feature in the Business Portal streamlines the quoting process by enabling customers to:

    -   Submit quote requests from within their portal experience
    -   Specify the overall budget and cumulative target price for each top-level product
    -   Track RFQ status and quotes in real time
    -   Accelerate sales response time with seamless quote-to-order conversion
-   **[Generate quotes from RFQs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/convert-rfq-quote-workspace.md)**

    View all RFQs submitted through the Business Portal in the CSM/FSM Configurable Workspace, eliminating the need for managing and tracking them offline. Convert RFQs into quotes with a single action, accelerating the quote-to-order process, improving turnaround times, and enabling scalable quote management.

-   **[Create orders from the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/order-mgt-create-an-order-using-customer-portal.md)**

    Deploying the Sales Cart plugin provides the following advantages to your B2B customers when they order products using the Business Portal:

    -   Preserve products and configurations added to the cart across sessions and devices so customers can review or update their selections without placing an order. They don't have to start their shopping process all over again if they get interrupted, leave the site, or decide to come back later.
    -   Enable better collaboration and decision making by downloading a cart summary in PDF format and reviewing products to be purchased and terms and conditions with business stakeholders.
    -   Sign the acknowledgment section and share the cart summary PDF with the seller to place an offline order.
    -   Provide the flexibility to select or modify billing and shipping addresses during the checkout process.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Order exception support for quantity and shipping location requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/request-order-changes-now-assist.md)**

    Enable customers to request quantity changes and shipping location updates for existing orders, in addition to expedited delivery, through the chat assistant on the Business Portal.

-   **[Voice assistant intake for order exception requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-order-mgmt-voice-aiagent.md)**

    Enable customers to submit expedite, quantity, and shipping location requests through the voice assistant. The voice assistant captures the request and creates an order case for the order case agent to resolve it in the CSM Configurable Workspace.

-   **[Scripted extension points for order exception checks and quote thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/create-atp-api-call.md)**

    Provide administrators pluggable scripted extension points so they can integrate the chat assistant with their inventory, ERP, and quote systems for delivery availability, quantity validation, shipping location validation, and quote threshold evaluation.

-   **[Consolidated extension point for order exception feasibility checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/create-atp-api-call.md)**

    Provide a single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) for the manage order operations chat assistant to validate delivery availability, quantity, and shipping location feasibility for order exception requests. This extension point replaces sn\_ord\_ops\_aias.orderExpeditionCheckEP, which previously handled only available-to-promise \(ATP\) checks for expedited delivery.

-   **[Account and contact populated on interaction records for order exception chats](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/view-interactions-on-order-case.md)**

    Provide live agents with the customer's account and contact details on the interaction record when an order exception chat is handed off from the Business Portal. The Account and Contact fields are auto-populated on the interaction record during the virtual assistant conversation, so the live agent immediately sees the customer context, and the chat summarization feature can summarize the conversation by using those details.

-   **[AI-generated chat summary for live agent handoff](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/resolve-invoice-case-now-assist-agent.md)**

    Provide human agents with an AI-generated summary of the customer's prior virtual assistant conversation at the point of live agent handoff, replacing the full conversation history to accelerate context understanding and improve agent productivity.

-   **[Order line quantity validation for invoice disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/configure-invoice-quantity-check-ep.md)**

    Provide the invoice dispute support assistant AI with an additional validation source for quantity disputes by checking order line quantities when sold product records are unavailable, supporting scenarios such as new orders, non-serialized products, and consumable services. The assistant auto-approves eligible disputes and escalates to a human agent only when order data is ambiguous or missing.


## Activation information

Install the following applications by requesting them from the ServiceNow Store:

-   Customer Request for Quote plugin \(sn\_cust\_rfq\)
-   Sales Cart plugin \(sn\_sales\_cart\)

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/sales-order-management-rn-landing.md)

