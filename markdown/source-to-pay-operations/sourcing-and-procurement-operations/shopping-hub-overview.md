---
title: Shopping Hub
description: Shopping Hub \(sn\_spend\_uib\) is a self-service procurement portal that employees use to purchase products and services. It supports browsing internal catalog items and supplier catalogs, submitting purchase requests, and tracking orders from checkout through fulfillment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/shopping-hub-overview.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 6
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

-   **[My purchases on Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/my-purchases.md)**  
As a shopper, you can view all the purchases made from your shopping account by selecting My purchases from your Shopping Hub profile.
-   **[Process visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/process-visibility.md)**  
You can track the complete procurement process post request submission. The process steps and work items can be configured to meet your business requirements.
-   **[Purchase refinement options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-refinement-options.md)**  
You can refine your purchases through filtering, sorting, searching, and perform actions from the My purchases landing page.
-   **[Purchase state indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-highlights.md)**  
Your purchases, which include purchase requisitions, purchase requisition lines, purchase orders, purchase order lines, and sourcing requests, are highlighted with color coding to help you quickly understand their state and due date. The progress bar on these purchases follows a similar color coding.
-   **[Activity stream](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activity-stream.md)**  
Track the updates on a selected purchase by navigating to the **Activity** tab. The activity stream shows the progress that your order has made since the time you placed it.
-   **[My to-dos and purchasing to-dos](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/my-todos-purchasing-todos.md)**  
As a shopper, you can review to-dos from the **To-dos** tab.
-   **[My requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/my-requests.md)**  
As a shopper, you can view all the order revisions from your shopping account anytime by selecting My requests from your profile in Shopping Hub.
-   **[Multi-currency support in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/sh-multicurrency-overview.md)**  
Shoppers can view and select their local currency during shopping in Shopping Hub, providing a seamless multi-currency experience.
-   **[Purchase requisition line-level questions in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/prl-question-shoppinghub.md)**  
Line-level questions let procurement admins capture product-specific information during checkout, improving data accuracy and enabling flexible purchase requisition workflows.
-   **[Purchase on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-on-behalf-sh.md)**  
Shoppers can purchase products and services on behalf of another user in Shopping Hub. When purchasing on behalf of another user, shoppers can also view the carts and purchases associated with that user. A shopper who is authorized to purchase on behalf of other users is referred to as a super shopper.
-   **[Decimal quantity support for service-based purchases in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/decimal-support-services.md)**  
As a shopper, you can now specify decimal quantity values for service-based products when you create or edit a purchase requisition \(PR\) or purchase order \(PO\) in Shopping Hub.

**Parent Topic:**[Explore Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/exploring-spo.md)

**Related topics**  


[Shopping Hub Mobile]()

[Performance Analytics for Sourcing and Procurement Operations]()

[Sourcing and Purchasing Automation]()

[Procurement Case Management]()

[Source-to-Pay Workspace]()

[Spend and Savings Management]()

[Sourcing Pipeline Management]()

[Understanding Punchout]()

[AI Search for Sourcing and Procurement Operations]()

[Universal Request in Sourcing and Procurement Operations]()

