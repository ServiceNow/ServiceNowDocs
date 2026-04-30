---
title: Managing inflight order changes and cancellation requests
description: Manage how your organization receives changes for customer orders, service orders or individual line items that are still being orchestrated and fulfilled. By using inflight change order management, you can designate when you permit such changes. You can also assess the impact of the requested changes for an order or order line item, and automatically generate a plan to compensate for them when you approve the revision or cancellation request.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Managing inflight order changes and cancellation requests

Manage how your organization receives changes for customer orders, service orders or individual line items that are still being orchestrated and fulfilled. By using inflight change order management, you can designate when you permit such changes. You can also assess the impact of the requested changes for an order or order line item, and automatically generate a plan to compensate for them when you approve the revision or cancellation request.

## Overview

An inflight order is an order that is in the process of being orchestrated and fulfilled but has some work pending. Inflight changes and cancellations can occur in large enterprise orders. An inflight order change refers to a change that is issued for an order line item that is currently undergoing fulfillment and pending completion.

Enterprise telecommunications order management is complex. It can take weeks or months to fulfill a multi-site order. Enterprise orders can involve the large-scale purchases of products and services, often for multiple locations around the world. Inflight orders can go through revisions that incorporate changes that are submitted by customers or identified by internal personnel during the order fulfillment process.

To revise an inflight order or order line items that have already been decomposed to suborders, service provider employees have to assess the impact of the requested changes. If there is no data-driven process and framework, users try to manage the changes with manual tasks that can lead to delays in the order delivery process and result in poor customer and employee experiences.

## Types of Inflight order changes

Order change requests typically originate from your customers for purchased products and services or from internal personnel, such as order fulfillment agents, when they are managing their fulfillment. When you submit an inflight order revision, you assign a change type to track the types of order changes that are submitted by users. The ServiceNow AI Platform supports Characteristic, Contact, Quantity, related items, and Price change types.

Customer-initiated requests

Based on the types of customer requests, you update an inflight order to do the actions that are listed in the following table.

|Type of change|Example|
|--------------|-------|
|Incorporate changes that are related to contact details. These changes can include an update, deletion, or addition of contact information for an order line item for a product or service in a location.|A customer supplies a new email address or the name and telephone number of a new corporate contact.|
|Incorporate changes that are related to pricing details.|A customer requests a reduction to a non-recurring charge or a monthly recurring charge on an order line item.|
|Add a product or service to an order.|A customer wants to add a new item to an existing order.|
|Increase or decrease the quantity of order line items in a product or service order.|A customer wants a higher or lower the quantity of an existing order.|
|Add, change, or cancel a product or service, or product or service options, in a related domain product or service order.|A customer wants to update the characteristic value of a product or service that the customer ordered at an earlier date. For example, the customer wants to change the speed of an internet service from 100 Mbps to 500 Mbps.|
|Incorporate changes that are applicable to the related items of a product or service order.|A customer wants to add or change an item to an order that has horizontal relationships. To learn more, see [Defining a horizontal relationship](horizontal-relationships.md).|

Fulfillment user-initiated requests

To expedite the completion of the order fulfillment process, the order fulfillment or service order agents and managers often request changes to product, service, or resource orders. Based on the types of internal requests, you update an inflight order to do the actions listed in the following table.

|Type of change|Example|
|--------------|-------|
|Incorporate changes that are related to contact details. These changes can include an update, deletion, or addition of contact information for an order line item for a product or service in a location.|A customer supplies information about a new corporate contact person on a pending delivery of an enterprise order.|
|Add, change, or cancel a product, including product options, in a related domain product order.|A customer orders a modem that is incompatible with the higher-speed 500-Mbps internet service that the customer ordered. It requires replacement by another modem model.|
|Add, change, or cancel the service domain orders and product inventory.|A customer wants to change the characteristics value of a product or service. For example, the customers wants to change the Firewall Security Service from Standard to Basic.|
|Add, change, or cancel a service, including service options, in a related domain service order.|A customer wants to change the standard warranty of 90 days to an extended service policy.|
|Add, change, or cancel a resource, including resource options, in a related domain resource order.|Revised installation instructions are available for a product that the customer ordered.|
|Incorporate changes that are applicable to the related items and product inventory of a product or service order. To learn more, see  and .|A customer wants to add or change an item to an order that has horizontal relationships. To learn more, see [Defining a horizontal relationship](horizontal-relationships.md).|

## Inflight Order Change processing

When a user or order fulfillment manager attempts to make any of these changes, the Inflight Change Order function proceeds through a structured processing sequence as shown in the following diagram.

![Infographic displaying the scenario and approach of Inflight order change high-level processing. For the text description, refer to the steps that follow.](../image/Inflight-order-change-high-level-approach.png "Inflight order change high-level approach")

The sequence for inflight change order processing is as follows:

1.  The Inflight Change Order function determines where in the processing cycle the order is. You can only create inflight order revision and cancellation requests for orders that are in an In Progress state.
2.  The ServiceNow AI Platform then determines whether the proposed revision can safely be made to the in-progress order. It evaluates the Point of No Return \(PONR\) status for the order and its current stage in the fulfillment process.

    The PONR flag represents the no or go point at which you can't change an order:

    -   You can make an inflight change only for order line items with an In Progress state.
    -   You can't make inflight changes for an order that has already been decomposed into its domain product, service, or resource orders, and product installation has already started.
    **Note:** You can find the **PONR** option when you are viewing or maintaining customer or service orders in the Customer Order and Order Line Item forms. To learn more, see:

    -    and
    -   
3.  After an operator makes the requested changes, this functionality evaluates the type of change and its magnitude and impact on the fulfillment process as follows:
    -   Simple informational changes, such as contact data, may or may not impact the fulfillment as configured in the orchestration plan.
    -   If the customer requests to delete an ordered product or service, the impact of the changes, if permitted, would be greater, depending on its progress in the order fulfillment process.
4.  The ServiceNow AI Platform then creates a compensation plan to trigger the tasks to fulfill the revised scope of the order as follows:
    -   The compensation plan creates the automated revisions that are required to the fulfillment workflow to adjust to the requested order changes.
    -   If the customer adds products or services to the order, the compensation plan generates additional order tasks to handle the fulfillment of the newly ordered items.
    -   For a product substitution, the compensation plan generates an undo task to release the old product or service and a redo task for assignment of the new product or service. After the old product has been released, it can be sold to another customer.
    -   For a product characteristic change, the compensation plan undoes some tasks to revert the work that is not applicable for a new characteristic value or option. The compensation plan can also include a few tasks that are required for some of the completed tasks. There could also be a few existing tasks that are unaffected by the revisions that were submitted as part of the order revision.
5.  A manager can then track the revised workflow. By using the Inflight Order Change functions, your organization can gain the following benefits:
    -   Reduced manual intervention that is required to manage an inflight change order.
    -   Reduced time to create a revised plan for a change, which results in faster order fulfillment cycles.

## Inflight order change example

The following diagram shows the process where PONR occurs for order changes that were made for an SD-WAN Service Package and its related products.

![Infographic showing the workflow of SD-WAN service package inflight order changes. For text description, refer to the Inflight order change example section that follows.](../image/inflight-sd-wan-order.png "SD-WAN Service Package inflight change orders")

For the top-level SD-WAN Service package, the PONR only occurs before the testing and turn up stage. A customer or internal fulfillment personnel can't change the ordered item after that point.

For subordinate products, such as the SD-WAN Edge device, the order can be changed before the Customer Premise Equipment \(CPE\) configuration completes. If CPE delivery is initiated but doesn't complete, and a product substitution is requested, the Inflight Change Order function can do the following actions:

-   Generate an undo task for the original item.
-   Generate a redo task for the replacement item.
-   Create undo and redo tasks for the Prepare and build CPE configuration and Allocate and Assign CPE tasks that are completed before revision. The Inflight Change Order function can generate these undo and redo tasks because the CPE delivery task is not complete for the replacement item.

After the CPE configuration is complete, no further changes are allowed in the order for that device. This scenario also applies to the SD-WAN Controller and SD-WAN Security selections.

-   **[Key inflight order change and cancellation request fields](key-inflight-order-change-cancellation-request-fields.md#)**  
Learn how the ServiceNow AI Platform uses key fields in the Customer Order and Order Line Item forms to track your order changes and cancellation requests. You can see how these fields operate and what information they show you when you revise or request a cancellation of an order, or order line items.
-   **[Revise an inflight order or request a cancellation](../task/revise-inflight-order-request-cancellation.md)**  
Revise an inflight order, or order line item, or request a cancellation of a customer order or a service order when a user requests it or your internal personnel determine an order revision or cancellation is necessary.
-   **[Review and approve order revisions or cancellation requests](../task/review-and-approve-or-decline-order-cancellation-requests.md)**  
Review a customer or service order that has a pending revision or cancellation request so that you can make sure that the order is correct and complete. You can also approve the order and order line item revisions or cancellations requests.

**Parent Topic:**[Using Order Management](reviewing-approving-fulfilling-orders.md)

