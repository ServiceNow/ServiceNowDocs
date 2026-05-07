---
title: Sales CRM for Telecommunications PSR catalog
description: The Sales CRM for Telecommunications Product, Service, and Resource \(PSR\) catalog is a unified catalog that defines all required entities in a single location, based on the TM Forum \(TMF\) Shared Information and Data \(SID\) model.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 2
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Sales CRM for Telecommunications PSR catalog

The Sales CRM for Telecommunications Product, Service, and Resource \(PSR\) catalog is a unified catalog that defines all required entities in a single location, based on the TM Forum \(TMF\) Shared Information and Data \(SID\) model.

The Sales CRM for Telecommunications PSR catalog consolidates product, service, and resource definitions into a single catalog structure, eliminating the need for product data synchronization between separate sales and fulfillment catalogs. It provides a consistent framework for managing telecom product offerings across multiple domains like B2C Retail Mobile, B2C Retail Wireline, B2B Enterprise Connectivity, and Beyond Connectivity. The following table contains examples of Mobile, Broadband and Dedicated leased lines.

Because the catalog defines and maps all necessary entities in one place, you don't need explicit entity-to-entity API mapping or separate product data harmonization across sales and service catalogs.

![Sales CRM for Telecommunications PSR catalog](../image/somt-psr-catalog.jpg)

## PSR catalog hierarchy

Each level in the catalog maps to a specific layer of the product-service-resource model:

-   Product offering: Defines the item to be sold to a customer. Pricing attributes include recurring charges \(RC\), one-time charges \(OTC\), ramp-up pricing, mark-up and mark-down percentages, and discounts. A product offering references a product specification which in turn can have child product specifications.
-   Product specification: The structured definition of a product. One product specification maps to exactly one service specification and can reference one or more resource specifications.
-   Service specification: Defines the service layer. Service specifications are of two types:
    -   CFSS: Represents the service provided to the customer, for example, Voice and Text CFSS or home fiber FTTH Access CFSS.
    -   RFSS: Represents the underlying network resource services that are used to deliver service to the customer, for example, Home Subscriber Server \(HSS\), RFSS or Optical Line Terminal \(OLT\) RFSS.
-   Resource specification: Defines the physical or logical network resources that fulfill the service, for example, IMSI or Modem RS.

## Commercial features

The PSR catalog supports the following commercial capabilities:

-   Product bundling and hierarchy: Supports product offer grouping, product offer-to-product specification definitions, and product specification hierarchies with relationships between specifications.
-   Product offer pricing rules: Supports multiple pricing rule types, including recurring charges, one-time charges, ramp-up pricing, mark-up pricing, mark-down pricing, contract-based pricing, and characteristic value-based pricing.
-   Multidimensional rules and relationships: Supports product offer-to-product offer relationships, product offer-to-product specification relationships, specification-level relationships, characteristic value-based rules, and context-based rules such as location and customer type.

## Fulfillment features

The PSR catalog supports the following order fulfillment capabilities:

-   Catalog-based decomposition: Decomposes a customer order into order line items based on product offerings and product specifications. Order line items are further decomposed into child or domain orders, such as product orders, service orders, and resource orders.
-   Quote data carry-over into orchestration: Maps attributes from the quote through to order tasks, making the correct data available to southbound APIs during service order orchestration.
-   Orchestration dependencies: Supports staggered decomposition based on catalog characteristic values and decomposition rules. This eliminates complex workflow rules when order line items have dependencies on each other.

