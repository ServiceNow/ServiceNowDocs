---
title: Create product models to group supplier products
description: Create product models to group your supplier products.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Setting up your product catalog, Setting up primary data for Shopping Hub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create product models to group supplier products

Create product models to group your supplier products.

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Model Management** &gt; **All Other Product Models**.

    ![ServiceNow navigation showing ShoppingHub > Model Management > All Other Product Models path](../image/spo-product-mod-nav.png)

2.  Select **New**.

    ![Product Models list view with New button highlighted.](../image/spo-product-mod-new.png)

3.  Select a model type that you want to create.

    ![Model type selection page showing various options.](../image/spo-product-mod-type.png)

4.  On the form, fill in the fields.

    The following table describes the fields that appear on all models, regardless of the type of model.

<table id="table_ijg_fpj_54"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the model.**Note:** The **Display name** field is auto-populated with the values of the **Manufacturer** and **Name** fields.

</td></tr><tr><td>

Manufacturer

</td><td>

Name of the manufacturer of the model.

</td></tr><tr><td>

Name

</td><td>

Manufacturer-assigned name of the model or abstract name that is specified by the model manager, such as Field Agent Laptop.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the model.

</td></tr><tr><td>

Model categories

</td><td>

Categories to which the model is assigned.

</td></tr><tr><td>

Asset tracking strategy

</td><td>

Process by which the model can be tracked. Select one of these options:-   **Leave to Category**: Model is transparent and the category defines the asset class.
-   **Create Consumable Asset**: Model forces the asset class to be consumable, regardless of what the category defines as the asset class.
-   **Don't create assets**: Model blocks asset instantiation, regardless of what the category defines as the asset class.


</td></tr><tr><td>

Acquisition method

</td><td>

Method for purchasing the model. Select **Both**, **Buy**, or **Lease**.

</td></tr><tr><td>

Cost

</td><td>

Cost of a single unit of the model.

</td></tr><tr><td>

Depreciation

</td><td>

Depreciation scheme for the model.

</td></tr><tr><td>

Salvage value

</td><td>

Estimated value that an asset realizes after its sale at the end of its useful life. This value must be less than or equal to the cost of the asset.

</td></tr><tr><td>

Model number

</td><td>

Specific model number that is assigned to the item by the manufacturer.

</td></tr><tr><td>

Barcode

</td><td>

Barcode number that is assigned to the model by the manufacturer.

</td></tr><tr><td>

Owner

</td><td>

Person responsible for the model.

</td></tr><tr><td>

Status

</td><td>

Status of the model. Select **In Production**, **Retired**, or **Sold**.

</td></tr><tr><td>

Expenditure type

</td><td>

Type of expenditure. Select one of these options: -   **Capex**: Capital expenditure is a one-time expenditure, where the value is realized over the years. For example, a photocopier.
-   **Opex**: Operational expenditure is an on-going expenditure. For example, toners for the photocopier.


</td></tr><tr><td>

Picture

</td><td>

Picture or icon to represent this product model.

</td></tr><tr><td>

Certified

</td><td>

Model that has an approval for its use.

</td></tr><tr><td>

Comments

</td><td>

Additional information about the model that is good to know.

</td></tr><tr><td>

Assets

</td><td>

Assets that are created from this model. You can have any combination of assets and configuration items. For example, with a single hardware model, you can have assets and no configuration items, configuration items and no assets, or both configuration items and assets.

</td></tr><tr><td>

Configuration Items

</td><td>

Configuration items that are created from this model. You can have any combination of assets and configuration items.

</td></tr><tr><td class="sub-head" colspan="2">

Purchasing Automation

</td></tr><tr><td>

Product category

</td><td>

Category to which this product belongs.

</td></tr><tr><td>

Spend categorization

</td><td>

Products of this category that can be sourced or not. The default value is based on the selected product category.

</td></tr><tr><td>

Product type

</td><td>

Type Good or Service.The default value is based on the selected product category.

</td></tr><tr><td>

Good receipt required

</td><td>

Goods receipt that is required or not. This field appears only if the product type selected is **Good**.

 The default value is based on the selected product category.

</td></tr><tr><td>

Acknowledgment type

</td><td>

Receipt of confirmation and the type of receipt. The options available are **Milestones**, **Service Acknowledgment**, and **Two Way Match**.The default value is based on the selected product category but the value provided here can override it.

 This field appears only if the product type selected is **Service.**

</td></tr><tr><td>

Sourcing time in days

</td><td>

Number of days that are required to source a product of this category from the supplier.This field is auto-populated based on the selected product category.

 For details, see [Lead time calculations](../reference/lead-time-calculations.md).

</td></tr><tr><td>

Purchasing time in days

</td><td>

Number of days that are required to complete a purchase order for products in this category. This field is auto-populated based on the selected product category.

 For details, see [Lead time calculations](../reference/lead-time-calculations.md).

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

-   Use the related lists of the model category form to view the product models, supplier products, and ledger assignment rules that are associated with this category.
-   Create ledger assignment rules for this product model. See [add a ledger assignment rule](create-ledger-assignment-rules.md).

**Parent Topic:**[Setting up your product catalog](create-product-catalogue.md)

