---
title: Create and publish a price list
description: Create a price list that defines the pricing for products and services in Sales and Order Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Create and publish a price list

Create a price list that defines the pricing for products and services in Sales and Order Management.

## Before you begin

Role required: sn\_csm\_pricing.pricelist\_administrator or sn\_csm\_pricing.pricelist\_manager

## About this task

You can create various types of price lists for your organization, such as price lists that are based on a standard currency or price lists that are based on a particular customer account. The first price list that you create for a specified currency is automatically set as the default price list. When you're creating a default price list, the start date must be either the current date or a date earlier than the current date. If you don’t want the price list as the default, deselect the **Default** option.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Prices** &gt; **Price Lists.**

3.  Select **New**.

4.  In the Details tab, fill in the fields.

<table id="table_customer_order_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-assigned number that identifies the price list.

</td></tr><tr><td>

Name

</td><td>

Name of the price list.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the price list name. Although the code is system-generated, you can edit it to represent any industry-specific product code.

</td></tr><tr><td>

Currency

</td><td>

Currency of the price list, for example USD for US dollars.

</td></tr><tr><td>

Account

</td><td>

Optional. Account of the customer to which this price list applies.

</td></tr><tr><td>

Default

</td><td>

Option for setting this price list as the default price list with the specified Currency or for the specified Account.

</td></tr><tr><td>

Sales agreement

</td><td>

If you're using the Sales Agreement Management application and a sales agreement was created by an agent, the unique system-assigned number that identifies the sales agreement associated with this price list.

</td></tr><tr><td>

Description

</td><td>

Description of the price list.

</td></tr><tr><td>

State

</td><td>

Stage of the price list:-   Draft: Initial state of the price list. Information is still being added to the price list and hasn’t been published to the catalog yet.
-   Published: Price list has been published to the catalog. After a price list is published, you can update, delete, retire, or archive it.
-   Retired: Price list has been retired and is no longer active. The price list and its price list lines cannot be updated.
-   Archived: Price list has been archived and is no longer available for use.
**Note:** A default price list cannot be deleted, retired, or archived.

</td></tr><tr><td>

Start Date

</td><td>

Starting date and time that the price list is effective. Select the Calendar icon ![](../image/field-calendar.png) to choose the start date and time, then select **OK**. **Note:** If this is a default price list, the start date must be either the current date or a date that is earlier than the current date.

</td></tr><tr><td>

End Date

</td><td>

Ending date and time of the price list. Select the Calendar icon ![](../image/field-calendar.png) to choose the end date and time, then select **OK**. After the ending time, the price list is no longer active.**Note:** If this is a default price list, the end date is ignored.

</td></tr></tbody>
</table>5.  Select **Save**.

    The price list is in the Draft state.

6.  Select **Publish**.

    The price list state changes to Published. The Price List Lines tab opens for creating a price list line.


## What to do next

[Create a price list line](som-create-price-list-line.md) for the price list.

