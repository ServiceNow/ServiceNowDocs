---
title: Create a product catalog item
description: Create hardware and software product catalog items to include in the product catalog and the service catalog.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Product catalog items, Product Catalog, Asset Management, IT Service Management]
---

# Create a product catalog item

Create hardware and software product catalog items to include in the product catalog and the service catalog.

## Before you begin

Role required: catalog\_admin

## About this task

You must [activate](t_ActivateAProductCatalogItem.md) the items separately before they appear in the product catalog or service catalog.

## Procedure

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Catalog Definition** &gt; **Hardware &amp; Software Items**.

2.  Select **New**.

3.  Complete the form.

    Some of the fields listed do not appear until you save the product catalog item.

<table id="table_imx_ffs_zp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the item as you want it displayed in the product catalog.

</td></tr><tr><td>

Catalogs

</td><td>

Catalog this item is listed in.

</td></tr><tr><td>

Vendor

</td><td>

Vendor that supplies the item. If the item is purchased from multiple vendors, use the vendor catalog and leave this field empty.

</td></tr><tr><td>

Rank tier

</td><td>

Overall ranking for the selected vendor's products and services. This field is shown in a Product Catalog Item record when the CI class is **Hardware Catalog** or **Software Catalog**.

</td></tr><tr><td>

Model

</td><td>

Specific version or configuration of the item.

</td></tr><tr><td>

Product ID

</td><td>

Item identification number assigned by your organization.

</td></tr><tr><td>

Price

</td><td>

Price at which the item is available in the product catalog. Enter a numerical value and select the appropriate currency.

</td></tr><tr><td>

Recurring price

</td><td>

Item's recurring price. For example, a subscription to a mobile phone contract could cost $500.00, with an $30.00 monthly recurring price.

</td></tr><tr><td>

Recurring price frequency

</td><td>

Interval at which the recurring price is accrued.

</td></tr><tr><td>

List Price

</td><td>

Price at which the item retails. This field is shown only when the **Class** is **Hardware Catalog** or **Software Catalog**.

</td></tr><tr><td>

Cost

</td><td>

Price at which the item was purchased from the vendor. The cost could be less than the **List Price** if your organization received a discount from the vendor. This field is shown in a product catalog item record only when the CI class is **Hardware Catalog** or **Software Catalog**.

</td></tr><tr><td>

Omit price in cart

</td><td>

When selected, hides the price when the item is displayed in the service catalog. Clear the check box to show the price in the service catalog. This field is only visible in a product catalog item record when the CI class is **Hardware Catalog**.

</td></tr><tr><td>

Workflow

</td><td>

Workflow associated with this item.You can view the activities, the conditions, and the stages associated with the workflow by selecting **Show Workflow**.

</td></tr><tr><td>

Execution plan

</td><td>

Execution plan associated with this item.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the item.

</td></tr><tr><td>

Ordered item link

</td><td>

List of links containing more information about items. The links can be reused across multiple items.

</td></tr><tr><td>

Class

</td><td>

Catalog item class this item belongs to. Select **Hardware Catalog** or **Software Catalog**. This field is visible by default. When you save the record as a hardware or software catalog item, the form is retitled Hardware Catalog or Software, respectively.

</td></tr><tr><td class="sub-head" colspan="2">

General section

</td></tr><tr><td>

Category

</td><td>

Named group of items to which the item belongs.

</td></tr><tr><td>

Delivery time

</td><td>

Amount of time it takes to deliver the item, starting from when it is ordered from the product catalog.

</td></tr><tr><td>

UPC

</td><td>

Barcode number used to identify and track items.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the item. The description is displayed in the product catalog listing.

</td></tr><tr><td class="sub-head" colspan="2">

Product Information section

</td></tr><tr><td>

Cost

</td><td>

Price at which the item was purchased from the vendor. This field is only visible when the **Class** is **Software Catalog**.

</td></tr><tr><td>

Specifications

</td><td>

Facts about the item, such as size, weight, version, or speed.

</td></tr><tr><td>

Features

</td><td>

Distinct properties or distinguishing characteristics of the item.

</td></tr><tr><td class="sub-head" colspan="2">

Images section

</td></tr><tr><td>

Icon

</td><td>

Small image that appears next to the name when the item is displayed in the service catalog. Supported file types are `jpg`, `png`, `bmp`, `gif`, and `jpeg`.

</td></tr><tr><td>

Picture

</td><td>

An image showing the item. Supported file types are `jpg`, `png`, `bmp`, `gif`, and `jpeg`.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Includes

</td><td>

More catalog items provided with this item. This related list is for informational purposes only.

</td></tr><tr><td>

Variables

</td><td>

Service catalog variables associated with this item. A service catalog variable captures and passes on information about choices a customer makes when ordering an item from the service catalog.

</td></tr><tr><td>

Vendor Catalog Items

</td><td>

Vendor catalog items associated with this item. Vendor catalog items allow you to track information about this item by its specifications for each vendor.

</td></tr></tbody>
</table>    Hardware catalog item record with an icon and picture of the item.

    ![Hardware catalog item for a laser printer](../image/HardwareCatalogItem.png "Hardware catalog item")

4.  Select **Try It** to preview the item as it appears in the service catalog.

5.  Select **Submit** or **Update**.


**Parent Topic:**[Product catalog items](../concept/c_ManagingProductCatalogItems.md)

**Related topics**  


[Activate a product catalog item](t_ActivateAProductCatalogItem.md)

[Deactivate a product catalog item](t_DeactivateAProductCatalogItem.md)

[Import a Product Catalog item](migrate-product-catalog-item.md)

[Create a vendor catalog item](t_CreateAVendorCatalogItem.md)

[Create an execution plan](https://www.servicenow.com/docs/access?context=t_CreateAnExecutionPlan&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Service catalog variables](https://www.servicenow.com/docs/access?context=c_ServiceCatalogVariables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

