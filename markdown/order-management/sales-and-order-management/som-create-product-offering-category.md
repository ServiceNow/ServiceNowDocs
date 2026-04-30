---
title: Create a product offering category
description: Define a product offering category used to organize similar product offerings in a catalog. Product categories make it easier for agents to browse and navigate product offerings when creating opportunities, quotes, and orders.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create a product offering category

Define a product offering category used to organize similar product offerings in a catalog. Product categories make it easier for agents to browse and navigate product offerings when creating opportunities, quotes, and orders.

## Before you begin

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Offerings** &gt; **Product Offering Categories**.

3.  Select **New**.

4.  In the form, fill in the fields.

<table id="table_klq_jdn_11c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique system-defined number that identifies the product category.

</td></tr><tr><td>

Name

</td><td>

Name of the category.

</td></tr><tr><td>

Leaf

</td><td>

Option indicating there are no subcategories for this category. Selecting **Leaf** means the category can have product offers but not subcategories. If **Leaf** isn’t selected, the category can only have subcategories but not product offers.

</td></tr><tr><td>

Thumbnail image

</td><td>

Thumbnail image for the product offering category. Select **Attach Image** to upload your image.

</td></tr><tr><td>

Image

</td><td>

Image of the product offering category. Select **Attach Image** to upload your image.

</td></tr><tr><td>

Description

</td><td>

A brief description of the category.

</td></tr><tr><td>

State

</td><td>

State of the category:-   Draft: Initial state of the category, before it's published.
-   Published: The product category has been published to the catalog. After a category is published, you can update it. You can delete, retire, or archive it if there are no associated product offerings.
-   Retired: Category has been retired and is no longer active. The category can’t be updated.
-   Archived: Category has been archived and is no longer available for use.
-   Copied to Catalog: The product category has been copied.


</td></tr><tr><td>

Start date

</td><td>

Date and time that the category is available in the catalog. Select the Calendar icon to choose the start date and time, then select **OK**.

</td></tr><tr><td>

End date

</td><td>

Date and time that the category is no longer used in the catalog. Select the Calendar icon to choose the end date and time, then select **OK**

</td></tr><tr><td>

Code

</td><td>

Product code for the category. The system automatically generates a code based on the category **Name** entered, but you can change the value to any desired alphanumeric string.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  Associate the category to a catalog.

    1.  In the Catalogs tab, select **New**.

    2.  In the Catalog Category form, select the published Catalog to which this category belongs and select **Save**.

7.  In the Details tab for the category, select **Publish**.

    The category state changes to Published and is added to the selected catalog.

8.  If needed, define the parent category and subcategories for the category using the Parent categories and Child categories tabs.


## What to do next

[Create product offerings](som-create-product-offering.md).

