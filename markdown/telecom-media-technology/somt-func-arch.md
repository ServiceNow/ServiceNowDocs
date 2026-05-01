---
title: Sales CRM for Telecommunications functional architecture
description: Sales CRM for Telecommunications is a comprehensive order management solution designed specifically for telecommunications service providers. SOMT serves as a critical orchestration layer within the larger telecommunications ecosystem, integrating with key systems to manage the complete journey from prospect identification to service activation.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Explore, Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Sales CRM for Telecommunications functional architecture

Sales CRM for Telecommunications is a comprehensive order management solution designed specifically for telecommunications service providers. SOMT serves as a critical orchestration layer within the larger telecommunications ecosystem, integrating with key systems to manage the complete journey from prospect identification to service activation.

## Sales CRM for Telecommunications in the Telecommunications ecosystem

Sales CRM for Telecommunications is a critical application in the telecommunications industry, serving as the central orchestration layer for order management. It acts as a central hub connecting various systems across the telecom operator's landscape:

-   Customer-facing channels: Mobile apps, web portals, and sales representatives.
-   Supporting systems: Product catalogs, inventory systems, and service qualification platforms.
-   Fulfillment systems: Field service management and network activation platforms.

Sales CRM for Telecommunications leverages TeleManagement Forum \(TMF\) industry standards to manage telecommunications orders across both selling and fulfillment phases while integrating with multiple upstream and downstream systems.

## Foundation components

Sales CRM for Telecommunications is built on the following core data entities that underpin the entire order management process:

-   Account: Customer account information and organizational hierarchy.
-   Contact: Customer contact details and relationships.
-   Location/Site: Service delivery locations and site information.
-   Product Model: Product specifications and definitions created using the Product-Service-Resource \(PSR\) framework.
-   Sold Product: Customer's purchased products and entitlements
-   Install base item: Customer's product configuration.
-   Entitlements: Entitlements associated with the sold products.
-   Contracts: Customer contract including account details and specific assets covered.

These foundational elements provide the essential data structures that support all operations, from lead management through service activation. The Sales CRM for Telecommunications functional architecture operates across two distinct phases: the Selling Phase and the Fulfillment Phase.

## Selling phase

This phase covers the customer acquisition and order capture process:

-   Lead Management: Initial prospect identification
-   Opportunity Management: Sales opportunity qualification
-   Product Catalog: Product offerings and configurations
-   Sales Agreement: Pre-sales contractual arrangements
-   Shopping Cart: Customer selection management
-   Quote: Pricing and proposal generation \(CPQ\)
-   Contract: Post-sales contractual obligations
-   Order Capture: Final order submission

During this phase, Sales CRM for Telecommunications integrates with digital apps, self-care portals, account managers, product catalogs, and service feasibility systems.

![SOMT selling phase](../image/somt-func-arch-1.jpg)

## Fulfillment phase

After order submission, the next phase is the fulfillment process:

-   Order Distribution: Decomposition into service orders and work orders.
-   Service Order Management: Tracking through activation lifecycle.
-   Activation Handoff: Submission to provisioning systems.

During this phase, Sales CRM for Telecommunications coordinates with Field Service Management for Telecommunication, external inventory systems, and network activation platforms.

![SOMT fulfillment phase](../image/somt-func-arch-2.jpg)

**Note:** Sales CRM for Telecommunications orchestrates the order management process and submits service orders to downstream activation systems but does not perform network activation or provisioning.

## TeleManagement Forum \(TMF\) Open APIs

The Sales CRM for Telecommunications leverages TeleManagement Forum \(TMF\) Open APIs throughout its architecture, ensuring standards-based integration with third-party systems. Key API integrations include:

-   Product catalog management API: Manage product catalog information from external systems. See [Product Catalog Open API](https://www.servicenow.com/docs/access?context=product-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Product inventory API: For ServiceNow applications or external CRM / CPQ submitting orders. See [Product Inventory Open API](https://www.servicenow.com/docs/access?context=product-inventory-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Service catalog API: For synching technical specifications with other network domain specific provisioning catalogs. See [Service Catalog Open API](https://www.servicenow.com/docs/access?context=service-catalog-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Service order API: Service Order API: Customer order is handled by another application and Sales CRM for Telecommunications acts as a service order manager or when the decomposition and orchestration is handled by the marketplace owner and sends order to Sales CRM for Telecommunications for fulfillment. See [Service Order Open API](https://www.servicenow.com/docs/access?context=service-order-open-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Technical service qualification API: Checks availability of resources and services before an order is submitted for fufillment. See [Technical Service Qualification Open API](https://www.servicenow.com/docs/access?context=ts-qualification-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Quote management API: Based on the TMF 648 API. See [Quote Management API](https://www.servicenow.com/docs/access?context=quote-management-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

## Non-TMF APIs

-   Entitlement API: Create and fetch entitlements. See [Entitlement API](https://www.servicenow.com/docs/access?context=entitlement-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Lead management API: Mapping and certification as per TMF 699. See [lead API](https://www.servicenow.com/docs/access?context=lead-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Order API: See [Order API](https://www.servicenow.com/docs/access?context=order_csm-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).
-   Sales agreement API: See [Sales Agreement API](https://www.servicenow.com/docs/access?context=sales_agreement-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

