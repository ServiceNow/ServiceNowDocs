---
title: Create product categories to group product models
description: Create categories for your product models to group your product models.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting up your product catalog, Setting up primary data for Shopping Hub, Configuring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create product categories to group product models

Create categories for your product models to group your product models.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Model Categories**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_kpz_mbz_ykb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Display name of your product category on the Shopping Hub portal.

</td></tr><tr><td>

Parent category

</td><td>

Existing category that you select as the parent of this category.

</td></tr><tr><td>

UNSPSC code

</td><td>

United Nations Standard Products and Services Code of the product category.

</td></tr><tr><td>

Picture or icon

</td><td>

Visual representation of the product category.

</td></tr><tr><td class="sub-head" colspan="2">

Purchasing Automation

</td></tr><tr><td>

Spend categorization

</td><td>

Products of this category that can be sourced or not sourced. Select **Addressable** or **Not Addressable**.

</td></tr><tr><td>

Product type

</td><td>

Product that is of the type Good or Service. Based on the product type, appropriate workflow options are initiated.

</td></tr><tr><td>

Goods receipt required

</td><td>

Goods receipt that is required or not required. This field appears only if the product type is set to **Good**.

</td></tr><tr><td>

Acknowledgment type

</td><td>

Receipt of confirmation and the type of receipt. The options are **Milestones**, **Service Acknowledgment**, or **Two Way Match**.This field appears only if the product type is set to **Service.**

</td></tr><tr><td>

Goods sourcing checkout

</td><td>

References the record producer used for sourcing requests of goods from this category.

</td></tr><tr><td>

Services sourcing checkout

</td><td>

References the record producer used for sourcing requests of services from this category.

</td></tr><tr><td>

Contract type

</td><td>

Contract types that are applicable to this product category. Related contracts, based on the specified contract models, are created for any purchase requisition of a product of this category.

</td></tr><tr><td>

Display pricing?

</td><td>

Determines if pricing is to be displayed in Shopping Hub for supplier products associated to this category.

</td></tr><tr><td>

Sourcing time in days

</td><td>

Number of days that are required to source a product of this category from the supplier.For details, see [Lead time calculations](../reference/lead-time-calculations.md).

</td></tr><tr><td>

Supplier onboarding time in days

</td><td>

Number of days that are required for a new supplier of a product in this category to onboard.For details, see [Lead time calculations](../reference/lead-time-calculations.md).

</td></tr><tr><td>

Purchasing time in days

</td><td>

Number of days that are required to complete a purchase order for products in this category.

</td></tr><tr><td class="sub-head" colspan="2">

Enterprise Asset Configuration

</td></tr><tr><td>

CI class

</td><td>

Configuration item \(CI\) class that represents any product of this category.You can't add the CI class to the model category later.

</td></tr><tr><td>

Asset class

</td><td>

Asset that represents any product of this category. Setting the asset class triggers the creation of assets depending on the model category selected.

 If you select **Consumable** or **Software License**, the **CI class** field becomes read-only because consumables and software licenses don’t create CIs. If you specify a CI class and then select **Consumable** or **Software License**, the **CI class** field is changed to **None** automatically.

 If you don’t select an asset class, the product category doesn’t create any asset.

 You can select an asset class from these options:

-   **Asset**: An item that can be tracked individually.
-   **Consumable**: An asset not tracked individually, such as keyboards.
-   **Hardware**: A physical piece of computer equipment, such as a laptop or server.
-   **Software License**: A legal statement that defines the uses of software, such as the number of installations that are allowed or the terms of distribution.


</td></tr><tr><td>

Allow pre-allocation

</td><td>

Option to determine if you want to track items in this category as pre-allocated assets.

</td></tr><tr><td>

Allow as primary

</td><td>

Option to determine if assets of this product category can be primary components of a bundle.

</td></tr><tr><td>

Allow in bundle

</td><td>

Option to determine if assets of this product category can be components of a bundle.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The product category is created and the form reopens with its related lists.

## What to do next

Use the related lists of the model category form to view the product models, supplier products, and ledger assignment rules that are associated with this category.

<table id="table_story_related_list"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Product Models

</td><td>

Product models that are associated with this product category.

</td></tr><tr><td>

Supplier Products

</td><td>

Supplier products that come under this product category.Select **New** to create a supplier product.

</td></tr><tr><td>

Ledger Assignment Rules

</td><td>

Ledger assignment rules for this product category.Select **New** to [add a ledger assignment rule](create-ledger-assignment-rules.md).

</td></tr></tbody>
</table>**Parent Topic:**[Setting up your product catalog](create-product-catalogue.md)

