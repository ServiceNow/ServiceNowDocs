---
title: Customer self-service using the Business Portal
description: Business-to-business \(B2B\) customers can use the Business Portal to browse product catalogs, create product orders, create and view order cases, manage invoice and invoice cases, and request for quotes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/order-mgt-business-portal.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Sales Customer Relationship Management]
---

# Customer self-service using the Business Portal

Business-to-business \(B2B\) customers can use the Business Portal to browse product catalogs, create product orders, create and view order cases, manage invoice and invoice cases, and request for quotes.

## Creating orders using the Business Portal

The Business Portal uses the product catalog to let customers browse and configure products. Customers can also build orders and submit them for fulfillment.

-   [Create orders from the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-create-an-order-using-customer-portal.md)
-   [View an order on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-view-order-using-customer-portal.md)

## Creating and viewing order cases

Customers can create and view order cases for orders or order line items using the Business Portal.

-   [Request updates for one or more orders](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-order-case-for-multiple-orders.md)
-   [Request updates for items in a single order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-order-case-specific-order-lines.md)
-   [View order case details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-order-case.md)
-   [Request order changes using ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/request-order-changes-now-assist.md)
-   [Request order changes via calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-voice-aiagent.md)

Customers can request changes to their unfulfilled orders from the ServiceNow Otto Virtual Agent in the Business Portal using chat and voice channels.

-   [Request order changes using ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/request-order-changes-now-assist.md)
-   [Request order changes via calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-voice-aiagent.md)

## Creating requests for quotes \(RFQs\)

Customers can request for quotes for products or services they're interested in via the Business Portal. They can specify budget and pricing preferences, and submit quote requests without engaging a sales agent. Simplify the RFQ life cycle from submission and internal review to quote generation and customer acceptance, ensuring faster turnaround times and improved transparency.

-   [Submit a request for quote from the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-rfq-business-portal.md)
-   [View requests for quotes \(RFQs\) on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-rfq-business-portal.md)
-   [View quotes from the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-quotes-business-portal.md)
-   [Create quotes from request for quotes \(RFQs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/convert-rfq-quote-workspace.md)

## Managing invoices and invoice cases

From the Business Portal, customers can view their invoices and invoice line details, including quantities, billing and shipping locations, and product information. If they notice a discrepancy such as a quantity mismatch, incorrect part number, or wrong billing or shipping location, they can submit a dispute using the self-service playbook, which guides them through the process step by step. They can dispute multiple line items on a single invoice, or raise issues across multiple invoices at once. For more information, see:

-   [View invoices on the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-invoices-business-portal.md)
-   [Dispute a specific line item on an invoice against your account using the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-invoice-case-single.md)
-   [Dispute multiple invoices against your account using the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-invoice-case-multiple.md)
-   [View invoice case details in the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-invoice-cases-business-portal.md)

Customers can also chat with an AI assistant or use voice commands to report discrepancies conversationally. For eligible quantity disputes, the AI assistant can validate their claim and resolve it on the spot by issuing a credit note or replacement order. If an issue needs further review, customers are seamlessly connected to a billing specialist with full context already in hand. For more information, see:

-   [Dispute invoice issues using ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/dispute-invoice-issues-now-assist.md)
-   [Dispute invoice cases via calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-invoice-mgmt-voice-aiagent.md)

.

## Managing order cases using ServiceNow Otto

Business-to-business \(B2B\) customers can request changes to their unfulfilled orders from the ServiceNow Otto Virtual Agent in the Business Portal using chat and voice channels.

-   [Request order changes using ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/request-order-changes-now-assist.md)
-   [Request order changes via calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-order-mgmt-voice-aiagent.md)

## Managing invoice cases using ServiceNow Otto

B2B customers can dispute invoice cases from the ServiceNow Otto Virtual Agent in the Business Portal using chat and voice channels.

-   [Dispute invoice issues using ServiceNow Otto Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/dispute-invoice-issues-now-assist.md)
-   [Dispute invoice cases via calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/now-assist-invoice-mgmt-voice-aiagent.md)

ServiceNow Otto for Order Management includes the invoice dispute assist agentic workflow. Billing specialists can invoke the invoice dispute assist agentic workflow from the ServiceNow Otto panel to review the invoice case, validate the dispute, view similar cases, and complete resolution actions using a guided experience. Using an agentic workflow helps reduce manual investigation, improves consistency, and helps agents resolve invoice disputes efficiently while keeping customers informed throughout the process. For more information, see [Resolve invoice disputes using agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/resolve-invoice-case-now-assist-agent.md).

Email notifications are sent to the customer when an invoice case is created or closed, but only for cases initiated through the ServiceNow Otto Virtual Agent in the Business Portal. Notifications are triggered for the following closure outcomes: Credit note issued or replacement order placed. Case closure can be performed either by the customer using the ServiceNow Otto Virtual Agent in the Business Portal, or by a billing specialist from the ServiceNow Otto in the CSM/FSM Configurable Workspace.

**Related topics**  


[Configuring the Business Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-management-configure-business-portal.md)

[Customer self-service for Sales Customer Relationship Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/som-self-service-business-portal.md)

