---
title: Shopping Hub
description: Shopping Hub \(sn\_spend\_uib\) is a self-service procurement portal that employees use to purchase products and services. It supports browsing internal catalog items and supplier catalogs, submitting purchase requests, and tracking orders from checkout through fulfillment.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 4
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Shopping Hub

Shopping Hub \(sn\_spend\_uib\) is a self-service procurement portal that employees use to purchase products and services. It supports browsing internal catalog items and supplier catalogs, submitting purchase requests, and tracking orders from checkout through fulfillment.

Shopping Hub is part of the Sourcing and Procurement Operations \(SPO\) application and runs on the Next Experience UI Framework.

## Key capabilities

The following table describes the primary capability areas available in Shopping Hub.

|Capability|Description|
|----------|-----------|
|Product discovery|Browse supplier catalogs by category or by supplier. Search using full-text queries. Access recently viewed products and role-based product suggestions.|
|Shopping cart|Add individual products or bundles to a cart, adjust quantities, save carts for later, and review cart contents before checkout.|
|Checkout|Select delivery location, delivery date, shipping method, payment method, cost center, and purchase reason during the checkout process. An express checkout path is available for faster submission.|
|Purchase management|View purchase history across purchase orders and requisitions. Track order status, request purchase modifications, and reorder from previous purchases using the Buy Again option.|
|Task and approval management|Complete workflow tasks from the My Tasks view, including approvals, supplier selection, receipt confirmation, service acknowledgment, document upload, milestone confirmation, and post-purchase clarifications.|
|Sourcing requests|View supplier quotes for a sourcing request, compare pricing across multiple suppliers, and select a supplier to fulfill the request.|
|Punchout integration|Access external supplier catalogs through punchout connections using the cXML protocol. Products from punchout catalogs follow a separate detail and checkout flow.|
|Credits|Apply available procurement or corporate credits toward purchases at checkout.|
|Multi-currency display|View product pricing in both the supplier currency and the local currency.|
|On-behalf purchasing|Submit purchases on behalf of other employees when you have the required permissions. Permission controls restrict this capability to authorized users.|

## Shopper workflow

A typical purchase in Shopping Hub begins with product discovery. You can browse the catalog by category or by supplier, or enter search terms to locate a specific product or service. Selecting a product opens its detail page, where pricing, availability, supplier information, and product attributes are available for review.

After adding products to the cart, you proceed to checkout to specify delivery details, a payment method, and a cost center. The full checkout flow supports per-product delivery date and location customization. After submitting the purchase, the portal creates a purchase order or requisition depending on the procurement configuration.

You monitor purchase status in **My Purchases**. If the procurement workflow generates tasks, such as approval actions, receipt confirmations, or supplier selections, those tasks appear in **My Tasks** for you to complete. For frequently purchased items, the **Buy Again** option in **My Purchases** shortens the process by pre-populating cart and checkout details from a previous order.

## Roles and access

Access to Shopping Hub is controlled by the following predefined roles.

|Role|Description|
|----|-----------|
|`sn_shop.shopper`|Can browse catalogs, manage carts, check out, track purchases, and complete workflow tasks.|
|`sn_shop.shopping_hub_admin`|Can configure and manage Shopping Hub settings.|

**Parent Topic:**[Explore Sourcing and Procurement Operations](exploring-spo.md)

**Related topics**  


[My purchases on Shopping Hub](my-purchases.md)

[Shopping Hub Mobile](shoppinghub-mobile.md)

[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

[Procurement Case Management](psd-overview.md)

[Source-to-Pay Workspace](procurement-specialist-workspace.md)

[Spend and Savings Management](spo-spend-mgmt.md)

[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

[Understanding Punchout](punchout-overview.md)

[AI Search for Sourcing and Procurement Operations](ai-search-sourcing-procurement-operations.md)

