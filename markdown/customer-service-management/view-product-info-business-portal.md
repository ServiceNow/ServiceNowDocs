---
title: View product information from Business Portal
description: View a list of products to track the products or services sold to your account and manage your services using service catalogs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Business Portal, Customer communication, Use, Customer Service Management]
---

# View product information from Business Portal

View a list of products to track the products or services sold to your account and manage your services using service catalogs.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.customer\_admin, sn\_customerservice.partner, or sn\_customerservice.partner\_admin

## About this task

You can view a list of products or services that have been sold to your account. You can also view any cases created on the product and all active contracts and entitlements for the product.

An entitlement is active if:

-   Its end date isn’t in the past or it has no end date.
-   The contract it’s linked to is also active.

A contract is active if:

-   Its state is set to active
-   It’s linked to a product with an active entitlement.

You can modify the **Active Entitlements** widget to define your own filters for active entitlements.

If product catalog items have been set up in your instance, you can use the **Service Catalogs** widget to view context-sensitive service catalogs based on the services you’re subscribed to. Extend your services using service catalogs and request additional items on the services that you have subscribed to.

## Procedure

1.  Navigate to the business portal.

2.  Select **My hub** &gt; **Manage sold products** in the header menu.

    The system displays a list of products or services sold to your account.

    You can only view sold products and all extensions of sold products that are not product inventories.

3.  On the form, fill in the fields.

<table id="table_b1t_22y_1fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the sold product.

</td></tr><tr><td>

Name

</td><td>

Name of the sold product.

</td></tr><tr><td>

Parent sold product

</td><td>

Parent of the sold product, if applicable.

</td></tr><tr><td>

Product Location

</td><td>

Location associated to the sold product.

</td></tr><tr><td>

Unit net price

</td><td>

Net price of a single unit of a sold product.

</td></tr><tr><td>

Product offering

</td><td>

Product offering that is associated with a sold product.

</td></tr><tr><td>

Product specification

</td><td>

The product specification associated with a sold product.**Note:** The **Product specification** field is available only if you have the Product Catalog Management Core \(com.sn\_prd\_pm\) plugin and is not available on the form by default.

</td></tr><tr><td>

Monthly recurring price

</td><td>

Price to be paid on a monthly basis for the usage of a product or service.

</td></tr><tr><td>

One time price

</td><td>

One-time price to be paid for the usage of a product or service.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of a product that is sold to a customer.

</td></tr></tbody>
</table>4.  Select a sold product to view the details associated to it.

    |Field|Description|
    |-----|-----------|
    |Number|Unique number of the sold product.|
    |Product|Reference to the product model from the CMDB table.|
    |Name|Name of the sold product.|
    |Account|Account associated with the sold product.|
    |Contact|Contact associated with the sold product.|
    |Product offering|Product offering that is associated to the sold product.|
    |Product specification|Product specification associated to the sold product.|
    |Product location|Location associated to the sold product.|
    |State|State of the sold product.|
    |Unit Net Price|Net price of a single unit of sold product.|
    |Quantity|Quantity of a product or service sold to a customer.|
    |Model categories|Reference to the model category table.|
    |Product model's short description|Brief description of the product model.|
    |Product model's description|Detailed description of the product model.|

5.  View the cases and characteristics associated to the sold product in the related list.

    |Related list|Description|
    |------------|-----------|
    |Cases|View all cases associated to the sold product.|
    |Characteristics|View the characteristics associated to a particular sold product like the characteristic value and the option.|
    |Child sold products|View the child sold products associated to the sold product.|
    |Product information|View the pricing related information of the sold product.|

6.  Perform one of the desired actions on the sold product.

    Install the Customer Life Cycle Management Self service plugin \(sn\_clm\_selfservice\) to perform the **Modify**, **Suspend**, **Resume**, and **Disconnect** actions. The flows can be performed only by the customer personas and only on the sold products where the **Contact** field is the same as the logged in user.

    -   Modify a sold product. To learn how to modify a sold product, see [Modify a sold product and hierarchy](modify-a-sold-product.md)
    -   Suspend a sold product. To learn how to suspend a sold product, see [Supending sold products](../concept/supending_sold_products.md#).
    -   Resume a sold product. To learn how to resume a sold product, see [Resuming sold products](../concept/resuming_sold_products.md#).
    -   Disconnect a sold product. To learn how to disconnect a sold product, see [Disconnecting sold products](../concept/disconnecting_sold_products.md#)

**Related topics**  


[Activate Customer Life Cycle Management Self-Service](activate-customer-life-cycle-management-self-service.md)

[View Product Inventory information on Business Portal](view-product-inventory-information-on-business-portal.md)

