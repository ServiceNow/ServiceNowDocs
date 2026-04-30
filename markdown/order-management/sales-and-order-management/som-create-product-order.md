---
title: Create an order in Order Management
description: Create a product or service order in Order Management.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Order Management, Using Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create an order in Order Management

Create a product or service order in Order Management.

## Before you begin

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

When you start an order, a pop-up prompts you for order information. You can choose to create a product order for a customer account or consumer. The pop-up changes depending on your choice.

-   Account – The order is created for an existing customer account.
-   Consumer – The order is created for an existing consumer.

**Note:** The following steps explain how to create a customer order. Whether you’re creating a customer order or a service order, the steps are the same.

## Procedure

1.  In the **Configurable Workspace**, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Customer Orders** &gt; **All** and select **New**.

    The **Create a new Order** pop-up opens.

    ![](../image/som-om-new-order-interceptor.png)

3.  In the **Create a new Order** pop-up, fill in the fields.

    -   To create an order for an account, select the **Account**.
    -   To create an order for a consumer, select the **Consumer** name.
<table id="choicetable_wss_lcm_11c"><thead><tr><th align="left" id="d35556e142">

To

</th><th align="left" id="d35556e145">

Description

</th></tr></thead><tbody><tr><td id="d35556e151">

**Create an order for an account**

</td><td>

Enter the following:-   Order Type: Order type can be service or customer.
-   Contact: Name of the primary customer contact.
-   Order action: Select the type of order action.


</td></tr><tr><td id="d35556e171">

**Create an order for a consumer**

</td><td>

Enter the following:-   Order Type: Order type can be service or customer.
-   Order action: Select the type of order action.


</td></tr></tbody>
</table>4.  In **Order action**, select **Add**.

    The **Order action** menu contains the following options.

    |Order Action|Description|
    |------------|-----------|
    |Add|Creates an order.|
    |Move|M|
    |Change|Creates a change order.|

5.  Select **Create**.

    The order is started and the **Order Catalog** opens.


-   **[Add products or services to an order in Order Management](som-add-products-services-to-orders.md)**  
Once an order is started, add order lines for products or services using the product catalog and product configurator in Order Management.
-   **[Add a sales agreement to an order in Order Management](som-add-sales-agreement-to-order.md)**  
Add a sales agreement to your order. A sales agreement is a contract to order a pre-identified set of products and services for a set price.
-   **[Set up and review product order lines in Order Management](som-om-setup-product-order-lines.md)**  
Once products and services are added to an order in Order Management, you can set up order lines with order characteristics, pricing adjustments, and other items.
-   **[Review and submit a product or service order in Order Management](som-om-review-and-submit-product-order.md)**  
After adding products and services to your order, review the order line items and submit the order for approval.
-   **[Approve a product or service order in Order Management](som-om-approve-product-order.md)**  
When an order is submitted, the next step is to review the order and approve it. Approved orders are ready to begin the fulfillment process in Order Management.
-   **[Updating specification versions](../concept/som-specification-version-update.md)**  
Enterprises frequently create and update new versions of product and service specifications. When these changes occur, it's important to update the existing product specification in ServiceNow®. Failure to update the product specifications can lead to difficulties with MACD \(Move, Add, Change, Delete\) operation when orders enter fulfillment.
-   **[Add covered products to order line items](som-update-covered-products.md)**  
Enhance orders by adding covered products such as contracts or entitlements at the order line level.
-   **[Update product locations at the order line level](order-mgt-copy-order-line-location.md)**  
Agents can use the copy function to update product locations at the order line level Order Management.
-   **[Filter product catalog by location](order-mgt-filter-catalog-by-location.md)**  
Agents can filter products in the catalog by using the location function in Order Management. The location filter helps agents be more efficient when creating orders.

**Parent Topic:**[Using Order Management](../concept/reviewing-approving-fulfilling-orders.md)

**Related topics**  


[Add products or services to an order in Order Management](som-add-products-services-to-orders.md)

