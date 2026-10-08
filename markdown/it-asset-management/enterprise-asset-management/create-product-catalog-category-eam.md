---
title: Create an enterprise catalog category
description: Create an enterprise catalog category to group related product catalog items within the Service Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/enterprise-asset-management/create-product-catalog-category-eam.html
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 2
keywords: [Enterprise Asset Management, EAM, product catalog, product catalog category, create category, admin center]
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Create an enterprise catalog category

Create an enterprise catalog category to group related product catalog items within the Service Catalog.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

Catalog categories organize related product catalog items into logical groupings within your product catalogs. These groupings can help users locate and request available product offerings more intuitively and efficiently. You can organize catalog categories hierarchically, using both parent and child catalog categories to reflect the hierarchical relationships between your products.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **Product catalog** &gt; **Product catalog categories**.

4.  Select **New**.

5.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the catalog category.

</td></tr><tr><td>

Catalog

</td><td>

Product catalog that the catalog category is associated with. Set this field to **Service Catalog**.**Note:** The Service Catalog is the default product catalog for all enterprise models.

</td></tr><tr><td>

Location

</td><td>

Geographic location that the catalog category is supported in.

</td></tr><tr><td>

Active

</td><td>

Option indicating that the catalog category is active.

</td></tr><tr><td>

Parent

</td><td>

Parent catalog category that this catalog category is a child of.

</td></tr><tr><td>

Roles

</td><td>

User roles that can access and request the product catalog items that are grouped under this catalog category.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the catalog category.

</td></tr><tr><td>

Desktop image

</td><td>

Catalog category image that appears on desktop versions of the product catalog home page. Use any of the following image formats:-   PNG
-   JPG
-   GIF
-   WebP


</td></tr><tr><td>

Icon

</td><td>

Icon that appears next to the catalog category name in the product catalog. Use an image size of either 64 x 64 pixels or 128 x 128 pixels.**Note:** This Icon is applicable only for child catalog categories.

</td></tr><tr><td>

Header icon

</td><td>

Icon that appears next to the catalog category header in the product catalog. Use an image size of either 64 x 64 pixels or 128 x 128 pixels.**Note:** This icon is applicable only for top-level catalog categories.

</td></tr></tbody>
</table>6.  Select **Save**.


## Result

The catalog category is added to the Service Catalog.

Each time you subsequently publish a related enterprise model to the Service Catalog, you must specify that it's associated with the given catalog category in the **Category** field of the Publish model to Enterprise Asset Catalog dialog box. The Enterprise Asset Management application automatically generates a corresponding product catalog item and then adds it to the given catalog category. You can view the list of all associated product catalog items in the **Catalog items** tab of the catalog category record. Users can locate and request the product catalog item under the given catalog category in the Service Catalog.

