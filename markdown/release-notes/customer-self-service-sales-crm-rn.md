---
title: Customer self-service for Sales Customer Relationship Management release notes
description: The ServiceNow Business Portal application enables B2B customers to build sales carts, place orders, request quotes, and get support for orders and invoices through a self-service web portal. See the following sections for release notes by version.REST APIs give an external ordering system programmatic control of a sales cart, from creating the cart through to submitting it as an order, and extend that control to consumers with a billing account and payment profile on each cart line item.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/customer-self-service-sales-crm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Sales Customer Relationship Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Customer self-service for Sales Customer Relationship Management release notes

The ServiceNow® Business Portal application enables B2B customers to build sales carts, place orders, request quotes, and get support for orders and invoices through a self-service web portal. See the following sections for release notes by version.

## About Customer self-service for Sales Customer Relationship Management

-   Shorten the sales cycle and accelerate revenue by letting B2B customers browse, configure, and place orders independently.
-   Speed up quoting by letting customers request and review quotes directly in the Business Portal.
-   Reduce support costs by deflecting routine order and invoice questions to self-service and AI, escalating only complex cases to a human agent with full context.
-   Improve billing transparency and speed up dispute resolution by giving customers direct visibility into invoices and a trackable channel to raise disputes.
-   Extend self-service ordering beyond your portal by letting account contacts and consumers transact from third-party systems through the Sales Cart API.

See [Customer self-service for Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/som-self-service-business-portal.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Business Portal application \(sn\_b2b\_portal\) is automatically installed when you install the Customer Service Portal \(sn\_csm\_portal\). Install the Customer Service Portal by requesting it from the [ServiceNow Store](https://store.servicenow.com/store). For activation and configuration information, see [Configuring the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/order-management-configure-business-portal.md).

-   **Additional requirements**

    Sales Cart REST APIs require the Billing Account Core \(sn\_billing\_account\) and Order Management \(sn\_ind\_tmt\_orm\) applications for supporting end-to-end ordering, billing, and payment flows.


## Accessibility and localization

-   **Localization information**

    Business Portal text is displayed in the language set for the active ServiceNow language pack, including Japanese, with right-to-left rendering support for locales such as Arabic and Hebrew. Language packs are installed automatically when the corresponding ServiceNow base system language plugin is active.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/sales-order-management-rn-landing.md)

## Brazil Early Availability

REST APIs give an external ordering system programmatic control of a sales cart, from creating the cart through to submitting it as an order, and extend that control to consumers with a billing account and payment profile on each cart line item.

### What's new

-   **[Sales Cart APIs for external ordering systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

    Create and manage sales carts from third-party consumer portals, partner portals, and headless ordering applications by using the Sales Cart REST API. External systems can create and retrieve carts, add or update line items, delete carts or top-level line items, and submit validated carts to create orders without relying on the Business Portal user interface. Carts created externally use the same records and cart-processing logic as carts created in the Business Portal.

-   **[Digital ordering support for B2C consumers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

    Extend digital ordering to B2C consumers by enabling authenticated consumers, in addition to account-and-contact customers \(B2B users\), to build and submit carts through external ordering experiences. Consumer carts derive the currency from the consumer’s country, resolve the price list from that currency, and use address information from the consumer record.

-   **[Billing account and payment profile support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/sales-cart-external-integration.md)**

    Complete orders with line-level billing information by assigning a billing account and payment profile to each cart line item. Different lines in the same cart can use different billing accounts, and both values carry to the corresponding order line items when the cart is submitted, eliminating manual re-entry for downstream billing.

-   **[View contracts and entitlements on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/contracts-entitlements-self-service.md)**

    View and access contracts and entitlements associated with your accounts on the Business Portal. Access contract and entitlement details including contract numbers, pricing details, dates, and contract line items.


