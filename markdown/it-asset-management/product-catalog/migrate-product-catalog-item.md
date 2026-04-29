---
title: Import a Product Catalog item
description: Import a hardware and software product catalog item from one ServiceNow instance to another ServiceNow instance to include it in the product catalog.
locale: en-US
release: australia
product: Product Catalog
classification: product-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [import product catalog item]
breadcrumb: [Product catalog items, Product Catalog, IT Asset Management]
---

# Import a Product Catalog item

Import a hardware and software product catalog item from one ServiceNow instance to another ServiceNow instance to include it in the product catalog.

## Before you begin

Role required: admin

## About this task

To import hardware or software product catalog items from one ServiceNow instance to another, use the product model and update sets XML file exported from the source ServiceNow instance.

**Note:** Product model records aren’t included in update sets. When you import an update set into the target instance, only the catalog item records are transferred. To avoid validation errors, first import the product model records, and then import the catalog item’s update set into the target ServiceNow instance.

## Procedure

1.  In the source ServiceNow instance, export the hardware or software product model record XML file.

<table id="choicetable_c1z_jby_3gc"><thead><tr><th align="left" id="d174051e110">

Option

</th><th align="left" id="d174051e113">

Description

</th></tr></thead><tbody><tr><td id="d174051e119">

**To export hardware product model record XML file**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**.
2.  Select the required hardware model name link.
3.  On the hardware model form, select the ![Additional actions](../image/additional-actions.png) Additional actions icon and then select **Export XML \(This record\)**.
4.  Save the exported hardware model XML file on your local system.


</td></tr><tr><td id="d174051e167">

**To export software product model record XML file**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Software Models**.
2.  Select the required software model name link.
3.  On the software model form, select the ![Additional actions](../image/additional-actions.png) Additional actions icon and then select **Export XML \(This record\)**.
4.  Save the exported software model XML file on your local system.


</td></tr></tbody>
</table>2.  In the source ServiceNow instance, perform these steps to export the local update set containing the catalog item.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.
    2.  Select the local update set name to open the update set record.
    3.  In the Related Links section, select **Export to XML**.
    4.  Save the exported update set XML file on your local system.
3.  In the target ServiceNow instance, import the hardware or software product model record XML file.

<table id="choicetable_z4t_ldy_3gc"><thead><tr><th align="left" id="d174051e281">

Option

</th><th align="left" id="d174051e284">

Description

</th></tr></thead><tbody><tr><td id="d174051e290">

**To import hardware model record XML file**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Hardware Models**.
2.  Hover over any column header in the Hardware Models list to display the Column Options ![Column options](../image/column-options.png) icon.
3.  Select Column options ![Column options](../image/column-options.png)icon and then select **Import XML**.
4.  Select **Choose File** and select the hardware model record XML file saved previously in Step 1.
5.  Select **Upload**.


</td></tr><tr><td id="d174051e353">

**To import software model record XML file**

</td><td>

1.  Navigate to **All** &gt; **Product Catalog** &gt; **Product Models** &gt; **Software Models**.
2.  Hover over any column header in the Software Models list to display the Column Options ![Column options](../image/column-options.png) icon.
3.  Select Column options ![Column options](../image/column-options.png) icon and then select **Import XML**.
4.  Select **Choose File** and select the software model record XML file saved previously in Step 1.
5.  Select **Upload**.


</td></tr></tbody>
</table>    The product model has been successfully imported into the target ServiceNow instance and appears on the models page.

4.  In the target ServiceNow instance, perform these steps to import the update set XML file that contains the catalog item.

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  In the Related Links section, select **Import Update Set from XML**.

    3.  Select **Choose File** and select the update set XML file saved previously in Step 2.

    4.  Select **Upload**.

        The imported update set record is available as a retrieved update set with state **Loaded**.

    5.  Open the retrieved update set and select **Preview Update Set**.

        Review updates and resolve any errors.


## Result

The catalog items are imported into the target ServiceNow instance.

## What to do next

Navigate to the Hardware Models or Software Models page in the target ServiceNow instance, View the imported hardware or software model record, along with its catalog items that are published.

**Parent Topic:**[Product catalog items](../concept/c_ManagingProductCatalogItems.md)

**Related topics**  


[Create a product catalog item](t_CreateAProductCatalogItem.md)

[Activate a product catalog item](t_ActivateAProductCatalogItem.md)

[Deactivate a product catalog item](t_DeactivateAProductCatalogItem.md)

