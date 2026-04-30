---
title: Request post-sale change orders
description: Learn how to create orders for disconnecting, suspending, resuming products or services and changing specifications, characteristics, or service location for orders after an initial order has been fulfilled.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-10-14"
reading_time_minutes: 2
breadcrumb: [Managing post-fulfillment order changes, Order Management, Use, Sales Customer Relationship Management]
---

# Request post-sale change orders

Learn how to create orders for disconnecting, suspending, resuming products or services and changing specifications, characteristics, or service location for orders after an initial order has been fulfilled.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent, sn\_ind\_tmt\_orm.service\_order\_agent, or sn\_ind\_tmt\_orm.service\_order\_manager

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to **Customer Orders** &gt; **All** or **Service Orders** &gt; **All** to create a product or service order respectively.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_x1q_jcv_4gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

The customer account for which you want to create an order.

</td></tr><tr><td>

Consumer

</td><td>

The consumer for which you want to create an order.

</td></tr><tr><td>

Order Type

</td><td>

The type or order you want to create. The available options are:-   Product
-   Service


</td></tr><tr><td>

Contact

</td><td>

The name of the contact for the order.

</td></tr><tr><td>

Order action

</td><td>

The available options include:-   Change - For changing product specifications or service location.
-   Disconnect - For disconnecting an active product or service.
-   Suspend - For suspending an active product or service.
-   Resume - For resuming a disconnected or suspended product or service.


</td></tr><tr><td>

Channel partner

</td><td>

\(Optional\) The name of the organization selling a product or service.

</td></tr></tbody>
</table>    **Note:** The fields displayed on the form change depending on whether you select account or consumer.

6.  Select **Create**.

    The product catalog displays your available inventory which includes all the product or services that are ordered by your customer and successfully fulfilled by you.

7.  Select **Manage** for a product inventory item you want to manage.

8.  For changing order quantity, specifications, or characteristics for a product offering, perform the following steps.

    1.  On the Modify order page, review the product configurations and select **Modify**.

    2.  Using the product configurator, select the new product characteristics or specifications or revise quantity.

    3.  Select **Update**.

        Order line items are created with Order line action as Change.

9.  For disconnecting, suspending, or resuming products or services, perform the following steps.

    1.  On the Modify order page, review the details and select one of the following options from the **Modify** drop-down menu.

        |Option|Description|
        |------|-----------|
        |Disconnect|Disconnect an active or suspended product or service.|
        |Suspend|Suspend an active product or service.|
        |Resume|Resume a suspended product or service.|

    2.  Enter suspension start and end dates for suspend requests and select **Suspend**.

        If you do not specify a date, the suspension is effective immediately. For more information, see [Suspend and resume products and services](../concept/order-mgt-suspend-resume-action.md).

10. Review the order lines by selecting the **Order Line Items** tab.

11. Verify the order details by selecting **Review &amp; Submit**.

12. Select **Submit** to place the order.

    The order state changes to New and is available for approval.


**Parent Topic:**[Managing post-fulfillment order changes](../concept/managing-orders.md)

**Related topics**  


[Suspend and resume products and services](../concept/order-mgt-suspend-resume-action.md)

