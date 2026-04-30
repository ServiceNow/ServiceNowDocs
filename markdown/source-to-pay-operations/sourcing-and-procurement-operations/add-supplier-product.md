---
title: Add a supplier product
description: Add supplier products to populate the primary data.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up your product catalog, Setting up primary data for Shopping Hub, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Add a supplier product

Add supplier products to populate the primary data.

## Before you begin

To add a supplier product, you must have already added a supplier, product category or model category, and product model to the primary data. For more information on how to add them, see [Add a supplier](create-supplier.md), [Create product categories](create-product-model-categories.md), and [Create product models](create-product-models.md).

Role required: sn\_shop.shopping\_hub\_admin or sn\_shop.procurement\_administrator

## About this task

You can add a supplier product and choose to publish it on the Shopping Hub portal. The products that you add, appear on the portal under various categories. You can add multiple products that are available with the suppliers.

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Supplier Products** &gt; **Published Products**.

    You can also navigate to **Sourcing and Purchasing Automation** &gt; **Primary Data** &gt; **Supplier Product**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_kcc_bcf_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the product at the supplier’s end.

</td></tr><tr><td>

Supplier

</td><td>

Supplier for this product.

</td></tr><tr><td>

Supplier part number

</td><td>

Unique number that is used by the supplier to identify this product.

</td></tr><tr><td>

Product model

</td><td>

Standardized definition for this product across suppliers.**Note:** For creating a product bundle, enter the name of the product model of type bundle in this field.

</td></tr><tr><td>

Product category

</td><td>

Category to which this product belongs.

</td></tr><tr><td>

Sales start date

</td><td>

Date when the supplier product is active and available for purchase in the catalog. This is a read-only field.

</td></tr><tr><td>

Sales end date

</td><td>

Date when the supplier product is discontinued and no longer published in the catalog. This is a read-only field.

</td></tr><tr><td>

Published

</td><td>

Option for specifying if the product is to be listed on the Shopping Hub portal.

</td></tr></tbody>
</table>    **Note:** The **Sales start date** and **Sales end date** fields are populated through third-party integration from the Catalog API using Source-to-Pay Integration Framework \(PIF\).

4.  Select the **Details** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Units available|Number of units of the product in stock with the supplier.|
    |Unit|Unit or rate in which the product is sold by the supplier.|
    |Short description|Brief description of the product for the buyer.|
    |Description|Detailed description of the product for the buyer.|

5.  Select the **Purchasing Automation** tab and fill in the fields.

    **Note:** These cascade down from the model category to the product model, to the supplier product, but can be overridden at the leaf level.

<table id="table_y2q_1df_flb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Spend categorization

</td><td>

Product that is addressable for negotiation. You can select one of these options:

 -   **Addressable**: Can be considered for negotiation.
-   **Not Addressable**: Cannot be considered for negotiation.


</td></tr><tr><td>

Product type

</td><td>

Type of product. The options are **Good** or **Service**.

</td></tr><tr><td>

Goods receipt required

</td><td>

Purchase and receipt of goods that are automated. The options are **Yes** or **No**.

</td></tr><tr><td>

Acknowledgment type

</td><td>

Type of receipt confirmation, if any, required for services. You can select one of these options:

 -   **None**
-   **Milestones**
-   **Service Acknowledgment**
-   **Two Way Match**


</td></tr><tr><td>

Capex account

</td><td>

General ledger account where capital expenses are posted on purchase.

</td></tr><tr><td>

Expense account

</td><td>

General ledger account where operational expenses are posted on purchases.

</td></tr><tr><td>

Pre-paid account

</td><td>

General ledger account where purchases of this product are posted when they are prepaid.

</td></tr><tr><td>

Sourcing required?

</td><td>

Option to mark if sourcing is required for this product. This is determined based on if there is an active contractual price for this supplier product or not.

</td></tr><tr><td>

Supplier delivers to

</td><td>

Countries where the suppliers can deliver the product.

</td></tr></tbody>
</table>    For more information, see [Manage delivery to valid address](manage-shipping-address.md).

6.  Select the **Lead Time** tab and review the fields.

    |Field|Description|
    |-----|-----------|
    |Total lead time in days|Estimated number of days to process the purchase order and deliver the product.|
    |Sourcing time in days|Estimated number of days to process the sourcing request.|
    |Purchasing time in days|Estimated number of days to complete the purchase requisition and create a purchase order.|
    |Shipping time in days|Estimated number of days to ship the product to the delivery location.|

    For more information, see [Lead time calculations](../reference/lead-time-calculations.md).

7.  Select **Submit**.


## What to do next

Use the related lists of the supplier product form to view the pricing, purchase order lines, product visuals, and ledger assignment rules that are associated with this supplier product.

**Parent Topic:**[Setting up your product catalog](create-product-catalogue.md)

