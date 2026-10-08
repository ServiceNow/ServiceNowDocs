---
title: Combined Customer self-service for Sales Customer Relationship Management release notes for upgrades from Xanadu to Zurich
description: Consolidated page of all release notes for Customer self-service for Sales Customer Relationship Management from Xanadu to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-xanadu-zurich/zurich-xanadu-customerselfserviceforsalescustomerrelationshipmanagement-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Customer self-service for Sales Customer Relationship Management release notes for upgrades from Xanadu to Zurich

Consolidated page of all release notes for Customer self-service for Sales Customer Relationship Management from Xanadu to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Customer self-service for Sales Customer Relationship Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Customer self-service for Sales Customer Relationship Management to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

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

-   **Upgrade information**

The new order checkout experience and improved cart capabilities are delivered through a new Sales Cart plugin \(sn\_sales\_cart\). As an admin, you must perform the [Post-upgrade order migration](https://www.servicenow.com/docs/access?context=post-upgrade-task-business-portal&family=zurich&ft:locale=en-US) to continue providing a seamless experience for your customers. Failing to perform the upgrade steps can result in your customers losing products added to their carts.


</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Customer self-service for Sales Customer Relationship Management.

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

-   **[Delivery note upload for quantity dispute validation](https://www.servicenow.com/docs/access?context=dispute-invoice-issues-now-assist&family=zurich&ft:locale=en-US)**

Provide customers an option to upload a delivery note during invoice case creation so that the invoice dispute intake assistant AI agent can instantly validate quantity disputes and resolve the issue without human intervention.

-   **[Automated email notifications for order cases](https://www.servicenow.com/docs/access?context=order-case-email-notifications&family=zurich&ft:locale=en-US)**

Keep your customers informed by sending automated emails when the manage order operations AI agent opens an order case from a Business Portal chat conversation and when the case is closed with a successful resolution. The closure email includes the resolution details, and the quote details when a quote was generated for the case. Order cases that are created through the voice channel don't trigger email notifications.


 -   **[Customer-initiated RFQs](https://www.servicenow.com/docs/access?context=create-rfq-business-portal&family=zurich&ft:locale=en-US)**

Request quotes for products and services without relying on manual outreach. The RFQ feature in the Business Portal streamlines the quoting process by enabling customers to:

    -   Submit quote requests from within their portal experience
    -   Specify the overall budget and cumulative target price for each top-level product
    -   Track RFQ status and quotes in real time
    -   Accelerate sales response time with seamless quote-to-order conversion
-   **[Generate quotes from RFQs](https://www.servicenow.com/docs/access?context=convert-rfq-quote-workspace&family=zurich&ft:locale=en-US)**

View all RFQs submitted through the Business Portal in the CSM/FSM Configurable Workspace, eliminating the need for managing and tracking them offline. Convert RFQs into quotes with a single action, accelerating the quote-to-order process, improving turnaround times, and enabling scalable quote management.


 -   **[Create orders from the Business Portal](https://www.servicenow.com/docs/access?context=order-mgt-create-an-order-using-customer-portal&family=zurich&ft:locale=en-US)**

Deploying the Sales Cart plugin provides the following advantages to your B2B customers when they order products using the Business Portal:

    -   Preserve products and configurations added to the cart across sessions and devices so customers can review or update their selections without placing an order. They don't have to start their shopping process all over again if they get interrupted, leave the site, or decide to come back later.
    -   Enable better collaboration and decision making by downloading a cart summary in PDF format and reviewing products to be purchased and terms and conditions with business stakeholders.
    -   Sign the acknowledgment section and share the cart summary PDF with the seller to place an offline order.
    -   Provide the flexibility to select or modify billing and shipping addresses during the checkout process.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Customer self-service for Sales Customer Relationship Management features.

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

-   **[Order exception support for quantity and shipping location requests](https://www.servicenow.com/docs/access?context=request-order-changes-now-assist&family=zurich&ft:locale=en-US)**

Enable customers to request quantity changes and shipping location updates for existing orders, in addition to expedited delivery, through the chat assistant on the Business Portal.

-   **[Voice assistant intake for order exception requests](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-voice-aiagent&family=zurich&ft:locale=en-US)**

Enable customers to submit expedite, quantity, and shipping location requests through the voice assistant. The voice assistant captures the request and creates an order case for the order case agent to resolve it in the CRM Workspace.

-   **[Scripted extension points for order exception checks and quote thresholds](https://www.servicenow.com/docs/access?context=create-atp-api-call&family=zurich&ft:locale=en-US)**

Provide administrators pluggable scripted extension points so they can integrate the chat assistant with their inventory, ERP, and quote systems for delivery availability, quantity validation, shipping location validation, and quote threshold evaluation.

-   **[Consolidated extension point for order exception feasibility checks](https://www.servicenow.com/docs/access?context=create-atp-api-call&family=zurich&ft:locale=en-US)**

Provide a single scripted extension point \(sn\_ord\_ops\_aias.orderExceptionCheckEP\) for the manage order operations chat assistant to validate delivery availability, quantity, and shipping location feasibility for order exception requests. This extension point replaces sn\_ord\_ops\_aias.orderExpeditionCheckEP, which previously handled only available-to-promise \(ATP\) checks for expedited delivery.

-   **[Account and contact populated on interaction records for order exception chats](https://www.servicenow.com/docs/access?context=view-interactions-on-order-case&family=zurich&ft:locale=en-US)**

Provide live agents with the customer's account and contact details on the interaction record when an order exception chat is handed off from the Business Portal. The Account and Contact fields are auto-populated on the interaction record during the virtual assistant conversation, so the live agent immediately sees the customer context, and the chat summarization feature can summarize the conversation by using those details.

-   **[AI-generated chat summary for live agent handoff](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&family=zurich&ft:locale=en-US)**

Provide human agents with an AI-generated summary of the customer's prior virtual assistant conversation at the point of live agent handoff, replacing the full conversation history to accelerate context understanding and improve agent productivity.

-   **[Order line quantity validation for invoice disputes](https://www.servicenow.com/docs/access?context=configure-invoice-quantity-check-ep&family=zurich&ft:locale=en-US)**

Provide the invoice dispute support assistant AI with an additional validation source for quantity disputes by checking order line quantities when sold product records are unavailable, supporting scenarios such as new orders, non-serialized products, and consumable services. The assistant auto-approves eligible disputes and escalates to a human agent only when order data is ambiguous or missing.


 -   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Customer self-service for Sales Customer Relationship Management features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Customer self-service for Sales Customer Relationship Management features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Customer self-service for Sales Customer Relationship Management.

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

-   **Activation information**

Install the following applications by requesting them from the ServiceNow Store:

    -   Customer Request for Quote plugin \(sn\_cust\_rfq\)
    -   Sales Cart plugin \(sn\_sales\_cart\)
Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


**Important:** Sales Cart plugin \(sn\_sales\_cart\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Customer self-service for Sales Customer Relationship Management we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Customer self-service for Sales Customer Relationship Management we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Customer self-service for Sales Customer Relationship Management, such as specific requirements or compliance levels.

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

-   **Accessibility information**
    -   **Dark theme**

The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Customer self-service for Sales Customer Relationship Management we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Customer self-service for Sales Customer Relationship Management we have noted them here.

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

-   Enable business-to-business \(B2B\) customers to request quantity changes and shipping location updates for their existing orders, in addition to expedited delivery, through AI-powered chat and voice assistants.
-   Provide customers with an automatically generated quote when a quantity-change request exceeds the configured price threshold.
-   Provide customers an option to upload a delivery note during invoice case creation so that the invoice dispute intake assistant AI agent can instantly validate quantity disputes.

 -   Enable customers to request for quotes \(RFQ\) from the Business Portal, improving customer autonomy and reducing sales cycle time.
-   Provide a persistent shopping cart experience to your B2B customers.
-   Enable your customers to download and share their cart summary with other stakeholders.
-   Provide seamless order checkout and an easy order creation process to your customers.

 See [Self-Service for Sales and Order Management](https://www.servicenow.com/docs/access?context=som-self-service-business-portal&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-xanadu-zurich/rn-combined-intro.md)

