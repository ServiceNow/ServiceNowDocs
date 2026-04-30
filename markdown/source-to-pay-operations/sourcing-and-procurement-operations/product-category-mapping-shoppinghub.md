---
title: Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub
description: You can map the product categories and units of measure for third-party products to the corresponding model categories. This ensures that during checkout, Shopping Hub accurately considers and displays the product category for the purchase order lines \(POL\) and purchase requisition lines \(PRL\) based on your predefined mappings.Create a third-party unit mapping to align the punchout supplier's unit of measure with the predefined units of measure.Create a third-party product category mapping to map the punchout supplier's product category to SPO's model category.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure punchout for third-party site purchases, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Mapping Product Categories and Units of Measure for seamless checkout in Shopping Hub

You can map the product categories and units of measure for third-party products to the corresponding model categories. This ensures that during checkout, Shopping Hub accurately considers and displays the product category for the purchase order lines \(POL\) and purchase requisition lines \(PRL\) based on your predefined mappings.

**Note:** You can configure the product category and unit of measure mappings for the products either before or after uploading the catalog index CSV file. However, it's recommended to define these mappings in advance whenever possible and reupload the CSV file if new mappings are added.

**Parent Topic:**[Configure punchout for third-party site purchases](../task/configure-supplier-punchout.md)

## Create third-party unit mapping

Create a third-party unit mapping to align the punchout supplier's unit of measure with the predefined units of measure.

### Before you begin

Role required: admin

### About this task

The Unit of Measure \(UOM\) in a product catalog and category refers to the standard measurement used to quantify products or services. It ensures consistency in how items are presented, sold, and tracked, maintaining uniformity across transactions and processes. By standardizing measurements, UOM allows for the proper categorization and comparability of products with similar attributes, even if they come from different suppliers or have varying specifications."

### Procedure

1.  Navigate to **All** &gt; **Procurement integrations** &gt; **Catalog** &gt; **Third-Party Units**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_c5l_qgm_5dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Third party unit

</td><td>

Standard of measurement defined by an external supplier for the products or services they provide.

</td></tr><tr><td>

Unit

</td><td>

Units defined within ServiceNow to which the third-party unit should be mapped.A unit defines specific ways the products or services are quantified, billed, or packaged.

The available standard units are:

-   Individual Unit
-   Fixed Fee
Any custom unit created will behave like an Individual Unit in the purchasing workflow. For example, if a unit called Box is created and a user purchases 10 Boxes, the system will treat it as a quantity of 10, even if each Box contains 5 Individual Units.

**Note:** Define a unit of measure conversion if you want to convert the purchased quantity into a different number of assets. For example, if a user purchases 10 Boxes, and each Box contains 5 Individual Units, the system will generate 50 assets.

</td></tr><tr><td>

Provider

</td><td>

Supplier selling the product or service.**Note:** The supplier name must match the one provided in the third-party registration record.

</td></tr><tr><td>

Default

</td><td>

Option to set a third-party unit mapping as default. The default mapping is used when a third-party unit does not match with any of the existing predefined units.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Navigate to **All** &gt; **Procurement integrations** &gt; **Catalog** &gt; **Third-Party Catalog**.

6.  Ensure that all unit of measure mappings are accurate, and make any necessary updates.


## Create third-party category mapping

Create a third-party product category mapping to map the punchout supplier's product category to SPO's model category.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Procurement integrations** &gt; **Catalog** &gt; **Third-Party Categories**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_c5l_qgm_5dc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Category defined by an external supplier for the products or services they provide.

</td></tr><tr><td>

Model category

</td><td>

Shopping Hub category that the third-party category should be mapped.

</td></tr><tr><td>

Provider

</td><td>

Supplier selling the product or service.**Note:** The supplier name must match the one provided in the third-party registration record.

</td></tr><tr><td>

Default

</td><td>

Option to set a third-party product category mapping as default. The default mapping is used when a third-party product does not match with any of the existing predefined model categories.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Navigate to **All** &gt; **Procurement integrations** &gt; **Catalog** &gt; **Third-Party Catalog**.

6.  Ensure that all product category mappings are accurate, and make any necessary updates.


