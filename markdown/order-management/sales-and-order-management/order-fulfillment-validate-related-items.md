---
title: Validate the related items of a customer order for its compatibility
description: Validate the related order line items of your customer order, which includes the horizontal specification relationships, to make sure that the order-related information is correctly generated to fulfill your customer order.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-13"
reading_time_minutes: 2
breadcrumb: [Approving orders, Order Management, Use, Sales Customer Relationship Management]
---

# Validate the related items of a customer order for its compatibility

Validate the related order line items of your customer order, which includes the horizontal specification relationships, to make sure that the order-related information is correctly generated to fulfill your customer order.

## Before you begin

A horizontal specification relationship is defined by defining a compatibility rule between the product, service, or resource specifications in a product catalog.

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order-fulfillment\_agent, or sn\_ind\_tmt\_orm.order\_fulfillment\_manager

## About this task

After you define a compatibility rule, when you capture a customer order, you can validate the order related items before you approve the order. For this validation, you review the specification relationships of the order line items and the order input data of your customer when you created the order.

Validations occur at two levels:

1.  Validations before the order approval. If these validations fail, the order decomposition process doesn't stop. The following validations take place:
    -   Source specification and source specification configuration
    -   Compatibles validation
    -   Compatibles quantity validation
2.  Validation at the time that a domain order is closed. If this validation fails, the order fulfillment process stops. The following validations take place:
    -   Source specification and source specification configuration
    -   Compatibles validation
    -   Compatibles quantity validation
    -   Compatibles configuration

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select the order that you want to validate.

5.  To validate the related items of the customer order, select the more actions icon ![](../image/more-options.png) and select **Validate Related Items**.

<table id="choicetable_xbn_3v1_c5b"><tbody><tr><td id="d97916e160">

**If the validation is successful**

</td><td>

The ServiceNow AI Platform displays the following message:Provided related inventory/order line items are compatible.

This message confirms that the order information doesn't require any additional input and you can proceed to the next steps of the order fulfillment.

</td></tr><tr><td id="d97916e175">

**If the validation is unsuccessful**

</td><td>

The ServiceNow AI Platform displays a message that confirms whether the order information requires additional details for its decomposition. You can provide the required information to proceed for the next process of the order fulfillment.

</td></tr></tbody>
</table>    **Note:** For change and disconnect type of customer orders, the following message is displayed for the validation of the related items of the customer order: `This validation is not applicable for order line items with change or disconnect action.`


## What to do next

[Approve orders in Order Management](som-om-approve-product-order.md)

**Note:** Upon approving for the change and disconnect type of order requests with horizontal relationships, the ServiceNow system analyzes its impact on the product inventory relationships and displays a message if it invalidates the existing relationships due to the impact of the requested change by the customer.

