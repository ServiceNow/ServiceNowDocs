---
title: Unified sales and order management
description: Sales CRM for Telecommunications consolidates product catalog, sales, and order fulfillment on one platform, carrying quote line items through to fulfilled services without intermediate transformation and decomposing customer orders into domain orders using catalog-defined rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/exploring-unified-sales-order-management-somt.html
release: australia
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 7
keywords: [unified sales and order management, USAM, PSR catalog, quote to order, order decomposition, domain orders, product inventory, TMF622, TMF641, TMF637, inflight changes]
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Unified sales and order management

Sales CRM for Telecommunications consolidates product catalog, sales, and order fulfillment on one platform, carrying quote line items through to fulfilled services without intermediate transformation and decomposing customer orders into domain orders using catalog-defined rules.

The Unified Sales and Order Management \(USAM\) platform in Sales CRM for Telecommunications brings product catalog, sales, and order fulfillment together in one system. A unified Product, Service, and Resource \(PSR\) catalog serves as the single source of truth for all definitions across sales and fulfillment, removing the need to synchronize data between separate systems.

When a customer accepts a quote, the platform creates a customer order directly — no intermediate transformation required. Quote line items carry forward to order line items, preserving commercial terms, pricing, and configuration through fulfillment. After approval, the platform decomposes the order into domain orders and routes them to the appropriate fulfillment system. The flow covers the full customer journey from lead capture through service activation, supporting inflight changes, product inventory management, and multi-domain orchestration aligned to TM Forum \(TMF\) Open API standards.

## Benefits

-   A unified PSR catalog serves as the single source of truth for all product, service, and resource definitions, removing the need to synchronize data between separate sales and fulfillment systems.
-   Quote line items carry forward to order line items without transformation, preserving commercial terms, pricing, and configuration through the fulfillment lifecycle.
-   Sales and fulfillment teams can modify quantity, service configuration, or product type at any stage of the order lifecycle without losing quote context or reconstructing the order.
-   Catalog-defined decomposition rules generate domain orders automatically after approval, removing manual order construction and reducing coordination overhead between teams.
-   A customer order decomposes into product orders, service orders, and resource orders, routed to the appropriate fulfillment system in parallel or in sequence using catalog-defined rules.
-   The platform instantiates product inventory from the same PSR catalog definition used to configure the quote, and updates inventory state automatically through upgrades, downgrades, suspensions, and disconnects.
-   Domain orders align to TMF622, TMF641, and TMF637 Open API standards, with TMF652 support planned, so third-party integrations don't require redesign when order types or fulfillment systems change.
-   Sales and operations teams track the full order lifecycle on one platform, from quote line item through domain orders and fulfillment tasks, reducing coordination overhead and escalations.

## Features

|Feature|Description|
|-------|-----------|
|Unified PSR catalog|Serves as the single source of truth for all product, service, and resource definitions across sales and fulfillment, aligned to the TMF SID model. Supports product bundling, multi-level hierarchies, pricing rules, and eligibility and compatibility rules.|
|Direct quote-to-order conversion|Converts an accepted quote into a customer order without an intermediate transformation step, preserving commercial terms, pricing, and configuration through the fulfillment lifecycle.|
|Inflight order changes|Supports quantity, configuration, and product type modifications at any stage of the order lifecycle without reconstructing the order. Applies to upgrade, downgrade, suspend, resume, and disconnect order types.|
|Catalog-driven order decomposition|Decomposes a customer order into product orders, service orders, and resource orders using specification relationships and decomposition rules in the PSR catalog. No manual order construction is required.|
|Multi-domain order routing|Routes domain orders to the appropriate fulfillment system based on catalog-defined rules, supporting parallel and sequential execution with dependency management across order line items.|
|Product inventory management|Instantiates product inventory from the same PSR catalog definition used to configure the quote and updates inventory state automatically as the order progresses through upgrades, downgrades, suspensions, and disconnects.|
|TMF standards alignment|Supports TMF622 \(Product Order\), TMF641 \(Service Order\), TMF637 \(Product Inventory\), and planned TMF652 \(Resource Order\) for standards-based integration with third-party systems without redesign.|
|End-to-end order visibility|Tracks the full order lifecycle from quote line item through domain orders and fulfillment tasks on one platform, giving sales and operations teams a shared view of order status, inventory state, and service activation.|

## PSR catalog components

The PSR catalog defines all product, service, and resource entities in a single location, based on the TMF Shared Information and Data \(SID\) model. The following components form the foundation of the unified sales and order management flow:

|Component|Description|
|---------|-----------|
|Product offering|The customer-facing catalog item that defines what is sold, including pricing, terms, and conditions. It references a product specification and can be a simple item or a bundle.|
|Bundle product offering|A product offering that groups two or more offerings into a single package. For example, a triple-play bundle of internet, TV, and voice. Component offerings are referenced rather than embedded, so the same item can appear across multiple bundles.|
|Product specification|The technical definition of a product that maps commercial offerings to service and resource implementations. One product specification maps to exactly one service specification and can reference one or more resource specifications.|
|Customer-facing service specification \(CFSS\)|Defines the service characteristics a customer purchases, such as internet access, independent of the underlying technology. One CFSS can support multiple product offerings.|
|Resource-facing service specification \(RFSS\)|Defines the technical, domain-specific service layer that maps to underlying network resources. For example, DSL, VPN, or MPLS. It translates CFSS requirements into the resources needed to deliver the service.|
|Resource specification|The template for physical or logical network resources, such as routers, SIM cards, or virtual network functions. Each resource instance is created from a resource specification.|

Because the PSR catalog defines and maps all entities in one place, explicit entity-to-entity API mapping and separate product data harmonization between sales and fulfillment catalogs aren't required.

## Quote to customer order

The sales flow begins with a quote containing one or more quote line items, each representing a product offering configured for the customer. When the customer accepts the quote, Sales CRM for Telecommunications creates a customer order directly from the quote. No intermediate transformation of the quote into a product order is required.

Quote line items map to order line items and this mapping is maintained throughout the fulfillment lifecycle. The persistent mapping produces the following outcomes:

-   Commercial terms, pricing, and configuration from the quote are available at every stage of the order lifecycle.
-   Inflight changes, quantity updates, service modifications, or configuration adjustments can be applied without losing the original quote context or requiring order reconstruction.
-   Traceability from quote line item to fulfilled service is preserved end to end, giving sales and operations teams a shared audit trail.

## Customer order to domain orders

After a customer order is approved, Sales CRM for Telecommunications decomposes it into a hierarchy of domain orders. Decomposition is driven entirely by the PSR catalog no manual order construction is required. The following table describes each level in the decomposition hierarchy:

|Entity|Description|
|------|-----------|
|Customer order|Top-level record created from the accepted quote. Contains one or more product offering bundle order line items \(OLI\).|
|Product order line item|Generated for each product offering. References the product specification in the PSR catalog and drives the creation of service and resource orders.|
|Order line item \(OLI\)|Decomposed view of a product order line item. Carries the attributes needed for downstream fulfillment systems.|
|Domain order|Created for each OLI using specification relationships and decomposition rules. Routes fulfillment work to service fulfillment, network provisioning, or field operations in parallel or in sequence.|

For example, a customer order containing two product offering bundles decomposes as follows:

-   Bundle 1 generates a product order line item \(PO1.PS1.OLI\), which decomposes into a product order \(PS1.DO = PO\) and a customer-facing service order \(PS1.CFSS.DO = SO\).
-   Bundle 2 generates a product order line item \(PO2.PS2.OLI\), which decomposes into its own product order \(PS1.DO = PO\), customer-facing service order \(PS1.CFSS.DO = PO\), and resource order \(PS2.RS.DO = RO\).

Decomposition rules function as exclusion rules. They prevent the creation of domain orders when the incoming order does not contain a specific characteristic or characteristic value. This supports optional components within a product or service offering without requiring separate catalog entries for every variant.

## Product inventory instantiation

Product inventory is instantiated from the same PSR catalog definition used to configure and price the quote. When the order is approved, inventory records are created with placeholders for all specifications generated after decomposition. Records remain in an Installation Pending state until fulfillment is confirmed, at which point associated specifications update to Active.

Because inventory is managed by the order throughout the fulfillment lifecycle:

-   Alignment between what was sold \(the product offering\) and what is provisioned \(the inventory record\) is maintained automatically.
-   Inventory does not affect availability until services are confirmed as deliverable.
-   Upgrades, downgrades, suspensions, and disconnects update the inventory record state automatically as the order progresses no separate synchronization step is required.
-   The need to maintain separate product data between sales and fulfillment catalogs is removed.

## TMF standards support

Sales CRM for Telecommunications aligns domain order creation and routing to TM Forum Open API standards, supporting standards-based integration with third-party fulfillment and provisioning systems. For more information about TMF APIs, see [TMF APIs for TMT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/tmt-api-reference.md).

