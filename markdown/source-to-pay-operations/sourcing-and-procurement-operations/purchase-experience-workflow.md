---
title: Sourcing and Purchasing Automation
description: Sourcing and Purchasing Automation for ShoppingHub includes workflows that help support the user interface purchasing experience for the shopper. These workflows consist of sourcing requests, negotiations, purchase requisitions, contracts, purchase orders, receipts, and invoices.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Purchasing Automation

Sourcing and Purchasing Automation for ShoppingHub includes workflows that help support the user interface purchasing experience for the shopper. These workflows consist of sourcing requests, negotiations, purchase requisitions, contracts, purchase orders, receipts, and invoices.

**Important:** Check your entitlements to determine whether you have access to Sourcing and Purchasing Automation.

-   **[Sourcing request](sourcing-request.md)**  
A sourcing request is created for when an item that a shopper, employee, or requester needs, must be sourced. This record is created when an active contractual price for the product that the shopper intends to purchase doesn’t exist. This includes items in both the product catalog and off-catalog.
-   **[Negotiations](negotiations.md)**  
A negotiation represents individual supplier negotiations and tracks the items and activities according to supplier. These activities involve obtaining the price for the products or services requested by the shopper, or negotiating the terms.
-   **[Sourcing events](negotiation-events.md)**  
Sourcing events represent the type of sourcing activity needed to negotiate with each supplier, and track the individual negotiations with each supplier. They help sourcing managers manage multi-supplier and multi-product negotiations.
-   **[Purchase requisition](purchase-requisition.md)**  
A purchase requisition represents a request that is sent internally within an organization to obtain purchased goods or services. It consists of items that need to be ordered, and may need to go through approvals for a purchase order to be created.
-   **[Purchase lines](purchase-lines.md)**  
Purchase lines provide information of the individual lines under a purchase requisition or a sourcing request for the referenced supplier.
-   **[Purchase requisition merging](../concept/purchase-requisition-merging.md)**  
Purchase requisitions can be merged if certain criteria are met. This avoids multiple purchase orders from being created unnecessarily and also helps enforce approval rule limits.
-   **[Purchasing tasks and procurement cases](purchasing-tasks.md)**  
All automated purchasing tasks and procurement cases are created using flow designer from the Service Delivery Common \(SDC\) application. The flow designer uses the underlying task and case generation decision tables, and purchasing tasks and procurement cases are created based on the conditions defined in the decision tables.
-   **[Purchase order](purchase-order.md)**  
A purchase order is a binding contract between a buyer and a supplier that authorizes a purchasing transaction. It contains the descriptions, quantities, prices, applicable discounts, payment terms, delivery dates, and other associated terms and conditions with the supplier.
-   **[Blanket purchase order workflow](blanket-purchase-order-workflow.md)**  
During checkout, when a shopper selects **I am not sure** in the delivery date option, it creates a purchase requisition with a blanket order type, which results in the creation of a blanket purchase order.
-   **[Purchase revisions](purchase-revisions.md)**  
Revisions for the quantity of the product, budget, or delivery location can be made to orders placed from ShoppingHub.
-   **[Contracts](contracts.md)**  
A contract defines the terms and conditions along with pricing agreed for a product with the supplier​. An active contractual price determines if the pricing of a product or service is displayed on ShoppingHub.
-   **[Pricing](pricing.md)**  
Pricing stores the relationship between supplier product, contracts, and price of a product.
-   **[Receipt tasks](receipt-tasks.md)**  
Receipt tasks are created when goods receipt is required for the purchase line.
-   **[Receipts](receipts.md)**  
Receipts reference a purchase order line. Depending on the product type of the purchase, a goods receipt or services receipt is generated.
-   **[Shipment details](shipment-details.md)**  
Shipment details display tracking information of a product that is shipped to the employee shopper.
-   **[Invoice tasks](invoice-tasks.md)**  
Invoice tasks, an extension of acknowledgment tasks, lists invoice tasks in the Open, Work in Progress, and Closed Rejected status.
-   **[Invoices](invoices.md)**  
Invoices are generated for a payment against a purchase order. A purchase order can have multiple invoices depending on the payment schedule.
-   **[Create an approval rule](../task/create-approval-rule.md)**  
Approve a purchase requisition, purchase order, sourcing request, or invoice, by defining an approval strategy and creating approval rules. This is a one-place configuration that can drive any kind of approval process that your organization may need.
-   **[Monitor an approval plan](../task/work-with-approval-plan.md)**  
During evaluation, the approval engine converts each approval rule into one or multiple approval plans. You can monitor approval plans to understand how the overall approval process is being executed, the routing and decision methods, the list of approvers involved, the status on the approvals, the list of purchase lines the approval is planned for, and so on.
-   **[Approvals reassessment](approvals-reassessment.md)**  
Review the conditions for approvals reassessment and their impact on purchase automation.
-   **[Create a purchasing assignment rule](../task/create-purchasing-assignment-rule.md)**  
Automatically assign a sourcing request, negotiation, or purchase requisition to a procurement specialist user or a task fulfiller’s group based on pre-defined conditions by using a purchasing assignment rule.
-   **[Define a capitalization policy](../task/define-capitalization-policy.md)**  
Create fixed asset shells automatically during purchase order creation, by defining a capitalization policy.
-   **[Fixed asset creation](../concept/fixed-asset-creation.md)**  
As a procurement administrator, you can create fixed assets for products that are purchased for long-term use and are not likely to be converted quickly into cash.
-   **[Inventory asset creation](../concept/inventory-asset-creation.md)**  
Inventory assets are not created upfront when fixed assets are created.
-   **[Shipping cost calculations](shipping-cost-calculations.md)**  
A framework to integrate shipping cost calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.
-   **[Tax calculations](tax-calculations.md)**  
A framework to integrate tax calculations into Sourcing and Purchasing Automation is implemented such that approvals can be done on the full value of purchases.

**Parent Topic:**[Explore Sourcing and Procurement Operations](../concept/exploring-spo.md)

**Related topics**  


[My purchases on Shopping Hub](../concept/my-purchases.md)

[Shopping Hub Mobile](../concept/shoppinghub-mobile.md)

[Performance Analytics for Sourcing and Procurement Operations](../concept/performance-analytics-for-spo.md)

[Procurement Case Management](../concept/psd-overview.md)

[Source-to-Pay Workspace](../concept/procurement-specialist-workspace.md)

[Spend and Savings Management](../concept/spo-spend-mgmt.md)

[Sourcing Pipeline Management](../concept/spo-sourcing-pipeline-mgmt.md)

[Understanding Punchout](../concept/punchout-overview.md)

[AI Search for Sourcing and Procurement Operations](../concept/ai-search-sourcing-procurement-operations.md)

[Install Sourcing and Procurement Operations](../task/activate-finance-spend-central.md)

[Application plugin installation sequence in Sourcing and Procurement Operations](application-plugin-list.md)

