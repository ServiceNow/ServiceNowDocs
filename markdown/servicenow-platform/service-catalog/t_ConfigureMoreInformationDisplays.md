---
title: Configure preview
description: Configure the number of items that have the Preview section expanded to display item details. You can also change the default number \(5\) of items and categories that display, and hide the Exists in categories information.By default, up to five items or categories appear in each category on the homepage.By default, catalog items that are in several categories show Exists in categories information that shows other categories that the items are available in. You can hide this information.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Catalog home page configuration, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure preview

Configure the number of items that have the **Preview** section expanded to display item details. You can also change the default number \(5\) of items and categories that display, and hide the **Exists in categories** information.

## Before you begin

Role required: admin

## About this task

By default, if not showing item details using pop-ups, the first two items listed in the category display have the **Preview** section expanded to display item details.

To change the number of items with this information expanded, set the **Number of Catalog Items to expand in browsing and search when not using pop-up icons to view details** \(glide.sc.auto\_expand\) property to the number required.

<table id="table_wvc_glq_lq"><tbody><tr><td>

Expanding to 2 items

</td><td>

Expanding to 1 item

</td></tr><tr><td>

![](../image/ConfigurePreview1.png)

</td><td>

![](../image/ConfigurePreview2.png)

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog home page configuration](../concept/c_ManagingTheHomepageForACatalog.md)

## Set number of items and categories to preview

By default, up to five items or categories appear in each category on the homepage.

### About this task

To change this number, set the **Number of Catalog Items/Categories to preview in a section** \(glide.sc.max\_items\) property to the required value.

<table id="simpletable_gk5_psq_bq"><tbody><tr><td>

![Screenshot for previewing five items](../image/ServiceCatalogPreview5Items.png "Previewing five items")

</td><td>

![Screenshot for previewing two items](../image/ServiceCatalogPreview2Items.png "Previewing two items")

</td></tr></tbody>
</table>## Hide the existing categories in the categories display

By default, catalog items that are in several categories show **Exists in categories** information that shows other categories that the items are available in. You can hide this information.

### Before you begin

Role required: admin

### Procedure

1.  Set the **Show the additional categories section when viewing a catalog item**\(glide.sc.show\_additional.cats\) property to **No**.

<table id="simpletable_gk5_psq_bq"><tbody><tr><td>

![Screenshot for showing additional categories](../image/ServiceCatalogShowAdditionaCatsOn.png "Showing additional categories")

</td><td>

![Screenshot for hiding additional categories](../image/ServiceCatalogShowAdditionaCatsOff.png "Hiding additional categories")

</td></tr></tbody>
</table>
