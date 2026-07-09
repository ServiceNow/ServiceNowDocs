---
title: Intent-based order fulfillment
description: Sales CRM for Telecommunications supports intent-based order fulfillment, translating non-catalog configuration inputs into order tasks without requiring explicit catalog entries for every product variant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/intent-based-order-fulfillment-somt.html
release: australia
topic_type: concept
last_updated: "2025-07-14"
reading_time_minutes: 2
keywords: [intent-based order fulfillment, order decomposition, non-catalog, SOMT, PSR catalog]
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Intent-based order fulfillment

Sales CRM for Telecommunications supports intent-based order fulfillment, translating non-catalog configuration inputs into order tasks without requiring explicit catalog entries for every product variant.

Sales CRM for Telecommunications extends catalog-driven order fulfillment with intent-based orchestration. Rather than requiring a catalog entry for every product variant, the platform translates configuration inputs — including non-catalog items — into structured order tasks using spec relationships, decomposition rules, and attribute mapping.

This approach separates the commercial catalog \(what is sold\) from the fulfillment view \(what is activated\), allowing sales and network operations teams to work from a shared order structure without manual translation between domains.

## How intent-based fulfillment works

When a customer order is submitted, Sales CRM for Telecommunications applies three catalog mechanisms to decompose it into executable order tasks:

-   **Spec relationships**

    Define how product specifications relate to service and resource specifications in the PSR catalog hierarchy. These relationships determine which service orders and resource orders are generated for each product offering line item \(OLI\).

-   **Decomposition rules**

    Control how a customer order is broken down into domain orders — product orders \(PO\), service orders \(SO\), and resource orders \(RO\). Rules support staggered decomposition and dependency sequencing across order line items.

-   **Attribute mapping**

    Carry quote and order attributes through to order tasks, making the correct data available to southbound APIs during service order orchestration. This eliminates manual data entry between sales and fulfillment systems.


## Order decomposition structure

A customer order decomposes into the following hierarchy:

-   Customer order contains one or more product offering bundle order line items \(OLI\)
-   Each OLI decomposes into product orders \(PO\) aligned to product specifications
-   Product orders decompose into service orders \(SO\) via customer-facing service specifications \(CFSS\)
-   Service orders decompose into resource orders \(RO\) via resource-facing service specifications \(RFSS\)

This structure maps directly to TM Forum standards: Service Catalog Management \(TMF633\), Product Order \(TMF620\), and Service Order \(TMF641\).

## Benefits

-   Non-catalog and variant products decompose automatically without new catalog entries.
-   Decomposition rules and spec relationships replace complex workflow logic, reducing configuration overhead.
-   Attribute mapping eliminates manual data transfer between sales and fulfillment systems.
-   The platform supports closed-loop extension, enabling automated feedback from activation systems back into the order lifecycle.
-   A shared order structure gives sales and network operations teams consistent visibility across decomposition, assignment, and execution stages.

## Features

|Feature|Description|
|-------|-----------|
|Non-catalog order support|Translates configuration inputs that fall outside the PSR catalog into structured order tasks using intent-based orchestration, without requiring explicit catalog entries for every variant.|
|Catalog-based decomposition|Decomposes customer orders into product orders, service orders, and resource orders based on spec relationships and decomposition rules defined in the PSR catalog.|
|Attribute mapping|Maps attributes from the quote through to order tasks, making the correct data available to southbound APIs during service order orchestration.|
|Dependency sequencing|Supports staggered decomposition based on catalog characteristic values, so dependent order line items activate in the correct sequence without manual coordination.|
|Closed-loop extension|Supports extension for closed-loop orchestration, enabling activation feedback from downstream systems to update order status automatically.|
|TMF standards alignment|Aligns to TM Forum Open APIs — TMF633 \(Service Catalog Management\), TMF620 \(Product Order\), and TMF641 \(Service Order\) — for standards-based integration with third-party systems.|

