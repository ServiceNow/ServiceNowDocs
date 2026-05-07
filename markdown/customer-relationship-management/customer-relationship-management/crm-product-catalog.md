---
title: Product catalog
description: A product catalog defines the products and services that your organization sells and supports.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 2
---

# Product catalog

A product catalog defines the products and services that your organization sells and supports.

## Product catalog overview

The product catalog connects what your organization offers to the records that track what customers have purchased and the requests they can make. It is structured around product models like the types of goods and services your organization offers.

## Catalog structure

The catalog is organized in three layers that connect what an organization offers to what customers can request.

-   **Product models:** Define the types of goods and services your organization sells and supports. Product models are the foundational entries in the catalog and everything else references them.
-   **Service offerings:** Associated with product models to represent specific support tiers available to customers. Service offerings flow through to sold product records, giving agents visibility into a customer's entitlements when a case is opened.
-   **Catalog items:** The requestable entries that customers and agents interact with. Catalog items are linked to product models through product-to-catalog item relationships, allowing customers to raise service requests directly from the products they own.

## Catalog connections across CRM

Product models in the catalog are referenced by sold products. When a product is sold, the sold product record points back to the catalog entry that defines it. Service offerings associated with a product model flow through to sold product records, giving agents visibility into a customer's entitlements when a case is opened.

In a Sales CRM context, the product catalog also underpins CPQ. The product definitions, pricing tiers, and bundling rules that CPQ enforces at the quoting stage are built on the same catalog foundation, ensuring consistency between what is sold and what is supported.

## Product catalog across CRM and Industries

The product catalog is a shared resource across the CRM portfolio and its industry solutions. Because all CRM products reference the same catalog, what is defined once is available consistently across selling, fulfillment, and service.

|Product|How the catalog works|
|-------|---------------------|
|CSM|Agents use catalog items to raise service requests on behalf of customers. Knowledge bases and service offerings in the catalog can be configured with product entitlements so that customers and agents see only the items relevant to what has been purchased.|
|Sales CRM and CPQ|The product catalog is the foundation for quoting and ordering. CPQ enforces product definitions, pricing tiers, and bundling rules defined in the catalog at the quoting stage. When an order is placed, the sold product record references the catalog entry that defined it.|
|Self-service portals|Customers interacting with the Customer Service Portal can view their purchased products and raise service requests directly from the catalog items associated with those products, without agent involvement.|
|Industry solutions|Industry solutions extend the product catalog with vertical-specific product models and service offerings. Telecommunications organizations use the catalog to define network services and bundles. Manufacturers define equipment and warranty offerings. Financial services organizations define financial products available for self-service requests.|

