---
title: View Product Inventory information on Business Portal
description: Enable customers to view and track the list of product inventories associated to their account.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 4
breadcrumb: [Business Portal, Customer communication, Use, Customer Service Management]
---

# View Product Inventory information on Business Portal

Enable customers to view and track the list of product inventories associated to their account.

## Before you begin

Role required: sn\_customerservice.customer, sn\_customerservice.customer\_admin, sn\_customerservice.partner, sn\_customerservice.partner\_admin

## About this task

Install the Customer Life Cycle Self Service plugin \(com.snc.customer\_lifecycle\_mgmt\_self\_service\) to perform the **Modify**, **Suspend**, **Resume**, and **Disconnect** actions on product inventories.

To learn how to install the Customer Life Cycle Self Service plugin \(com.snc.customer\_lifecycle\_mgmt\_self\_service\), see [Activate Customer Life Cycle Management Self-Service](activate-customer-life-cycle-management-self-service.md).

## Procedure

1.  Navigate to the business portal.

2.  Select **My Hub** and then **Manage product inventories** from the header menu.

    The system displays a list of product inventories associated to your account.

3.  On the product inventories form, fill in the fields.

<table id="table_hv4_1jy_1fc"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the product inventory.

</td></tr><tr><td>

Number

</td><td>

Number of the product inventory.

</td></tr><tr><td>

Parent product

</td><td>

Parent of the product inventory, if applicable.

</td></tr><tr><td>

State

</td><td>

State of the product inventory, whether active or inactive.

</td></tr><tr><td>

Location

</td><td>

Location associated to the product inventory.

</td></tr><tr><td>

Unit net price

</td><td>

Net price of a single unit of product inventory.

</td></tr><tr><td>

Product offering

</td><td>

Product offering associated to the product inventory.

</td></tr><tr><td>

Product specification

</td><td>

The product specification associated with a product inventory.**Note:** The **Product specification** field is available only if you have the Product Catalog Management Core \(com.sn\_prd\_pm\) plugin and is not available on the form by default.

</td></tr><tr><td>

Monthly recurring price

</td><td>

Price to be paid on a monthly basis for the usage of a product or service.

</td></tr><tr><td>

One-time price

</td><td>

One-time price to be paid for the usage of a product or service.

</td></tr><tr><td>

Quantity

</td><td>

Quantity of a product that is sold to a customer.

</td></tr></tbody>
</table>4.  Select a product inventory to view the record details.

<table id="table_hmy_qjy_1fc"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number of the product inventory.

</td></tr><tr><td>

Product

</td><td>

Reference to the product model from the CMDB table.

</td></tr><tr><td>

Name

</td><td>

Name of the product inventory.

</td></tr><tr><td>

Account

</td><td>

Account associated to the product inventory.

</td></tr><tr><td>

Contact

</td><td>

Contact associated to the product inventory.

</td></tr><tr><td>

Product offering

</td><td>

Product offering associated to a product inventory.

</td></tr><tr><td>

Product specification

</td><td>

Product specification associated with a product inventory.

</td></tr><tr><td>

Location

</td><td>

Location of the product inventory.

</td></tr><tr><td>

State

</td><td>

State of the product inventory.**Note:** If the state is **Active**, you can't perform the **Resume** action on the product inventory.

</td></tr><tr><td>

Unit net price

</td><td>

Net price of a single unit of a product inventory.

</td></tr></tbody>
</table>5.  View the cases and characteristics associated to the product inventory in the related list.

    |Related list|Description|
    |------------|-----------|
    |Cases|View all cases associated to the product inventory.|
    |Characteristics|View the characteristics associated to a particular sold product like the characteristic value and the option.|
    |Child sold products|View the child sold products associated to the sold product.|
    |Product information|View the pricing related information of the sold product.|

6.  Perform one of the desired actions on the product inventory.

    Install the Customer Life Cycle Management Self service plugin \(sn\_clm\_selfservice\) to perform the **Modify**, **Suspend**, **Resume**, and **Disconnect** actions. The flows can be performed only by the customer personas and only on the sold products where the **Contact** field is the same as the logged in user.

    -   Modify a product inventory. To learn how to modify a product inventory, see [Modify product inventory records](modify_product_inventory_records.md)
    -   Suspend a product inventory. To learn how to suspend a product inventory, see [Suspend product inventory records](suspend_product_inventory_records.md).
    -   Resume a product inventory. To learn how to resume a sold product, see [Resume product inventory records](resume_product_inventory_records.md).
    -   Disconnect a product inventory. To learn how to disconnect a sold product, see [Disconnect product inventory records](disconnect_product_inventory_records.md)

**Related topics**  


[Activate Customer Life Cycle Management Self-Service](activate-customer-life-cycle-management-self-service.md)

[View product information from Business Portal](view-product-info-business-portal.md)

