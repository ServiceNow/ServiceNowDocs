---
title: Purchase revision roles and responsibilities
description: As a procurement administrator, you can create workflows that blend automation, integration, and human review to process the purchase modification requests raised by shoppers.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Purchase revision flows, Using Shopping Hub, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase revision roles and responsibilities

As a procurement administrator, you can create workflows that blend automation, integration, and human review to process the purchase modification requests raised by shoppers.

Purchase revision workflow involves the steps to route the request through various stakeholders. The following workflow shows how the admin facilitates the purchase modification process to create requests, resolve request, and communicate with stakeholders:

## Administrator

As an admin or process owner, you can facilitate shoppers with a process to raise edit or cancel requests from Service Catalog and ShoppingHub. Define a unified task-view playbook experience for agents to process the approval workflows:

## Shopper

As a shopper, you can raise the edit or cancel requests for the following objects from ShoppingHub or Service Catalog:

-   **Purchase requisition**: A purchase request that tracks all tasks and approvals, and associates the purchase to a contract and supplier. Purchase requisitions contain one or more purchase line items. A purchase order is created from a purchase requisition task.​​
-   **Purchase line**: An individual line item that includes all the details of the goods or services for procurement. Purchase requisitions contain multiple purchase line items.
-   **Purchase order**: A purchase order includes one or more purchase order lines. Once the business unit approves the purchase requisition, a purchase order is issued to the supplier with the requested goods or services.
-   **Purchase order line**: An individual line item that includes all the details of the goods or services for procurement. Purchase orders contain multiple purchase order line items.

## Agent

As an agent or fulfiller or buyer, you can process these requests from the Source-to-Pay Workspace [playbook](process-automation-designer-flows-psm.md):

-   Approve or reject an **Edit** order with the revised quantity or delivery location of the purchase requisitions.
-   Reject or approve a **Cancel** request of the entire order or line items.

## Edit flows

You can use these steps to raise an edit request for purchase line item. The following image explains the process of request creation by shopper and request resolution by buyer or agent.

![Raise an edit request from ShoppingHub](../image/edit-flow.png "Edit request overview")

## Cancel flows

You can use these steps to raise a cancel request for purchase line items or an entire purchase. Here's an overview of the process from request creation and request resolution.

![Raise a cancel request from ShoppingHub](../image/cancel-flow.png "Cancel request overview")

**Parent Topic:**[Purchase revision flows](purchase-revision-flows.md)

