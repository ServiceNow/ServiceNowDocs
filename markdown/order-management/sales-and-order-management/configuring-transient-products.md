---
title: Defining transient products
description: When you create product offerings and technical specifications, you can identify single-use products and services as transient, to differentiate them from persistent products. Examples of one-time use products include installation or consulting services.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create product offerings, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Defining transient products

When you create product offerings and technical specifications, you can identify single-use products and services as transient, to differentiate them from persistent products. Examples of one-time use products include installation or consulting services.

When new orders with transient products are submitted for fulfillment in ServiceNow® Order Management, the sold product or product inventory records are created with an Installation pending state. After new orders with transient products are fulfilled, the sold product or product inventory state changes to Inactive. Your fulfillment managers can then quickly see which products aren’t part of the active inventory. Agents can’t perform Move, Add, Change, Delete \(MACD\) actions on inactive sold product or product inventory records.

## Guidelines for defining transient products

When you’re defining product offerings, use the **Transient** option in the Create New Product Offering form to identify a transient product. If the product has associated technical specifications, you also set the **Transient** option in the appropriate Product, Service, and Resource Specification forms.

When defining transient products, note the following restrictions:

-   Create New Product Offering form: The **Transient** option and the **Create contract** option can't be enabled at the same time for the product.
-   Parent and child product offerings: Transient parent product offerings and parent specifications must have transient child product offerings and child specifications. However, non-transient parent product offerings and parent specifications can have transient child product offerings and child product specifications.
-   Linking product offerings to product specifications: A transient product offering must be linked to a transient product specification and vice versa.
-   Specification relationships: When defining specification relationships for a transient product, you can associate only a transient service specification or resource specification. Transient product orders are decomposed as indicated in the associated specification.

For details on setting the **Transient** option for product offerings and specifications, see the following sections:

-   [Create product offerings](../task/som-create-product-offering.md)
-   
-   Create and publish service specifications
-   

